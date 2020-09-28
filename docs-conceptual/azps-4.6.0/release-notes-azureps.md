---
title: Az Azure PowerShell kibocsátási megjegyzései
description: Megismerheti az Azure PowerShell-modulok legújabb frissítéseit.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 52129f31202a8ae04bf80988b5aa07b12fe081b8
ms.sourcegitcommit: 15f21c40dcb7610e2fbaaabf264ad925e4224500
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/22/2020
ms.locfileid: "90913382"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="4ffb6-103">Az Azure PowerShell kibocsátási megjegyzései</span><span class="sxs-lookup"><span data-stu-id="4ffb6-103">Azure PowerShell release notes</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="4ffb6-104">4.6.0 – 2020. augusztus</span><span class="sxs-lookup"><span data-stu-id="4ffb6-104">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4ffb6-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4ffb6-105">Az.Accounts</span></span>
* <span data-ttu-id="4ffb6-106">Az összes nyilvános felhőkörnyezet betöltődik, ha a felderítési végpont nem ad vissza alapértelmezett AzureCloud- vagy más nyilvános környezetet [#12633]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-106">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="4ffb6-107">A SubscriptionPolicies elérhetővé lett téve a 'Get-AzSubscription' parancsmagban [#12551]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-107">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4ffb6-108">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4ffb6-108">Az.Automation</span></span>
* <span data-ttu-id="4ffb6-109">A '-RunOn' paraméterek hozzá lettek adva a 'Set-AzAutomationWebhook' parancsmaghoz hibridfeldolgozó-csoport megadásához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-109">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4ffb6-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-110">Az.Compute</span></span>
* <span data-ttu-id="4ffb6-111">Az '-EncryptionAtHost' paraméter hozzá lett adva a 'New-AzVm', a 'New-AzVmss', a 'New-AzVMConfig', a 'New-AzVmssConfig', az 'Update-AzVM' és az 'Update-AzVmss' parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-111">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="4ffb6-112">A 'SecurityProfile' hozzá lett adva a 'Get-AzVm' és a 'Get-AzVmssVM' visszaadott objektumhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-112">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="4ffb6-113">Az '-InstanceView' kapcsoló hozzá lett adva választható paraméterként a 'Get-AzHostGroup' parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-113">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="4ffb6-114">Hozzá lett adva az új 'Invoke-AzVmPatchAssessment' parancsmag</span><span class="sxs-lookup"><span data-stu-id="4ffb6-114">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4ffb6-115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4ffb6-115">Az.DataFactory</span></span>
* <span data-ttu-id="4ffb6-116">A hiányzó tulajdonságok hozzá lettek adva a PSPipelineRun osztályhoz.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-116">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4ffb6-117">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4ffb6-117">Az.HDInsight</span></span>
* <span data-ttu-id="4ffb6-118">Támogatottá vált a fürtlétrehozás a gazdagépen végzett titkosítási funkcióval.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-118">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4ffb6-119">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4ffb6-119">Az.KeyVault</span></span>
* <span data-ttu-id="4ffb6-120">Figyelmeztető üzenetek lettek hozzáadva a helyreállítható törlés letiltásának tervezésekor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-120">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="4ffb6-121">Figyelmeztető üzenetek lettek hozzáadva a SecretValueText attribútum eltávolításának tervezésekor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-121">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="4ffb6-122">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="4ffb6-122">Az.Maintenance</span></span>
* <span data-ttu-id="4ffb6-123">Opcionális ütemezéssel kapcsolatos mezők lettek hozzáadva a 'New-AzMaintenanceConfiguration' parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-123">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="4ffb6-124">Új parancsmag lett hozzáadva a 'Get-AzMaintenancePublicConfiguration' használatához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-124">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="4ffb6-125">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-125">Az.ManagedServices</span></span>
* <span data-ttu-id="4ffb6-126">Kompatibilitástörő változásra figyelmeztető üzenetek lettek hozzáadva a felügyelt szolgáltatások hozzárendeléséhez és definíciójához tartozó parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-126">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4ffb6-127">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-127">Az.Monitor</span></span>
* <span data-ttu-id="4ffb6-128">A 'set-AzDiagnosticSetting' paraméterkészlete ki lett bővítve a naplók és metrikák engedélyezésének szétválasztása érdekében [#12482]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-128">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="4ffb6-129">Ki lett javítva az 'Add-AzMetricAlertRuleV2' folyamatból érkező metrikariasztáskor jelentkező hibája</span><span class="sxs-lookup"><span data-stu-id="4ffb6-129">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="4ffb6-130">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-130">Az.Resources</span></span>
* <span data-ttu-id="4ffb6-131">Frissült a 'Get-AzPolicyAlias'-válasz, amely mostantól információt tartalmaz arról, hogy az alias módosítható-e az Azure Policyval.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-131">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="4ffb6-132">Létre lett hozva az új 'Set-AzRoleAssignment' parancsmag</span><span class="sxs-lookup"><span data-stu-id="4ffb6-132">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="4ffb6-133">Hozzá lett adva a 'Get-AzDeploymentManagementGroupWhatIfResult' az ARM-sablon What-If típusú eredményeinek a felügyeleti csoport hatókörében történő lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-133">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="4ffb6-134">Hozzá lett adva az új 'Get-AzTenantWhatIfResult' parancsmag az ARM-sablonok What-If típusú eredményeinek bérlői hatókörben történő lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-134">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="4ffb6-135">A '-WhatIf' és a '-Confirm' felül lett bírálva a 'New-AzManagementGroupDeployment' és a 'New-AzTenantDeployment' esetében az ARM-sablon What-If típusú eredményeinek használata érdekében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-135">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="4ffb6-136">Ki lett javítva a '-WhatIf' és a '-Confirm' viselkedése az új üzembehelyezési parancsmagok esetében, hogy megfeleljenek a $WhatIfPreference és a $ConfirmPreference paramétereknek.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-136">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with $WhatIfPreference and $ConfirmPreference.</span></span>
* <span data-ttu-id="4ffb6-137">Ki lett javítva a szerializálási hiba a '-TemplateObject' és a 'TemplateParameterObject' esetében [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-137">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="4ffb6-138">Kompatibilitástörő változást okozó attribútum lett hozzáadva a 'Get-AzResourceGroupDeploymentOperation' parancsmaghoz a kimenet típusának közelgő változása miatt</span><span class="sxs-lookup"><span data-stu-id="4ffb6-138">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="4ffb6-139">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="4ffb6-139">Az.SignalR</span></span>
* <span data-ttu-id="4ffb6-140">Ki lettek javítva a 'Restart-AzSignalR' és az 'Update-AzSignalR' súgófájljainak hibái</span><span class="sxs-lookup"><span data-stu-id="4ffb6-140">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="4ffb6-141">Hozzá lett adva az 'Update-AzSignalRNetworkAcl' és a 'Set-AzSignalRUpstream' parancsmag</span><span class="sxs-lookup"><span data-stu-id="4ffb6-141">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4ffb6-142">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4ffb6-142">Az.Storage</span></span>
* <span data-ttu-id="4ffb6-143">A blobok lekérdezésgyorsítása támogatottá vált</span><span class="sxs-lookup"><span data-stu-id="4ffb6-143">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="4ffb6-144">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="4ffb6-144">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="4ffb6-145">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="4ffb6-145">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="4ffb6-146">Frissült a súgófájl, több leírás lett hozzáadva, és javítva lett egy elírás</span><span class="sxs-lookup"><span data-stu-id="4ffb6-146">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="4ffb6-147">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4ffb6-147">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="4ffb6-148">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="4ffb6-148">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="4ffb6-149">Ki lett javítva a hiba, amely során meghiúsult a blobletöltés, ha a megfelelő alkönyvtár nem létezett [#12592]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-149">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="4ffb6-150">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4ffb6-150">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="4ffb6-151">Támogatottá vált a Storage-fiókok objektumreplikációs szabályzatának lekérése/beállítása/eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-151">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="4ffb6-152">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="4ffb6-152">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="4ffb6-153">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="4ffb6-153">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="4ffb6-154">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="4ffb6-154">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="4ffb6-155">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="4ffb6-155">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="4ffb6-156">Támogatottá vált a Blob szolgáltatásbeli változáscsatorna engedélyezése/letiltása a Storage-fiókoknál</span><span class="sxs-lookup"><span data-stu-id="4ffb6-156">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="4ffb6-157">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="4ffb6-157">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="4ffb6-158">4.5.0 – 2020. augusztus</span><span class="sxs-lookup"><span data-stu-id="4ffb6-158">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4ffb6-159">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4ffb6-159">Az.Accounts</span></span>
* <span data-ttu-id="4ffb6-160">„Connect-AzAccount” parancsmag frissítve a „MaxContextPopulation” paraméter elfogadására [#9865]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-160">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="4ffb6-161">A SubscriptionClient-verzió frissítve a 2019. 06. 01. verzióra és a bérlői tartományok megjelenítése [#9838]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-161">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="4ffb6-162">Az előfizetés támogatott otthoni bérlői és managedBy bérlői információi</span><span class="sxs-lookup"><span data-stu-id="4ffb6-162">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="4ffb6-163">A modul neve és a verzió adatai javítva a telemetriai adatokban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-163">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="4ffb6-164">Korrigált SqlDatabaseDnsSuffix és ServiceManagementUrl, ha a környezeti metaadatok végpontja inkompatibilis értéket ad vissza</span><span class="sxs-lookup"><span data-stu-id="4ffb6-164">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="4ffb6-165">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4ffb6-165">Az.Aks</span></span>
* <span data-ttu-id="4ffb6-166">A „ClientIdAndSecret” eltávolítva és lecserélve a ServicePrincipalIdAndSecret parancsmagra, és „ClientIdAndSecret” beállítva aliasként [#12381].</span><span class="sxs-lookup"><span data-stu-id="4ffb6-166">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="4ffb6-167">A „Get-AzAks”/„New-AzAks”/„Remove-AzAks”/„Set-AzAks” eltávolítva és lecserélve a „Get-AzAksCluster”/„New-AzAksCluster”/„Remove-AzAksCluster”/„Set-AzAksCluster” parancsmagra, és az eredetiek beállítva aliasként [#12373].</span><span class="sxs-lookup"><span data-stu-id="4ffb6-167">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4ffb6-168">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4ffb6-168">Az.ApiManagement</span></span>
* <span data-ttu-id="4ffb6-169">Új 'Add-AzApiManagementApiToGateway' parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-169">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="4ffb6-170">Új „Get-AzApiManagementGateway” parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-170">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="4ffb6-171">Új „Get-AzApiManagementGatewayHostnameConfiguration” parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-171">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="4ffb6-172">Új „Get-AzApiManagementGatewayKey” parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-172">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="4ffb6-173">Új „New-AzApiManagementGateway” parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-173">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="4ffb6-174">Új „New-AzApiManagementGatewayHostnameConfiguration” parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-174">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="4ffb6-175">Új „New-AzApiManagementResourceLocationObject” parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-175">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="4ffb6-176">Új „Remove-AzApiManagementApiFromGateway” parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-176">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="4ffb6-177">Új „Remove-AzApiManagementGateway” parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-177">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="4ffb6-178">Új „Remove-AzApiManagementGatewayHostnameConfiguration” parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-178">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="4ffb6-179">Új „Update-AzApiManagementGateway” parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-179">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="4ffb6-180">Új választható [-GatewayId] paramétert hozzáadva a „Get-AzApiManagementApi” parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-180">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4ffb6-181">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-181">Az.CognitiveServices</span></span>
* <span data-ttu-id="4ffb6-182">A „Deny” utasítás kifejezetten a NetworkRules alapértelmezett műveleteként lett használva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-182">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4ffb6-183">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-183">Az.FrontDoor</span></span>
* <span data-ttu-id="4ffb6-184">Kijavítottunk egy hibát, ahol kivétel történt, amikor az Enum.Parse null értéket próbált kényszeríteni egy engedélyezett vagy letiltott enumerálási értékre [#12344]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-184">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4ffb6-185">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4ffb6-185">Az.HDInsight</span></span>
* <span data-ttu-id="4ffb6-186">Támogatott a fürtlétrehozás az átvitel közbeni titkosítási funkcióval.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-186">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="4ffb6-187">Új „EncryptionInTransit” paraméter hozzáadva a „New-AzHDInsightCluster” parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-187">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="4ffb6-188">Új „EncryptionInTransit” paraméter hozzáadva a „New-AzHDInsightClusterConfig” parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-188">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="4ffb6-189">Támogatotta a fürtlétrehozás a privát kapcsolat funkcióval:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-189">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="4ffb6-190">Új „PublicNetworkAccessType” és az „OutboundPublicNetworkAccessType” paraméterek hozzáadva a „New-AzHDInsightCluster” parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-190">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="4ffb6-191">Új „PublicNetworkAccessType” és az „OutboundPublicNetworkAccessType” paraméterek hozzáadva a „New-AzHDInsightClusterConfig” parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-191">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="4ffb6-192">Virtuális hálózati adatok visszaadása a „New-AzHDInsightCluster” vagy a „Get-AzHDInsightCluster” meghívásakor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-192">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4ffb6-193">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-193">Az.Network</span></span>
* <span data-ttu-id="4ffb6-194">Az AddressPrefixType paraméter mostantól támogatott a Remove-AzExpressRouteCircuitConnectionConfig esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-194">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="4ffb6-195">Hozzáadott nem kompatibilitástörő változások: PeerAddressType funkció a privát társviszony-létesítéshez a „Remove-AzExpressRouteCircutPeeringConfig” parancsmagban.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-195">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="4ffb6-196">A kód úgy lett módosítva, hogy figyelmen kívül hagyja az AddressPrefixType és a PeerAddressType paramétert.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-196">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="4ffb6-197">A „New-AzLoadBalancerFrontendIpConfig”, „New-AzPublicIpAddress” és „New-AzPublicIpPrefix” figyelmeztető üzenete módosult.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-197">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4ffb6-198">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4ffb6-198">Az.OperationalInsights</span></span>
* <span data-ttu-id="4ffb6-199">A „-ForceDelete” kapcsoló hozzáadva a „Remove-AzOperationalInsightsworkspace” parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-199">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="4ffb6-200">Új „Get-AzOperationalInsightsDeletedWorkspace” parancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-200">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="4ffb6-201">Új „Restore-AzOperationalInsightsWorkspace” parancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-201">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4ffb6-202">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-202">Az.RecoveryServices</span></span>
* <span data-ttu-id="4ffb6-203">Az Azure Backup tároló-/elemfelderítési funkciója továbbfejlesztve.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-203">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4ffb6-204">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-204">Az.Resources</span></span>
* <span data-ttu-id="4ffb6-205">A „Condition”, a „ConditionVersion” és a „Description” tulajdonság hozzáadva a „New-AzRoleAssignment” parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-205">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="4ffb6-206">Ebbe beletartozik az adatmodellek összes kapcsolódó változása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-206">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="4ffb6-207">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-207">Az.Sql</span></span>
* <span data-ttu-id="4ffb6-208">Ki lett javítva a „New-AzSqlServer” és a „set-AzSqlServer” esetében a kiszolgálónevekben a kis- és nagybetűk meg nem különböztetését eredményező hiba</span><span class="sxs-lookup"><span data-stu-id="4ffb6-208">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="4ffb6-209">A „New-AzSqlDatabaseSecondary” parancsmagban egy meglévő adatbázishiba miatt helytelen adatbázisnevet visszaadó hiba javítva lett</span><span class="sxs-lookup"><span data-stu-id="4ffb6-209">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4ffb6-210">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4ffb6-210">Az.Storage</span></span>
* <span data-ttu-id="4ffb6-211">A tároló/blob SAS-jogkivonat létrehozása támogatott az új x,t engedéllyel</span><span class="sxs-lookup"><span data-stu-id="4ffb6-211">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="4ffb6-212">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="4ffb6-212">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="4ffb6-213">„New-AzStorageContainerSASToken”</span><span class="sxs-lookup"><span data-stu-id="4ffb6-213">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="4ffb6-214">A fiók SAS-jogkivonat létrehozása támogatott az új x,t,f engedéllyel</span><span class="sxs-lookup"><span data-stu-id="4ffb6-214">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="4ffb6-215">„New-AzStorageAccountSASToken”</span><span class="sxs-lookup"><span data-stu-id="4ffb6-215">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="4ffb6-216">Az egyetlen fájlmegosztás használatának lekérése támogatott</span><span class="sxs-lookup"><span data-stu-id="4ffb6-216">Supported get single file share usage</span></span>
    - <span data-ttu-id="4ffb6-217">„Get-AzRmStorageShare”</span><span class="sxs-lookup"><span data-stu-id="4ffb6-217">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="4ffb6-218">4.4.0 – 2020. július</span><span class="sxs-lookup"><span data-stu-id="4ffb6-218">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4ffb6-219">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4ffb6-219">Az.Accounts</span></span>
* <span data-ttu-id="4ffb6-220">Invoke-AzRestMethod új parancsmag hozzáadása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-220">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="4ffb6-221">Kijavítottunk egy olyan problémát, amely hitelesítési hibákat okozhat az olyan többfolyamatos forgatókönyvekben, mint például több Azure PowerShell parancsmag futtatása a Start-Job paranccsal [#9448]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-221">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="4ffb6-222">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4ffb6-222">Az.Aks</span></span>
* <span data-ttu-id="4ffb6-223">Ki lett javítva az a hiba, amely miatt a Get-AzAks nem kér le minden fürtöt [#12296]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-223">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4ffb6-224">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-224">Az.AnalysisServices</span></span>
* <span data-ttu-id="4ffb6-225">A hitelesítés projekthivatkozása eltávolítva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-225">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4ffb6-226">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4ffb6-226">Az.Automation</span></span>
* <span data-ttu-id="4ffb6-227">Ki lett javítva az a hiba, amely miatt a feloldójeleket tartalmazó sztringek nem alakíthatók át JSON-objektummá.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-227">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4ffb6-228">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-228">Az.Compute</span></span>
* <span data-ttu-id="4ffb6-229">Figyelmeztetés jelenik meg a New-AzVmss a „latest” rendszerképverzió nélküli használatakor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-229">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4ffb6-230">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4ffb6-230">Az.DataFactory</span></span>
* <span data-ttu-id="4ffb6-231">Globális paraméterek hozzáadva a Data Factoryhez.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-231">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="4ffb6-232">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4ffb6-232">Az.EventGrid</span></span>
* <span data-ttu-id="4ffb6-233">Frissítve a 2020-06-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-233">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="4ffb6-234">Új funkciók hozzáadva:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-234">Added new features:</span></span>
    - <span data-ttu-id="4ffb6-235">Bemenetleképezés</span><span class="sxs-lookup"><span data-stu-id="4ffb6-235">Input mapping</span></span>
    - <span data-ttu-id="4ffb6-236">Eseménykézbesítési séma</span><span class="sxs-lookup"><span data-stu-id="4ffb6-236">Event Delivery Schema</span></span>
    - <span data-ttu-id="4ffb6-237">Privát kapcsolat</span><span class="sxs-lookup"><span data-stu-id="4ffb6-237">Private Link</span></span>
    - <span data-ttu-id="4ffb6-238">V10 felhő-eseményséma</span><span class="sxs-lookup"><span data-stu-id="4ffb6-238">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="4ffb6-239">Service Bus-témakör célértékként</span><span class="sxs-lookup"><span data-stu-id="4ffb6-239">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="4ffb6-240">Azure-függvény célértékként</span><span class="sxs-lookup"><span data-stu-id="4ffb6-240">Azure Function As Destination</span></span>
    - <span data-ttu-id="4ffb6-241">Webhookkötegelés</span><span class="sxs-lookup"><span data-stu-id="4ffb6-241">WebHook Batching</span></span>
    - <span data-ttu-id="4ffb6-242">Biztonságos webhook (AAD-támogatás)</span><span class="sxs-lookup"><span data-stu-id="4ffb6-242">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="4ffb6-243">IP-szűrés</span><span class="sxs-lookup"><span data-stu-id="4ffb6-243">IpFiltering</span></span>
* <span data-ttu-id="4ffb6-244">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-244">Updated cmdlets:</span></span>
    - <span data-ttu-id="4ffb6-245">New-AzEventGridSubscription/Update-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-245">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="4ffb6-246">Új választható paraméterek lettek hozzáadva a webhookkötegelés támogatásáért.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-246">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="4ffb6-247">Új választható paraméterek lettek hozzáadva a biztonságos webhook AAD-vel való használatának támogatásáért.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-247">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="4ffb6-248">Új felsorolási érték lett hozzáadva az EndpointType paraméterhez az Azure-függvény és a Service Bus-témakör új célértékként való támogatásáért.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-248">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="4ffb6-249">Új választható paraméter lett hozzáadva a kézbesítési sémához.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-249">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="4ffb6-250">New-AzEventGridTopic/Update-AzEventGridTopic és New-AzEventGridDomain/Update-AzEventGridDomain:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-250">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="4ffb6-251">Új választható paraméterek lettek hozzáadva az IP-szűrés támogatásáért.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-251">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="4ffb6-252">New-AzEventGridTopic/New-AzEventGridDomain:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-252">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="4ffb6-253">Új választható paraméterek lettek hozzáadva a bemenetleképezés támogatásáért.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-253">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4ffb6-254">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-254">Az.FrontDoor</span></span>
* <span data-ttu-id="4ffb6-255">Modul frissítve a 2020-05-01-es API-verzió használatára</span><span class="sxs-lookup"><span data-stu-id="4ffb6-255">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="4ffb6-256">Privátkapcsolat-támogatás hozzáadva a Storage-, KeyVault- és Web App Service-erőforrásokhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-256">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4ffb6-257">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4ffb6-257">Az.HDInsight</span></span>
* <span data-ttu-id="4ffb6-258">ADLSGen1/2-tárolóval rendelkező fürt országos felhőkben való létrehozásának támogatása.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-258">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4ffb6-259">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-259">Az.Monitor</span></span>
* <span data-ttu-id="4ffb6-260">Ki lett javítva a Get-AzDiagnosticSetting hibája, amely miatt a metrikák vagy naplók null értékűek [#12272]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-260">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4ffb6-261">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-261">Az.Network</span></span>
* <span data-ttu-id="4ffb6-262">A paraméterek felcserélése ki lett javítva a VWan–HubVnet kapcsolatban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-262">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="4ffb6-263">Új parancsmagok lettek hozzáadva az Azure hálózati virtuális berendezések helyéhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-263">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="4ffb6-264">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="4ffb6-264">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="4ffb6-265">New-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="4ffb6-265">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="4ffb6-266">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="4ffb6-266">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="4ffb6-267">Update-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="4ffb6-267">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="4ffb6-268">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="4ffb6-268">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="4ffb6-269">Új parancsmagok lettek hozzáadva az Azure hálózati virtuális berendezésekhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-269">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="4ffb6-270">Get-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="4ffb6-270">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="4ffb6-271">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="4ffb6-271">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="4ffb6-272">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="4ffb6-272">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="4ffb6-273">Update-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="4ffb6-273">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="4ffb6-274">Get-AzNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="4ffb6-274">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="4ffb6-275">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="4ffb6-275">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="4ffb6-276">Application Gateway előkészítve a Private Link gyakori parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-276">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="4ffb6-277">StorageSync előkészítve a Private Link gyakori parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-277">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="4ffb6-278">SignalR előkészítve a Private Link gyakori parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-278">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4ffb6-279">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-279">Az.RecoveryServices</span></span>
* <span data-ttu-id="4ffb6-280">A hitelesítés projekthivatkozása eltávolítva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-280">Removed project reference to Authentication</span></span>
* <span data-ttu-id="4ffb6-281">Azure Backup-parancsmagok finomhangolása a pontosabb szövegért.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-281">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="4ffb6-282">Az Azure Backup mostantól támogatott az MAB-ügynökfeladatok beolvasásához a Get-AzRecoveryServicesBackupJob parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-282">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4ffb6-283">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-283">Az.Resources</span></span>
* <span data-ttu-id="4ffb6-284">A Save-AzResourceGroupDeploymentTemplate frissítése az SDK használatához.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-284">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="4ffb6-285">Unregister-AzResourceProvider parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-285">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="4ffb6-286">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-286">Az.Sql</span></span>
* <span data-ttu-id="4ffb6-287">Szolgáltatásnév és vendégfelhasználók támogatása hozzáadva a Set-AzSqlInstanceActiveDirectoryAdministrator parancsmagban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-287">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="4ffb6-288">Ki lett javítva egy hiba az adatbesorolási parancsmagokban.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-288">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="4ffb6-289">A felügyelt Azure SQL-példány feladatátvétele mostantól támogatott: Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="4ffb6-289">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4ffb6-290">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4ffb6-290">Az.Storage</span></span>
* <span data-ttu-id="4ffb6-291">Ki lett javítva az a probléma, amely miatt a UserAgent nem adható hozzá egyes adatsíkparancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-291">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="4ffb6-292">Storage-fiók létrehozásának/frissítésének támogatása a MinimumTlsVersion és az AllowBlobPublicAccess használatával</span><span class="sxs-lookup"><span data-stu-id="4ffb6-292">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="4ffb6-293">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ffb6-293">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="4ffb6-294">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ffb6-294">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="4ffb6-295">A Storage-fiókok Blob service-beli verziószámozása engedélyezésének/letiltásának támogatása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-295">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="4ffb6-296">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="4ffb6-296">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="4ffb6-297">Blobok blobverziókkal való listázásának támogatása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-297">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="4ffb6-298">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="4ffb6-298">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="4ffb6-299">Egyetlen blobpillanatkép vagy blobverzió lekérésének/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-299">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="4ffb6-300">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="4ffb6-300">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="4ffb6-301">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="4ffb6-301">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="4ffb6-302">Az Azure.Storage.Blobs 12-es verziójában létrehozott blobobjektum folyamatának támogatása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-302">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="4ffb6-303">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4ffb6-303">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="4ffb6-304">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="4ffb6-304">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="4ffb6-305">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="4ffb6-305">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="4ffb6-306">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4ffb6-306">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="4ffb6-307">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4ffb6-307">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="4ffb6-308">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="4ffb6-308">Az.StorageSync</span></span>
* <span data-ttu-id="4ffb6-309">A 2020-03-01-es API-verziót célzó StorageSync SDK új verziója hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-309">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="4ffb6-310">Tárolószinkronizálási szolgáltatás frissítési parancsmagja hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-310">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="4ffb6-311">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="4ffb6-311">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="4ffb6-312">IncomingTrafficPolicy és PrivateEndpointConnections hozzáadva a StorageSyncService parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-312">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4ffb6-313">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4ffb6-313">Az.Websites</span></span>
* <span data-ttu-id="4ffb6-314">Támogatás hozzáadva az olyan Pontok műveleteinek elvégzéséhez, amelyek nem abban az erőforráscsoportban vannak, amelyben az App Service-csomag</span><span class="sxs-lookup"><span data-stu-id="4ffb6-314">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="4ffb6-315">4.3.0 – 2020. június</span><span class="sxs-lookup"><span data-stu-id="4ffb6-315">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4ffb6-316">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4ffb6-316">Az.Accounts</span></span>
* <span data-ttu-id="4ffb6-317">A környezetfelderítés beállítása és a környezet hozzáadása az Add-AzEnvironment használatával alapértelmezés szerint támogatott</span><span class="sxs-lookup"><span data-stu-id="4ffb6-317">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="4ffb6-318">Előre betöltött szerelvények frissítése [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-318">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="4ffb6-319">Az Azure.Core szerelvény frissült</span><span class="sxs-lookup"><span data-stu-id="4ffb6-319">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="4ffb6-320">Ki lett javítva egy probléma, amely a Connect-AzAccount meghiúsulását okozhatta többszálas végrehajtás esetében [#11201]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-320">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="4ffb6-321">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4ffb6-321">Az.Aks</span></span>
* <span data-ttu-id="4ffb6-322">A régi [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) használata helyébe a [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) és a [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) API-k meghívása lépett</span><span class="sxs-lookup"><span data-stu-id="4ffb6-322">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4ffb6-323">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4ffb6-323">Az.Batch</span></span>
* <span data-ttu-id="4ffb6-324">Frissítve lett az Az.Batch a Microsoft.Azure.Management.Batch SDK 11.0.0-s verziójának használatára</span><span class="sxs-lookup"><span data-stu-id="4ffb6-324">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="4ffb6-325">Hozzá lett adva a BatchAccount identitás beállításának lehetősége a New-AzBatchAccount parancsmagban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-325">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4ffb6-326">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-326">Az.CognitiveServices</span></span>
* <span data-ttu-id="4ffb6-327">A fiók képességeinek megjelenítése támogatott.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-327">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="4ffb6-328">Támogatott a PublicNetworkAccess paraméter módosítása.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-328">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4ffb6-329">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-329">Az.Compute</span></span>
* <span data-ttu-id="4ffb6-330">A SimulateEviction paraméter hozzá lett adva a Set-AzVm és a Set-AzVmssVM parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-330">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="4ffb6-331">A Premium_LRS hozzá lett adva a StorageAccountType paraméter argumentumbefejezőjéhez a New-AzGalleryImageVersion parancsmagban.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-331">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="4ffb6-332">Alállapotok lettek hozzáadva a VMCustomScriptExtension bővítményhez [#11297]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-332">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="4ffb6-333">A Törlés lehetőség hozzá lett adva az EvictionPolicy paraméter argumentumbefejezőjéhez a New-AzVM és a New-AzVMConfig parancsmagokban.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-333">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="4ffb6-334">Az új virtuálisgép-bővítmény neve ki lett javítva az SAP esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-334">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4ffb6-335">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4ffb6-335">Az.DataFactory</span></span>
* <span data-ttu-id="4ffb6-336">Az ADF .Net SDK a 4.9.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="4ffb6-336">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4ffb6-337">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4ffb6-337">Az.EventHub</span></span>
* <span data-ttu-id="4ffb6-338">Managed Identity-paraméterek lettek hozzáadva a New-AzEventHubNamespace és a Set-AzEventHubNamespace parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-338">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="4ffb6-339">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="4ffb6-339">Az.Functions</span></span>
* <span data-ttu-id="4ffb6-340">A PowerShell 7.0- és a Java 11-függvényalkalmazások létrehozása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="4ffb6-340">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4ffb6-341">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4ffb6-341">Az.HDInsight</span></span>
* <span data-ttu-id="4ffb6-342">Támogatott a gazdagépek listázása és a HDInsight-fürt adott gazdagépeinek újraindítása.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-342">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="4ffb6-343">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="4ffb6-343">Az.HealthcareApis</span></span>
* <span data-ttu-id="4ffb6-344">Az SDK a 1.1.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="4ffb6-344">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="4ffb6-345">Az exportálási beállítások és a Managed Identity mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="4ffb6-345">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4ffb6-346">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-346">Az.Monitor</span></span>
* <span data-ttu-id="4ffb6-347">Ki lett javítva a bemeneti objektumparaméter a Set-AzActivityLogAlert parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-347">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="4ffb6-348">Ki lett javítva az InputObject paraméter a Set-AzActionGroup parancsmag esetében [#10868]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-348">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4ffb6-349">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-349">Az.Network</span></span>
* <span data-ttu-id="4ffb6-350">Az AddressPrefixType paraméter mostantól támogatott a Remove-AzExpressRouteCircuitConnectionConfig esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-350">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="4ffb6-351">Új parancsmagok lettek hozzáadva az Azure FirewallPolicy szabályzathoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-351">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="4ffb6-352">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="4ffb6-352">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="4ffb6-353">A tűzfalszabályzathoz tartozó hálózati szabályok céltartományneveinek támogatása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-353">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="4ffb6-354">A háttércímkészlet műveletei mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="4ffb6-354">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="4ffb6-355">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="4ffb6-355">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="4ffb6-356">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4ffb6-356">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="4ffb6-357">Set-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4ffb6-357">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="4ffb6-358">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4ffb6-358">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="4ffb6-359">Get-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4ffb6-359">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="4ffb6-360">A New-AzIpGroup névérvényesítése hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-360">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="4ffb6-361">Új parancsmagok lettek hozzáadva az Azure FirewallPolicy szabályzathoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-361">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="4ffb6-362">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="4ffb6-362">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="4ffb6-363">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: Egyéni DNS-kiszolgálók beállítása/eltávolítása a VirtualWan-P2SVpnGateway átjárón.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-363">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="4ffb6-364">Frissült a New-AzP2sVpnGateway: A -CustomDnsServer opcionális paraméter hozzá lett adva az ügyfelek számára, hogy megadhassák a P2SVpnGateway átjárón beállítani kívánt DNS-kiszolgálókat (ezeket pont–hely ügyfelek is használhatják).</span><span class="sxs-lookup"><span data-stu-id="4ffb6-364">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="4ffb6-365">Frissült az AzP2sVpnGateway: A -CustomDnsServer opcionális paraméter hozzá lett adva az ügyfelek számára, hogy megadhassák a P2SVpnGateway átjárón beállítani kívánt DNS-kiszolgálókat (ezeket pont–hely ügyfelek is használhatják).</span><span class="sxs-lookup"><span data-stu-id="4ffb6-365">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="4ffb6-366">Frissült az Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4ffb6-366">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="4ffb6-367">A -BgpPeeringAddress opcionális paraméter hozzá lett adva az ügyfelek számára a VPN Gateway átjárón beállítani kívánt egyéni bgps megadásához.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-367">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="4ffb6-368">Új parancsmag lett hozzáadva a VirtualHub-erőforrás útválasztási állapota visszaállításának támogatásához:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-368">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="4ffb6-369">Reset-AzHubRouter</span><span class="sxs-lookup"><span data-stu-id="4ffb6-369">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="4ffb6-370">A tűzfalszabályzat legutóbbi Swagger-módosításának megfelelően frissültek az alábbi tételek</span><span class="sxs-lookup"><span data-stu-id="4ffb6-370">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="4ffb6-371">A RuleGroup, a RuleCollectionGroup és a RuleType neve megváltozott</span><span class="sxs-lookup"><span data-stu-id="4ffb6-371">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="4ffb6-372">Mostantól támogatott a tűzfalszabályzat NAT-szabálygyűjteménye esetében több NAT-szabálygyűjtemény használata</span><span class="sxs-lookup"><span data-stu-id="4ffb6-372">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="4ffb6-373">[Kompatibilitástörő változás] Kötelező SourceIpGroup paraméter lett hozzáadva a New-AzFirewallPolicyApplicationRule és a New-AzFirewallPolicyNetworkRule esetében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-373">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="4ffb6-374">[Kompatibilitástörő változás] A New-AzFirewallPolicyApplicationRule ki lett javítva, a SourceAddress paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-374">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="4ffb6-375">[Kompatibilitástörő változás] A New-AzFirewallPolicyApplicationRule ki lett javítva, a SourceAddress paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-375">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="4ffb6-376">[Kompatibilitástörő változás] Eltávolított kötelező paraméterek: TranslatedAddress, TranslatedPort a New-AzFirewallPolicyNatRuleCollection esetében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-376">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="4ffb6-377">Új parancsmagok lettek hozzáadva a PrivateLink támogatásához az Application Gatewayen</span><span class="sxs-lookup"><span data-stu-id="4ffb6-377">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="4ffb6-378">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ffb6-378">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="4ffb6-379">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ffb6-379">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="4ffb6-380">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ffb6-380">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="4ffb6-381">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ffb6-381">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="4ffb6-382">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ffb6-382">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="4ffb6-383">New-AzApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ffb6-383">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="4ffb6-384">Új parancsmagok lettek hozzáadva a VirtualHub HubRouteTables gyermekerőforrásai esetében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-384">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="4ffb6-385">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-385">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="4ffb6-386">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="4ffb6-386">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="4ffb6-387">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="4ffb6-387">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="4ffb6-388">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="4ffb6-388">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="4ffb6-389">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="4ffb6-389">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="4ffb6-390">Frissültek a meglévő parancsmagok az opcionális RoutingConfiguration bemeneti paraméter támogatásához az egyéni útválasztás esetében a VirtualWanban.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-390">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="4ffb6-391">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="4ffb6-391">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="4ffb6-392">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="4ffb6-392">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="4ffb6-393">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="4ffb6-393">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="4ffb6-394">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="4ffb6-394">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="4ffb6-395">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="4ffb6-395">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="4ffb6-396">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="4ffb6-396">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="4ffb6-397">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4ffb6-397">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="4ffb6-398">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4ffb6-398">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4ffb6-399">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4ffb6-399">Az.OperationalInsights</span></span>
* <span data-ttu-id="4ffb6-400">Ki lett javítva az a PSWorkspace-hiba, amely miatt meghiúsult az IOperationalInsightsWorkspace implementálása [#12135]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-400">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="4ffb6-401">A pergb2018 hozzá lett adva az SKU paraméter érvényes értékéhez a Set-AzOperationalInsightsWorkspace esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-401">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="4ffb6-402">A FunctionParameters alias hozzá lett adva a FunctionParameter paraméterhez a következők esetében:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-402">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="4ffb6-403">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="4ffb6-403">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="4ffb6-404">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="4ffb6-404">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4ffb6-405">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-405">Az.RecoveryServices</span></span>
* <span data-ttu-id="4ffb6-406">Az Azure Backup mostantól támogatott az MAB-elemek beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-406">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="4ffb6-407">Az Azure Site Recovery támogatja a StandardSSD_LRS lemeztípust</span><span class="sxs-lookup"><span data-stu-id="4ffb6-407">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="4ffb6-408">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-408">Az.Resources</span></span>
* <span data-ttu-id="4ffb6-409">A UsageLocation, GivenName, Surname, AccountEnabled, MailNickname, Mail paraméterek hozzá lettek adva a PSADUser esetében [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-409">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="4ffb6-410">Ki lett javítva az a hiba, hogy a -Mail nem működött a Get-AzADUser esetében [#11981]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-410">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="4ffb6-411">Az -ExcludeChangeType paraméter hozzá lett adva a következőkhöz: Get-AzDeploymentWhatIfResult és Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="4ffb6-411">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="4ffb6-412">A -WhatIfExcludeChangeType paraméter hozzá lett adva a következőkhöz: New-AzDeployment és New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4ffb6-412">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="4ffb6-413">A Test-Az\*Deployment parancsmagok frissültek a megfelelőbb hibaüzenetek megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-413">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="4ffb6-414">Ki lett javítva az üzemelő példány -Name paraméterének súgóüzenete a create és a What-If parancsmagok esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-414">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="4ffb6-415">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-415">Az.Sql</span></span>
* <span data-ttu-id="4ffb6-416">Szolgáltatásnév támogatása hozzáadva a Set SQL Server Azure Active Directory Admin parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-416">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="4ffb6-417">Ki lett javítva a szinkronizálási probléma az adatbesorolási parancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-417">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="4ffb6-418">Támogatott az e-mail-cím alapján történő felhasználókeresés a következő esetében: Set-AzSqlServerActiveDirectoryAdministrator [#12192]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-418">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4ffb6-419">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4ffb6-419">Az.Storage</span></span>
* <span data-ttu-id="4ffb6-420">Támogatott a tárfiók RequireInfrastructureEncryption használatával való létrehozása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-420">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="4ffb6-421">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ffb6-421">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="4ffb6-422">Át lett helyezve az Azure.Core betöltési logikája Az.Accounts modulba</span><span class="sxs-lookup"><span data-stu-id="4ffb6-422">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4ffb6-423">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4ffb6-423">Az.Websites</span></span>
* <span data-ttu-id="4ffb6-424">Hozzáadott védelem a létrehozott webalkalmazás törléséhez, ha a visszaállítás nem sikerült a Restore-AzDeletedWebApp esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-424">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="4ffb6-425">A SourceWebApp.Location paraméter hozzá lett adva a New-AzWebApp és a New-AzWebAppSlot esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-425">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="4ffb6-426">Ki lett javítva az a hiba, amely megakadályozta a tárolóbeállítások módosítását a Set-AzWebApp és a Set-AzWebAppSlot esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-426">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="4ffb6-427">Ki lett javítva a SiteConfig lekérésének hibája, ha a -Name nem lett megadva a Get-AzWebApp esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-427">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="4ffb6-428">Támogatás hozzáadva ASP létráhozásához Linux-alkalmazások esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-428">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="4ffb6-429">Kivételek hozzáadva az erőforráscsoportok közötti klónozás esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-429">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="4ffb6-430">4.2.0 – 2020. június</span><span class="sxs-lookup"><span data-stu-id="4ffb6-430">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4ffb6-431">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4ffb6-431">Az.Accounts</span></span>
* <span data-ttu-id="4ffb6-432">Kijavítottunk egy problémát, amely miatt az Az Azure Automation-naplókat vagy PowerShell-feladatokat hagyott ki [#11492]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-432">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4ffb6-433">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-433">Az.AnalysisServices</span></span>
* <span data-ttu-id="4ffb6-434">Frissítettük az adatsík parancsmagjainak szerelvényverzióját</span><span class="sxs-lookup"><span data-stu-id="4ffb6-434">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4ffb6-435">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4ffb6-435">Az.ApiManagement</span></span>
* <span data-ttu-id="4ffb6-436">Frissítettük a szolgáltatásfelügyeleti parancsmagok szerelvényverzióját</span><span class="sxs-lookup"><span data-stu-id="4ffb6-436">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="4ffb6-437">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="4ffb6-437">Az.Billing</span></span>
* <span data-ttu-id="4ffb6-438">Frissítettük a felhasználási parancsmagok szerelvényverzióját</span><span class="sxs-lookup"><span data-stu-id="4ffb6-438">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4ffb6-439">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-439">Az.CognitiveServices</span></span>
* <span data-ttu-id="4ffb6-440">A PrivateEndpoint és a PublicNetworkAccess vezérlők támogatása.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-440">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="4ffb6-441">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4ffb6-441">Az.DataFactory</span></span>
* <span data-ttu-id="4ffb6-442">Frissítettük a Data Factory V2 parancsmagjainak szerelvényverzióját</span><span class="sxs-lookup"><span data-stu-id="4ffb6-442">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="4ffb6-443">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="4ffb6-443">Az.DataShare</span></span>
* <span data-ttu-id="4ffb6-444">Az Az.DataShare modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-444">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="4ffb6-445">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="4ffb6-445">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="4ffb6-446">Az „Az.DesktopVirtualization” modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-446">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4ffb6-447">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4ffb6-447">Az.OperationalInsights</span></span>
* <span data-ttu-id="4ffb6-448">SDK frissítve a 0.21.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="4ffb6-448">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="4ffb6-449">Választható paraméterek hozzáadva a következőkhöz:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-449">Added optional parameters to</span></span> 
    - <span data-ttu-id="4ffb6-450">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="4ffb6-450">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="4ffb6-451">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="4ffb6-451">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4ffb6-452">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4ffb6-452">Az.PolicyInsights</span></span>
* <span data-ttu-id="4ffb6-453">Javítottuk a Start-AzPolicyComplianceScan 3. példáját</span><span class="sxs-lookup"><span data-stu-id="4ffb6-453">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="4ffb6-454">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="4ffb6-454">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="4ffb6-455">Frissítettük a PowerBI-parancsmagok szerelvényverzióját</span><span class="sxs-lookup"><span data-stu-id="4ffb6-455">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="4ffb6-456">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="4ffb6-456">Az.PrivateDns</span></span>
* <span data-ttu-id="4ffb6-457">Javítottuk a Remove-AzPrivateDnsRecordSet kimeneti sztringjének formázását</span><span class="sxs-lookup"><span data-stu-id="4ffb6-457">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4ffb6-458">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-458">Az.RecoveryServices</span></span>
* <span data-ttu-id="4ffb6-459">Azure Site Recovery-támogatás helyreállítási terv létrehozásához az xml-bemenetből kezdeményezett, zónák közötti replikáció esetében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-459">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="4ffb6-460">Frissítettük a SiteRecovery és a Backup parancsmagok szerelvényverzióját</span><span class="sxs-lookup"><span data-stu-id="4ffb6-460">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="4ffb6-461">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-461">Az.Resources</span></span>
* <span data-ttu-id="4ffb6-462">Szélsőérték paraméter hozzáadva a Get-AzDeploymentScriptLog és a Save-AzDeploymentScriptLog parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-462">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="4ffb6-463">Kimeneti tulajdonság formázása és megjelenítése a Get-AzDeploymentScript parancsmag kimenetén</span><span class="sxs-lookup"><span data-stu-id="4ffb6-463">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="4ffb6-464">A -DeploymentScriptInputObject paraméter új neve -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="4ffb6-464">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="4ffb6-465">Javítottuk a parancsmagüzenetek hiányzó fájl-/célnevét.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-465">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="4ffb6-466">Frissítettük a Resource Manager és a címkék parancsmagjainak szerelvényverzióját</span><span class="sxs-lookup"><span data-stu-id="4ffb6-466">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="4ffb6-467">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-467">Az.Sql</span></span>
* <span data-ttu-id="4ffb6-468">UsePrivateLinkConnection hozzáadva a következőkhöz: New-AzSqlSyncGroup, Update-AzSqlSyncGroup, New-AzSqlSyncMember és Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="4ffb6-468">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="4ffb6-469">SyncMemberAzureDatabaseResourceId hozzáadva a következőkhöz: New-AzSqlSyncMember és Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="4ffb6-469">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="4ffb6-470">Vendégfelhasználó-keresés támogatása hozzáadva a Set SQL Server Azure Active Directory Admin parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-470">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4ffb6-471">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4ffb6-471">Az.Storage</span></span>
* <span data-ttu-id="4ffb6-472">Frissítettük az adatsík parancsmagjainak szerelvényverzióját</span><span class="sxs-lookup"><span data-stu-id="4ffb6-472">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="4ffb6-473">4.1.0 – 2020. május</span><span class="sxs-lookup"><span data-stu-id="4ffb6-473">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="4ffb6-474">A legutóbbi kiadás óta bevezetett újdonságok</span><span class="sxs-lookup"><span data-stu-id="4ffb6-474">Highlights since the last release</span></span>
* <span data-ttu-id="4ffb6-475">Támogatott PowerShell-verziók: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="4ffb6-475">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="4ffb6-476">Az Az.Functions általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-476">General availability of Az.Functions</span></span> 
* <span data-ttu-id="4ffb6-477">A következők rendelkeznek nagyobb kiadással: Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources és Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4ffb6-477">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4ffb6-478">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4ffb6-478">Az.Accounts</span></span>
* <span data-ttu-id="4ffb6-479">Frissítve lett az Add-AzEnvironment és a Set-AzEnvironment parancsmag, amelyek mostantól elfogadják az AzureSynapseAnalyticsEndpointResourceId és az AzureSynapseAnalyticsEndpointSuffix paramétereket</span><span class="sxs-lookup"><span data-stu-id="4ffb6-479">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="4ffb6-480">Hozzá lettek adva az Azure.Core-hoz kapcsolódó szerelvények az Az.Accounts-hoz, a támogatott platformok a Windows PowerShell 5.1, a PowerShell Core 6.2.4 és a PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="4ffb6-480">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="4ffb6-481">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4ffb6-481">Az.Aks</span></span>
* <span data-ttu-id="4ffb6-482">Az API-verzió frissítve lett a 2019-10-01-es verzióra</span><span class="sxs-lookup"><span data-stu-id="4ffb6-482">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="4ffb6-483">Az AKS Windows-tárolókkal történő létrehozásának támogatása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-483">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="4ffb6-484">Elérhető új parancsmagok: New-AzAksNodePool, Update-AzAksNodePool, Remove-AzAksNodePool,        Get-AzAksNodePool, Install-AzAksKubectl, Get-AzAksVersion</span><span class="sxs-lookup"><span data-stu-id="4ffb6-484">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4ffb6-485">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4ffb6-485">Az.ApiManagement</span></span>
* <span data-ttu-id="4ffb6-486">New-AzApiManagement és Set-AzApiManagement: az [-AssignIdentity] paraméter új neve [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-486">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="4ffb6-487">New-AzApiManagement és Set-AzApiManagement: Új paraméter lett hozzáadva: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-487">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="4ffb6-488">A Get-AzApiManagementProperty át lett nevezve a következőre: Get-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-488">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="4ffb6-489">A PropertyId paraméter át lett nevezve a következőre: NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-489">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="4ffb6-490">A New-AzApiManagementProperty át lett nevezve a következőre: New-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-490">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="4ffb6-491">A PropertyId paraméter át lett nevezve a következőre: NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-491">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="4ffb6-492">A Set-AzApiManagementProperty át lett nevezve a következőre: Set-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-492">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="4ffb6-493">A PropertyId paraméter át lett nevezve a következőre: NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-493">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="4ffb6-494">A Remove-AzApiManagementProperty át lett nevezve a következőre: Remove-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-494">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="4ffb6-495">A PropertyId paraméter át lett nevezve a következőre: NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-495">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="4ffb6-496">Hozzá lett adva az új Get-AzApiManagementAuthorizationServerClientSecret parancsmag, valamint a Get-AzApiManagementAuthorizationServer már nem ad vissza titkos ügyfélkulcsot.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-496">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="4ffb6-497">Hozzá lett adva az új Get-AzApiManagementNamedValueSecretValue parancsmag, és a Get-AzApiManagementNamedValue nem ad vissza titkos kulcsot.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-497">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="4ffb6-498">Hozzá lett adva az új Get-AzApiManagementOpenIdConnectProviderClientSecret parancsmag, valamint a Get-AzApiManagementOpenIdConnectProvider már nem ad vissza titkos ügyfélkulcsot.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-498">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="4ffb6-499">Hozzá lett adva az új Get-AzApiManagementSubscriptionKey parancsmag, és a Get-AzApiManagementSubscription már nem ad vissza előfizetési azonosítót.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-499">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="4ffb6-500">Hozzá lett adva az új Get-AzApiManagementTenantAccessSecret parancsmag, és a Get-AzApiManagementTenantAccess már nem ad vissza kulcsot.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-500">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="4ffb6-501">Hozzá lett adva az új Get-AzApiManagementTenantGitAccessSecret parancsmag, és a Get-AzApiManagementTenantGitAccess már nem ad vissza kulcsot.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-501">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="4ffb6-502">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="4ffb6-502">Az.ApplicationInsights</span></span>
* <span data-ttu-id="4ffb6-503">Hozzáadott paraméterek: A New-AzApplicationInsights esetében: RetentionInDays, PublicNetworkAccessForIngestion, PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="4ffb6-503">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="4ffb6-504">Létre lett hozva az Update-AzApplicationInsights parancsmag</span><span class="sxs-lookup"><span data-stu-id="4ffb6-504">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="4ffb6-505">Parancsmagok lettek létrehozva a társított tárfiókhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-505">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4ffb6-506">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4ffb6-506">Az.Batch</span></span>
* <span data-ttu-id="4ffb6-507">Frissítve lett az Az.Batch a Microsoft.Azure.Batch SDK 13.0.0.-s verziójának és a Microsoft.Azure.Management.Batch SDK 9.0.0-s verziójának használatára.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-507">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="4ffb6-508">Kiválaszthatóvá vált a hozzáadni kívánt tanúsítvány típusa a New-AzBatchCertificate új -CertificateKind paraméterének használatával.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-508">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="4ffb6-509">El lett távolítva az ApplicationPackages tulajdonság a PSApplicationből, amelynek típusa eddig mindig '' volt.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-509">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="4ffb6-510">Most már lekérhetők az alkalmazásokon belüli adott csomagok a Get-AzBatchApplicationPackage használatával.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-510">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="4ffb6-511">Például: Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-511">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="4ffb6-512">Egy készlet New-AzBatchPool használatával történő létrehozásakor a PSImageReference VirtualMachineImageId tulajdonsága már csak a Shared Image Gallery-ben található rendszerképre hivatkozhat.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-512">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="4ffb6-513">Egy készlet New-AzBatchPool használatával történő létrehozásakor a készlet nyilvános IP-cím nélkül is létrehozható a PSNetworkConfiguration új PublicIPAddressConfiguration tulajdonságával.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-513">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="4ffb6-514">A PSNetworkConfiguration PublicIPs tulajdonsága a PSPublicIPAddressConfiguration esetében is elérhető.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-514">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="4ffb6-515">Ez a tulajdonság csak akkor adható meg, ha az IPAddressProvisioningType UserManaged típusú.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-515">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4ffb6-516">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-516">Az.Compute</span></span>
* <span data-ttu-id="4ffb6-517">A HostId paraméter hozzá lett adva az Update-AzVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-517">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="4ffb6-518">Frissültek a New-AzVMConfig, New-AzVmssConfig, Update-AzVmss, Set-AzVMOperatingSystem és Set-AzVmssOsProfile parancsmagok súgódokumentumai.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-518">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="4ffb6-519">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="4ffb6-519">Breaking changes</span></span>
    - <span data-ttu-id="4ffb6-520">A FilterExpression paraméter el lett távolítva a Get-AzVMImage parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-520">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="4ffb6-521">Az AssignIdentity paraméter el lett távolítva a New-AzVmssConfig, New-AzVMConfig és Update-AzVM parancsmagokból.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-521">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="4ffb6-522">Az AutomaticRepairMaxInstanceRepairsPercent paraméter el lett távolítva a New-AzVmssConfig és az Update-AzVmss parancsmagokból.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-522">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="4ffb6-523">Az AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus és VirtualMachineScaleSetsColocationStatus tulajdonságok el lettek távolítva a ProximityPlacementGroup paraméterből.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-523">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="4ffb6-524">A MaxInstanceRepairsPercent tulajdonság el lett távolítva a következőből: AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-524">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="4ffb6-525">Az AvailabilitySets, VirtualMachines és VirtualMachineScaleSets típusa IList<SubResource> helyett mostantól IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-525">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="4ffb6-526">Frissült a Get-AzVM parancsmag leírása, hogy pontosabban ismertesse a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-526">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="4ffb6-527">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4ffb6-527">Az.DataFactory</span></span>
* <span data-ttu-id="4ffb6-528">Adatfolyam futtatókörnyezeti tulajdonságaihoz tartozó CRUD támogatása a felügyelt IR-ben.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-528">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4ffb6-529">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-529">Az.FrontDoor</span></span>
* <span data-ttu-id="4ffb6-530">Új parancsmagok lettek hozzáadva a Front Door szabálymotor-objektumának létrehozására, frissítésére, lekérésére és törlésére.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-530">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="4ffb6-531">Hozzá lettek adva segítő parancsmagok a Front Door szabálymotor-objektumának létrehozásához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-531">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="4ffb6-532">Hozzá lett adva a szabálymotor-referencia a Front Door útválasztásiszabály-objektumához.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-532">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="4ffb6-533">Hozzá lettek adva privát kapcsolati paraméterek a Front Door háttérobjektumához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-533">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="4ffb6-534">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="4ffb6-534">Az.Functions</span></span>
* <span data-ttu-id="4ffb6-535">Az Az.Functions modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-535">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4ffb6-536">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4ffb6-536">Az.HDInsight</span></span>
* <span data-ttu-id="4ffb6-537">Az ügyfél által felügyelt kulcson alapuló lemeztitkosítás mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-537">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="4ffb6-538">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="4ffb6-538">Az.HealthcareApis</span></span>
* <span data-ttu-id="4ffb6-539">A hozzáférési szabályzatok már nem tartoznak alapértelmezés szerint az aktuális rendszerbiztonsági taghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-539">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4ffb6-540">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4ffb6-540">Az.IotHub</span></span>
* <span data-ttu-id="4ffb6-541">Hozzá lett adva egy parancsmag, amellyel egy SQL-szerű nyelv használatával végzett, információkat lekérő lekérdezés indítható el az IoT Hubban.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-541">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="4ffb6-542">Javítva a hiba, amely miatt az Add-AzIotHubDevice gyermekeszköz nélkül nem tudott Edge-kompatibilis eszközt létrehozni [#11597]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-542">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="4ffb6-543">Hozzá lett adva egy parancsmag egy SAS-token létrehozásához az IoT Hub, eszköz vagy modul számára.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-543">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="4ffb6-544">Hozzá lett adva egy parancsmag a konfiguráció-metrikák lekérdezésének meghívásához.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-544">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="4ffb6-545">Az IoT Edge nagy léptékű automatikus üzembe helyezésének kezelése.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-545">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="4ffb6-546">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-546">New cmdlets are:</span></span>
    - <span data-ttu-id="4ffb6-547">Add-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="4ffb6-547">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="4ffb6-548">Get-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="4ffb6-548">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="4ffb6-549">Remove-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="4ffb6-549">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="4ffb6-550">Set-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="4ffb6-550">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="4ffb6-551">Hozzá lett adva egy parancsmag, amellyel az IoT Edge üzembehelyezési metrikáit lekérő lekérdezést hívható meg.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-551">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="4ffb6-552">Hozzá lett adva egy parancsmag a konfiguráció tartalmának egy adott Edge-eszközre történő alkalmazásához.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-552">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4ffb6-553">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4ffb6-553">Az.KeyVault</span></span>
* <span data-ttu-id="4ffb6-554">A következő két alias el lett távolítva: New-AzKeyVaultCertificateAdministratorDetails és New-AzKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="4ffb6-554">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="4ffb6-555">Alapértelmezés szerint engedélyezve lett a helyreállítható törlés egy kulcstartó létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-555">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="4ffb6-556">Kulcstartó létrehozásakor a hálózati szabályok beállíthatók a megadott hálózati helyekről való hozzáférés szabályozására</span><span class="sxs-lookup"><span data-stu-id="4ffb6-556">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="4ffb6-557">A saját kulcs használata (BYOK) már támogatott</span><span class="sxs-lookup"><span data-stu-id="4ffb6-557">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="4ffb6-558">Az Add-AzKeyVaultKey támogatja a kulcscserekulcsok létrehozását</span><span class="sxs-lookup"><span data-stu-id="4ffb6-558">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="4ffb6-559">A Get-AzKeyVaultKey támogatja a nyilvános kulcsok PEM formátumban való letöltését</span><span class="sxs-lookup"><span data-stu-id="4ffb6-559">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="4ffb6-560">Frissült az Add-AzKeyVaultKey súgódokumentációjának KeyOps része</span><span class="sxs-lookup"><span data-stu-id="4ffb6-560">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4ffb6-561">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-561">Az.Monitor</span></span>
* <span data-ttu-id="4ffb6-562">Javítva a Set-AzDiagnosticSettings hibája, amely miatt a megtartási szabályzat nem vonatkozott minden kategóriára [#11589]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-562">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="4ffb6-563">A WebTest rendelkezésre állási feltételeinek támogatása a 2-es verziójú metrikariasztás esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-563">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="4ffb6-564">New-AzMetricAlertRuleV2Criteria: mostantól megadhatók a webteszt rendelkezésre állási feltételei</span><span class="sxs-lookup"><span data-stu-id="4ffb6-564">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="4ffb6-565">Add-AzMetricAlertRuleV2: támogatja a webteszt új rendelkezésre állási feltételeit</span><span class="sxs-lookup"><span data-stu-id="4ffb6-565">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="4ffb6-566">El lett távolítva a RetentionPolicy redundáns definíciója a PSLogProfile-ból [#7608]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-566">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="4ffb6-567">El lettek távolítva a PSEventData objektumban meghatározott redundáns tulajdonságok [#11353]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-567">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="4ffb6-568">A Get-Azlog át lett nevezve a következőre: Get-AzActivityLog</span><span class="sxs-lookup"><span data-stu-id="4ffb6-568">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4ffb6-569">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-569">Az.Network</span></span>
* <span data-ttu-id="4ffb6-570">Kompatibilitástörő változást okozó attribútum lett hozzáadva, amely figyelmeztet a Zone alapértelmezett viselkedésének változásáról</span><span class="sxs-lookup"><span data-stu-id="4ffb6-570">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="4ffb6-571">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4ffb6-571">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="4ffb6-572">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4ffb6-572">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="4ffb6-573">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4ffb6-573">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="4ffb6-574">Hozzá lett adva az új, SecurityPartnerProvider legfelsőbb szintű erőforrás támogatása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-574">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="4ffb6-575">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-575">New cmdlets added:</span></span>
        - <span data-ttu-id="4ffb6-576">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="4ffb6-576">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="4ffb6-577">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="4ffb6-577">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="4ffb6-578">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="4ffb6-578">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="4ffb6-579">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="4ffb6-579">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="4ffb6-580">Hozzá lett adva a RequiredZoneNames tulajdonság a PSPrivateLinkResource esetében, és a GroupId a PSPrivateEndpointConnection esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-580">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="4ffb6-581">Kijavítva a SuccessThresholdRoundTripTimeMs paraméter típusa a New-AzNetworkWatcherConnectionMonitorTestConfigurationObject esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-581">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="4ffb6-582">Frissítve lettek a VirtualWan parancsmagok az AllowVnetToVnetTraffic argumentum True értékre való állításához.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-582">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="4ffb6-583">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="4ffb6-583">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="4ffb6-584">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="4ffb6-584">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="4ffb6-585">Új parancsmagok lettek hozzáadva a privát végpontok DNS-zónacsoportjainak támogatásához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-585">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="4ffb6-586">New-AzPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="4ffb6-586">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="4ffb6-587">Get-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="4ffb6-587">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="4ffb6-588">New-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="4ffb6-588">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="4ffb6-589">Set-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="4ffb6-589">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="4ffb6-590">Remove-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="4ffb6-590">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="4ffb6-591">Hozzá lett adva a DNSEnableProxy, a DNSRequireProxyForNetworkRules és a DNSServers paraméter az AzureFirewall-hoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-591">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="4ffb6-592">Hozzá lett adva az EnableDnsProxy, a DnsProxyNotRequiredForNetworkRule és a DnsServer paraméter az AzureFirewall-hoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-592">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="4ffb6-593">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-593">Updated cmdlet:</span></span>
        - <span data-ttu-id="4ffb6-594">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4ffb6-594">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4ffb6-595">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4ffb6-595">Az.OperationalInsights</span></span>
* <span data-ttu-id="4ffb6-596">Frissítve lett a régi kód az újonnan létrehozott SDK alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-596">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="4ffb6-597">Az elavult API-k miatt törölt parancsmagok</span><span class="sxs-lookup"><span data-stu-id="4ffb6-597">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="4ffb6-598">Get-AzOperationalInsightsSavedSearchResult (alias: Get-AzOperationalInsightsSavedSearchResults)</span><span class="sxs-lookup"><span data-stu-id="4ffb6-598">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="4ffb6-599">Get-AzOperationalInsightsSearchResult (alias: Get-AzOperationalInsightsSearchResults)</span><span class="sxs-lookup"><span data-stu-id="4ffb6-599">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="4ffb6-600">Get-AzOperationalInsightsLinkTarget (alias: Get-AzOperationalInsightsLinkTargets)</span><span class="sxs-lookup"><span data-stu-id="4ffb6-600">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="4ffb6-601">Paraméterek lettek hozzáadva a Set-AzOperationalInsightsWorkspace és New-AzOperationalInsightsWorkspace parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-601">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="4ffb6-602">Parancsmagok lettek létrehozva a társított tárfiókhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-602">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="4ffb6-603">Parancsmagok lettek létrehozva a fürtökhöz és a társított szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-603">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4ffb6-604">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-604">Az.RecoveryServices</span></span>
* <span data-ttu-id="4ffb6-605">Hozzá lett adva az Azure Site Recovery-támogatás a közelségi elhelyezési csoportokban lévő virtuális gépek védelme érdekében, az Azure–Azure szolgáltatók esetében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-605">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="4ffb6-606">Hozzá lett adva az Azure Site Recovery-támogatás a zónák közötti replikáció esetében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-606">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="4ffb6-607">Az Azure Backup már támogatja a hosszú távú megőrzést az Azure FileShare helyreállítási pontok esetében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-607">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="4ffb6-608">Hozzá lettek adva az Azure Backup lemezkizárási tulajdonságok a Get-AzRecoveryServicesBackupItem parancsmag kimenetéhez.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-608">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="4ffb6-609">Hozzá lett adva a privát végpont a Vault hitelesítési fájljaihoz a Site Recovery szolgáltatás esetében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-609">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4ffb6-610">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-610">Az.Resources</span></span>
* <span data-ttu-id="4ffb6-611">Hozzá lett adva a megtekintés késéséről figyelmeztető üzenet az új szerepkör-definíció létrehozása során</span><span class="sxs-lookup"><span data-stu-id="4ffb6-611">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="4ffb6-612">Módosítva lettek a szabályzat-parancsmagok a szigorú típusmegadású objektumok megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-612">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="4ffb6-613">El lett távolítva a Get-AzResourceLock parancsmaghoz használt -TenantLevel paraméter [#11335]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-613">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="4ffb6-614">Javítva a Remove-AzResourceGroup -Id ResourceId parancsmag [#9882]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-614">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="4ffb6-615">Hozzá lett adva egy új parancsmag az ARM-sablon What-If típusú eredményeinek lekéréséhez az erőforráscsoport hatókörében: Get-AzDeploymentResourceGroupWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="4ffb6-615">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="4ffb6-616">Hozzá lett adva egy új parancsmag az ARM-sablonok What-If típusú eredményeinek lekéréséhez az előfizetés hatókörében: Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="4ffb6-616">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="4ffb6-617">Alias: Get-AzSubscriptionDeploymentWhatIf</span><span class="sxs-lookup"><span data-stu-id="4ffb6-617">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="4ffb6-618">A -WhatIf és a -Confirm paraméter felül lett írva a New-AzDeployment és a New-AzResourceGroupDeployment parancsmagok esetében az ARM-sablon What-If típusú eredményeinek használata érdekében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-618">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="4ffb6-619">Hozzá lett adva az elavulási üzenet az ApiVersion paraméterhez az üzembehelyezési parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-619">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="4ffb6-620">Hozzá lett adva egy képesség, amely lehetővé teszi, hogy fejlettebb hibaüzenetek jelenjenek meg az üzembehelyezési hibák esetén</span><span class="sxs-lookup"><span data-stu-id="4ffb6-620">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="4ffb6-621">Hozzá lett adva a correlationId-naplózása az üzembehelyezési hibák esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-621">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="4ffb6-622">Hozzá lett adva az error tulajdonság az üzembehelyezési szkript kimenetéhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-622">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="4ffb6-623">A Microsoft.Azure.Management.ResourceManager NuGet frissítve lett a 3.7.1-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="4ffb6-623">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="4ffb6-624">El lettek távolítva adott tesztesetek, mivel a DeploymentValidateResult Error tulajdonsága csak olvasható állapotúra változott a NuGet 3.7.1-preview verziójától kezdődően</span><span class="sxs-lookup"><span data-stu-id="4ffb6-624">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="4ffb6-625">A GenericResourceExpanded át lett hozva a ResourceManager SDK 3.7.1-preview verziójából</span><span class="sxs-lookup"><span data-stu-id="4ffb6-625">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="4ffb6-626">Hozzá lett adva a címketámogatás az összes, üzembe helyezéshez használt Get parancsmaghoz, valamint a következőkhöz:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-626">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="4ffb6-627">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="4ffb6-627">'New-AzDeployment'</span></span>
    - <span data-ttu-id="4ffb6-628">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4ffb6-628">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="4ffb6-629">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4ffb6-629">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="4ffb6-630">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="4ffb6-630">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4ffb6-631">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4ffb6-631">Az.ServiceFabric</span></span>
* <span data-ttu-id="4ffb6-632">Javítva a hiba, amely hibás tanúsítvány-ujjlenyomatot kért le a tanúsítvány --SecretIdentifier használatával történő hozzáadásakor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-632">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="4ffb6-633">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-633">Az.Sql</span></span>
* <span data-ttu-id="4ffb6-634">Javult a következők teljesítménye:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-634">Enhance performance of:</span></span>
    - <span data-ttu-id="4ffb6-635">Set-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="4ffb6-635">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="4ffb6-636">Set-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="4ffb6-636">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="4ffb6-637">Remove-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="4ffb6-637">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="4ffb6-638">Remove-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="4ffb6-638">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="4ffb6-639">Enable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="4ffb6-639">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="4ffb6-640">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="4ffb6-640">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="4ffb6-641">Disable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="4ffb6-641">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="4ffb6-642">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="4ffb6-642">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="4ffb6-643">El lett távolítva a RetentionDays paraméter ügyféloldali érvényesítése a Set-AzSqlDatabaseBackupShortTermRetentionPolicy parancsmagból</span><span class="sxs-lookup"><span data-stu-id="4ffb6-643">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="4ffb6-644">A Vnet-ben található tárfiók naplózása, javítva a Storage Blob-adatok közreműködői szerepkörének létrehozásakor fellépő hiba.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-644">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4ffb6-645">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4ffb6-645">Az.Storage</span></span>
* <span data-ttu-id="4ffb6-646">Hozzá lett adva az -AsJob a fiók Get-AzStorageAccount parancsmagjának lekéréséhez vagy listázásához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-646">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="4ffb6-647">A KeyVersion választható lett a Storage-fiók KeyvaultEncryption használatával történő frissítésekor a kulcs automatikus rotálásának támogatásához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-647">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="4ffb6-648">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ffb6-648">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="4ffb6-649">Javítva a hiba, amely során az Azure File Directory eltávolítása egy folyamattal meghiúsult</span><span class="sxs-lookup"><span data-stu-id="4ffb6-649">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="4ffb6-650">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="4ffb6-650">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="4ffb6-651">[#9880] javítva: Módosítva lett a NetWorkRule DefaultAction értékdefiníciója, hogy megfeleljen a Swaggernek.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-651">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="4ffb6-652">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="4ffb6-652">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="4ffb6-653">Get-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="4ffb6-653">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="4ffb6-654">[#11624] javítva: Duplikált szabályok kihagyása NetworkRules hozzáadásakor a kiszolgáló meghibásodásának elkerülése érdekében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-654">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="4ffb6-655">Add-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4ffb6-655">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="4ffb6-656">A Microsoft.Azure.Cosmos.Table SDK verziója 1.0.7-re frissült</span><span class="sxs-lookup"><span data-stu-id="4ffb6-656">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="4ffb6-657">Hozzá lett adva egy figyelmeztető üzenet, amely emlékezteti a felhasználót, hogy listázzon újra a ContinuationToken használatával, ha csak részleges elemeket ad vissza a rendszer a Data Lake Gen2 elemek listáján</span><span class="sxs-lookup"><span data-stu-id="4ffb6-657">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="4ffb6-658">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="4ffb6-658">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="4ffb6-659">Storage-fiók létrehozásának és frissítésének támogatása Azure Files Active Directory Domain Service-hitelesítéssel</span><span class="sxs-lookup"><span data-stu-id="4ffb6-659">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="4ffb6-660">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ffb6-660">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="4ffb6-661">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ffb6-661">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="4ffb6-662">Storage-fiók Kerberos-kulcsai listázásának vagy új Kerberos-kulcsok létrehozásának támogatása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-662">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="4ffb6-663">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="4ffb6-663">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="4ffb6-664">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="4ffb6-664">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="4ffb6-665">Feladatátvételi Storage-fiók támogatása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-665">Supported failover Storage account</span></span>
    - <span data-ttu-id="4ffb6-666">Invoke-AzStorageAccountFailover</span><span class="sxs-lookup"><span data-stu-id="4ffb6-666">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="4ffb6-667">Frissítve a Get-AzStorageBlobCopyState súgója</span><span class="sxs-lookup"><span data-stu-id="4ffb6-667">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="4ffb6-668">Frissítve a Get-AzStorageFileCopyState és a Start-AzStorageBlobCopy súgója</span><span class="sxs-lookup"><span data-stu-id="4ffb6-668">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="4ffb6-669">A Storage-ügyfélkódtár 12-es verziója integrálva lett a Queue és a File parancsmagokba</span><span class="sxs-lookup"><span data-stu-id="4ffb6-669">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="4ffb6-670">A kimenet típusa CloudFile helyett mostantól AzureStorageFile, az eredeti kimenet az új kimenet gyermektulajdonsága lesz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-670">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="4ffb6-671">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="4ffb6-671">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="4ffb6-672">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="4ffb6-672">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="4ffb6-673">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4ffb6-673">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="4ffb6-674">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4ffb6-674">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="4ffb6-675">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="4ffb6-675">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="4ffb6-676">A kimenet típusa CloudFileDirectory helyett mostantól AzureStorageFileDirectory, az eredeti kimenet az új kimenet gyermektulajdonsága lesz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-676">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="4ffb6-677">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="4ffb6-677">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="4ffb6-678">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="4ffb6-678">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="4ffb6-679">A kimenet típusa CloudFileShare helyett mostantól AzureStorageFileShare, az eredeti kimenet az új kimenet gyermektulajdonsága lesz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-679">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="4ffb6-680">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="4ffb6-680">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="4ffb6-681">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="4ffb6-681">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="4ffb6-682">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="4ffb6-682">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="4ffb6-683">A kimenet típusa FileShareProperties helyett mostantól AzureStorageFileShare, az eredeti kimenet az új kimenet gyermek-altulajdonsága lesz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-683">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="4ffb6-684">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="4ffb6-684">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="4ffb6-685">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="4ffb6-685">Az.TrafficManager</span></span>
* <span data-ttu-id="4ffb6-686">Javítva a hibás profilnév a DisableAzureTrafficManagerEndpoint részletes kimenetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-686">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4ffb6-687">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4ffb6-687">Az.Websites</span></span>
* <span data-ttu-id="4ffb6-688">Javítva az elgépelés az Update-AzWebAppAccessRestrictionConfig súgójában.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-688">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="4ffb6-689">3.8.0 – 2020. április</span><span class="sxs-lookup"><span data-stu-id="4ffb6-689">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="4ffb6-690">A legutóbbi kiadás óta bevezetett újdonságok</span><span class="sxs-lookup"><span data-stu-id="4ffb6-690">Highlights since the last release</span></span>
* <span data-ttu-id="4ffb6-691">Az Az.Storage által támogatott PowerShell-verziók: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="4ffb6-691">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4ffb6-692">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4ffb6-692">Az.Accounts</span></span>
* <span data-ttu-id="4ffb6-693">Frissítve lett az Azure PowerShell-felmérés URL-címe a következő helyen: Resolve-AzError [#11507]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-693">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4ffb6-694">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4ffb6-694">Az.ApiManagement</span></span>
* <span data-ttu-id="4ffb6-695">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó értesítés az Azure File parancsmagok kimenetére vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-695">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="4ffb6-696">Set-AzApiManagementGroup – Frissítve lett a dokumentáció a GroupId paraméter meghatározása érdekében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-696">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4ffb6-697">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4ffb6-697">Az.Cdn</span></span>
* <span data-ttu-id="4ffb6-698">Ki lett javítva a díjszabási termékváltozat megjelenítése a ChinaCDN kapcsán</span><span class="sxs-lookup"><span data-stu-id="4ffb6-698">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4ffb6-699">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-699">Az.CognitiveServices</span></span>
* <span data-ttu-id="4ffb6-700">Támogatott identitás, Titkosítás, UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="4ffb6-700">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4ffb6-701">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-701">Az.Compute</span></span>
* <span data-ttu-id="4ffb6-702">Hozzá lett adva a Set-AzVmssOrchestrationServiceState parancsmag.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-702">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="4ffb6-703">A Get-AzVmss az InstanceView használatával az OrchestrationService állapotait mutatja.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-703">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4ffb6-704">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4ffb6-704">Az.IotHub</span></span>
* <span data-ttu-id="4ffb6-705">Az IoT-ikereszköz konfigurációjának kezelése, Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-705">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="4ffb6-706">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="4ffb6-706">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="4ffb6-707">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="4ffb6-707">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="4ffb6-708">Hozzá lett adva egy parancsmag a közvetlen metódusok az IoT Hubban lévő eszközökön való meghívásához.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-708">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="4ffb6-709">Az IoT-ikereszköz modulja konfigurációjának kezelése, Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-709">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="4ffb6-710">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="4ffb6-710">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="4ffb6-711">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="4ffb6-711">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="4ffb6-712">Nagy méretekben történő automatikus IoT-eszközfelügyelet konfigurációjának kezelése.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-712">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="4ffb6-713">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-713">New cmdlets are:</span></span>
    - <span data-ttu-id="4ffb6-714">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ffb6-714">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="4ffb6-715">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ffb6-715">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="4ffb6-716">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ffb6-716">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="4ffb6-717">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ffb6-717">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="4ffb6-718">Hozzá lett adva egy parancsmag az Edge-modul metódusok az IoT Hubban való meghívásához.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-718">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4ffb6-719">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4ffb6-719">Az.KeyVault</span></span>
* <span data-ttu-id="4ffb6-720">Hozzá lett adva egy új Update-AzKeyVault parancsmag a helyreállító törlés és végleges törlés elleni védelem tárolón való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-720">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="4ffb6-721">Támogatás a következőhöz: Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-721">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="4ffb6-722">Ki lettek javítva a Remove-AzKeyVaultManagedStorageSasDefinition [#11479] példáinak hibái</span><span class="sxs-lookup"><span data-stu-id="4ffb6-722">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="4ffb6-723">Támogatás a privát végponthoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-723">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="4ffb6-724">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="4ffb6-724">Az.Maintenance</span></span>
* <span data-ttu-id="4ffb6-725">Karbantartási parancsmagok végleges verziójának közzététele az általánosan elérhető kiadás számára</span><span class="sxs-lookup"><span data-stu-id="4ffb6-725">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4ffb6-726">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-726">Az.Monitor</span></span>
* <span data-ttu-id="4ffb6-727">Parancsmagok hozzáadva a privát kapcsolat hatóköréhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-727">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="4ffb6-728">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="4ffb6-728">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="4ffb6-729">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="4ffb6-729">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="4ffb6-730">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="4ffb6-730">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="4ffb6-731">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="4ffb6-731">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="4ffb6-732">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="4ffb6-732">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="4ffb6-733">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="4ffb6-733">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="4ffb6-734">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="4ffb6-734">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4ffb6-735">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-735">Az.Network</span></span>
* <span data-ttu-id="4ffb6-736">Frissítve lettek a parancsmagok a virtuális hálózati átjáróhoz való csatlakozás engedélyezéséhez magánhálózati IP-cím esetében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-736">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="4ffb6-737">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4ffb6-737">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="4ffb6-738">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4ffb6-738">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="4ffb6-739">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4ffb6-739">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="4ffb6-740">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4ffb6-740">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="4ffb6-741">Frissítve lettek a parancsmagok az FQDN-alapú LocalNetworkGateways és VpnSites engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-741">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="4ffb6-742">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4ffb6-742">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="4ffb6-743">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="4ffb6-743">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="4ffb6-744">Az IPv6-címcsalád támogatása a következőben: ExpressRouteCircuitConnectionConfig (Global Reach)</span><span class="sxs-lookup"><span data-stu-id="4ffb6-744">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="4ffb6-745">Hozzá lett adva a Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="4ffb6-745">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="4ffb6-746">lehetővé teszi az összes meglévő tulajdonság beállítását, beleértve a következőt is: IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="4ffb6-746">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="4ffb6-747">Frissítve lett az Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="4ffb6-747">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="4ffb6-748">Hozzá lett adva egy másik opcionális AddressPrefixType paraméter a címelőtag címcsaládjának meghatározásához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-748">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="4ffb6-749">Frissítve lettek a parancsmagok a DPD-időtúllépés beállításának engedélyezéséhez a virtuális hálózati átjáró kapcsolatain.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-749">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="4ffb6-750">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4ffb6-750">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="4ffb6-751">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4ffb6-751">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4ffb6-752">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4ffb6-752">Az.PolicyInsights</span></span>
* <span data-ttu-id="4ffb6-753">Hozzá lett adva a Start-AzPolicyComplianceScan parancsmag a szabályzatok megfelelőségi vizsgálatának elindításához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-753">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="4ffb6-754">Szabályzatdefiníció, készletdefiníció és hozzárendelési verziók hozzáadva a Get-AzPolicyState kimenetéhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-754">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4ffb6-755">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4ffb6-755">Az.ServiceFabric</span></span>
* <span data-ttu-id="4ffb6-756">Tovább lett fejlesztve a kódok formázása és a használhatóság a New-AzServiceFabricCluster példái esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-756">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="4ffb6-757">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-757">Az.Sql</span></span>
* <span data-ttu-id="4ffb6-758">Hozzá lettek adva a Get-AzSqlInstanceOperation és a Stop-AzSqlInstanceOperation parancsmagok</span><span class="sxs-lookup"><span data-stu-id="4ffb6-758">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="4ffb6-759">Naplózás támogatása egy VNet-ben található tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-759">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4ffb6-760">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4ffb6-760">Az.Storage</span></span>
* <span data-ttu-id="4ffb6-761">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó értesítés az Azure File parancsmagok kimenetére vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-761">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="4ffb6-762">Támogatott új SkuName StandardGZRS, StandardRAGZRS a Storage-fiók létrehozása/frissítése során</span><span class="sxs-lookup"><span data-stu-id="4ffb6-762">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="4ffb6-763">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ffb6-763">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="4ffb6-764">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ffb6-764">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="4ffb6-765">Támogatott Data Lake Gen2</span><span class="sxs-lookup"><span data-stu-id="4ffb6-765">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="4ffb6-766">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="4ffb6-766">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="4ffb6-767">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="4ffb6-767">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="4ffb6-768">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="4ffb6-768">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="4ffb6-769">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="4ffb6-769">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="4ffb6-770">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="4ffb6-770">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="4ffb6-771">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="4ffb6-771">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="4ffb6-772">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="4ffb6-772">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="4ffb6-773">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="4ffb6-773">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="4ffb6-774">0.10.0-s előzetes verzió – 2020. április</span><span class="sxs-lookup"><span data-stu-id="4ffb6-774">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="4ffb6-775">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="4ffb6-775">General</span></span>
* <span data-ttu-id="4ffb6-776">Az Az modulok előzetes verziója mostantól elérhető az Azure Stack Hubon.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-776">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="4ffb6-777">Ez lehetővé teszi a platformok közötti kompatibilitást a Linux és a macOs rendszerekkel.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-777">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="4ffb6-778">A Azure Stack Hub mostantól támogatja a PowerShell Core-t az Az modulokkal, további információt [itt](https://aka.ms/az4AzureStack) talál</span><span class="sxs-lookup"><span data-stu-id="4ffb6-778">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="4ffb6-779">Az Az modulok támogatják a 2019-03-01-hybrid profilt:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-779">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="4ffb6-780">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="4ffb6-780">Az.Billing</span></span>
  - <span data-ttu-id="4ffb6-781">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-781">Az.Compute</span></span>
  - <span data-ttu-id="4ffb6-782">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="4ffb6-782">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="4ffb6-783">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4ffb6-783">Az.EventHub</span></span>
  - <span data-ttu-id="4ffb6-784">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4ffb6-784">Az.IotHub</span></span>
  - <span data-ttu-id="4ffb6-785">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4ffb6-785">Az.KeyVault</span></span>
  - <span data-ttu-id="4ffb6-786">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-786">Az.Monitor</span></span>
  - <span data-ttu-id="4ffb6-787">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-787">Az.Network</span></span>
  - <span data-ttu-id="4ffb6-788">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-788">Az.Resources</span></span>
  - <span data-ttu-id="4ffb6-789">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4ffb6-789">Az.Storage</span></span>
  - <span data-ttu-id="4ffb6-790">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4ffb6-790">Az.Websites</span></span>
* <span data-ttu-id="4ffb6-791">A következő három új PowerShell-modul lett bevezetve, amelyek használhatók az Azure Stack Hubbal: Az.Databox, Az.IotHub és Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4ffb6-791">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="4ffb6-792">A parancsok viszonylag változatlanok maradnak, kisebb módosításokkal. Például az Az helyébe az AzureRM lép.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-792">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="4ffb6-793">Az Azure Stack Hubhoz kapcsolódó PowerShell-dokumentáció frissített hivatkozását [itt](https://aka.ms/InstallASHPowerShell) találja</span><span class="sxs-lookup"><span data-stu-id="4ffb6-793">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="4ffb6-794">3.7.0 – 2020. március</span><span class="sxs-lookup"><span data-stu-id="4ffb6-794">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4ffb6-795">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4ffb6-795">Az.Accounts</span></span>
* <span data-ttu-id="4ffb6-796">Ki lett javítva az a hiba, hogy a Get-AzTenant/Get-AzDefault/Set-AzDefault parancs NullReferenceException hibát ad vissza kijelentkezett állapotban [#10292]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-796">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4ffb6-797">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-797">Az.Compute</span></span>
* <span data-ttu-id="4ffb6-798">A következő paraméterek lettek hozzáadva a New-AzDiskConfig parancsmaghoz:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-798">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="4ffb6-799">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="4ffb6-799">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="4ffb6-800">Engedélyezve lett a New-AzGalleryImageVersion parancsmag célparaméterének titkosítási tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-800">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="4ffb6-801">Ki lett javítva a tempDisk hibája a Set-AzVmss -Reimage és az Invoke-AzVMReimage parancsmag esetében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-801">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="4ffb6-802">[#11354]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-802">[#11354]</span></span>
* <span data-ttu-id="4ffb6-803">Az alábbi parancsmagok mostantól támogatottak az új SAP-bővítmény esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-803">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="4ffb6-804">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="4ffb6-804">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="4ffb6-805">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="4ffb6-805">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="4ffb6-806">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="4ffb6-806">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="4ffb6-807">Update-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="4ffb6-807">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="4ffb6-808">Ki lettek javítva a súgódokumentáció példáinak hibái</span><span class="sxs-lookup"><span data-stu-id="4ffb6-808">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="4ffb6-809">Táblázatos formátumban jelenítette meg a sztring pontos értékét a PowerState virtuális gép esetében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-809">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="4ffb6-810">New-AzVmssConfig: ki lett javítva az AutomaticRepairs tulajdonság szerializálása a SinglePlacementGroup letiltott állapota esetén.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-810">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="4ffb6-811">[#11257]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-811">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4ffb6-812">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4ffb6-812">Az.DataFactory</span></span>
* <span data-ttu-id="4ffb6-813">Az ADF .Net SDK a 4.8.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="4ffb6-813">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="4ffb6-814">Opcionális paraméterek lettek hozzáadva az Invoke-AzDataFactoryV2Pipeline parancshoz az újrafuttatás támogatásához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-814">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4ffb6-815">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4ffb6-815">Az.DataLakeStore</span></span>
* <span data-ttu-id="4ffb6-816">Hozzá lett adva a kompatibilitástörő változás leírása az Export-AzDataLakeStoreItem és az Import-AzDataLakeStoreItem parancsok esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-816">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="4ffb6-817">A bájtkódolási lehetőség hozzá lett adva a New-AzDataLakeStoreItem, az Add-AzDAtaLakeStoreItemContent és a Get-AzDAtaLakeStoreItemContent parancsok esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-817">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4ffb6-818">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4ffb6-818">Az.HDInsight</span></span>
* <span data-ttu-id="4ffb6-819">Fürt létrehozásakor a minimálisan támogatott TLS-verzió megadása támogatott.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-819">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4ffb6-820">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4ffb6-820">Az.IotHub</span></span>
* <span data-ttu-id="4ffb6-821">Hozzá lett adva az elosztott beállítások eszközönkénti felügyeletének támogatása.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-821">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="4ffb6-822">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-822">New Cmdlets are:</span></span>
    - <span data-ttu-id="4ffb6-823">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="4ffb6-823">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="4ffb6-824">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="4ffb6-824">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4ffb6-825">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4ffb6-825">Az.KeyVault</span></span>
* <span data-ttu-id="4ffb6-826">Kompatibilitástörő változást okozó attribútumok lettek hozzáadva a New-AzKeyVault parancshoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-826">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4ffb6-827">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-827">Az.Monitor</span></span>
* <span data-ttu-id="4ffb6-828">Frissült a New-AzScheduledQueryRuleLogMetricTrigger dokumentációja</span><span class="sxs-lookup"><span data-stu-id="4ffb6-828">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4ffb6-829">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-829">Az.Network</span></span>
* <span data-ttu-id="4ffb6-830">Frissültek a parancsmagok a több-bérlős VirtualHubVnetConnections engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-830">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="4ffb6-831">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="4ffb6-831">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="4ffb6-832">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="4ffb6-832">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="4ffb6-833">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="4ffb6-833">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="4ffb6-834">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="4ffb6-834">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="4ffb6-835">Az SQL Management SDK-függőség el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-835">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4ffb6-836">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4ffb6-836">Az.PolicyInsights</span></span>
* <span data-ttu-id="4ffb6-837">Továbbfejlesztett hibaüzenetek</span><span class="sxs-lookup"><span data-stu-id="4ffb6-837">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4ffb6-838">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-838">Az.RecoveryServices</span></span>
* <span data-ttu-id="4ffb6-839">Hozzá lett adva az Azure Site Recovery-támogatás az Azure Diskkel titkosított virtuális gépek védelmének újbóli beállítása és frissített virtuálisgép-tulajdonságai esetében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-839">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="4ffb6-840">Hozzá lett adva az Azure Site Recovery VmwareToAzure tulajdonságainak vészhelyreállítási monitorozása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-840">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="4ffb6-841">Hozzá lett adva az Azure Backup-támogatás a sikertelen elemekre vonatkozó szabályzatfrissítés újbóli végrehajtása esetében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-841">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="4ffb6-842">Hozzá lett adva az Azure Backup-támogatás a lemezkizárási beállításokhoz a biztonsági mentés és a visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-842">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="4ffb6-843">Hozzá lett adva az Azure Backup-támogatás több fájl/mappa visszaállításához az AzureFileShare-ben</span><span class="sxs-lookup"><span data-stu-id="4ffb6-843">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="4ffb6-844">Hozzá lett adva az Azure Backup-támogatás a felhasználó által megadott erőforráscsoport támogatásához az IaasVM-szabályzat frissítésekor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-844">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="4ffb6-845">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-845">Az.Resources</span></span>
* <span data-ttu-id="4ffb6-846">Ki lett javítva a Get-AzResource-ResourceGroupName-Name-ExpandProperties-ResourceType parancs, hogy ezentúl az erőforrások aktuális API-verzióját használja az alapértelmezett verzió helyett [#11267]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-846">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="4ffb6-847">Hozzá lett adva a CorrelationId-naplózás a hibaforgatókönyvek esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-847">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="4ffb6-848">A Get-AzResourceLock dokumentációjában kisebb módosítás történt.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-848">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="4ffb6-849">Példa hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-849">Added example.</span></span>
* <span data-ttu-id="4ffb6-850">A szimpla idézőjel fel lett oldva a Get-AzADUser paraméterértékében [#11317]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-850">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="4ffb6-851">Új parancsmagok lettek hozzáadva az üzembehelyezési szkriptekhez (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript)</span><span class="sxs-lookup"><span data-stu-id="4ffb6-851">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="4ffb6-852">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-852">Az.Sql</span></span>
* <span data-ttu-id="4ffb6-853">Olvasható másodlagos paraméter lett hozzáadva az Invoke-AzSqlDatabaseFailover parancshoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-853">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="4ffb6-854">A Disable-AzSqlServerActiveDirectoryOnlyAuthentication parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-854">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="4ffb6-855">Az érzékenységi besorolás mentése megtörténik az adatbázis oszlopainak osztályozásakor.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-855">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="4ffb6-856">Az.Support</span><span class="sxs-lookup"><span data-stu-id="4ffb6-856">Az.Support</span></span>
* <span data-ttu-id="4ffb6-857">Az Az.Support modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-857">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4ffb6-858">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4ffb6-858">Az.Websites</span></span>
* <span data-ttu-id="4ffb6-859">Mostantól támogatott a webalkalmazások forgalom-útválasztási szabályainak az alábbi új parancsmagokkal történő használata</span><span class="sxs-lookup"><span data-stu-id="4ffb6-859">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="4ffb6-860">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="4ffb6-860">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="4ffb6-861">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="4ffb6-861">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="4ffb6-862">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="4ffb6-862">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="4ffb6-863">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="4ffb6-863">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="4ffb6-864">3.6.1 – 2020. március</span><span class="sxs-lookup"><span data-stu-id="4ffb6-864">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4ffb6-865">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4ffb6-865">Az.Accounts</span></span>
* <span data-ttu-id="4ffb6-866">Azure PowerShell felmérési oldal megnyitása itt: Send-Feedback [#11020]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-866">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="4ffb6-867">Azure PowerShell-felmérés URL-címének megjelenítése itt: Resolve-Error [#11021]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-867">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="4ffb6-868">Az-verzió hozzáadva az UserAgenthez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-868">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4ffb6-869">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4ffb6-869">Az.ApiManagement</span></span>
* <span data-ttu-id="4ffb6-870">Mostantól támogatott az egyéni tartomány lekérése és konfigurálása a DeveloperPortal végpontján [#11007]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-870">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="4ffb6-871">Export-AzApiManagementAPi – Mostantól támogatott az Api-definíció Json formátumban való letöltése [#9987]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-871">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="4ffb6-872">Import-AzApiManagementApi – Az OpenAPI 3.0-definíció Json-dokumentumokból való importálása mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-872">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="4ffb6-873">New-AzApiManagementIdentityProvider és Set-AzApiManagementIdentityProvider – A Signin Tenant konfigurálása az AAD B2C-szolgáltató esetében mostantól támogatott. [#9784]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-873">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4ffb6-874">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4ffb6-874">Az.DataLakeStore</span></span>
* <span data-ttu-id="4ffb6-875">A System.Buffershez hivatkozásának explicit hozzáadása a következőkben: csproj és psd1</span><span class="sxs-lookup"><span data-stu-id="4ffb6-875">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4ffb6-876">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4ffb6-876">Az.IotHub</span></span>
* <span data-ttu-id="4ffb6-877">Az eszközök az IoT Hubban való kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-877">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="4ffb6-878">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-878">New Cmdlets are:</span></span>
    - <span data-ttu-id="4ffb6-879">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="4ffb6-879">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="4ffb6-880">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="4ffb6-880">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="4ffb6-881">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="4ffb6-881">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="4ffb6-882">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="4ffb6-882">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="4ffb6-883">A cél IoT-eszközökön lévő modulok IoT Hubban való kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-883">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="4ffb6-884">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-884">New Cmdlets are:</span></span>
    - <span data-ttu-id="4ffb6-885">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="4ffb6-885">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="4ffb6-886">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="4ffb6-886">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="4ffb6-887">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="4ffb6-887">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="4ffb6-888">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="4ffb6-888">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="4ffb6-889">Parancsmag hozzáadva egy IoT Hubban lévő cél IoT-eszköz kapcsolati sztringjének lekéréséhez.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-889">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="4ffb6-890">Parancsmag hozzáadva egy IoT Hubban lévő cél IoT-eszköz modulja kapcsolati sztringjének lekéréséhez.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-890">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="4ffb6-891">Az IoT-eszközök szülő eszközének lekérése/beállítása mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-891">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="4ffb6-892">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-892">New Cmdlets are:</span></span>
    - <span data-ttu-id="4ffb6-893">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="4ffb6-893">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="4ffb6-894">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="4ffb6-894">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="4ffb6-895">Az eszközök szülő-gyermek kapcsolatainak kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-895">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4ffb6-896">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-896">Az.Monitor</span></span>
* <span data-ttu-id="4ffb6-897">A Get-AzMetricDefinition kimeneti értéke javítva [#9714]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-897">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4ffb6-898">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-898">Az.Network</span></span>
* <span data-ttu-id="4ffb6-899">SQL Management SDK frissítve.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-899">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="4ffb6-900">Kijavítottuk a PrivateLinkServiceConnectionState osztály eltérő elnevezéssel kapcsolatos hibáját.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-900">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="4ffb6-901">Az ActionsRequired mező leképezése a követezőre: ActionRequired</span><span class="sxs-lookup"><span data-stu-id="4ffb6-901">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="4ffb6-902">PublicNetworkAccess hozzáadva a következőhöz: New-AzSqlServer és Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="4ffb6-902">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="4ffb6-903">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-903">Az.Resources</span></span>
* <span data-ttu-id="4ffb6-904">A Get-AzRoleAssignment null értékű hivatkozásra vonatkozó hibája javítva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-904">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="4ffb6-905">A -Force és a -PassThru kapcsoló nem kötelezőként lett megjelölve a Remove-AzADGroup esetében [#10849]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-905">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="4ffb6-906">Javítva a hiba, amely miatt a MailNickname nem lett visszaadva Remove-AzADGroup esetében [#11167]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-906">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="4ffb6-907">A Remove-AzADGroup folyamatművelet működési hibája kijavítva [#11171]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-907">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="4ffb6-908">A GetAzureRoleAssignmentCommand null értékű hivatkozásra vonatkozó hibája javítva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-908">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="4ffb6-909">Kompatibilitástörő változás hozzáadva a szabályzati parancsmagok soron következő változásaihoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-909">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="4ffb6-910">Frissült a Get-AzResourceGroup az erőforráscsoport-címke kiszolgálóoldali szűrésének elvégzéséhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-910">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="4ffb6-911">A címkeparancsmagok kiterjesztése a -ResourceID elfogadása érdekében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-911">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="4ffb6-912">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ffb6-912">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="4ffb6-913">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ffb6-913">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="4ffb6-914">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ffb6-914">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="4ffb6-915">Új címkeparancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-915">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="4ffb6-916">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ffb6-916">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="4ffb6-917">A ScopedDeployment áthozva az SDK 3.3.0-ból</span><span class="sxs-lookup"><span data-stu-id="4ffb6-917">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="4ffb6-918">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-918">Az.Sql</span></span>
* <span data-ttu-id="4ffb6-919">PublicNetworkAccess hozzáadva a következőhöz: New-AzSqlServer és Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="4ffb6-919">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="4ffb6-920">Támogatás hozzáadva a biztonsági másolatok hosszú távú megőrzési konfigurációjához a felügyelt adatbázisok esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-920">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="4ffb6-921">LTR-szabályzat lekérése/beállítása felügyelt adatbázison</span><span class="sxs-lookup"><span data-stu-id="4ffb6-921">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="4ffb6-922">LTR biztonsági másolat(ok) lekérése felügyelt adatbázis, felügyelt példány vagy hely szerint</span><span class="sxs-lookup"><span data-stu-id="4ffb6-922">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="4ffb6-923">LTR biztonsági másolat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-923">Remove an LTR backup</span></span>
    - <span data-ttu-id="4ffb6-924">LTR biztonsági másolat visszaállítása új felügyelt adatbázis létrehozásához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-924">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="4ffb6-925">MinimalTlsVersion hozzáadva a következőkhöz: New-AzSqlServer és Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="4ffb6-925">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="4ffb6-926">MinimalTlsVersion hozzáadva a következőkhöz: New-AzSqlInstance és Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4ffb6-926">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="4ffb6-927">Az SQL SDK-verzió felléptetése a következőhöz: AZ.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-927">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4ffb6-928">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4ffb6-928">Az.Storage</span></span>
* <span data-ttu-id="4ffb6-929">Támogatott AllowProtectedAppendWrite a következőben: ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="4ffb6-929">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="4ffb6-930">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="4ffb6-930">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="4ffb6-931">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó figyelmeztető üzenet az AzureStorageTable típusának módosítására vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-931">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="4ffb6-932">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="4ffb6-932">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="4ffb6-933">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="4ffb6-933">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4ffb6-934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4ffb6-934">Az.Websites</span></span>
* <span data-ttu-id="4ffb6-935">Címke paraméter hozzáadva a következőkhöz: New-AzAppServicePlan és Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="4ffb6-935">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="4ffb6-936">A parancsmag végrehajtásának leállítása, ha egy egyéni tartomány webhelyhez történő hozzáadásakor a rendszer kivételt ad vissza</span><span class="sxs-lookup"><span data-stu-id="4ffb6-936">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="4ffb6-937">Támogatás hozzáadva az olyan App Services műveletek elvégzéséhez, amelyek nem abban az erőforráscsoportban vannak, amelyben az App Service-csomag</span><span class="sxs-lookup"><span data-stu-id="4ffb6-937">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="4ffb6-938">Hozzáférési korlátozás alkalmazva a különböző erőforráscsoportokban lévő webalkalmazásokra/függvényekre</span><span class="sxs-lookup"><span data-stu-id="4ffb6-938">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="4ffb6-939">Az egyéni WebAppSlots-gazdanevek beállítására vonatkozó hiba kijavítva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-939">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="4ffb6-940">3.5.0 – 2020. február</span><span class="sxs-lookup"><span data-stu-id="4ffb6-940">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4ffb6-941">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="4ffb6-941">Highlights since the last major release</span></span>
* <span data-ttu-id="4ffb6-942">Frissült az ügyféloldali telemetria.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-942">Updated client side telemetry.</span></span>
* <span data-ttu-id="4ffb6-943">Az.IotHub: parancsmagok hozzáadva az eszközkezelés támogatásához.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-943">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="4ffb6-944">Az.SqlVirtualMachine: parancsmagok hozzáadva a rendelkezésreállási csoport figyelőjéhez.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-944">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4ffb6-945">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4ffb6-945">Az.Accounts</span></span>
* <span data-ttu-id="4ffb6-946">A SubscriptionId, a TenantId és a végrehajtási idő hozzáadva az ügyféloldali telemetria adataihoz.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-946">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4ffb6-947">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4ffb6-947">Az.Automation</span></span>
* <span data-ttu-id="4ffb6-948">Ki lett javítva a „New-AzAutomationSoftwareUpdateConfiguration” referenciadokumentációjának 1. példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="4ffb6-948">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4ffb6-949">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-949">Az.CognitiveServices</span></span>
* <span data-ttu-id="4ffb6-950">Az SDK a 7.0-ás verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="4ffb6-950">Updated SDK to 7.0</span></span>
* <span data-ttu-id="4ffb6-951">Tovább lett fejlesztve a hibaüzenet, amely akkor jelenik meg, ha a kiszolgáló üres törzset ad vissza válaszként</span><span class="sxs-lookup"><span data-stu-id="4ffb6-951">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4ffb6-952">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-952">Az.Compute</span></span>
* <span data-ttu-id="4ffb6-953">A ProximityPlacementGroupId mostantól üres értékkel is rendelkezhet a frissítés során</span><span class="sxs-lookup"><span data-stu-id="4ffb6-953">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4ffb6-954">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-954">Az.FrontDoor</span></span>
* <span data-ttu-id="4ffb6-955">Új parancsmag hozzáadva a WAF-ban használható felügyelt szabálydefiníciók lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-955">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4ffb6-956">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4ffb6-956">Az.IotHub</span></span>
* <span data-ttu-id="4ffb6-957">Az eszközök az IoT Hubban való kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-957">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="4ffb6-958">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-958">New Cmdlets are:</span></span>
    - <span data-ttu-id="4ffb6-959">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="4ffb6-959">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="4ffb6-960">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="4ffb6-960">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="4ffb6-961">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="4ffb6-961">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="4ffb6-962">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="4ffb6-962">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4ffb6-963">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4ffb6-963">Az.KeyVault</span></span>
* <span data-ttu-id="4ffb6-964">Ki lett javítva az Add-AzKeyVaultKey.md duplikált szövege</span><span class="sxs-lookup"><span data-stu-id="4ffb6-964">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4ffb6-965">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-965">Az.Monitor</span></span>
* <span data-ttu-id="4ffb6-966">Ki lett javítva a Get-AzLog parancsmag leírása.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-966">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="4ffb6-967">Egy új, ActionGroupId nevű paraméter lett hozzáadva a „New-AzMetricAlertRuleV2” parancshoz.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-967">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="4ffb6-968">A felhasználó a következőket adhatja meg: ActionGroupId(string) vagy ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="4ffb6-968">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4ffb6-969">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-969">Az.Network</span></span>
* <span data-ttu-id="4ffb6-970">Hozzá lett adva egy extra paramétermegjegyzés a „New-AzPrivateLinkService” parancsmag „-EnableProxyProtocol” paraméteréhez.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-970">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="4ffb6-971">A Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és a Start-AzVirtualnetworkGatewayPacketCapture.md FilterData kapcsolójának példái ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-971">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="4ffb6-972">Hozzá lett adva egy csomagrögzítési példa a Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és Start-AzVirtualnetworkGatewayPacketCapture.md minden belső és külső csomagjának rögzítéséhez.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-972">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="4ffb6-973">Az Azure Firewall-szabályzat mostantól támogatott a Vnet-tűzfalakon</span><span class="sxs-lookup"><span data-stu-id="4ffb6-973">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="4ffb6-974">Nem lettek hozzáadva új parancsmagok.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-974">No new cmdlets are added.</span></span> <span data-ttu-id="4ffb6-975">Enyhítve lettek a tűzfalszabályzat korlátozásai a Vnet-tűzfalak esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-975">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4ffb6-976">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-976">Az.RecoveryServices</span></span>
* <span data-ttu-id="4ffb6-977">A fájlokként történő visszaállítás mostantól támogatott az SQL-adatbázisok esetében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-977">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4ffb6-978">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-978">Az.Resources</span></span>
* <span data-ttu-id="4ffb6-979">Újra lettek tervezve a sablonalapú üzembehelyezési parancsmagok</span><span class="sxs-lookup"><span data-stu-id="4ffb6-979">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="4ffb6-980">Új parancsmagok lettek hozzáadva a felügyeleti csoportban való üzembe helyezés kezeléséhez: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4ffb6-980">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="4ffb6-981">Új parancsmagok lettek hozzáadva a bérlői hatókörben való üzembe helyezés kezeléséhez: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="4ffb6-981">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="4ffb6-982">Az \*-AzDeployment parancsmagok kifejezetten az előfizetési hatókörben való működéshez lettek újratervezve</span><span class="sxs-lookup"><span data-stu-id="4ffb6-982">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="4ffb6-983">Az \*-AzSubscriptionDeployment aliasok lettek létrehozva az \*-AzDeployment parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-983">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="4ffb6-984">Ki lett javítva az „Update-AzADApplication” nem beállított „AvailableToOtherTenants” paraméter esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-984">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="4ffb6-985">Az ApplicationObjectWithoutCredentialParameterSet el lett távolítva az AmbiguousParameterSetException elkerülése érdekében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-985">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="4ffb6-986">A súgófájlok újra létre lettek hozva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-986">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="4ffb6-987">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-987">Az.Sql</span></span>
* <span data-ttu-id="4ffb6-988">Az előfizetések közötti időponthoz kötött visszaállítás mostantól támogatott a felügyelt példányokon.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-988">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="4ffb6-989">A már meglévő felügyelt SQL-példány hardvergenerációjának módosítása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="4ffb6-989">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="4ffb6-990">Ki lettek javítva az „Update-AzSqlServerVulnerabilityAssessmentSetting” súgópéldái: paraméter/tulajdonságkimenet – EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="4ffb6-990">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="4ffb6-991">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4ffb6-991">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="4ffb6-992">Parancsmagokat hozzáadva a rendelkezésreállási csoport figyelőjéhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-992">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="4ffb6-993">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="4ffb6-993">Az.StorageSync</span></span>
* <span data-ttu-id="4ffb6-994">Frissültek az „Invoke-AzStorageSyncCompatibilityCheck” támogatott karakterkészletei.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-994">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="4ffb6-995">3.4.0 – 2020. február</span><span class="sxs-lookup"><span data-stu-id="4ffb6-995">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4ffb6-996">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="4ffb6-996">Highlights since the last major release</span></span>
* <span data-ttu-id="4ffb6-997">Megjelent az Az.CosmosDB 0.1.0-s kezdeti verziója</span><span class="sxs-lookup"><span data-stu-id="4ffb6-997">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="4ffb6-998">Az.Network ConnectionMonitor V2 támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-998">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4ffb6-999">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4ffb6-999">Az.Accounts</span></span>
* <span data-ttu-id="4ffb6-1000">A környezet automatikus mentésének letiltása, ha az AzureRmContext.json nem érhető el</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1000">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="4ffb6-1001">Az Azure Powershell Common referenciájának frissítése 1.3.5-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1001">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4ffb6-1002">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1002">Az.ApiManagement</span></span>
* <span data-ttu-id="4ffb6-1003">**Get-AzApiManagementApiSchema** Az API-val társított Open-API séma kijavítása   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1003">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="4ffb6-1004">**New-AzApiManagementProduct**\* és **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1004">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="4ffb6-1005">https://github.com/Azure/azure-powershell/issues/10472 dokumentációja kijavítva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1005">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="4ffb6-1006">**Set-AzApiManagementApi** A ServiceUrl parancsmaggal való frissítését bemutató példa hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1006">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4ffb6-1007">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1007">Az.Compute</span></span>
* <span data-ttu-id="4ffb6-1008">A virtuális gép állapotának korlátozása 100 értékre, hogy ne legyen szabályozás, ha a Get-AzVM -Status a virtuális gép neve nélkül lett végrehajtva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1008">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="4ffb6-1009">Update-AzDiskEncryptionSet parancsmagok hozzáadása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1009">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="4ffb6-1010">Az EncryptionType és a DiskEncryptionSetId paraméterek hozzáadása a következő parancsmagokhoz:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1010">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="4ffb6-1011">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1011">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="4ffb6-1012">A ColocationStatus paraméter hozzáadva a Get-AzProximityPlacementGroup parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1012">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4ffb6-1013">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1013">Az.DataFactory</span></span>
* <span data-ttu-id="4ffb6-1014">Az ADF .Net SDK frissítve lett a 4.7.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1014">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="4ffb6-1015">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1015">Az.DeploymentManager</span></span>
* <span data-ttu-id="4ffb6-1016">LIST műveletek hozzáadása az erőforrásokhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1016">Adds LIST operations for resources</span></span>
* <span data-ttu-id="4ffb6-1017">Műveletek végrehajtásának lehetősége az állapotellenőrzés lépésein</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1017">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4ffb6-1018">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1018">Az.HDInsight</span></span>
* <span data-ttu-id="4ffb6-1019">A New-AzHDInsightCluster dokumentációs hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1019">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4ffb6-1020">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1020">Az.KeyVault</span></span>
* <span data-ttu-id="4ffb6-1021">Name alias hozzáadása a VaultName attribútumhoz, hogy a Remove-AzureKeyVault konzisztens legyen a New-AzureKeyVault paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1021">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4ffb6-1022">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1022">Az.Network</span></span>
* <span data-ttu-id="4ffb6-1023">Új példa hozzáadva a Set-AzNetworkWatcherConfigFlowLog.md fájlhoz a Traffic Analytics-letiltási forgatókönyv szemléltetésére.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1023">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="4ffb6-1024">Felügyeleti IP-konfiguráció támogatás hozzáadva az Azure Firewallhoz – egy dedikált alhálózat és nyilvános IP-cím, amelyet a tűzfal a forgalom felügyeléséhez használni fog</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1024">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="4ffb6-1025">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1025">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="4ffb6-1026">Hozzá lett adva a (nem kötelező) -PublicIpAddress-ManagementPublicIpAddress paraméter, amely egy nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1026">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="4ffb6-1027">Hozzá lett adva a SetManagementIpConfiguration metódus a tűzfalobjektumok esetében – nyilvános IP-cím-objektumokat fogad el bemeneti adatként – az alhálózat nevének AzureFirewallManagementSubnet értéknek kell lennie</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1027">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="4ffb6-1028">A Get-AzNetworkSecurityGroup példái javítva, hogy hálózati biztonsági csoportok példáit tartalmazzák hálózati adapterek helyett.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1028">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="4ffb6-1029">Javítottunk egy elírást a New-AzVpnSite parancsban, amely megakadályozta, hogy az erőforrásazonosító-kiegészítő kiegészítsen egy paramétert.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1029">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="4ffb6-1030">Az Application Gateway szabály-újraírási műveletkészletének URL-konfigurálása mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1030">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="4ffb6-1031">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1031">New cmdlets added:</span></span>
        - <span data-ttu-id="4ffb6-1032">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1032">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="4ffb6-1033">A parancsmagok frissültek a nem kötelező UrlConfiguration paraméterrel</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1033">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="4ffb6-1034">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1034">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="4ffb6-1035">A Network Watcher Connection Monitor 2-es verziójú erőforrások támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1035">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4ffb6-1036">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1036">Az.PolicyInsights</span></span>
* <span data-ttu-id="4ffb6-1037">A javítandó erőforrások azonosítása előtti megfelelőségértékelés támogatása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1037">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="4ffb6-1038">-ResourceDiscoverMode paraméter hozzáadása a Start-AzPolicyRemediation parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1038">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="4ffb6-1039">A szabályzatok metaadat-erőforrásainak elérésére szolgáló Get-AzPolicyMetadata parancsmag hozzáadása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1039">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="4ffb6-1040">A Get-AzPolicyState és a Get-AzPolicyStateSummary frissült a 2019-10-01 API-verzióhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1040">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4ffb6-1041">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1041">Az.RecoveryServices</span></span>
* <span data-ttu-id="4ffb6-1042">Azure Site Recovery-támogatás a replikált lemezek eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1042">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="4ffb6-1043">Hozzáadott Azure Backup-támogatás a helyreállítási tárak létrehozása közbeni címkehozzáadáshoz.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1043">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4ffb6-1044">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1044">Az.Resources</span></span>
* <span data-ttu-id="4ffb6-1045">A -Scope választható a \*-AzPolicyAssignment parancsmagokban; az alapértelmezett érték a környezeti előfizetés</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1045">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="4ffb6-1046">Az ADServicePrincipal jelszó és kulcs típusú hitelesítő adatokkal való létrehozását szemléltető példák hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1046">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="4ffb6-1047">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1047">Az.Sql</span></span>
<span data-ttu-id="4ffb6-1048">A New-AzSqlDatabaseSecondary parancsmag javítva, hogy a PartnerDatabaseName létezését ellenőrizze a DatabaseName létezése helyett.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1048">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4ffb6-1049">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1049">Az.Storage</span></span>
* <span data-ttu-id="4ffb6-1050">A Table/Queue Encryption Keytype készlet beállításának támogatása Storage-fiók létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1050">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="4ffb6-1051">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1051">New-AzStorageAccount</span></span>
* <span data-ttu-id="4ffb6-1052">RequestId megjelenítése, ha a StorageException nem rendelkezik ExtendedErrorInformation paraméterrel</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1052">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="4ffb6-1053">A Start-AzStorageBlobCopy parancsmag 6. példájának kijavítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1053">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4ffb6-1054">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1054">Az.Websites</span></span>
* <span data-ttu-id="4ffb6-1055">A Set-AzWebapp és a Set-AzWebappSlot támogatja az AlwaysOn, a MinTls és a FtpsState tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1055">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="4ffb6-1056">Javítva a hiba, amely miatt a HttpsOnly és az AppservicePlan Set-AzWebApp paranccsal történő egyidejű módosításakor a HttpsOnly paraméter alaphelyzetbe állt.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1056">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="4ffb6-1057">3.3.0 – 2020. január</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1057">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4ffb6-1058">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1058">Az.Accounts</span></span>
* <span data-ttu-id="4ffb6-1059">Frissítve lettek az Add-AzEnvironment és Set-AzEnvironment parancsmagok, amelyek mostantól elfogadják az AzureAttestationServiceEndpointResourceId és AzureAttestationServiceEndpointSuffix paramétereket</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1059">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4ffb6-1060">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1060">Az.Cdn</span></span>
* <span data-ttu-id="4ffb6-1061">A hibaválasz részleteinek láthatóvá tétele a New-AzCdnEndpoint parancsmagban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1061">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4ffb6-1062">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1062">Az.Compute</span></span>
* <span data-ttu-id="4ffb6-1063">Javítva lett a Set-AzVMCustomScriptExtension parancsmag az olyan virtuális gépek esetében, amelyek felügyelt operációsrendszer-lemeze nem rendelkezik operációsrendszer-profillal.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1063">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="4ffb6-1064">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1064">Az.ContainerInstance</span></span>
* <span data-ttu-id="4ffb6-1065">Javítva lettek a New-AzContainerGroup parancsmagpélda által használt paraméternevek</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1065">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="4ffb6-1066">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1066">Az.DataBoxEdge</span></span>
* <span data-ttu-id="4ffb6-1067">Hozzá lett adva a Get-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1067">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="4ffb6-1068">Az Edge Storage-tároló lekérése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1068">Get the Edge Storage Container</span></span>
* <span data-ttu-id="4ffb6-1069">Hozzá lett adva a New-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1069">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="4ffb6-1070">Új Edge Storage-tároló létrehozása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1070">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="4ffb6-1071">Hozzá lett adva a Remove-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1071">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="4ffb6-1072">Az Edge Storage-tároló eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1072">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="4ffb6-1073">Hozzá lett adva az Invoke-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1073">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="4ffb6-1074">Meghívási művelet az Edge Storage-tárolóban lévő adatok frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1074">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="4ffb6-1075">Hozzá lett adva a Get-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1075">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="4ffb6-1076">Az Edge Storage-fiók lekérése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1076">Get the Edge Storage Account</span></span>
* <span data-ttu-id="4ffb6-1077">Hozzá lett adva a New-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1077">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="4ffb6-1078">Új Edge Storage-fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1078">Create new Edge Storage Account</span></span>
* <span data-ttu-id="4ffb6-1079">Hozzá lett adva a Remove-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1079">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="4ffb6-1080">Az Edge Storage-fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1080">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="4ffb6-1081">Hozzá lett adva az Invoke-AzDataBoxEdgeShare parancsmag</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1081">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="4ffb6-1082">Meghívási művelet a megosztott adatok frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1082">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="4ffb6-1083">Hozzá lett adva a Set-AzDataBoxEdgeStorageAccountCredential parancsmag</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1083">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="4ffb6-1084">Az Az.DataBoxEdge tárfiók hitelesítő adatainak beállítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1084">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4ffb6-1085">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1085">Az.DataFactory</span></span>
* <span data-ttu-id="4ffb6-1086">Hozzá lettek adva az AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId és VersionStatus tulajdonságok a Get-AzDataFactoryV2IntegrationRuntime parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1086">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="4ffb6-1087">Az ADF .Net SDK frissítve lett a 4.6.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1087">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="4ffb6-1088">A PublicIPs paraméter hozzá lett adva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz statikus nyilvános IP-címekkel rendelkező Azure-SSIS IR létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1088">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="4ffb6-1089">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1089">Az.DevTestLabs</span></span>
* <span data-ttu-id="4ffb6-1090">A hibás hivatkozás el lett távolítva a Get-AzDtlAllowedVMSizesPolicy.md parancsmagból</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1090">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4ffb6-1091">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1091">Az.EventHub</span></span>
* <span data-ttu-id="4ffb6-1092">A 10634-es hiba javítása: Ki lett javítva a nullértékű objektumhivatkozás a remove eventhubnamespace esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1092">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4ffb6-1093">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1093">Az.HDInsight</span></span>
* <span data-ttu-id="4ffb6-1094">Ki lett javítva az Invoke-AzHDInsightHiveJob.md hibája.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1094">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="4ffb6-1095">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1095">Az.MachineLearning</span></span>
* <span data-ttu-id="4ffb6-1096">El lettek távolítva az alábbi parancsmagok, mivel a MachineLearningCompute már nem érhető el</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1096">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="4ffb6-1097">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1097">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="4ffb6-1098">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1098">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="4ffb6-1099">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1099">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="4ffb6-1100">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1100">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="4ffb6-1101">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1101">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="4ffb6-1102">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1102">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="4ffb6-1103">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1103">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4ffb6-1104">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1104">Az.Network</span></span>
* <span data-ttu-id="4ffb6-1105">Frissítve lett a Microsoft.Azure.Management.Sql függősége: 1.36-preview helyett 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1105">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4ffb6-1106">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1106">Az.RecoveryServices</span></span>
* <span data-ttu-id="4ffb6-1107">Módosított Azure Site Recovery-támogatás azon felügyelt lemezeken található, inaktív állapotban titkosított virtuális gépeknél, amelyekhez felhasználó által kezelt kulcsok tartoznak a következő esetében: Azure – Azure-szolgáltató.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1107">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="4ffb6-1108">Azure Site Recovery-támogatás a lemeztitkosítási csoportazonosító megadásának opcionálissá tételéhez a védelem engedélyezése során a következő esetében: VMware – Azure.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1108">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="4ffb6-1109">Azure Site Recovery-támogatás a lemeztitkosítási csoportazonosító megadásának opcionálissá tételéhez a lemez szintjén a védelem engedélyezéséhez a következő esetében: VMware – Azure.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1109">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="4ffb6-1110">Azure Site Recovery-támogatás a Replikációval védett, lemeztitkosítási csoportleképezéssel ellátott elemek frissítéséhez a következő esetében: HyperV – Azure.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1110">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4ffb6-1111">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1111">Az.Resources</span></span>
* <span data-ttu-id="4ffb6-1112">Javítva lett egy hiba a Remove-AzTag súgódokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1112">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="4ffb6-1113">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1113">Az.Sql</span></span>
* <span data-ttu-id="4ffb6-1114">Javítva lett a sebezhetőségi felmérés csoportszintű alapkonfigurációs parancsmagjainak működése: az Azure-adatbázis főadatbázisában használható, a felügyelt példányok rendszeradatbázisaiban korlátozott.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1114">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="4ffb6-1115">Ki lett javítva egy hiba az SQL-példányok feladatátvételi csoportjainak létrehozása esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1115">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="4ffb6-1116">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1116">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="4ffb6-1117">Hozzá lett adva a DR, mint új érvényes licenctípus</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1117">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4ffb6-1118">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1118">Az.Storage</span></span>
* <span data-ttu-id="4ffb6-1119">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó figyelmeztető üzenet a DefaultAction értékének módosítására vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1119">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="4ffb6-1120">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1120">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="4ffb6-1121">Támogatott a tárfiók legutóbbi szinkronizálási időpontjának lekérése a get-AzureRMStorageAccount parancsmag -IncludeGeoReplicationStats paraméterrel való futtatásával</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1121">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="4ffb6-1122">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1122">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="4ffb6-1123">3.2.0 – 2019. december</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1123">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="4ffb6-1124">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1124">General</span></span>
* <span data-ttu-id="4ffb6-1125">A .psd1 hivatkozásai frissítve, hogy minden modulhoz a relatív elérési utat használják</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1125">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4ffb6-1126">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1126">Az.Accounts</span></span>
* <span data-ttu-id="4ffb6-1127">A megfelelő felhasználói ügynök beállítva az ügyféloldali telemetriához az Az 4.0 előzetes verziójában</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1127">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="4ffb6-1128">Felhasználóbarát hibaüzenet megjelenítése, ha az Az 4.0 előzetes verziójában a környezet null értékű</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1128">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4ffb6-1129">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1129">Az.Batch</span></span>
* <span data-ttu-id="4ffb6-1130">Ki lett javítva a [10602-es](https://github.com/Azure/azure-powershell/issues/10602) számú hiba, amely miatt a **New-AzBatchPool** nem megfelelően küldte el a „VirtualMachineConfiguration.ContainerConfiguration” és a „VirtualMachineConfiguration.DataDisks” paramétereket a kiszolgálónak.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1130">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4ffb6-1131">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1131">Az.DataFactory</span></span>
* <span data-ttu-id="4ffb6-1132">Az ADF .Net SDK a 4.5.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1132">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4ffb6-1133">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1133">Az.FrontDoor</span></span>
* <span data-ttu-id="4ffb6-1134">A WAF felügyeleti szabályok kizárása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1134">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="4ffb6-1135">Hozzá lett adva a SocketAddr automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1135">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="4ffb6-1136">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1136">Az.HealthcareApis</span></span>
* <span data-ttu-id="4ffb6-1137">Kivételkezelés</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1137">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4ffb6-1138">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1138">Az.KeyVault</span></span>
* <span data-ttu-id="4ffb6-1139">Ki lett javítva az esetleg nem beállított értékek hozzáférésével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1139">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="4ffb6-1140">Az elliptikus görbéjű titkosítási tanúsítványok kezelése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1140">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="4ffb6-1141">A görbe tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1141">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4ffb6-1142">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1142">Az.Monitor</span></span>
* <span data-ttu-id="4ffb6-1143">Opcionális argumentum hozzáadva a Diagnosztikai beállítások hozzáadása parancshoz.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1143">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="4ffb6-1144">Ez egy kapcsoló argumentum, amely megléte esetén azt jelzi, hogy a Log Analyticsbe történő exportálást egy rögzített séma (más néven</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1144">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="4ffb6-1145">dedikált adattípus) szerint kell végrehajtani</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1145">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4ffb6-1146">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1146">Az.Network</span></span>
* <span data-ttu-id="4ffb6-1147">Támogatás az Ip-csoportok számára az AzureFirewall alkalmazás, valamint a Nat- és a hálózati szabályok esetében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1147">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4ffb6-1148">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1148">Az.Resources</span></span>
* <span data-ttu-id="4ffb6-1149">Ki lett javítva az a hiba, amely miatt a sablonalapú üzembe helyezés során a sablonparamétert nem lehet olvasni, ha a sablonparaméter és egy beépített paraméter neve között névütközés áll fenn.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1149">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="4ffb6-1150">Frissültek a szabályzat parancsmagjai a 2019. 09. 01. dátumú új API-verzió használatára, amely bevezeti a szabályzatkészlet-definíciókon belüli csoportos támogatást.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1150">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="4ffb6-1151">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1151">Az.Sql</span></span>
* <span data-ttu-id="4ffb6-1152">Frissítve lett a sebezhetőségi felmérés automatikus engedélyezéséhez szükséges tárterület létrehozása a Storagev2-ben</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1152">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4ffb6-1153">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1153">Az.Storage</span></span>
* <span data-ttu-id="4ffb6-1154">A blob-/tárolóidentitás-alapú SAS-token Oauth-hitelesítésen alapuló Storage-környezettel való létrehozásának támogatása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1154">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="4ffb6-1155">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1155">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="4ffb6-1156">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1156">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="4ffb6-1157">Támogatott lett a tárfiókhoz tartozó felhasználódelegálási kulcsok visszavonása, így minden identitásalapú SAS-token visszavonható</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1157">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="4ffb6-1158">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1158">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="4ffb6-1159">Frissítés a Microsoft.Azure.Management.Storage 14.2.0-s verziójára az új API-verzió (2019. 06. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1159">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="4ffb6-1160">A QuotaGiB (gigabájtban megadott megosztási kvóta) esetében támogatottak az 5120-nál nagyobb értékek a fájlmegosztási parancsmagok felügyeleti síkján, és hozzá lett adva a Quota paraméteralias a QuotaGiB paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1160">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="4ffb6-1161">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1161">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="4ffb6-1162">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1162">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="4ffb6-1163">A „QuotaGiB” paraméteralias hozzáadva a „kvóta” paraméterhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1163">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="4ffb6-1164">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1164">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="4ffb6-1165">Ki lett javítva az a hiba, amely miatt a Set-AzStorageContainerAcl parancsmag el tudta távolítani a tárolt hozzáférési szabályzatot</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1165">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="4ffb6-1166">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1166">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="4ffb6-1167">3.1.0 – 2019. november</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1167">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4ffb6-1168">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1168">Highlights since the last major release</span></span>
* <span data-ttu-id="4ffb6-1169">Az.DataBoxEdge 1.0.0 kiadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1169">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="4ffb6-1170">Az.SqlVirtualMachine 1.0.0 kiadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1170">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4ffb6-1171">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1171">Az.Compute</span></span>
* <span data-ttu-id="4ffb6-1172">A virtuális gépek Reapply funkciója</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1172">VM Reapply feature</span></span>
    - <span data-ttu-id="4ffb6-1173">A Reapply paraméter hozzá lett adva a Set-AzVM parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1173">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="4ffb6-1174">A virtuálisgép-méretezési csoportok AutomaticRepairs funkciója:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1174">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="4ffb6-1175">Az EnableAutomaticRepair, az AutomaticRepairGracePeriod és az AutomaticRepairMaxInstanceRepairsPercent paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1175">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="4ffb6-1176">Több-bérlős katalógus-rendszerkép támogatása a New-AzVM parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1176">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="4ffb6-1177">A Spot hozzá lett adva a New-AzVM, a New-AzVMConfig és a New-AzVmss parancsmag Priority paraméterének argumentumbefejezőjéhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1177">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="4ffb6-1178">A DiskIOPSReadWrite és a DiskMBpsReadWrite paraméter hozzá lett adva az Add-AzVmssDataDisk parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1178">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="4ffb6-1179">A New-AzGalleryImageVersion parancsmag SourceImageId paramétere mostantól nem kötelező</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1179">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="4ffb6-1180">A New-AzGalleryImageVersion parancsmag az OSDiskImage és a DataDiskImage paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1180">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="4ffb6-1181">A HyperVGeneration paraméter mostantól elérhető a New-AzGalleryImageDefinition parancsmagban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1181">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="4ffb6-1182">A SkipExtensionsOnOverprovisionedVMs paraméter hozzá lett adva a New-AzVmss, a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1182">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="4ffb6-1183">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1183">Az.DataBoxEdge</span></span>
* <span data-ttu-id="4ffb6-1184">A(z) `Get-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1184">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="4ffb6-1185">Megrendelés lekérése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1185">Get the Order</span></span>
* <span data-ttu-id="4ffb6-1186">A(z) `New-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1186">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="4ffb6-1187">Új megrendelés létrehozása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1187">Create new Order</span></span>
* <span data-ttu-id="4ffb6-1188">A(z) `Remove-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1188">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="4ffb6-1189">Megrendelés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1189">Remove the Order</span></span>
* <span data-ttu-id="4ffb6-1190">`New-AzDataBoxEdgeShare` parancsmag módosítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1190">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="4ffb6-1191">Mostantól helyi megosztást hoz létre</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1191">Now creates Local Share</span></span>
* <span data-ttu-id="4ffb6-1192">A(z) `Set-AzDataBoxEdgeRole` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1192">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="4ffb6-1193">Mostantól az IotRole leképezhető a Share-re</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1193">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="4ffb6-1194">A(z) `Invoke-AzDataBoxEdgeDevice` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1194">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="4ffb6-1195">Frissítések keresésének, letöltésének, telepítésének indítása az eszközön</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1195">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="4ffb6-1196">A(z) `Get-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1196">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="4ffb6-1197">Triggerek információinak lekérdezése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1197">Gets the information about Triggers</span></span>
* <span data-ttu-id="4ffb6-1198">A(z) `New-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1198">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="4ffb6-1199">Új triggerek létrehozása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1199">Create new Triggers</span></span>
* <span data-ttu-id="4ffb6-1200">A(z) `Remove-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1200">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="4ffb6-1201">Triggerek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1201">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4ffb6-1202">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1202">Az.DataFactory</span></span>
* <span data-ttu-id="4ffb6-1203">Az ADF .Net SDK a 4.4.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1203">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="4ffb6-1204">Az ExpressCustomSetup paraméter hozzá lett adva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz a beállítási konfigurációk és külső összetevők egyéni beállítási szkript nélkül történő engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1204">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4ffb6-1205">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1205">Az.DataLakeStore</span></span>
* <span data-ttu-id="4ffb6-1206">Frissült a Get-AzDataLakeStoreDeletedItem és a Restore-AzDataLakeStoreDeletedItem dokumentációja</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1206">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4ffb6-1207">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1207">Az.EventHub</span></span>
* <span data-ttu-id="4ffb6-1208">A 10301-es hiba javítása: Az SAS-token dátumformátumának javítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1208">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4ffb6-1209">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1209">Az.FrontDoor</span></span>
* <span data-ttu-id="4ffb6-1210">Az Enable-AzFrontDoorCustomDomainHttps és a New-AzFrontDoorFrontendEndpointObject a MinimumTlsVersion paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1210">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="4ffb6-1211">A New-AzFrontDoorHealthProbeSettingObject a HealthProbeMethod és az EnabledState paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1211">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="4ffb6-1212">Új parancsmag érhető el a Front Door létrehozásakor/frissítésekor megadandó BackendPoolsSettings objektum létrehozásához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1212">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="4ffb6-1213">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1213">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4ffb6-1214">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1214">Az.Network</span></span>
* <span data-ttu-id="4ffb6-1215">A Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és a Start-AzVirtualnetworkGatewayPacketCapture.md FilterData kapcsolójának példái módosultak.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1215">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="4ffb6-1216">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1216">Az.PrivateDns</span></span>
* <span data-ttu-id="4ffb6-1217">A PrivateDns .net sdk frissült az 1.0.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1217">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4ffb6-1218">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1218">Az.RecoveryServices</span></span>
* <span data-ttu-id="4ffb6-1219">Mostantól Azure Site Recovery-támogatás érhető el a lemeztípus kiválasztásához a védelem engedélyezésekor.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1219">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="4ffb6-1220">Azure Site Recovery-hibajavítás a visszaállítási terv műveletének szerkesztéséhez.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1220">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="4ffb6-1221">SQL-visszaállítási támogatás az Azure Backuphoz a fájlstream-adatbázisok elfogadása érdekében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1221">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="4ffb6-1222">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1222">Az.RedisCache</span></span>
* <span data-ttu-id="4ffb6-1223">A MinimumTlsVersion paraméter hozzá lett adva a New-AzRedisCache és a Set-AzRedisCache parancsmagban.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1223">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="4ffb6-1224">Emellett a MinimumTlsVersion hozzá lett adva a Get-AzRedisCache parancsmag kimenetéhez.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1224">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="4ffb6-1225">Mostantól elérhető a -Size paraméter érvényesítése a Set-AzRedisCache és a New-AzRedisCache parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1225">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="4ffb6-1226">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1226">Az.Resources</span></span>
- <span data-ttu-id="4ffb6-1227">Frissültek a szabályzat parancsmagjai a 2019. 06. 01. dátumú új API-verzió használatára, amely tartalmazza az új EnforcementMode tulajdonságot a szabályzat-hozzárendelésekben.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1227">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="4ffb6-1228">Frissült a létrehozási szabályzat definíciójának súgóbeli példája</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1228">Updated create policy definition help example</span></span>
- <span data-ttu-id="4ffb6-1229">Kijavítottuk azt a hibát, amikor a Remove-AZADServicePrincipal -ServicePrincipalName null értékű hivatkozást ad vissza, ha az egyszerű szolgáltatásnév nem található.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1229">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="4ffb6-1230">Kijavítottuk azt a hibát, amikor a New-AZADServicePrincipal null értékű hivatkozást ad vissza, ha a bérlőnek nincs előfizetése.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1230">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="4ffb6-1231">A New-AzAdServicePrincipal módosult, és már csak a társított alkalmazáshoz ad hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1231">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="4ffb6-1232">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1232">Az.Sql</span></span>
* <span data-ttu-id="4ffb6-1233">Az adatbázisbeli ReadReplicaCount mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1233">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="4ffb6-1234">A Set-AzSqlDatabase ki lett javítva nem beállított zónaredundancia esetén</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1234">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="4ffb6-1235">3.0.0 – 2019. november</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1235">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="4ffb6-1236">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1236">General</span></span>
* <span data-ttu-id="4ffb6-1237">Megjelent az Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1237">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4ffb6-1238">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1238">Az.Accounts</span></span>
* <span data-ttu-id="4ffb6-1239">A Resolve-Error aliast érintő elavulási üzenet hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1239">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="4ffb6-1240">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1240">Az.Advisor</span></span>
* <span data-ttu-id="4ffb6-1241">Új Működésbeli kiválóság kategória hozzáadva a Get-AzAdvisorRecommendation parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1241">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4ffb6-1242">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1242">Az.Batch</span></span>
* <span data-ttu-id="4ffb6-1243">A `CoreQuota` átnevezve `BatchAccountContext` értékre a következőn: `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1243">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="4ffb6-1244">Emellett egy új `LowPriorityCoreQuota` elem is található.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1244">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="4ffb6-1245">Ez hatással van a következőre: **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1245">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="4ffb6-1246">A **New-AzBatchTask** `-ResourceFile` paraméter most már `PSResourceFile` objektumok gyűjteményét használja, amely az új **New-AzBatchResourceFile** parancsmaggal hozható létre.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1246">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="4ffb6-1247">Új **New-AzBatchResourceFile** parancsfájl a szükséges `PSResourceFile` objektumok létrehozásának elősegítéséhez.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1247">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="4ffb6-1248">Ezek az **New-AzBatchTask**`-ResourceFile` paraméterénél adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1248">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="4ffb6-1249">Ez két új típusú erőforrásfájlt támogat a meglévő `HttpUrl` mód mellett:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1249">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="4ffb6-1250">Az `AutoStorageContainerName`-alapú erőforrásfájlok egy teljes automatikus tárolót töltenek le a Batch-csomópontra.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1250">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="4ffb6-1251">A `StorageContainerUrl`-alapú erőforrásfájlok az URL-címben megadott tárolót töltik le a Batch-csomópontra.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1251">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="4ffb6-1252">A `PSApplication`**Get-AzBatchApplication** által visszaadott `ApplicationPackages` tulajdonsága eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1252">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="4ffb6-1253">Most már lekérhetők az alkalmazásokon belüli adott csomagok a **Get-AzBatchApplicationPackage** használatával.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1253">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="4ffb6-1254">Például: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1254">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="4ffb6-1255">Az `ApplicationId` átnevezve `ApplicationName` értékre a **Get-AzBatchApplicationPackage**, a **New-AzBatchApplicationPackage**, a **Remove-AzBatchApplicationPackage**, a **Get-AzBatchApplication**, a **New-AzBatchApplication**, a **Remove-AzBatchApplication** és a **Set-AzBatchApplication** esetében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1255">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="4ffb6-1256">Az `ApplicationId` mostantól az `ApplicationName` aliasa.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1256">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="4ffb6-1257">Az új `PSWindowsUserConfiguration` tulajdonság hozzáadva a következőhöz: `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1257">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="4ffb6-1258">A `Version` átnevezve `Name` értékre a `PSApplicationPackage` esetében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1258">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="4ffb6-1259">A `BlobSource` átnevezve `HttpUrl` értékre a `PSResourceFile` esetében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1259">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="4ffb6-1260">Az `OSDisk` tulajdonság eltávolítva a következőből: `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1260">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="4ffb6-1261">A **Set-AzBatchPoolOSVersion** eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1261">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="4ffb6-1262">Ez a művelet már nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1262">This operation is no longer supported.</span></span>
* <span data-ttu-id="4ffb6-1263">`PSCloudServiceConfiguration``TargetOSVersion` eleme eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1263">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="4ffb6-1264">A `CurrentOSVersion` átnevezve `OSVersion` értékre a `PSCloudServiceConfiguration` esetében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1264">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="4ffb6-1265">`DataEgressGiB` és `DataIngressGiB` eltávolítva a következőből: `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1265">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="4ffb6-1266">A **Get-AzBatchNodeAgentSku** eltávolítva és a **Get-AzBatchSupportedImage** parancsmaggal helyettesítve.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1266">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="4ffb6-1267">A **Get-AzBatchSupportedImage** ugyanazokat az adatokat jeleníti meg, mint a **Get-AzBatchNodeAgentSku**, csak egyszerűbb formátumban.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1267">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="4ffb6-1268">Most már új, nem ellenőrzött rendszerképeket is visszaad a rendszer.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1268">New non-verified images are also now returned.</span></span> <span data-ttu-id="4ffb6-1269">Minden rendszerképről további, `Capabilities` és `BatchSupportEndOfLife` típusú információk is szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1269">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="4ffb6-1270">Lehetőség arra, hogy távoli fájlrendszereket lehessen csatlakoztatni egy készlet minden csomópontjára a **New-AzBatchPool** új `MountConfiguration` paraméterével.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1270">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="4ffb6-1271">Most már támogatja a hálózati biztonsági szabályokat, amelyek a letiltják a készletekhez való hozzáférést a forgalom forrásportja alapján.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1271">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="4ffb6-1272">Ez a `PSNetworkSecurityGroupRule``SourcePortRanges` tulajdonsága alapján történik.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1272">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="4ffb6-1273">Tároló futtatásakor a Batch támogatja a feladat végrehajtását a tároló munkakönyvtárában vagy a Batch-feladat munkakönyvtárában.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1273">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="4ffb6-1274">Ezt a `PSTaskContainerSettings``WorkingDirectory` tulajdonsága szabályozza.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1274">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="4ffb6-1275">Új lehetőség nyilvános IP-gyűjtemény megadására az érintett `PSNetworkConfiguration` elemen az új `PublicIPs` tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1275">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="4ffb6-1276">Ez garantálja, hogy a készletben található csomópontok rendelkeznek majd IP-címmel a felhasználó által megadott IP-listáról.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1276">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="4ffb6-1277">Ha nincs megadva, a `PSSTartTask` alapértelmezett `WaitForSuccess` értéke `$True` (korábban `$False` volt).</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1277">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="4ffb6-1278">Ha nincs megadva, a `PSAutoUserSpecification` alapértelmezett `Scope` értéke `Pool` (korábban Windowson `Task`, Linuxon pedig `Pool` volt).</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1278">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4ffb6-1279">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1279">Az.Cdn</span></span>
* <span data-ttu-id="4ffb6-1280">A RulesEngine tartalmazza az új UrlRewriteAction és a CacheKeyQueryStringAction műveleteket.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1280">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="4ffb6-1281">Javítva számos olyan hiba, mint a New-AzDeliveryRuleCondition parancsmag hiányzó Selector bemenete.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1281">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4ffb6-1282">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1282">Az.Compute</span></span>
* <span data-ttu-id="4ffb6-1283">Lemeztitkosítási készlet funkció</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1283">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="4ffb6-1284">Új parancsmagok:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1284">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="4ffb6-1285">A DiskEncryptionSetId paraméter hozzá lett adva a következő parancsmagokhoz:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1285">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="4ffb6-1286">A DiskEncryptionSetId és az EncryptionType paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1286">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="4ffb6-1287">A PublicIPAddressVersion paraméter hozzá lett adva a New-AzVmssIPConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1287">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="4ffb6-1288">Egyéni szkriptbővítmény FileUris tulajdonságának módosítása nyilvánosról védett beállításra</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1288">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="4ffb6-1289">ScaleInPolicy hozzáadva a New-AzVmss, New-AzVmssConfig és Update-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1289">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="4ffb6-1290">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1290">Breaking changes</span></span>
    - <span data-ttu-id="4ffb6-1291">A New-AzDiskConfig esetében a DiskSizeGB helyett az UploadSizeInBytes paramétert kell használni, ha a CreateOption értéke Upload</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1291">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="4ffb6-1292">A PublishingProfile.Source.ManagedImage.Id elemet a StorageProfile.Source.Id helyettesíti a GalleryImageVersion objektumban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1292">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4ffb6-1293">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1293">Az.DataFactory</span></span>
* <span data-ttu-id="4ffb6-1294">Az ADF .Net SDK a 4.3.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1294">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4ffb6-1295">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1295">Az.DataLakeStore</span></span>
* <span data-ttu-id="4ffb6-1296">Az ADLS SDK-verziójának frissítése (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) , a következő javításokkal</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1296">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="4ffb6-1297">Kivétel jelzésének elkerülése, amikor a lomtár vagy a könyvtár bejegyzésének CreationTime tulajdonsága nem deszerializálható.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1297">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="4ffb6-1298">Beállítás megjelenítése minden kérelem-időtúllépés esetén az adlsclient objektumban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1298">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="4ffb6-1299">Az eredeti syncflag átadásának javítása a badoffset helyreállításához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1299">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="4ffb6-1300">Az EnumerateDirectory javítása a folytatási token válaszellenőrzés utáni lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1300">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="4ffb6-1301">Concat-hiba javítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1301">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4ffb6-1302">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1302">Az.FrontDoor</span></span>
* <span data-ttu-id="4ffb6-1303">Különféle elgépelések kijavítva a modulban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1303">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4ffb6-1304">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1304">Az.HDInsight</span></span>
* <span data-ttu-id="4ffb6-1305">Kijavítva az a hiba, amely miatt az ügyfél a Nem érvényes Base-64-sztring hibát kapta, amikor a Get-AzHDInsightCluster használatával próbálta lekérni a fürtöt az ADLSGen1 tároló esetében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1305">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="4ffb6-1306">Új, ApplicationId nevű paraméter hozzáadva az Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig és New-AzHDInsightCluster nevű három parancsmaghoz, hogy az ügyfél megadhassa a szolgáltatásnév alkalmazásazonosítóját az Azure Data Lake eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1306">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="4ffb6-1307">A Microsoft.Azure.Management.HDInsight 2.1.0 módosítva a következőre: 5.1.0</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1307">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="4ffb6-1308">Öt parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1308">Removed five cmdlets:</span></span>
    - <span data-ttu-id="4ffb6-1309">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1309">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="4ffb6-1310">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1310">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="4ffb6-1311">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1311">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="4ffb6-1312">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1312">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="4ffb6-1313">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1313">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="4ffb6-1314">Három parancsmag hozzáadva:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1314">Added three cmdlets:</span></span>
    - <span data-ttu-id="4ffb6-1315">Get-AzHDInsightMonitoring a Get-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1315">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="4ffb6-1316">Enable-AzHDInsightMonitoring az Enable-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1316">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="4ffb6-1317">Disable-AzHDInsightMonitoring a Disable-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1317">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="4ffb6-1318">A Get-AzHDInsightProperties javítva, hogy támogassa a képességinformációk adott helyről történő beszerzését.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1318">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="4ffb6-1319">Paraméterkészletek (Spark1, Spark2) eltávolítva a következőből: Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1319">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="4ffb6-1320">Az Add-AzHDInsightSecurityProfile parancsmag súgódokumentumai példákkal bővültek.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1320">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="4ffb6-1321">A következő parancsmagok kimeneti típusa megváltozott:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1321">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="4ffb6-1322">A Get-AzHDInsightProperties kimeneti típusa CapabilitiesResponse értékről AzureHDInsightCapabilities értékre változott.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1322">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="4ffb6-1323">A Remove-AzHDInsightCluster kimeneti típusa ClusterGetResponse értékről logikai értékre változott.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1323">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="4ffb6-1324">A Set-AzHDInsightGatewaySettings HttpConnectivitySettings kimeneti típusa GatewaySettings értékre változott.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1324">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="4ffb6-1325">Néhány forgatókönyvi teszteset hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1325">Added some scenario test cases.</span></span>
* <span data-ttu-id="4ffb6-1326">Néhány alias eltávolítva: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1326">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4ffb6-1327">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1327">Az.IotHub</span></span>
* <span data-ttu-id="4ffb6-1328">Kompatibilitástörő változások:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1328">Breaking changes:</span></span>
    - <span data-ttu-id="4ffb6-1329">Az Add-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1329">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="4ffb6-1330">Az Add-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1330">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="4ffb6-1331">A Get-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1331">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="4ffb6-1332">A Get-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1332">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="4ffb6-1333">A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1333">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="4ffb6-1334">A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1334">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="4ffb6-1335">A New-AzIotHubExportDevice parancsmag már nem támogatja a New-AzIotHubExportDevices aliast.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1335">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="4ffb6-1336">A New-AzIotHubImportDevice parancsmag már nem támogatja a New-AzIotHubImportDevices aliast.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1336">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="4ffb6-1337">A Remove-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1337">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="4ffb6-1338">A Remove-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1338">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="4ffb6-1339">A Set-AzIotHub parancsmag a továbbiakban nem támogatja az OperationsMonitoringProperties paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1339">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="4ffb6-1340">A Set-AzIotHub parancsmaghoz tartozó UpdateOperationsMonitoringProperties paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1340">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4ffb6-1341">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1341">Az.RecoveryServices</span></span>
* <span data-ttu-id="4ffb6-1342">Azure Site Recovery-támogatás az olyan hálózati erőforrások konfigurálásához, mint a hálózati biztonsági csoportok, a nyilvános IP-címek és az Azure–Azure belső terheléselosztók.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1342">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="4ffb6-1343">Azure Site Recovery-támogatás felügyelt lemezekre történő íráshoz VMware-ről az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1343">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="4ffb6-1344">Azure Site Recovery-támogatás hálózati adapter csökkentéséhez VMware-ről az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1344">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="4ffb6-1345">Azure Site Recovery-támogatás a hálózat felgyorsításához Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1345">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="4ffb6-1346">Azure Site Recovery-támogatás az automatikus frissítési ügynök biztosításához Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1346">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="4ffb6-1347">Azure Site Recovery-támogatás standard SSD-meghajtóhoz Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1347">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="4ffb6-1348">Azure Site Recovery-támogatás az Azure Disk Encryption kétlépéses hitelesítéséhez Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1348">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="4ffb6-1349">Azure Site Recovery-támogatás az újonnan hozzáadott lemez védelméhez Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1349">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="4ffb6-1350">SoftDelete funkció hozzáadva a virtuális géphez, továbbá a softdelete-hez hozzáadott tesztek</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1350">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="4ffb6-1351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1351">Az.Resources</span></span>
* <span data-ttu-id="4ffb6-1352">A Microsoft.Extensions.Caching.Memory függőségi szerelvény frissítése 1.1.1-esről 2.2-es verzióra</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1352">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4ffb6-1353">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1353">Az.Network</span></span>
* <span data-ttu-id="4ffb6-1354">A PrivateEndpointConnection összes parancsmagjának módosítása az általános szolgáltató támogatásához.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1354">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="4ffb6-1355">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1355">Updated cmdlet:</span></span>
        - <span data-ttu-id="4ffb6-1356">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1356">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4ffb6-1357">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1357">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4ffb6-1358">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1358">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4ffb6-1359">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1359">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4ffb6-1360">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1360">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="4ffb6-1361">Új parancsmag hozzáadása a PrivateLinkResource-hoz, valamint az általános szolgáltató támogatása.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1361">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="4ffb6-1362">Új parancsmag:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1362">New cmdlet:</span></span>
        - <span data-ttu-id="4ffb6-1363">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1363">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="4ffb6-1364">Új mezőket és paramétereket ad a Proxy Protocol V2 funkcióhoz.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1364">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="4ffb6-1365">Hozzáadja az EnableProxyProtocol tulajdonságot a PrivateLinkService osztályban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1365">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="4ffb6-1366">Hozzáadja a LinkIdentifier tulajdonságot a PrivateEndpointConnection osztályban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1366">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="4ffb6-1367">New-AzPrivateLinkService frissítve az új, választható EnableProxyProtocol paraméter hozzáadásával.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1367">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="4ffb6-1368">Ki lett javítva a New-AzApplicationGatewaySku referenciadokumentációjában található helytelen paraméterleírás</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1368">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="4ffb6-1369">Új parancsmagok az Azure Firewall-szabályzat támogatásához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1369">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="4ffb6-1370">A VirtualHub RouteTables gyermekerőforrásának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1370">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="4ffb6-1371">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1371">New cmdlets added:</span></span>
        - <span data-ttu-id="4ffb6-1372">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1372">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="4ffb6-1373">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1373">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="4ffb6-1374">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1374">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="4ffb6-1375">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1375">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="4ffb6-1376">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1376">Set-AzVirtualHub</span></span>
* <span data-ttu-id="4ffb6-1377">Az új termékváltozat és VirtualWANType tulajdonság támogatásának hozzáadása a VirtualHub, illetve a VirtualWan esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1377">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="4ffb6-1378">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1378">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="4ffb6-1379">New-AzVirtualHub: Sku paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1379">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="4ffb6-1380">Update-AzVirtualHub: Sku paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1380">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="4ffb6-1381">New-AzVirtualWan: VirtualWANType paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1381">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="4ffb6-1382">Update-AzVirtualWan: VirtualWANType paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1382">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="4ffb6-1383">Az EnableInternetSecurity tulajdonság támogatásának hozzáadása a HubVnetConnection, a VpnConnection és az ExpressRouteConnection esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1383">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="4ffb6-1384">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1384">New cmdlets added:</span></span>
        - <span data-ttu-id="4ffb6-1385">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1385">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="4ffb6-1386">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1386">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="4ffb6-1387">New-AzureRmVirtualHubVnetConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1387">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="4ffb6-1388">New-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1388">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="4ffb6-1389">Update-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1389">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="4ffb6-1390">New-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1390">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="4ffb6-1391">Set-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1391">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="4ffb6-1392">TopLevel WebApplicationFirewall-szabályzat beállításának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1392">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="4ffb6-1393">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1393">New cmdlets added:</span></span>
        - <span data-ttu-id="4ffb6-1394">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1394">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="4ffb6-1395">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1395">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="4ffb6-1396">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1396">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="4ffb6-1397">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1397">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="4ffb6-1398">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1398">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="4ffb6-1399">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1399">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="4ffb6-1400">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1400">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="4ffb6-1401">New-AzApplicationGatewayFirewallPolicy: PolicySetting, ManagedRule paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1401">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="4ffb6-1402">A CustomRule Geo-Match operátorának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1402">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="4ffb6-1403">A GeoMatch hozzáadva a FirewallCondition operátorához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1403">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="4ffb6-1404">perListener és a perSite tűzfalszabályzat támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1404">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="4ffb6-1405">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1405">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="4ffb6-1406">New-AzApplicationGatewayHttpListener: FirewallPolicy, FirewallPolicyId paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1406">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="4ffb6-1407">New-AzApplicationGatewayPathRuleConfig: FirewallPolicy, FirewallPolicyId paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1407">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="4ffb6-1408">Javítva: a PSBastion esetében a szükséges AzureBastionSubnet alhálózat nevében nem kell megkülönböztetni a kis- és nagybetűket</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1408">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="4ffb6-1409">A hálózati szabályok céltartományneveinek és a NAT-szabályok lefordított tartományneveinek támogatása az Azure Firewallban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1409">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="4ffb6-1410">Az IpGroup legfelsőbb szintű RouteTables erőforrásának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1410">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="4ffb6-1411">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1411">New cmdlets added:</span></span>
        - <span data-ttu-id="4ffb6-1412">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1412">New-AzIpGroup</span></span>
        - <span data-ttu-id="4ffb6-1413">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1413">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="4ffb6-1414">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1414">Get-AzIpGroup</span></span>
        - <span data-ttu-id="4ffb6-1415">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1415">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4ffb6-1416">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1416">Az.ServiceFabric</span></span>
* <span data-ttu-id="4ffb6-1417">Az Add-AzServiceFabricApplicationCertificate parancsmag el lett távolítva, mivel az Add-AzVmssSecret lefedi ezt a forgatókönyvet.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1417">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="4ffb6-1418">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1418">Az.Sql</span></span>
* <span data-ttu-id="4ffb6-1419">Törölt adatbázisok visszaállításának támogatása hozzáadva a felügyelt példányokon.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1419">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="4ffb6-1420">A régi naplózási parancsmagok elavulttá váltak a kódban.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1420">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="4ffb6-1421">A következő elavult aliasok el lettek távolítva:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1421">Removed deprecated aliases:</span></span>
* <span data-ttu-id="4ffb6-1422">Get-AzSqlDatabaseIndexRecommendations (a Get-AzSqlDatabaseIndexRecommendation használata javasolt helyette)</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1422">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="4ffb6-1423">Get-AzSqlDatabaseRestorePoints (a Get-AzSqlDatabaseRestorePoint használata javasolt helyette)</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1423">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="4ffb6-1424">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag eltávolítva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1424">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="4ffb6-1425">Az elavult sebezhetőség-felmérési beállítások parancsmagjainak aliasai eltávolítva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1425">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="4ffb6-1426">A fejlett fenyegetésészlelési beállítások parancsmagjai elavulttá váltak</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1426">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="4ffb6-1427">Parancsmagok hozzáadása egy adatbázis oszlopait érintő érzékenységi javaslatok letiltása és engedélyezése céljából.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1427">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4ffb6-1428">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1428">Az.Storage</span></span>
* <span data-ttu-id="4ffb6-1429">Nagy fájlok megosztásának engedélyezése Storage-fiók létrehozása vagy frissítése esetén</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1429">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="4ffb6-1430">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1430">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="4ffb6-1431">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1431">Set-AzStorageAccount</span></span>
* <span data-ttu-id="4ffb6-1432">Fájlkezelő bezárása/lekérése esetén a fájlkönyvtár vagy fájl bemeneti elérési út ellenőrzése kimarad, hogy a DeletePending állapotban lévő objektum ne okozhasson hibát</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1432">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="4ffb6-1433">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1433">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="4ffb6-1434">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1434">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="4ffb6-1435">2.8.0 – 2019. október</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1435">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="4ffb6-1436">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1436">General</span></span>
* <span data-ttu-id="4ffb6-1437">Az.HealthcareApis 1.0.0-s kiadás</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1437">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4ffb6-1438">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1438">Az.Accounts</span></span>
* <span data-ttu-id="4ffb6-1439">A telemetria és az URL-címek újraírásának frissítése a létrehozott modulok esetében, a Windows-egységek tesztelésének javítása.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1439">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4ffb6-1440">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1440">Az.ApiManagement</span></span>
* <span data-ttu-id="4ffb6-1441">**Set-AzApiManagementApi** – Az API a következőre való frissítésének támogatása: ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1441">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="4ffb6-1442">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1442">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4ffb6-1443">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1443">Az.Automation</span></span>
* <span data-ttu-id="4ffb6-1444">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag a Linux újraindítási beállítási paramétere kapcsán.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1444">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4ffb6-1445">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1445">Az.Batch</span></span>
* <span data-ttu-id="4ffb6-1446">A **Get-AzBatchNodeAgentSku** elavult, így a 2.0.0-ás verziótól a **Get-AzBatchSupportImage** váltja fel.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1446">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4ffb6-1447">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1447">Az.Compute</span></span>
* <span data-ttu-id="4ffb6-1448">A Priority, EvictionPolicy és MaxPrice paraméterek hozzáadása a New-AzVM és a New-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1448">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="4ffb6-1449">Az Add-AzVMAdditionalUnattendContent és az Add-AzVMSshPublicKey parancsmagok figyelmeztető üzenetének és súgójának kijavítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1449">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="4ffb6-1450">A -skipVmBackup kivétel kijavítása felügyelt lemezekkel rendelkező Linux rendszerű virtuális gépek esetében a Set-AzVMDiskEncryptionExtension kapcsán.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1450">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="4ffb6-1451">A titkosítási beállítások frissítési hibájának kijavítása a Set-AzVMDiskEncryptionExtension kétmenetes forgatókönyvében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1451">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4ffb6-1452">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1452">Az.DataFactory</span></span>
* <span data-ttu-id="4ffb6-1453">CRUD-parancsok lettek hozzáadva az ADF V2-adatfolyamhoz: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow és Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1453">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="4ffb6-1454">Műveleti parancsok lettek hozzáadva az ADF V2-adatfolyam hibakeresési munkamenetéhez: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand és Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1454">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="4ffb6-1455">Az ADF .Net SDK a 4.2.0-ás verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1455">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4ffb6-1456">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1456">Az.DataLakeStore</span></span>
* <span data-ttu-id="4ffb6-1457">A fiókérvényesítés javítása, hogy a "-" jelölésű fiókok tartomány nélkül is továbbíthatók legyenek</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1457">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="4ffb6-1458">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1458">Az.HealthcareApis</span></span>
* <span data-ttu-id="4ffb6-1459">A PowerShell az 1.0.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1459">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="4ffb6-1460">Az SDK a 1.0.2-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1460">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="4ffb6-1461">Frissítés a tesztekben az új SDK-verzióra való hivatkozáshoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1461">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="4ffb6-1462">A kimeneti struktúra beágyazottról simítottra frissült.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1462">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4ffb6-1463">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1463">Az.IotHub</span></span>
* <span data-ttu-id="4ffb6-1464">Új útválasztási forrás hozzáadása: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1464">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="4ffb6-1465">Kisebb hibajavítás: A Get-AzIothub nem adja vissza a következőt: subscriptionId</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1465">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4ffb6-1466">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1466">Az.Monitor</span></span>
* <span data-ttu-id="4ffb6-1467">Új műveleticsoport-fogadók hozzáadva a következő műveleti csoporthoz:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1467">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="4ffb6-1468">Az általános riasztási séma használata engedélyezve a fogadók számára.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1468">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="4ffb6-1469">Ez nem vonatkozik az SMS, az Azure App leküldéses üzenetei, az ITSM és a Voice fogadóira.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1469">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="4ffb6-1470">A webhookok mostantól az Azure Active Directory-hitelesítés használatát is támogatják.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1470">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4ffb6-1471">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1471">Az.Network</span></span>
* <span data-ttu-id="4ffb6-1472">Új Get-AzAvailableServiceAlias parancsmag hozzáadva, amely a szolgáltatásvégpont-szabályzatokhoz használható aliasok beszerzéséhez hívható meg.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1472">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="4ffb6-1473">Forgalomválasztók hozzáadásának támogatása a virtuális hálózati átjáró kapcsolataihoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1473">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="4ffb6-1474">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1474">New cmdlets added:</span></span>
        - <span data-ttu-id="4ffb6-1475">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1475">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="4ffb6-1476">Parancsmagok frissítve választható paraméterekkel -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1476">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="4ffb6-1477">Az ESP és AH protokollok támogatása a hálózati biztonsági szabályzati konfigurációkban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1477">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="4ffb6-1478">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1478">Updated cmdlets:</span></span>
        - <span data-ttu-id="4ffb6-1479">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1479">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="4ffb6-1480">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1480">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="4ffb6-1481">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1481">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="4ffb6-1482">Tovább javult a Cortex-parancsmagok kivételeinek kezelése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1482">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="4ffb6-1483">A VirtualNetworkGateways új generációi és termékváltozatai</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1483">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="4ffb6-1484">A VirtualNetworkGateways új generációinak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1484">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="4ffb6-1485">A VirtualNetworkGateways új, nagy átviteli sebességű termékváltozatainak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1485">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="4ffb6-1486">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1486">Az.RedisCache</span></span>
* <span data-ttu-id="4ffb6-1487">Frissült a Set-AzRedisCache referenciadokumentációja, amely most már tartalmazza a -Size paraméter hiányzó értékeit.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1487">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="4ffb6-1488">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1488">Az.Sql</span></span>
* <span data-ttu-id="4ffb6-1489">Az Active Directory-rendszergazda a felügyelt példányon való beállításának támogatása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1489">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4ffb6-1490">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1490">Az.Storage</span></span>
* <span data-ttu-id="4ffb6-1491">Az Storage-ügyfélkódtár a 11.1.0-s verzióra frissült.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1491">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="4ffb6-1492">A Management plane API-val rendelkező tárolók listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1492">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="4ffb6-1493">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1493">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="4ffb6-1494">A tárfiókok előfizetésből történő listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1494">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="4ffb6-1495">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1495">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="4ffb6-1496">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1496">Az.StorageSync</span></span>
* <span data-ttu-id="4ffb6-1497">A Reset-AzStorageSyncServerCertificate 9810-es hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1497">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4ffb6-1498">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1498">Az.Websites</span></span>
* <span data-ttu-id="4ffb6-1499">Egy alkalmazáshoz tartozó ASP Set-AzWebApp általi frissítése sikertelen volt</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1499">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="4ffb6-1500">2.7.0 – 2019. szeptember</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1500">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="4ffb6-1501">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1501">Az.ApiManagement</span></span>
* <span data-ttu-id="4ffb6-1502">Frissítve lett a „-Format” paraméter leírása a „Set-AzApiManagementPolicy” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1502">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="4ffb6-1503">El lettek távolítva az elavult „Update-AzApiManagementDeployment” parancsmag referenciái a referenciadokumentációból.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1503">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="4ffb6-1504">A „Set-AzApiManagement” használható helyette.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1504">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4ffb6-1505">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1505">Az.Automation</span></span>
* <span data-ttu-id="4ffb6-1506">Ki lett javítva a „Register-AzAutomationDscNode” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1506">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="4ffb6-1507">Hozzá lett adva az operációs rendszerrel kapcsolatos korlátozások pontosítása a Register-AzAutomationDSCNode parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1507">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="4ffb6-1508">Ki lett javítva a Start-AzAutomationRunbook parancsmag null értékű hivatkozás okozta kivétele a -Wait paraméter esetén.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1508">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4ffb6-1509">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1509">Az.Compute</span></span>
* <span data-ttu-id="4ffb6-1510">Hozzá lett adva az UploadSizeInBytes paraméter a New-AzDiskConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1510">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="4ffb6-1511">Hozzá lett adva az Incremental paraméter a New-AzSnapshotConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1511">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="4ffb6-1512">Alacsony prioritású virtuálisgép-funkció hozzáadása:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1512">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="4ffb6-1513">Hozzá lett adva a MaxPrice, az EvictionPolicy és a Priority paraméter a New-AzVMConfig parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1513">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="4ffb6-1514">Hozzá lett adva a MaxPrice paraméter a New-AzVmssConfig, az Update-AzVM és az Update-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1514">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="4ffb6-1515">Ki lett javítva a Get-AzAvailabilitySet parancsmag virtuálisgép-hivatkozással kapcsolatos hibája, amely miatt a parancsmag az előfizetésben található összes rendelkezésreállási csoportot listázta.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1515">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="4ffb6-1516">Ki lett javítva a Get-AzRemoteDesktopFile parancsmag esetében jelentkező null kivétel.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1516">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="4ffb6-1517">Ki lett javítva virtuális merevlemezek Seek metódusa a végrelatív pozíció esetében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1517">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="4ffb6-1518">Ki lett javítva az UltraSSD hibája a New-AzVM és az Update-AzVM parancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1518">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4ffb6-1519">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1519">Az.DataFactory</span></span>
* <span data-ttu-id="4ffb6-1520">Hozzá lett adva 3 új parancs (az Add-AzDataFactoryV2TriggerSubscription, a Remove-AzDataFactoryV2TriggerSubscription és a Get-AzDataFactoryV2TriggerSubscriptionStatus) az ADF V2-höz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1520">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="4ffb6-1521">Az ADF .Net SDK a 4.1.3-as verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1521">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4ffb6-1522">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1522">Az.HDInsight</span></span>
* <span data-ttu-id="4ffb6-1523">Kompatibilitástörő változások a meghívással kapcsolatban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1523">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4ffb6-1524">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1524">Az.IotHub</span></span>
* <span data-ttu-id="4ffb6-1525">Hozzá lett adva az IoTHubok földrajzilag párosított vészhelyreállítási régiójába történő feladatátvétel meghívásának támogatása.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1525">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="4ffb6-1526">Hozzá lett adva az IoTHubok üzenetbővítés-kezelésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1526">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="4ffb6-1527">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1527">New cmdlets are:</span></span>
    - <span data-ttu-id="4ffb6-1528">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1528">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="4ffb6-1529">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1529">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="4ffb6-1530">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1530">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="4ffb6-1531">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1531">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4ffb6-1532">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1532">Az.Monitor</span></span>
* <span data-ttu-id="4ffb6-1533">A legújabb Monitor SDK-ra mutat, azaz a 0.24.1-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1533">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="4ffb6-1534">Nem kompatibilitástörő változásokkal bővíti a Metrics parancsmagokat, így az egységek számbavétele számos új értéket támogat.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1534">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="4ffb6-1535">Ezek írásvédett parancsmagok, ezért a parancsmagok bemenetében nem történik változás.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1535">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="4ffb6-1536">Az **ActionGroups**-kérések api-version értéke mostantól **2019-06-01**, korábban **2018-03-01** volt.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1536">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="4ffb6-1537">A forgatókönyvtesztek frissültek, így igazodnak a változáshoz.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1537">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="4ffb6-1538">Az **EmailReceiver** és a **WebhookReceiver** osztályok konstruktoraihoz hozzá lett adva egy új kötelező argumentum, a **useCommonAlertSchema** nevű logikai érték.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1538">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="4ffb6-1539">A kompatibilitástörő változás parancsmagok elől való elrejtése érdekében a rögzített érték jelenleg a **false** (hamis).</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1539">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="4ffb6-1540">**MEGJEGYZÉS**: Ez egy átmeneti módosítás, amelyet a Riasztások csapatnak érvényesítenie kell.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1540">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="4ffb6-1541">A **Source** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1541">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="4ffb6-1542">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1542">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="4ffb6-1543">Az **AlertingAction** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1543">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="4ffb6-1544">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1544">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="4ffb6-1545">A dinamikus küszöbérték kritériumainak támogatása a 2-es verziójú metrikariasztás esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1545">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="4ffb6-1546">New-AzMetricAlertRuleV2Criteria: mostantól a dinamikus küszöbértékek kritériumait is létrehozza</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1546">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="4ffb6-1547">Add-AzMetricAlertRuleV2: mostantól a dinamikus küszöbértékek kritériumait is elfogadja</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1547">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="4ffb6-1548">Az ütemezett lekérdezési szabályok parancsmagjainak (SQR) fejlesztései</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1548">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="4ffb6-1549">A parancsmagok a „Location” paraméter mindkét formátumát elfogadják: a helyet (például eastus) és a hely megjelenített nevét is (például USA keleti régiója)</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1549">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="4ffb6-1550">Megfelelően ábrázolva lett az „Enabled” paraméter a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1550">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="4ffb6-1551">Példák lettek hozzáadva az „ActionGroup” opcionális paraméterhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1551">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="4ffb6-1552">Általánosan továbbfejlesztett súgófájlok</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1552">Overall improved help files</span></span>
* <span data-ttu-id="4ffb6-1553">Ki lett javítva a „Set-AzActionRule” hatókörtípusának meghatározásával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1553">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4ffb6-1554">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1554">Az.Network</span></span>
* <span data-ttu-id="4ffb6-1555">Ki lett javítva a „New-AzApplicationGateway” referenciadokumentációjában található helytelen példa</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1555">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="4ffb6-1556">Hozzá lett adva egy csomagrögzítés összes tulajdonságának lekérésével kapcsolatos megjegyzés a „Get-AzNetworkWatcherPacketCapture” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1556">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="4ffb6-1557">Ki lett javítva a „Test-AzNetworkWatcherIPFlow” referenciadokumentációjában található példa a hálózati adapterek megfelelő számbavétele érdekében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1557">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="4ffb6-1558">Tovább lett fejlesztve a felhőkivétel-elemzés az esetleges további részletek megjelenítése érdekében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1558">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="4ffb6-1559">Tovább lett fejlesztve a felhőkivétel-elemzés az SDK-kivételek további típusainak kezelése érdekében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1559">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="4ffb6-1560">Ki lett javítva a biztonságiszabály-modellek helytelen leképezése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1560">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="4ffb6-1561">Hozzá lettek adva a privát IP-cím funkcióval kapcsolatos tulajdonságok a hálózati adapterhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1561">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="4ffb6-1562">Hozzá lett adva a „PrivateEndpoint” tulajdonság PSResourceId típusúként a PSNetworkInterface osztályhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1562">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="4ffb6-1563">Hozzá lett adva a „PrivateLinkConnectionProperties” tulajdonság PSIpConfigurationConnectivityInformation típusúként a PSNetworkInterfaceIPConfiguration osztályhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1563">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="4ffb6-1564">Hozzá lett adva a PSIpConfigurationConnectivityInformation nevű új modellosztály</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1564">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="4ffb6-1565">Hozzá lett adva az új ApplicationRuleProtocolType „mssql” az Azure Firewall-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1565">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="4ffb6-1566">MultiLink-támogatás a Virtuális WAN-ben</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1566">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="4ffb6-1567">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1567">New cmdlets</span></span>
        - <span data-ttu-id="4ffb6-1568">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1568">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="4ffb6-1569">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1569">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="4ffb6-1570">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1570">Updated cmdlet:</span></span>
        - <span data-ttu-id="4ffb6-1571">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1571">New-VpnSite</span></span>
        - <span data-ttu-id="4ffb6-1572">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1572">Update-VpnSite</span></span>
        - <span data-ttu-id="4ffb6-1573">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1573">New-VpnConnection</span></span>
        - <span data-ttu-id="4ffb6-1574">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1574">Update-VpnConnection</span></span>
* <span data-ttu-id="4ffb6-1575">Ki lettek javítva bizonyos PowerShell-példák dokumentumai, hogy az AzureRM-parancsmagok helyett az Az-parancsmagokat használják</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1575">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4ffb6-1576">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1576">Az.RecoveryServices</span></span>
* <span data-ttu-id="4ffb6-1577">Frissítve lett az AzureVMpolicy objektum a ProtectedItemsCount attribútummal</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1577">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="4ffb6-1578">Tesztek lettek hozzáadva a virtuális gép szabályzatához és az eredeti Storage-fiók visszaállításához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1578">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="4ffb6-1579">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1579">Az.Resources</span></span>
* <span data-ttu-id="4ffb6-1580">Ki lett javítva a hiba, amely miatt a New-AzRoleAssignment parancsot nem lehetett meghívni a Scope paraméter nélkül.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1580">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4ffb6-1581">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1581">Az.ServiceFabric</span></span>
* <span data-ttu-id="4ffb6-1582">Ki lett javítva az „Update-AzServiceFabricReliability” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1582">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="4ffb6-1583">Új parancsmagok lettek hozzáadva az alkalmazás és a szolgáltatások felügyeletéhez:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1583">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="4ffb6-1584">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1584">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="4ffb6-1585">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1585">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="4ffb6-1586">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1586">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="4ffb6-1587">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1587">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="4ffb6-1588">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1588">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="4ffb6-1589">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1589">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="4ffb6-1590">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1590">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="4ffb6-1591">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1591">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="4ffb6-1592">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1592">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="4ffb6-1593">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1593">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="4ffb6-1594">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1594">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="4ffb6-1595">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1595">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="4ffb6-1596">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1596">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="4ffb6-1597">A Service Fabric SDK az 1.2.0-s verzióra frissült, amely a Service Fabric erőforrás-szolgáltató 2019-03-01 api-versionjét használja.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1597">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="4ffb6-1598">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1598">Az.SignalR</span></span>
* <span data-ttu-id="4ffb6-1599">Hozzá lettek adva az Update, Restart, CheckNameAvailability és GetUsage parancsmagok</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1599">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="4ffb6-1600">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1600">Az.Sql</span></span>
* <span data-ttu-id="4ffb6-1601">Frissítve lett a „Get-AzSqlElasticPool” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1601">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="4ffb6-1602">Hozzá lett adva egy rugalmas készlet létrehozását bemutató virtuálismag-példa (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1602">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="4ffb6-1603">El lett távolítva az EmailAddresses érvényesítése és annak ellenőrzése, hogy az EmailAdmins értéke hamis-e abban az esetben, ha az EmailAddresses üres a Set-AzSqlServerAdvancedThreatProtectionPolicy és a Set-AzSqlDatabaseAdvancedThreatProtectionPolicy parancsmagban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1603">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="4ffb6-1604">Engedélyezve lettek a kiszolgáló-/adatbázis-naplózási beállítások abban az esetben, ha több olyan diagnosztikai beállítás létezik, amelyek engedélyezik a naplózási kategóriát.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1604">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="4ffb6-1605">Ki lett javítva az e-mail-címek ellenőrzése több, SQL-sebezhetőségi felméréshez használt parancsmagban (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting és Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1605">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4ffb6-1606">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1606">Az.Storage</span></span>
* <span data-ttu-id="4ffb6-1607">Frissítve lett a „Get-AzStorageAccountKey” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1607">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="4ffb6-1608">A forrásfájl SMB-tulajdonságai (fájlattribútumok, fájl létrehozásának ideje, fájl utolsó írásának ideje) célfájlban történő megtartásának támogatása az Azure File-beli feltöltés/letöltés esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1608">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="4ffb6-1609">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1609">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="4ffb6-1610">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1610">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="4ffb6-1611">Ki lett javítva a tulajdonság-/metaadathibával meghiúsuló blokkblobfeltöltés a tárolóképes ImmutabilityPolicy esetében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1611">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="4ffb6-1612">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1612">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="4ffb6-1613">Az Azure File-megosztások Management plane API-val történő kezelésének támogatása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1613">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="4ffb6-1614">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1614">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="4ffb6-1615">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1615">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="4ffb6-1616">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1616">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="4ffb6-1617">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1617">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4ffb6-1618">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1618">Az.Websites</span></span>
* <span data-ttu-id="4ffb6-1619">Ki lett javítva az a probléma, amely miatt a webalkalmazás Címkéi törölve lettek az alkalmazás új ASP-be történő migrálásakor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1619">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="4ffb6-1620">Ki lett javítva a Publish-AzureWebapp parancs a Linux és Windows rendszeren történő működés érdekében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1620">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="4ffb6-1621">Frissítve lett a „Get-AzWebAppPublishingProfile” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1621">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="4ffb6-1622">2.6.0 – 2019. augusztus</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1622">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="4ffb6-1623">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1623">General</span></span>
* <span data-ttu-id="4ffb6-1624">Különféle elgépelések kijavítva több modulban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1624">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4ffb6-1625">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1625">Az.Accounts</span></span>
* <span data-ttu-id="4ffb6-1626">Felhasználó által hozzárendelt MSI támogatása az Azure Functions-hitelesítésben (#9479)</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1626">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="4ffb6-1627">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1627">Az.Aks</span></span>
* <span data-ttu-id="4ffb6-1628">A Get-AzAks kimenetével kapcsolatos probléma ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1628">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="4ffb6-1629">További információ: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1629">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4ffb6-1630">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1630">Az.ApiManagement</span></span>
* <span data-ttu-id="4ffb6-1631">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1631">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="4ffb6-1632">Frissült a .net nuget verziója, amely nem kényszeríti ki a productId, az apiId, a groupId és a userId korlátozásait</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1632">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="4ffb6-1633">**Get-AzApiManagementProduct** – A termékek API-val történő lekérdezése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1633">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="4ffb6-1634">**New-AzApiManagementApiRevision** – Ki lett javítva az a probléma, amely miatt az ApiRevisionDescription nem lett beállítva az új API-változat létrehozásakor https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1634">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="4ffb6-1635">Ki lett javítva a PsApiManagementOAuth2AuthrozationServer modell elírása PsApiManagementOAuth2AuthorizationServer értékre</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1635">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4ffb6-1636">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1636">Az.Batch</span></span>
* <span data-ttu-id="4ffb6-1637">Ki lett javítva a súgóüzenetben és a dokumentációban található elgépelés, nagy kezdőbetűs Windows értékre</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1637">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4ffb6-1638">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1638">Az.Cdn</span></span>
* <span data-ttu-id="4ffb6-1639">Ki lett javítva egy elgépelés CDN modulátalakító segédben</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1639">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4ffb6-1640">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1640">Az.Compute</span></span>
* <span data-ttu-id="4ffb6-1641">Új VmssId a New-AzVMConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1641">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="4ffb6-1642">Új TerminateScheduledEvents és a TerminateScheduledEventNotBeforeTimeoutInMinutes paraméterek a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1642">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="4ffb6-1643">Új HyperVGeneration tulajdonság a VM-rendszerképobjektumhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1643">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="4ffb6-1644">Új Host és HostGroup jellemzők</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1644">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="4ffb6-1645">Új parancsmagok:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1645">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="4ffb6-1646">Új HostId paraméter a New-AzVMConfig és a New-AzVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1646">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="4ffb6-1647">Az Invoke-AzVMRunCommand dokumentációjában található példa frissítve lett a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1647">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="4ffb6-1648">A -VolumeType leírása frissítve lett a set-AzVMDiskEncryptionExtension és a set-AzVmssDiskEncryptionExtension referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1648">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4ffb6-1649">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1649">Az.DataFactory</span></span>
* <span data-ttu-id="4ffb6-1650">A New-AzDataFactoryEncryptValue dokumentációjában a Windows szó nagy kezdőbetűsre lett javítva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1650">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="4ffb6-1651">Az ADF .Net SDK a 4.1.2-es verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1651">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="4ffb6-1652">Új DataProxyIntegrationRuntimeName, DataProxyIntegrationRuntimeName és DataProxyStagingPath paraméterek lettek hozzáadva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz, lehetővé téve a helyi integrációs modul SSIS integrációs modul proxyjaként való beállítását</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1652">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="4ffb6-1653">Frissítve lett a PSTriggerRun, hogy megjelenítse az aktivált folyamatokat, üzeneteket és tulajdonságokat, illetve a PSActivityRun, hogy megjelenítse a tevékenységtípust</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1653">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4ffb6-1654">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1654">Az.DataLakeStore</span></span>
* <span data-ttu-id="4ffb6-1655">Ki lett javítva a Get-DataLakeStoreDeletedItem lefagyása hibák vagy távoli kivételek esetén.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1655">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4ffb6-1656">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1656">Az.EventHub</span></span>
* <span data-ttu-id="4ffb6-1657">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNteworkRule paraméter a Set-AzEventHubNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1657">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="4ffb6-1658">Ki lett javítva a 9558-as számú hiba: Set-AzEventHubNamespace a PUT helyett a PATCH kérést használta</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1658">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="4ffb6-1659">új EnableKafka paraméter a Set-AzEventHubNamespace parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1659">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="4ffb6-1660">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1660">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="4ffb6-1661">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1661">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="4ffb6-1662">Ki lett javítva egy elgépelés a dokumentációban, ahol az Azure csupa kisbetűvel szerepelt</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1662">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4ffb6-1663">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1663">Az.Monitor</span></span>
* <span data-ttu-id="4ffb6-1664">Hibás paraméternév lett kijavítva a súgódokumentációban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1664">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4ffb6-1665">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1665">Az.Network</span></span>
* <span data-ttu-id="4ffb6-1666">Frissítve lett a New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1666">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="4ffb6-1667">A PublicIpAddress elavult, mert a kiszolgálóoldalon nem használatos.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1667">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="4ffb6-1668">Hozzá lett adva egy opcionális Primary paraméter, amely azt jelzi, hogy a jelenlegi IP-konfiguráció elsődleges-e.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1668">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="4ffb6-1669">Javítva lett az SDK kérelemhiba-kivételének kezelése – kijavítja azt a problémát, amely miatt az SDK-kivételek kezelése korábban nem volt megfelelő, és a fontos hibarészletek nem jelentek meg</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1669">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="4ffb6-1670">Be lett állítva, hogy az IPv6 IP-előtag ellenőrzési logikája ellenőrizze az IPv6-előtag hosszának megfelelőségét.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1670">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="4ffb6-1671">Frissült a Get-AzVirtualNetworkSubnetConfig: Új paraméterkészlet lett hozzáadva az alhálózat erőforrás-azonosítója szerinti lekéréshez.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1671">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="4ffb6-1672">Frissült az AzNetworkServiceTag Location paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1672">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4ffb6-1673">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1673">Az.OperationalInsights</span></span>
* <span data-ttu-id="4ffb6-1674">Frissült a New-AzOperationalInsightsLinuxSyslogDataSource dokumentációja</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1674">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="4ffb6-1675">Példa hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1675">Added example</span></span>
    - <span data-ttu-id="4ffb6-1676">A -Name paraméter leírása frissítve lett</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1676">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="4ffb6-1677">Új példa lett hozzáadva a New-AzOperationalInsightsWindowsEventDataSource parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1677">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="4ffb6-1678">Módosult a New-AzOperationalInsightsWindowsEventDataSource -Name paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1678">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4ffb6-1679">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1679">Az.RecoveryServices</span></span>
* <span data-ttu-id="4ffb6-1680">Frissült a Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1680">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="4ffb6-1681">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1681">Az.Resources</span></span>
* <span data-ttu-id="4ffb6-1682">A Microsoft.Resource mostantól támogatja a 2019-05-10-es új api-verziót</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1682">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="4ffb6-1683">Mostantól támogatott a copy.count = 0 a változók, erőforrások és tulajdonságok esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1683">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="4ffb6-1684">A condition = false vagy copy.count = 0 tulajdonságú erőforrások teljes módban törölve lesznek</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1684">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="4ffb6-1685">A súgódokumentációhoz hozzá lett adva egy példa a szabályzatok előfizetési szinten történő hozzárendeléséhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1685">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4ffb6-1686">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1686">Az.ServiceBus</span></span>
* <span data-ttu-id="4ffb6-1687">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNetworkRule paraméter a Set-AzServiceBusNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1687">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="4ffb6-1688">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1688">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="4ffb6-1689">Új Test-AzServiceBusNameAvailability parancs lett hozzáadva annak ellenőrzésére, hogy az üzenetsor és a témakör neve elérhető-e</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1689">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4ffb6-1690">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1690">Az.ServiceFabric</span></span>
* <span data-ttu-id="4ffb6-1691">Ki lettek javítva a csomóponttípus-hozzáadási parancsmag hibái:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1691">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="4ffb6-1692">NullReferenceException hiba történt, ha az erőforráscsoport más, a Service Fabric-fürthöz nem kapcsolódó VMSS-sel rendelkezett.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1692">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="4ffb6-1693">Kijavított hiba: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1693">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="4ffb6-1694">Ki lett javítva egy hiba, amely miatt a parancsmag futása meghiúsult, ha a virtualNetwork a fürttől eltérő erőforráscsoportban volt.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1694">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="4ffb6-1695">kijavított hiba: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1695">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="4ffb6-1696">Az Add-AzServiceFabricApplicationCertificate parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1696">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="4ffb6-1697">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1697">Az.Sql</span></span>
* <span data-ttu-id="4ffb6-1698">Frissült a régi naplózási parancsmagok dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1698">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4ffb6-1699">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1699">Az.Storage</span></span>
* <span data-ttu-id="4ffb6-1700">A Get/Close-AzStorageFileHandle súgója további parancsmagpélda-forgatókönyvek hozzáadásával és a paraméterek leírásának frissítésével változott</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1700">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="4ffb6-1701">A StandardBlobTier mostantól támogatott a blobfeltöltési és -másolási műveletekhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1701">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="4ffb6-1702">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1702">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="4ffb6-1703">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1703">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="4ffb6-1704">A rehidratálás prioritása mostantól támogatott a blobmásoláskor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1704">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="4ffb6-1705">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1705">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4ffb6-1706">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1706">Az.Websites</span></span>
* <span data-ttu-id="4ffb6-1707">Magyarázat hozzáadva a Set-AzWebApp és a Set-AzWebAppSlot parancsmagok -AppSettings paraméteréhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1707">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="4ffb6-1708">2.5.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1708">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4ffb6-1709">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1709">Az.Accounts</span></span>
* <span data-ttu-id="4ffb6-1710">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1710">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="4ffb6-1711">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1711">Az.ApplicationInsights</span></span>
* <span data-ttu-id="4ffb6-1712">A Remove-AzApplicationInsightsApiKey dokumentáció példájában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1712">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4ffb6-1713">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1713">Az.Automation</span></span>
* <span data-ttu-id="4ffb6-1714">Az erőforrássztringben található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1714">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4ffb6-1715">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1715">Az.CognitiveServices</span></span>
* <span data-ttu-id="4ffb6-1716">NetworkRuleSet támogatás hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1716">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4ffb6-1717">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1717">Az.Compute</span></span>
* <span data-ttu-id="4ffb6-1718">A virtuálisgép-példány nézetobjektumaiból hiányzó tulajdonságok (ComputerName, OsName, OsVersion és HyperVGeneration) hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1718">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="4ffb6-1719">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1719">Az.ContainerRegistry</span></span>
* <span data-ttu-id="4ffb6-1720">A Remove-AzContainerRegistryReplication Replikáció paraméterében lévő elírás javítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1720">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="4ffb6-1721">További információ: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1721">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4ffb6-1722">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1722">Az.DataFactory</span></span>
* <span data-ttu-id="4ffb6-1723">Az ADF .Net SDK a 4.1.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1723">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="4ffb6-1724">A Get-AzDataFactoryV2PipelineRun dokumentációjában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1724">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4ffb6-1725">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1725">Az.EventHub</span></span>
* <span data-ttu-id="4ffb6-1726">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1726">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="4ffb6-1727">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1727">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4ffb6-1728">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1728">Az.KeyVault</span></span>
* <span data-ttu-id="4ffb6-1729">A KeySize tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1729">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4ffb6-1730">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1730">Az.LogicApp</span></span>
* <span data-ttu-id="4ffb6-1731">A Get-AzIntegrationAccountMap javítása, hogy minden leképezéstípust listázzon</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1731">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="4ffb6-1732">Új MapType paraméter hozzáadva a szűréshez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1732">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="4ffb6-1733">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1733">Az.ManagedServices</span></span>
* <span data-ttu-id="4ffb6-1734">Az API 2019. 06. 01-én kiadott (GA) verziójának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1734">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4ffb6-1735">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1735">Az.Network</span></span>
* <span data-ttu-id="4ffb6-1736">A privát végpont és privát kapcsolatszolgáltatás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1736">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="4ffb6-1737">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1737">New cmdlets</span></span>
        - <span data-ttu-id="4ffb6-1738">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1738">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="4ffb6-1739">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1739">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="4ffb6-1740">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1740">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4ffb6-1741">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1741">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4ffb6-1742">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1742">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4ffb6-1743">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1743">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4ffb6-1744">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1744">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="4ffb6-1745">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1745">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="4ffb6-1746">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies jelző a VirtualNetwork alhálózatban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1746">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="4ffb6-1747">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig frissítve</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1747">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="4ffb6-1748">Hozzá lett adva a -PrivateEndpointNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát végpont esetében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1748">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="4ffb6-1749">Hozzá lett adva a -PrivateLinkServiceNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát kapcsolati szolgáltatás esetében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1749">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="4ffb6-1750">Az AzPrivateLinkService parancsmag ServiceName paramétere átnevezve a Name névre a ServiceName aliasszal a visszamenőleges kompatibilitás érdekében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1750">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="4ffb6-1751">ICMP-protokoll engedélyezése a hálózati biztonsági szabályzati konfigurációkhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1751">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="4ffb6-1752">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1752">Updated cmdlets</span></span>
        - <span data-ttu-id="4ffb6-1753">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1753">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="4ffb6-1754">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1754">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="4ffb6-1755">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1755">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="4ffb6-1756">A ConnectionProtocolType (Ikev1/Ikev2) hozzáadva a New-AzVirtualNetworkGatewayConnection konfigurálható paramétereként</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1756">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="4ffb6-1757">PrivateIpAddressVersion hozzáadva a LoadBalancerFrontendIpConfigurationhöz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1757">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="4ffb6-1758">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1758">Updated cmdlet:</span></span>
        - <span data-ttu-id="4ffb6-1759">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1759">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="4ffb6-1760">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1760">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="4ffb6-1761">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1761">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="4ffb6-1762">Application Gateway New-AzApplicationGatewayProbeConfig parancs frissítése a mintavétel egyéni portjának támogatásához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1762">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="4ffb6-1763">Frissített New-AzApplicationGatewayProbeConfig: A Port opcionális paraméter hozzáadva, amelyet a rendszer a háttérrendszer-kiszolgáló mintavételére használ.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1763">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="4ffb6-1764">Ez a paraméter a Standard_V2 és WAF_V2 termékváltozatokban használható.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1764">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4ffb6-1765">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1765">Az.OperationalInsights</span></span>
* <span data-ttu-id="4ffb6-1766">A mentett keresések alapértelmezett verziója 1 értékre frissítve.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1766">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="4ffb6-1767">Null reguláris kifejezések kezelése javítva az egyéni naplókban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1767">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4ffb6-1768">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1768">Az.RecoveryServices</span></span>
* <span data-ttu-id="4ffb6-1769">A Get-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1769">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="4ffb6-1770">A Get-AzRecoveryServicesBackupContainer.md frissítése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1770">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="4ffb6-1771">A Get-AzRecoveryServicesVault.md frissítése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1771">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="4ffb6-1772">A Wait-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1772">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="4ffb6-1773">A Set-AzRecoveryServicesVaultContext.md frissítése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1773">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="4ffb6-1774">A Get-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1774">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="4ffb6-1775">A Get-AzRecoveryServicesBackupRecoveryPoint.md frissítése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1775">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="4ffb6-1776">A Restore-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1776">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="4ffb6-1777">A tároló Azure-fájlmegosztásban való regisztrációjának törlésére szolgáló szolgáltatáshívás frissítése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1777">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="4ffb6-1778">A Set-AzRecoveryServicesAsrAlertSetting.md frissítése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1778">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="4ffb6-1779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1779">Az.Resources</span></span>
- <span data-ttu-id="4ffb6-1780">A New-AzResourceGroupDeployment dokumentációban hivatkozott hiányzó parancsmag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1780">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="4ffb6-1781">A szabályzat parancsmagjai frissítve a 2019. 01. 01. dátumú új API-verzió használatára</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1781">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4ffb6-1782">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1782">Az.ServiceBus</span></span>
* <span data-ttu-id="4ffb6-1783">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1783">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="4ffb6-1784">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1784">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="4ffb6-1785">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1785">Az.Sql</span></span>
* <span data-ttu-id="4ffb6-1786">A Set-AzSqlDatabaseSecondary parancsmag hiányzó példáinak javítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1786">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="4ffb6-1787">A biztonságirés-felmérés e-mail-cím megadása nélkül beállított ismétlődő vizsgálatának javítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1787">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="4ffb6-1788">Egy kis elírás javítása egy figyelmeztető üzenetben.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1788">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4ffb6-1789">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1789">Az.Storage</span></span>
* <span data-ttu-id="4ffb6-1790">A Get-AzStorageAccount hivatkozási dokumentációjában található példa frissítése a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1790">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="4ffb6-1791">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1791">Az.StorageSync</span></span>
* <span data-ttu-id="4ffb6-1792">Az Invoke-AzStorageSyncChangeDetection parancsmag hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1792">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="4ffb6-1793">A 9551-es hiba javítása a TierFilesOlderThanDays betartásához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1793">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4ffb6-1794">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1794">Az.Websites</span></span>
* <span data-ttu-id="4ffb6-1795">A hiba elhárítása, amely miatt a Get-AzWebApp és a Set-AzWebApp nem adott vissza egyes SiteConfig tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1795">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="4ffb6-1796">Egy új Location paraméter hozzáadása a Get-AzDeletedWebApp és a Restore-AzDeletedWebApp parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1796">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="4ffb6-1797">A webalkalmazás-tárhelyek New-AzWebApp -IncludeSourceWebAppSlots használatával történő klónozásakor jelentkező hiba javítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1797">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="4ffb6-1798">2.4.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1798">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4ffb6-1799">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1799">Az.Accounts</span></span>
* <span data-ttu-id="4ffb6-1800">Profilparancsmagok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1800">Add support for profile cmdlets</span></span>
* <span data-ttu-id="4ffb6-1801">A létrehozott parancsmagokban lévő környezetek és adatsíkok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1801">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="4ffb6-1802">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen végpontot használt az adatsík parancsmagjaihoz Windows PowerShellben</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1802">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="4ffb6-1803">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1803">Az.Advisor</span></span>
* <span data-ttu-id="4ffb6-1804">Az Az.Advisor GA-kiadása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1804">GA release of Az.Advisor</span></span>
* <span data-ttu-id="4ffb6-1805">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1805">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4ffb6-1806">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1806">Az.ApiManagement</span></span>
* <span data-ttu-id="4ffb6-1807">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1807">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="4ffb6-1808">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1808">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="4ffb6-1809">Előfizetések felhasználó és termék szerinti lekérdezésének támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1809">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="4ffb6-1810">„/”, „/apis”, „/apis/echo-api” hatókör használatával történő lekérdezés támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1810">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="4ffb6-1811">A következő hibák ki lettek javítva: https://github.com/Azure/azure-powershell/issues/9307 és https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1811">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="4ffb6-1812">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1812">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="4ffb6-1813">Az „ApiVersion” és az „ApiVersionSetId” megadhatóvá vált az API-k importálásakor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1813">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4ffb6-1814">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1814">Az.Automation</span></span>
* <span data-ttu-id="4ffb6-1815">A Set-AzAutomationConnectionFieldValue parancsmag sztringértékek kezelése esetén fellépő hibája javítva lett.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1815">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4ffb6-1816">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1816">Az.Compute</span></span>
* <span data-ttu-id="4ffb6-1817">A HyperVGeneration paraméter hozzáadása a New-AzImageConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1817">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4ffb6-1818">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1818">Az.DataFactory</span></span>
* <span data-ttu-id="4ffb6-1819">A tevékenység-, folyamat- és eseményindító-futtatási kimenetek lekérdezési ADF-parancsmagjainak frissítése a Select-Object folyamat támogatásához.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1819">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="4ffb6-1820">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1820">Az.EventGrid</span></span>
* <span data-ttu-id="4ffb6-1821">Az elgépelés ki lett javítva a New-AzEventGridSubscription dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1821">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4ffb6-1822">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1822">Az.IotHub</span></span>
* <span data-ttu-id="4ffb6-1823">Az engedélyezési szabályzati kulcsok újragenerálásának támogatása hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1823">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4ffb6-1824">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1824">Az.Network</span></span>
* <span data-ttu-id="4ffb6-1825">A „RoutingPreference” hozzáadva a nyilvános IP-címkékhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1825">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="4ffb6-1826">Javítottuk a példákat a „Get-AzNetworkServiceTag” referenciadokumentációban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1826">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4ffb6-1827">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1827">Az.PolicyInsights</span></span>
* <span data-ttu-id="4ffb6-1828">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyState parancsmagban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1828">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="4ffb6-1829">További információ: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1829">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4ffb6-1830">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1830">Az.OperationalInsights</span></span>
* <span data-ttu-id="4ffb6-1831">Javítottuk a Get-AzOperationalInsightsDataSource parancsmagban visszaadott CustomLog adatforrásmodellt</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1831">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4ffb6-1832">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1832">Az.RecoveryServices</span></span>
* <span data-ttu-id="4ffb6-1833">Az IaaSVMs get-policy parancsának javítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1833">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="4ffb6-1834">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1834">Az.Resources</span></span>
    - <span data-ttu-id="4ffb6-1835">A Get-AzPolicyState -Top paraméter súgószövegének javítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1835">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="4ffb6-1836">Ügyféloldali lapozás támogatásának hozzáadása a Get-AzPolicyAlias parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1836">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="4ffb6-1837">Új (-PolicyParameters és -PolicyParametersObject) paraméterek hozzáadása a Set-AzPolicyAssignment parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1837">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="4ffb6-1838">A Policy-parancsmagok néhány dokumentumának és példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1838">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4ffb6-1839">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1839">Az.ServiceBus</span></span>
* <span data-ttu-id="4ffb6-1840">A 4938-as hiba javítása – A New-AzureRmServiceBusQueue parancsmag BadRequest értéket ad vissza a MaxSizeInMegabytes megadásakor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1840">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="4ffb6-1841">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1841">Az.Sql</span></span>
* <span data-ttu-id="4ffb6-1842">A példány-feladatátvételi csoportok parancsmagjainak hozzáadása az előzetes kiadásból a nyilvános kiadáshoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1842">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="4ffb6-1843">Az Azure SQL Server\Database Auditing támogatása új parancsmagokkal.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1843">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="4ffb6-1844">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1844">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="4ffb6-1845">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1845">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="4ffb6-1846">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1846">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="4ffb6-1847">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1847">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="4ffb6-1848">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1848">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="4ffb6-1849">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1849">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="4ffb6-1850">E-mailes korlátozások eltávolítása a sebezhetőségi felmérés beállításaiból</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1850">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4ffb6-1851">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1851">Az.Storage</span></span>
* <span data-ttu-id="4ffb6-1852">Az „-IndexDocument” és „-ErrorDocument404Path” paraméter módosítása kötelezőről opcionálisra a következő parancsmagban:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1852">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="4ffb6-1853">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1853">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="4ffb6-1854">A Get-AzStorageBlobContent súgójának frissítése egy példa hozzáadásával</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1854">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="4ffb6-1855">További hibaadatok megjelenítése, ha a parancsmag futtatása StorageException miatt meghiúsul</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1855">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="4ffb6-1856">Storage-fiók létrehozásának és frissítésének támogatása Azure Files AAD DS-hitelesítéssel</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1856">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="4ffb6-1857">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1857">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="4ffb6-1858">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1858">Set-AzStorageAccount</span></span>
* <span data-ttu-id="4ffb6-1859">Támogatás a fájlmegosztások, fájlkönyvtárak vagy fájlok fájlleíróinak listázásához vagy bezárásához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1859">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="4ffb6-1860">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1860">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="4ffb6-1861">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1861">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="4ffb6-1862">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1862">Az.StorageSync</span></span>
* <span data-ttu-id="4ffb6-1863">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1863">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="4ffb6-1864">2.3.2 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1864">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4ffb6-1865">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1865">Az.Accounts</span></span>
* <span data-ttu-id="4ffb6-1866">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen URL-címeket használt a Functions-hívásokhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1866">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="4ffb6-1867">További információ: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1867">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="4ffb6-1868">Javítva lett az aliasok hibája az AzureRM–Az parancsmagok közötti átvitel esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1868">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="4ffb6-1869">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1869">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="4ffb6-1870">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1870">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4ffb6-1871">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1871">Az.Compute</span></span>
* <span data-ttu-id="4ffb6-1872">A „New-AzVm” és „New-AzVmss” egyszerű paraméterkészletek mostantól elfogadják a „ProximityPlacementGroup” paramétert.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1872">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="4ffb6-1873">Az elgépelés ki lett javítva a „New-AzVM” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1873">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="4ffb6-1874">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1874">Az.Dns</span></span>
* <span data-ttu-id="4ffb6-1875">Az elgépelés ki lett javítva a „Set-AzDnsZone” súgópéldáinál.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1875">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="4ffb6-1876">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1876">Az.EventGrid</span></span>
* <span data-ttu-id="4ffb6-1877">Frissítve a 2019-06-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1877">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="4ffb6-1878">Új parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1878">New cmdlets:</span></span>
    - <span data-ttu-id="4ffb6-1879">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1879">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="4ffb6-1880">Létrehoz egy új Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1880">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="4ffb6-1881">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1881">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="4ffb6-1882">Lekéri egy Event Grid-tartomány részleteit, vagy az aktuális Azure-előfizetéshez tartozó összes Event Grid-tartomány listáját.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1882">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="4ffb6-1883">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1883">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="4ffb6-1884">Eltávolít egy Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1884">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="4ffb6-1885">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1885">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="4ffb6-1886">Újra létrehozza a megosztott hozzáférési kulcsot az Azure Event Grid-tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1886">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="4ffb6-1887">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1887">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="4ffb6-1888">Lekéri az Event Grid-tartományban való esemény-közzétételhez használt megosztott hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1888">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="4ffb6-1889">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1889">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="4ffb6-1890">Új Azure Event Grid-tartományi témakört hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1890">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="4ffb6-1891">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1891">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="4ffb6-1892">Lekéri egy Event Grid-tartományi témakör részleteit, vagy az aktuális Azure-előfizetés adott Event Grid-tartományához tartozó Event Grid-tartományi témakörök listáját</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1892">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="4ffb6-1893">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1893">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="4ffb6-1894">Eltávolít egy meglévő Azure Event Grid-tartományi témakört.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1894">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="4ffb6-1895">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1895">Updated cmdlets:</span></span>
    - <span data-ttu-id="4ffb6-1896">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1896">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="4ffb6-1897">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1897">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="4ffb6-1898">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1898">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="4ffb6-1899">Új paraméterkészletek lettek hozzáadva tartományok és tartományi témakörök esetében, lehetővé téve a meglévő paraméterek (például EndPointType, SubjectBeginsWith stb.) újbóli felhasználását.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1899">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="4ffb6-1900">Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1900">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="4ffb6-1901">Esemény-előfizetés lejárati dátuma,</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1901">Event subscription expiration date,</span></span>
            - <span data-ttu-id="4ffb6-1902">Speciális szűrési paraméterek.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1902">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="4ffb6-1903">Új felsorolási érték lett hozzáadva a servicebusqueue elem célértékeként.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1903">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="4ffb6-1904">Nem engedélyezett az -IncludedEventType beállításnál az „All” érték használata és a következővel való helyettesítése:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1904">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="4ffb6-1905">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1905">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="4ffb6-1906">Új opcionális paraméterek (Top, ODataQuery és NextLink) az eredmények tördelésének és szűrésének támogatásához.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1906">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="4ffb6-1907">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1907">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="4ffb6-1908">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1908">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="4ffb6-1909">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1909">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4ffb6-1910">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1910">Az.FrontDoor</span></span>
* <span data-ttu-id="4ffb6-1911">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1911">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="4ffb6-1912">Hozzá lett adva az átalakítások támogatása és az új operátorértékek automatikus kitöltése (RegEx)</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1912">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="4ffb6-1913">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1913">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="4ffb6-1914">Hozzá lett adva az új értékek automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1914">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4ffb6-1915">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1915">Az.Network</span></span>
* <span data-ttu-id="4ffb6-1916">Virtuális hálózati átjárók erőforrás-támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1916">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="4ffb6-1917">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1917">New cmdlets</span></span>
        - <span data-ttu-id="4ffb6-1918">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1918">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="4ffb6-1919">AvailablePrivateEndpointType hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1919">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="4ffb6-1920">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1920">New cmdlets</span></span>
        - <span data-ttu-id="4ffb6-1921">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1921">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="4ffb6-1922">PrivatePrivateLinkService hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1922">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="4ffb6-1923">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1923">New cmdlets</span></span>
        - <span data-ttu-id="4ffb6-1924">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1924">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="4ffb6-1925">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1925">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="4ffb6-1926">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1926">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="4ffb6-1927">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1927">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="4ffb6-1928">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1928">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="4ffb6-1929">PrivateEndpoint hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1929">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="4ffb6-1930">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1930">New cmdlets</span></span>
        - <span data-ttu-id="4ffb6-1931">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1931">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="4ffb6-1932">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1932">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="4ffb6-1933">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1933">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="4ffb6-1934">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1934">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="4ffb6-1935">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: UseLocalAzureIpAddress jelző a VpnConnection elemen</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1935">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="4ffb6-1936">Frissítve lett a New-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1936">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="4ffb6-1937">Frissítve lett a Set-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1937">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="4ffb6-1938">Hozzá lett adva az írásvédett PeeredConnections mező az ExpressRoute-társhálózatlétesítések esetében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1938">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="4ffb6-1939">Hozzá lett adva az írásvédett GlobalReachEnabled mező az ExpressRoute esetében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1939">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="4ffb6-1940">Kompatibilitástörő változást okozó attribútum lett hozzáadva, amely jelzi az AllowGlobalReach mező elavulását az ExpressRouteCircuit-modellben</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1940">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="4ffb6-1941">Javítva lett a 8756-os hiba a TargetListenerID AzApplicationGatewayRedirectConfiguration-parancsmagokkal való használata során</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1941">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="4ffb6-1942">Javítva lett a hiba a New-AzApplicationGatewayPathRuleConfig parancsmagban, amely megakadályozta az átírási szabálykészlet beállítását.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1942">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="4ffb6-1943">Javítva lett a VirtualNetworkTaps megjelenítése a NetworkInterfaceIpConfiguration esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1943">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="4ffb6-1944">Javítva lettek a Cortex Get-parancsmagok az összes rész felsorolásához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1944">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="4ffb6-1945">Javítva lett a VirtualHub-hivatkozás létrehozása az ExpressRouteGateways, VpnGateway esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1945">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="4ffb6-1946">Hozzá lett adva a rendelkezésreállási zónák támogatása az AzureFirewall és a NatGateway esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1946">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="4ffb6-1947">Hozzá lett adva a Get-AzNetworkServiceTag parancsmag</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1947">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="4ffb6-1948">Hozzá lett adva a több nyilvános IP-cím támogatása az Azure Firewall esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1948">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="4ffb6-1949">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1949">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="4ffb6-1950">Hozzá lett adva a -PublicIpAddress paraméter, amely egy vagy több nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1950">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="4ffb6-1951">Hozzá lett adva a -VirtualNetwork paraméter, amely virtuális hálózati objektumokat fogad el</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1951">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="4ffb6-1952">Hozzá lett adva az AddPublicIpAddress és RemovePublicIpAddress metódus a tűzfalobjektumok esetében, és nyilvános IP-cím-objektumokat fogadnak el bemeneti adatként</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1952">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="4ffb6-1953">Elavult a -PublicIpName és a -VirtualNetworkName paraméter</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1953">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="4ffb6-1954">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: VpnClient AAD-alapú hitelesítési beállítások megadása a virtuális hálózati átjárók erőforrásaihoz.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1954">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="4ffb6-1955">Frissült a New-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1955">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="4ffb6-1956">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1956">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="4ffb6-1957">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva a RemoveAadAuthentication opcionális kapcsolóparaméter a VpnClient AAD-alapú hitelesítési beállítások eltávolításához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1957">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4ffb6-1958">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1958">Az.OperationalInsights</span></span>
* <span data-ttu-id="4ffb6-1959">Engedélyezve lett a **pergb2018** tarifacsomag a „New-AzureRmOperationalInsightsWorkspace” parancs esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1959">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="4ffb6-1960">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1960">Az.Resources</span></span>
* <span data-ttu-id="4ffb6-1961">További sablonexportálási beállítások támogatása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1961">Support for additional Template Export options</span></span>
    - <span data-ttu-id="4ffb6-1962">Hozzá lett adva a „-SkipResourceNameParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1962">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="4ffb6-1963">Hozzá lett adva a „-SkipAllParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1963">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="4ffb6-1964">Hozzá lett adva a „-Resource” paraméter az Export-AzResourceGroup esetében az exportált erőforrások szűréséhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1964">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4ffb6-1965">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1965">Az.ServiceFabric</span></span>
* <span data-ttu-id="4ffb6-1966">Ki lett javítva az a hiba, hogy a ByExistingKeyVault tanúsítvány hozzáadása bizonyos esetekben helytelen ujjlenyomatot kért le</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1966">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="4ffb6-1967">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1967">Az.Sql</span></span>
* <span data-ttu-id="4ffb6-1968">Javítva lett az Advanced Threat Protection Storage-végpontjának utótagja</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1968">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="4ffb6-1969">Javítva lett, hogy az Advanced Data Security engedélyezése felülbírálja az Advanced Threat Protection-szabályzatot</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1969">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="4ffb6-1970">Új parancsmagok lettek hozzáadva a Management.Sql esetében, amelyek lehetővé teszik az ügyfelek számára TDE-kulcsok hozzáadását és TDE-védő beállítását a felügyelt példányokhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1970">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="4ffb6-1971">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1971">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="4ffb6-1972">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1972">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="4ffb6-1973">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1973">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="4ffb6-1974">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1974">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="4ffb6-1975">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1975">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4ffb6-1976">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1976">Az.Storage</span></span>
* <span data-ttu-id="4ffb6-1977">A FileStorage és az SkuName Premium_ZRS altípus támogatása Storage-fiókok létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1977">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="4ffb6-1978">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1978">New-AzStorageAccount</span></span>
* <span data-ttu-id="4ffb6-1979">Egyértelműsítve lett a blobmódosíthatatlansági parancsmag leírása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1979">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="4ffb6-1980">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1980">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4ffb6-1981">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1981">Az.Websites</span></span>
* <span data-ttu-id="4ffb6-1982">Optimalizálva lett a Get-AzWebAppCertificate parancsmag, hogy erőforráscsoport szerint szűrjön a kiszolgálón, ne ügyfél szerint</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1982">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="4ffb6-1983">Hozzá lett adva a -UseDisasterRecovery kapcsolóparaméter a Get-AzWebAppSnapshot parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1983">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="4ffb6-1984">2.2.0 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1984">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="4ffb6-1985">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1985">Az.Cdn</span></span>
* <span data-ttu-id="4ffb6-1986">Frissített parancsmagok a rulesEngine szolgáltatás támogatásához a 2019. 04. 15. API-verzión</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1986">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4ffb6-1987">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1987">Az.Compute</span></span>
* <span data-ttu-id="4ffb6-1988">A `NoWait` paraméter hozzáadása, amely elindítja a műveletet, és azonnal visszatér, még a művelet befejezése előtt.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1988">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="4ffb6-1989">Frissített parancsmagok:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1989">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4ffb6-1990">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1990">Az.EventHub</span></span>
* <span data-ttu-id="4ffb6-1991">A 9231-es hiba javítása – a Get-AzEventHubNamespace nem ad vissza címkéket</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1991">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="4ffb6-1992">A 9230-as hiba javítása – a Get-AzEventHubNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1992">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4ffb6-1993">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1993">Az.Network</span></span>
* <span data-ttu-id="4ffb6-1994">ResourceID és InputObject frissítése a Nat-átjárón</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1994">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="4ffb6-1995">ResourceID és InputObject aliasának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1995">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4ffb6-1996">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1996">Az.PolicyInsights</span></span>
* <span data-ttu-id="4ffb6-1997">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyEvent parancsmagban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1997">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4ffb6-1998">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1998">Az.RecoveryServices</span></span>
* <span data-ttu-id="4ffb6-1999">Az IaaSVM szabályzat minimális megőrzési ideje 7 napról 1-re módosult</span><span class="sxs-lookup"><span data-stu-id="4ffb6-1999">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4ffb6-2000">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2000">Az.ServiceBus</span></span>
* <span data-ttu-id="4ffb6-2001">A 9182-es hiba javítása – a Get-AzServiceBusNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2001">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4ffb6-2002">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2002">Az.ServiceFabric</span></span>
* <span data-ttu-id="4ffb6-2003">Az Update-AzServiceFabricReliability hibaüzenetében lévő gépelési hiba kijavítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2003">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="4ffb6-2004">A Service Fabric parancssorok hiányzó karakterének pótlása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2004">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="4ffb6-2005">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2005">Az.Sql</span></span>
* <span data-ttu-id="4ffb6-2006">A DnsZonePartner paraméter hozzáadása a New-AzureSqlInstance parancsmaghoz az AutoDr képesség a felügyelt példányon való támogatásához.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2006">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="4ffb6-2007">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag kivezetése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2007">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="4ffb6-2008">Threat Detection parancsmagok átnevezése Advanced Threat Protection névre</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2008">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="4ffb6-2009">A New-AzSqlInstance, - StorageSizeInGB és - LicenseType paraméterek mostantól nem kötelezőek.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2009">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4ffb6-2010">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2010">Az.Websites</span></span>
* <span data-ttu-id="4ffb6-2011">javítja azt a hibát, amely miatt a Set-AzWebApp és a Set-AzWebAppSlot a -WebApp tulajdonsággal való használata eltávolította a címkéket</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2011">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="4ffb6-2012">2.1.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2012">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="4ffb6-2013">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2013">Az.ApiManagement</span></span>
* <span data-ttu-id="4ffb6-2014">Új parancsmagok a globális és API-szintű diagnosztika kezeléshez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2014">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="4ffb6-2015">**Get-AzApiManagementDiagnostic** – A globális vagy API hatókörre konfigurált diagnosztika beolvasása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2015">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="4ffb6-2016">**New-AzApiManagementDiagnostic** – Új diagnosztika létrehozása a globális vagy API szintű hatókörhöz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2016">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="4ffb6-2017">**New-AzApiManagementHttpMessageDiagnostic** – Diagnosztikai beállítás létrehozása arra vonatkozóan, hogy mely fejléceknél naplózzon a rendszer, és mekkora legyen a törzs mérete bájtban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2017">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="4ffb6-2018">**New-AzApiManagementPipelineDiagnosticSetting** – Diagnosztikai beállítások létrehozása az átjáróra érkező és onnan induló HTTP-üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2018">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="4ffb6-2019">**New-AzApiManagementSamplingSetting** – Mintavételezési beállítások létrehozása diagnosztikai kérésekhez/válaszokhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2019">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="4ffb6-2020">**Remove-AzApiManagementDiagnostic** – Diagnosztikai entitás eltávolítása globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2020">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="4ffb6-2021">**Set-AzApiManagementDiagnostic** – Diagnosztikai entitás frissítése globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2021">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="4ffb6-2022">Új parancsmagok az ApiManagement szolgáltatás gyorsítótárának kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2022">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="4ffb6-2023">**Get-AzApiManagementCache** – Az azonosító által megadott vagy az összes gyorsítótár részleteinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2023">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="4ffb6-2024">**New-AzApiManagementCache** – Új alapértelmezett gyorsítótár létrehozása vagy gyorsítótár létrehozása adott Azure-régióban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2024">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="4ffb6-2025">**Remove-AzApiManagementCache** – Gyorsítótár eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2025">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="4ffb6-2026">**Update-AzApiManagementCache** – Gyorsítótár frissítése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2026">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="4ffb6-2027">Új parancsmagok az API-séma kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2027">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="4ffb6-2028">**New-AzApiManagementSchema** – Új séma létrehozása egy API-hoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2028">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="4ffb6-2029">**Get-AzApiManagementSchema** – Az API-ban konfigurált sémák beolvasása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2029">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="4ffb6-2030">**Remove-AzApiManagementSchema** – Az API-ban konfigurált sémák eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2030">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="4ffb6-2031">**Set-AzApiManagementSchema** – Az API-ban konfigurált séma frissítése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2031">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="4ffb6-2032">Új parancsmag a felhasználói jogkivonat létrehozásához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2032">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="4ffb6-2033">**New-AzApiManagementUserToken** – Új, alapértelmezés szerint 8 órán át érvényes felhasználói jogkivonat létrehozása. Ezen parancsmag használatával lehet a „GIT” felhasználó számára jogkivonatot létrehozni.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2033">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="4ffb6-2034">Új parancsmag a hálózat állapotának lekérdezéséhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2034">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="4ffb6-2035">**Get-AzApiManagementNetworkStatus** – Azon erőforrások hálózati állapotának beolvasása, amelyektől az API Management szolgáltatás függ.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2035">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="4ffb6-2036">Ez hasznos lehet, ha az ApiManagement szolgáltatást virtuális hálózatra telepíti, és ellenőrizni kell, hogy rendben működnek-e a függőségek.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2036">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="4ffb6-2037">A **New-AzApiManagement** parancsmag frissítése az ApiManagement szolgáltatás kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2037">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="4ffb6-2038">Mostantól az új „Consumption” SKU is támogatott</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2038">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="4ffb6-2039">Mostantól az „EnableClientCertificate” jelző a „Consumption” SKU-hoz is bekapcsolható</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2039">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="4ffb6-2040">Az új **New-AzApiManagementSslSetting** parancsmag lehetővé teszi a „TLS/SSL” beállítás konfigurálását a „Háttér” és „Előtér” esetén is.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2040">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="4ffb6-2041">Ez egy ApiManagement szolgáltatás előterén a titkosítások, mint például a 3DES, valamint a szerverprotokollok, mint például a Http2 konfigurálására is alkalmas.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2041">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="4ffb6-2042">Mostantól támogatott a „DeveloperPortal” gazdanév ApiManagement szolgáltatáson történő konfigurálása.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2042">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="4ffb6-2043">A **Get-AzApiManagementSsoToken** parancsmagok frissítése a „PsApiManagement” objektum bemenetként való használatához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2043">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="4ffb6-2044">A parancsmag frissítése a hibaüzenetek beágyazott megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2044">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="4ffb6-2045">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hibakód: ValidationError Hibaüzenet: Egy vagy több mező hibás értéket tartalmaz: Hiba részletei:    [Kód=ValidationError, Üzenet=Hiba a log-to-eventhub elemben, 3. sor, 10. oszlop: A naplózó nem található, Cél=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2045">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="4ffb6-2046">Az **Export-AzApiManagementApi** parancsmag frissítse az API-k OpenApi 3.0 formátumban való exportálásához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2046">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="4ffb6-2047">Az **Import-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2047">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="4ffb6-2048">API importálása az OpenApi 3.0 dokumentumspecifikációból</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2048">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="4ffb6-2049">A bármely (Swagger, Wadl, Wsdl, OpenAPI) dokumentumban megadott PsApiManagementSchema tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2049">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="4ffb6-2050">A bármely dokumentumban megadott ServiceUrl tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2050">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="4ffb6-2051">A **Get-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) való visszaadásához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2051">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="4ffb6-2052">A **Set-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) és XML-nek megfelelő feloldójeles formátumban (xml használatával) való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2052">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="4ffb6-2053">A **New-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2053">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="4ffb6-2054">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2054">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="4ffb6-2055">API létrehozása ApiVersionSet tulajdonságban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2055">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="4ffb6-2056">API klónozása SourceApiId és SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2056">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="4ffb6-2057">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2057">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="4ffb6-2058">A **Set-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2058">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="4ffb6-2059">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2059">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="4ffb6-2060">API frissítése ApiVersionSet tulajdonságba</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2060">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="4ffb6-2061">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2061">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="4ffb6-2062">A **New-AzApiManagementRevision** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2062">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="4ffb6-2063">Létező változat klónozása (címkék, termékek, műveletek és szabályzatok másolása) a SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2063">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="4ffb6-2064">Az új változat a szülő ApiId értékét veszi át</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2064">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="4ffb6-2065">ApiRevisionDescription biztosítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2065">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="4ffb6-2066">A „ServiceUrl” felülírása API klónozáskor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2066">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="4ffb6-2067">A **New-AzApiManagementIdentityProvider** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2067">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="4ffb6-2068">AAD vagy AADB2C konfigurálása hitelesítésszolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2068">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="4ffb6-2069">SignupPolicy, SigninPolicy, ProfileEditingPolicy és PasswordResetPolicy beállítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2069">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="4ffb6-2070">A **New-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2070">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="4ffb6-2071">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2071">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="4ffb6-2072">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2072">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="4ffb6-2073">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2073">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="4ffb6-2074">A **Set-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2074">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="4ffb6-2075">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2075">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="4ffb6-2076">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2076">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="4ffb6-2077">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2077">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="4ffb6-2078">Az alábbi parancsmagok frissültek a ResourceID bemenetként való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2078">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="4ffb6-2079">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2079">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="4ffb6-2080">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2080">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="4ffb6-2081">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2081">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="4ffb6-2082">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2082">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="4ffb6-2083">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2083">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="4ffb6-2084">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2084">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="4ffb6-2085">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2085">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="4ffb6-2086">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2086">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="4ffb6-2087">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2087">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="4ffb6-2088">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2088">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="4ffb6-2089">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2089">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="4ffb6-2090">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2090">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4ffb6-2091">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2091">Az.Automation</span></span>
* <span data-ttu-id="4ffb6-2092">A Get-AzAutomationJobOutputRecord frissítése a JSON- és a szövegrekordértékek kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2092">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="4ffb6-2093">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2093">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="4ffb6-2094">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2094">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="4ffb6-2095">A Start-AzAutomationDscCompilationJob viselkedésének módosítása a munka elindítására a befejezésre való várakozás helyett</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2095">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="4ffb6-2096">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2096">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="4ffb6-2097">A Get-AzAutomationDscNode azon hibájának javítása, amely miatt a -Name használatakor az összes csomópontot visszaadta.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2097">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="4ffb6-2098">Most már csak az egyező csomópontot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2098">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4ffb6-2099">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2099">Az.Compute</span></span>
* <span data-ttu-id="4ffb6-2100">A ProtectFromScaleIn és a ProtectFromScaleSetAction paraméterek hozzáadása az Update-AzVmssVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2100">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="4ffb6-2101">A New-azvm fedőparaméter-készlet mostantól alapértelmezetten egy elérhető helyet használ, ha az USA keleti régiója nem támogatott</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2101">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4ffb6-2102">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2102">Az.DataLakeStore</span></span>
* <span data-ttu-id="4ffb6-2103">Az ADLS SDK frissítése a httpclient használatához, integrált adatsíkteszteléssel az Azure-keretrendszerben</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2103">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4ffb6-2104">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2104">Az.Monitor</span></span>
* <span data-ttu-id="4ffb6-2105">A hibás paraméternevek kijavítása a súgópéldákban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2105">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4ffb6-2106">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2106">Az.Network</span></span>
* <span data-ttu-id="4ffb6-2107">DisableBgpRoutePropagation jelölő hozzáadása az érvényes útválasztási táblázathoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2107">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="4ffb6-2108">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2108">Updated cmdlet:</span></span>
        - <span data-ttu-id="4ffb6-2109">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2109">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="4ffb6-2110">A dupla kötőjel kijavítása a New-AzApplicationGatewayTrustedRootCertificate dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2110">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="4ffb6-2111">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2111">Az.Resources</span></span>
* <span data-ttu-id="4ffb6-2112">Új Get-AzureRmDenyAssignment parancsmag hozzáadása a megtagadási hozzárendelések lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2112">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="4ffb6-2113">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2113">Az.Sql</span></span>
* <span data-ttu-id="4ffb6-2114">Advanced Threat Protection parancsmagok átnevezése Advanced Data Security névre és a sebezhetőségi felmérés alapértelmezett engedélyezése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2114">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="4ffb6-2115">2.0.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2115">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4ffb6-2116">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2116">Az.Accounts</span></span>
* <span data-ttu-id="4ffb6-2117">Az Authentication Library frissítése a felhasználóneves/jelszavas hitelesítéssel kapcsolatos ADFS-problémák kijavításához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2117">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4ffb6-2118">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2118">Az.CognitiveServices</span></span>
* <span data-ttu-id="4ffb6-2119">Csak a Bing jogi nyilatkozat jelenik meg a Bing Search-szolgáltatásoknál.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2119">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="4ffb6-2120">A sikertelen fióklétrehozás hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2120">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4ffb6-2121">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2121">Az.Compute</span></span>
* <span data-ttu-id="4ffb6-2122">Közelségi elhelyezési csoport szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2122">Proximity placement group feature.</span></span>
    - <span data-ttu-id="4ffb6-2123">A következő új parancsmagok lettek hozzáadva:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2123">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="4ffb6-2124">Az új ProximityPlacementGroupId paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2124">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="4ffb6-2125">A StorageAccountType paraméter hozzá lett adva a New-AzGalleryImageVersion parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2125">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="4ffb6-2126">A New-AzGalleryImageVersion TargetRegion paramétere tartalmazhatja a következőt: StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2126">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="4ffb6-2127">A SkipShutdown kapcsolóparaméter hozzá lett adva a Stop-AzVM és Stop-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2127">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="4ffb6-2128">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2128">Breaking changes</span></span>
    - <span data-ttu-id="4ffb6-2129">A Set-AzVMBootDiagnostics parancsmag új neve: Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2129">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="4ffb6-2130">Az Export-AzLogAnalyticThrottledRequests parancsmag új neve: Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2130">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="4ffb6-2131">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2131">Az.DeploymentManager</span></span>
* <span data-ttu-id="4ffb6-2132">Az Azure Deployment Manager-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2132">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="4ffb6-2133">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2133">Az.Dns</span></span>
* <span data-ttu-id="4ffb6-2134">Automatikus DNS NameServer-delegálás</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2134">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="4ffb6-2135">A DNS-zóna létrehozási parancsmag további opcionális paraméterként elfogadja a szülőzóna nevét.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2135">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="4ffb6-2136">Névkiszolgálói rekordokat ad hozzá a szülőzónában az újonnan létrehozott gyermekzóna számára.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2136">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4ffb6-2137">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2137">Az.FrontDoor</span></span>
* <span data-ttu-id="4ffb6-2138">Az Azure FrontDoor-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2138">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="4ffb6-2139">A WAF-parancsmagok új neve tartalmazza a „Waf” sztringet</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2139">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="4ffb6-2140">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2140">Az.HDInsight</span></span>
* <span data-ttu-id="4ffb6-2141">A következő két parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2141">Removed two cmdlets:</span></span>
    - <span data-ttu-id="4ffb6-2142">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2142">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="4ffb6-2143">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2143">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="4ffb6-2144">Egy új, Set-AzHDInsightGatewayCredential nevű parancsmag lett hozzáadva a Grant-AzHDInsightHttpServicesAccess helyett</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2144">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="4ffb6-2145">A Get-AzHDInsightJobOutput parancsmag frissítve lett, hogy különbséget tegyen az olvasói és a HDInsight-operátori szerepkör között:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2145">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="4ffb6-2146">Az olvasói szerepkörrel rendelkező felhasználóknak explicit módon meg kell adniuk a DefaultStorageAccountKey paramétert, ellenkező esetben hiba történik.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2146">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="4ffb6-2147">A HDInsight-operátori szerepkörrel rendelkező felhasználókat ez nem érinti.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2147">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4ffb6-2148">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2148">Az.Monitor</span></span>
* <span data-ttu-id="4ffb6-2149">Az SQR API (ütemezett lekérdezési szabály) új parancsmagjai</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2149">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="4ffb6-2150">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2150">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="4ffb6-2151">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2151">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="4ffb6-2152">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2152">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="4ffb6-2153">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2153">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="4ffb6-2154">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2154">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="4ffb6-2155">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2155">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="4ffb6-2156">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2156">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="4ffb6-2157">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2157">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="4ffb6-2158">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2158">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="4ffb6-2159">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2159">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="4ffb6-2160">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2160">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="4ffb6-2161">[További](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) információk az SQR API-ról</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2161">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="4ffb6-2162">A frissített Az.Monitor.md tartalmazza a GenV2 (nem klasszikus) metrikaalapú riasztási szabály parancsmagjait</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2162">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4ffb6-2163">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2163">Az.Network</span></span>
* <span data-ttu-id="4ffb6-2164">A NAT-átjáró erőforrás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2164">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="4ffb6-2165">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2165">New cmdlets</span></span>
        - <span data-ttu-id="4ffb6-2166">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2166">New-AzNatGateway</span></span>
        - <span data-ttu-id="4ffb6-2167">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2167">Get-AzNatGateway</span></span>
        - <span data-ttu-id="4ffb6-2168">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2168">Set-AzNatGateway</span></span>
        - <span data-ttu-id="4ffb6-2169">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2169">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="4ffb6-2170">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2170">Updated cmdlets</span></span>
        - <span data-ttu-id="4ffb6-2171">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2171">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="4ffb6-2172">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2172">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="4ffb6-2173">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: Egyéni útvonalak beállítása/eltávolítása a Brooklyn Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2173">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="4ffb6-2174">Frissült a New-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2174">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="4ffb6-2175">Frissült a Set-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2175">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4ffb6-2176">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2176">Az.PolicyInsights</span></span>
* <span data-ttu-id="4ffb6-2177">A szabályzat-kiértékelési adatok lekérdezésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2177">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="4ffb6-2178">Az -Expand paraméter hozzá lett adva a Get-AzPolicyState parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2178">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="4ffb6-2179">Az -Expand PolicyEvaluationDetails támogatása.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2179">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4ffb6-2180">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2180">Az.RecoveryServices</span></span>
* <span data-ttu-id="4ffb6-2181">Az előfizetések közötti Azure–Azure Site Recovery átvitel támogatása.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2181">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="4ffb6-2182">Az Azure Site Recovery jövőbeni kompatibilitástörő változásainak jelölése.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2182">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="4ffb6-2183">Ki lett javítva az Azure Site Recovery helyreállítási és műveletterve.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2183">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="4ffb6-2184">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure hálózatleképezés.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2184">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="4ffb6-2185">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure védelemirány felügyelt lemezek esetében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2185">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="4ffb6-2186">További kisebb javítások.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2186">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="4ffb6-2187">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2187">Az.Relay</span></span>
* <span data-ttu-id="4ffb6-2188">Az elgépelések ki lettek javítva az ügyféloldali üzenetekben</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2188">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4ffb6-2189">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2189">Az.ServiceBus</span></span>
* <span data-ttu-id="4ffb6-2190">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2190">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4ffb6-2191">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2191">Az.Storage</span></span>
* <span data-ttu-id="4ffb6-2192">A Storage ügyféloldali kódtárának frissítése a 10.0.1-es verziójára (az SDK összes objektuma esetében módosul a névtér a Microsoft.WindowsAzure.Storage. *névtérről a Microsoft.Azure.Storage.* névtérre)</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2192">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="4ffb6-2193">Frissítés a Microsoft.Azure.Management.Storage 11.0.0-s verziójára az új API-verzió (2019. 04. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2193">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="4ffb6-2194">A Tárfiók létrehozása parancs esetében az alapértelmezett Storage-fiókaltípus a Storage helyett mostantól a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2194">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="4ffb6-2195">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2195">New-AzStorageAccount</span></span>
* <span data-ttu-id="4ffb6-2196">A Storage-fiók Sku.Name parancsmagkimenete módosul, hogy igazodjon a bemeneti SkuName paraméterhez, egy aláhúzásjel („_”) hozzáadásával – például a StandardLRS a Standard_LRS névre módosul</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2196">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="4ffb6-2197">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2197">New-AzStorageAccount</span></span>
    - <span data-ttu-id="4ffb6-2198">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2198">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="4ffb6-2199">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2199">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4ffb6-2200">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2200">Az.Websites</span></span>
* <span data-ttu-id="4ffb6-2201">Az Altípus tulajdonság mostantól meg lesz adva a Get-AzWebApp által visszaadott PSSite objektumokhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2201">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="4ffb6-2202">A Get-AzWebApp\*Metrics és a Get-AzAppServicePlanMetrics megjelölve elavultként</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2202">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="4ffb6-2203">1.8.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2203">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4ffb6-2204">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2204">Highlights since the last major release</span></span>
* <span data-ttu-id="4ffb6-2205">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2205">General availability of `Az` module</span></span>
* <span data-ttu-id="4ffb6-2206">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2206">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="4ffb6-2207">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2207">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="4ffb6-2208">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2208">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="4ffb6-2209">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2209">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="4ffb6-2210">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2210">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="4ffb6-2211">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2211">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4ffb6-2212">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2212">Az.Accounts</span></span>
* <span data-ttu-id="4ffb6-2213">Eltávolítás-AzureRm megfelelően törölni a Mac modulok frissítése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2213">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4ffb6-2214">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2214">Az.Batch</span></span>
* <span data-ttu-id="4ffb6-2215">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2215">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4ffb6-2216">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2216">Az.Cdn</span></span>
* <span data-ttu-id="4ffb6-2217">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2217">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4ffb6-2218">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2218">Az.CognitiveServices</span></span>
* <span data-ttu-id="4ffb6-2219">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2219">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4ffb6-2220">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2220">Az.Compute</span></span>
* <span data-ttu-id="4ffb6-2221">Az AEM telepítési kapcsolatos problémák megoldásához, ha a lemezek erőforrás-azonosítók kisbetűs resourcegroups volt az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2221">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="4ffb6-2222">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2222">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4ffb6-2223">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2223">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4ffb6-2224">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2224">Az.DataFactory</span></span>
* <span data-ttu-id="4ffb6-2225">Adjon hozzá SsisProperties, ha a NodeCount felügyelt integrációs modul nem null értékű.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2225">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4ffb6-2226">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2226">Az.DataLakeStore</span></span>
* <span data-ttu-id="4ffb6-2227">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2227">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="4ffb6-2228">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2228">Az.EventGrid</span></span>
* <span data-ttu-id="4ffb6-2229">A Súgó szöveg jelzi, hogy erőforrásokat kell létrehozni a create/update eseményt előfizetés parancsmagok használata előtt végpont frissítése.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2229">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4ffb6-2230">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2230">Az.EventHub</span></span>
* <span data-ttu-id="4ffb6-2231">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2231">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4ffb6-2232">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2232">Az.HDInsight</span></span>
* <span data-ttu-id="4ffb6-2233">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2233">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4ffb6-2234">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2234">Az.IotHub</span></span>
* <span data-ttu-id="4ffb6-2235">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2235">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4ffb6-2236">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2236">Az.KeyVault</span></span>
* <span data-ttu-id="4ffb6-2237">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2237">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4ffb6-2238">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2238">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="4ffb6-2239">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2239">Az.MachineLearning</span></span>
* <span data-ttu-id="4ffb6-2240">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2240">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="4ffb6-2241">Az.Media</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2241">Az.Media</span></span>
* <span data-ttu-id="4ffb6-2242">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2242">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4ffb6-2243">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2243">Az.Monitor</span></span>
  * <span data-ttu-id="4ffb6-2244">Riasztási szabály (nem klasszikus) GenV2 mérőszám-alapú új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2244">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="4ffb6-2245">Új AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2245">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="4ffb6-2246">Új AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2246">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="4ffb6-2247">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2247">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="4ffb6-2248">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2248">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="4ffb6-2249">Adjon hozzá AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2249">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="4ffb6-2250">Frissített verzió 0.22.0-preview figyelő SDK</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2250">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4ffb6-2251">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2251">Az.Network</span></span>
* <span data-ttu-id="4ffb6-2252">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2252">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4ffb6-2253">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2253">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="4ffb6-2254">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2254">Az.NotificationHubs</span></span>
* <span data-ttu-id="4ffb6-2255">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2255">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4ffb6-2256">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2256">Az.OperationalInsights</span></span>
* <span data-ttu-id="4ffb6-2257">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2257">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="4ffb6-2258">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2258">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="4ffb6-2259">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2259">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4ffb6-2260">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2260">Az.RecoveryServices</span></span>
* <span data-ttu-id="4ffb6-2261">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2261">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4ffb6-2262">Frissített táblázatos formában az SQL azure-beli virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2262">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="4ffb6-2263">A hozzáadott alternatív módszert AzureFileShare hely beolvasása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2263">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="4ffb6-2264">Frissített ScheduleRunDays SchedulePolicy objektumban időzóna szerint</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2264">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="4ffb6-2265">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2265">Az.RedisCache</span></span>
* <span data-ttu-id="4ffb6-2266">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2266">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4ffb6-2267">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2267">Az.Resources</span></span>
* <span data-ttu-id="4ffb6-2268">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2268">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="4ffb6-2269">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2269">Az.Sql</span></span>
* <span data-ttu-id="4ffb6-2270">Cserélje le a függőségi figyelő SDK közös kód</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2270">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="4ffb6-2271">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2271">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4ffb6-2272">Továbbfejlesztett folyamat, amely több oszlop osztályozási.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2272">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="4ffb6-2273">Termékváltozat tulajdonságok (termékváltozat neve, családi, kapacitás) válasz a Get-AzSqlServerServiceObjective és formátum táblaként alapértelmezés szerint tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2273">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="4ffb6-2274">Lehetővé teszi a Get-AzSqlServerServiceObjective anélkül, hogy a régióban egy már létező kiszolgáló hely alapján.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2274">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="4ffb6-2275">Hozzon létre felügyelt példányt az időzóna-paraméter támogatása.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2275">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="4ffb6-2276">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2276">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4ffb6-2277">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2277">Az.Websites</span></span>
* <span data-ttu-id="4ffb6-2278">a Set-AzWebApp és a Set-AzWebAppSlot távolítja el a címkék a végrehajtási javítások</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2278">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="4ffb6-2279">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2279">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4ffb6-2280">A webhelyek SDK frissítése.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2280">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="4ffb6-2281">A AdminSiteName tulajdonság PSAppServicePlan eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2281">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="4ffb6-2282">1.7.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2282">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4ffb6-2283">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2283">Highlights since the last major release</span></span>
* <span data-ttu-id="4ffb6-2284">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2284">General availability of `Az` module</span></span>
* <span data-ttu-id="4ffb6-2285">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2285">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="4ffb6-2286">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2286">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="4ffb6-2287">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2287">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="4ffb6-2288">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2288">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="4ffb6-2289">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2289">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="4ffb6-2290">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2290">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4ffb6-2291">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2291">Az.Accounts</span></span>
* <span data-ttu-id="4ffb6-2292">Frissített Add-AzEnvironment és Set-AzEnvironment parancsmag az AzureAnalysisServicesEndpointResourceId paraméter elfogadásához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2292">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4ffb6-2293">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2293">Az.AnalysisServices</span></span>
* <span data-ttu-id="4ffb6-2294">ServiceClient használata DataPlane-parancsmagokban és az eredeti hitelesítési logika eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2294">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="4ffb6-2295">Az Add-AzureASAccount burkolóként való megadása a Connect-AzAccount számára a kompatibilitástörő változás elkerüléséhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2295">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4ffb6-2296">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2296">Az.Automation</span></span>
* <span data-ttu-id="4ffb6-2297">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag belefoglalásokat érintő hibája.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2297">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="4ffb6-2298">Az IncludedKbNumber és az IncludedPackageNameMask paraméter mostantól működőképes.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2298">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="4ffb6-2299">Hibajavítás az Azure Automation frissítéskezelési dinamikus csoportja esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2299">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4ffb6-2300">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2300">Az.Compute</span></span>
* <span data-ttu-id="4ffb6-2301">HyperVGeneration paraméter hozzáadása a New-AzDiskConfig és a New-AzSnapshotConfig parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2301">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="4ffb6-2302">Virtuális gépek más bérlők katalógus-rendszerképével való létrehozásának engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2302">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="4ffb6-2303">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2303">Az.ContainerInstance</span></span>
* <span data-ttu-id="4ffb6-2304">Ki lett javítva a New-AzContainerGroup üres záró argumentumot hozzáadó -Command paraméterével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2304">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4ffb6-2305">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2305">Az.DataFactory</span></span>
* <span data-ttu-id="4ffb6-2306">Az ADF .Net SDK verziója 3.0.2-re frissült.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2306">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="4ffb6-2307">A Set-AzDataFactoryV2 parancsmag a RepoConfiguration beállításaihoz tartozó kiegészítő paraméterekkel lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2307">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4ffb6-2308">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2308">Az.Resources</span></span>
* <span data-ttu-id="4ffb6-2309">Továbbfejlesztett szolgáltatókezelés a Get-AzResource esetében, -ResourceId vagy -ResourceGroupName, -Name és -ResourceType paraméterek megadásakor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2309">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="4ffb6-2310">Továbbfejlesztett hibakezelés a Test-AzDeployment és a Test-AzResourceGroupDeployment esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2310">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="4ffb6-2311">A hibákat nem a telepítés ellenőrzése során kezeli, hanem a parancs kimenetébe foglalja bele</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2311">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="4ffb6-2312">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2312">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="4ffb6-2313">-IgnoreDynamicParameters kapcsolóparaméter hozzáadása telepítési parancsmagokhoz a rendszer által feltett kérdések szkriptekben és feladatokban való mellőzéséhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2313">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="4ffb6-2314">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2314">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="4ffb6-2315">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2315">Az.Sql</span></span>
* <span data-ttu-id="4ffb6-2316">Adatbázisadat-besorolás támogatása.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2316">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4ffb6-2317">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2317">Az.Storage</span></span>
* <span data-ttu-id="4ffb6-2318">Részletes hibaüzenet megjelenítése Storage-környezet -UseConnectedAccount paraméterrel történő létrehozásakor az Azure-fiókba való bejelentkezés nélkül</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2318">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="4ffb6-2319">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2319">New-AzStorageContext</span></span>
* <span data-ttu-id="4ffb6-2320">Adott Storage-fiók Blob service-tulajdonságai kezelésének támogatása Management plane API-val</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2320">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="4ffb6-2321">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2321">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="4ffb6-2322">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2322">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="4ffb6-2323">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2323">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="4ffb6-2324">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2324">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="4ffb6-2325">Az -AsJob támogatása blobok és fájlok feltöltéséhez, valamint parancsmagok letöltéséhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2325">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="4ffb6-2326">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2326">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="4ffb6-2327">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2327">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="4ffb6-2328">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2328">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="4ffb6-2329">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2329">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="4ffb6-2330">1.6.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2330">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4ffb6-2331">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2331">Highlights since the last major release</span></span>
* <span data-ttu-id="4ffb6-2332">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2332">General availability of `Az` module</span></span>
* <span data-ttu-id="4ffb6-2333">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2333">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="4ffb6-2334">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2334">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="4ffb6-2335">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2335">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="4ffb6-2336">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2336">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="4ffb6-2337">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2337">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="4ffb6-2338">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2338">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4ffb6-2339">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2339">Az.Automation</span></span>
* <span data-ttu-id="4ffb6-2340">Az Azure Automation frissítéskezelése módosult, hogy támogassa az alábbi új funkciókat:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2340">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="4ffb6-2341">Dinamikus csoportosítás</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2341">Dynamic grouping</span></span>
    * <span data-ttu-id="4ffb6-2342">Előzetesen és utólagosan futtatandó szkriptek</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2342">Pre-Post script</span></span>
    * <span data-ttu-id="4ffb6-2343">Újraindítási beállítás</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2343">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4ffb6-2344">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2344">Az.Compute</span></span>
* <span data-ttu-id="4ffb6-2345">Ki lett javítva az elérési útvonal feloldásával kapcsolatos hiba a Get-AzVmBootDiagnosticsData esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2345">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="4ffb6-2346">A Compute ügyfélkódtár frissült a 25.0.0 verzióra</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2346">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4ffb6-2347">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2347">Az.KeyVault</span></span>
* <span data-ttu-id="4ffb6-2348">Helyettesítő karakterek támogatásának hozzáadása a KeyVault-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2348">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4ffb6-2349">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2349">Az.Network</span></span>
* <span data-ttu-id="4ffb6-2350">Az Intelligens veszélyforrás-felderítés támogatásának hozzáadása az Azure Firewallhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2350">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="4ffb6-2351">Az Application Gateway-tűzfalszabályzat legfelső szintű erőforrása és egyéni szabályok hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2351">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4ffb6-2352">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2352">Az.RecoveryServices</span></span>
* <span data-ttu-id="4ffb6-2353">A SnapshotRetentionInDays hozzáadása az Azure-beli virtuális gépek szabályzatához az azonnali RP támogatása érdekében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2353">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="4ffb6-2354">Folyamat támogatásának hozzáadása a regisztrációtörlési tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2354">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="4ffb6-2355">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2355">Az.Resources</span></span>
* <span data-ttu-id="4ffb6-2356">Helyettesítő karakterek támogatásának hozzáadása a Get-AzResource és Get-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2356">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="4ffb6-2357">Az ARM általános hívása esetén használt hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2357">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="4ffb6-2358">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2358">Az.Sql</span></span>
* <span data-ttu-id="4ffb6-2359">A Fenyegetésészlelés parancsmagjainak paramétere (ExcludeDetectionType) a DetectionType helyett string[] lett, hogy a jövőben is használható legyen az új DetectionType-ok hozzáadásakor, valamint az automatikus kitöltés támogatása érdekében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2359">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4ffb6-2360">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2360">Az.Storage</span></span>
* <span data-ttu-id="4ffb6-2361">Tárfiók felügyeleti szabályzata lekérésének/beállításának/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2361">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="4ffb6-2362">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2362">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="4ffb6-2363">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2363">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="4ffb6-2364">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2364">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="4ffb6-2365">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2365">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="4ffb6-2366">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2366">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="4ffb6-2367">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2367">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4ffb6-2368">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2368">Az.Websites</span></span>
* <span data-ttu-id="4ffb6-2369">Ki lett javítva az ARM-sablon azon hibája, amely miatt meghiúsul az összes tárolóhely a New-AzWebApp - IncludeSourceWebAppSlots használatával történő klónozása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2369">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="4ffb6-2370">1.5.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2370">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4ffb6-2371">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2371">Az.Accounts</span></span>
* <span data-ttu-id="4ffb6-2372">A Register-AzModule parancs hozzáadása az AutoRest által létrehozott parancsmagok támogatásához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2372">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="4ffb6-2373">A Connect-AzAccount példáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2373">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4ffb6-2374">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2374">Az.Automation</span></span>
* <span data-ttu-id="4ffb6-2375">A bizonyos havi ütemezések lekérésekor jelentkező hiba kijavítva számos Azure Automation-parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2375">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="4ffb6-2376">Ki lett javítva a hiba, amely miatt a Get-AzAutomationDscNode csak az első 20 csomópontot adta vissza.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2376">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="4ffb6-2377">Most már az összes csomópontot visszaadja</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2377">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4ffb6-2378">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2378">Az.Cdn</span></span>
* <span data-ttu-id="4ffb6-2379">Új Powershell-parancsmagok hozzáadva az Egyéni tartományi Https engedélyezése/letiltása szolgáltatáshoz, a régiek elavultak</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2379">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4ffb6-2380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2380">Az.Compute</span></span>
* <span data-ttu-id="4ffb6-2381">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2381">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4ffb6-2382">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2382">Az.DataFactory</span></span>
* <span data-ttu-id="4ffb6-2383">Az ADF .Net SDK verziója 3.0.1-re frissült</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2383">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4ffb6-2384">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2384">Az.LogicApp</span></span>
* <span data-ttu-id="4ffb6-2385">Ki lett javítva a hiba, amely miatt a ListWorkflows csak az eredmények első oldalát kérte le</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2385">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4ffb6-2386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2386">Az.Network</span></span>
* <span data-ttu-id="4ffb6-2387">Helyettesítő karakterek támogatásának hozzáadása a Network-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2387">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4ffb6-2388">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2388">Az.RecoveryServices</span></span>
* <span data-ttu-id="4ffb6-2389">Azure-beli virtuális gépen futtatott SQL Server támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2389">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="4ffb6-2390">SDK-frissítés</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2390">SDK Update</span></span>
* <span data-ttu-id="4ffb6-2391">VMappContainer ellenőrzés eltávolítva a Get-ProtectableItem parancsmagból</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2391">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="4ffb6-2392">Name és ServerName paraméterek hozzáadva a Get-ProtectableItem parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2392">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="4ffb6-2393">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2393">Az.Resources</span></span>
* <span data-ttu-id="4ffb6-2394">`-TemplateObject` paraméter hozzáadva az üzembe helyező parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2394">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="4ffb6-2395">További információ: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2395">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="4ffb6-2396">Ki lett javítva a hiba, amely akkor jelentkezett, amikor a(z) `Get-AzResource` eredménye át lett irányítva a következőbe: `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2396">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="4ffb6-2397">További információ: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2397">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="4ffb6-2398">Ki lett javítva a JSON-adattípus módosításával kapcsolatos probléma, amely a(z) `Set-AzResource` futtatásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2398">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="4ffb6-2399">További információ: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2399">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="4ffb6-2400">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2400">Az.Sql</span></span>
* <span data-ttu-id="4ffb6-2401">Az AuditingEndpointsCommunicator frissítése.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2401">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="4ffb6-2402">Ki lett javítva az új diagnosztikai beállítások létrehozásakor jelentkező ritka eset viselkedése.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2402">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4ffb6-2403">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2403">Az.Storage</span></span>
* <span data-ttu-id="4ffb6-2404">A BlockBlobStorage altípus támogatása a Storage-fiók létrehozásakor      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2404">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="4ffb6-2405">1.4.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2405">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="4ffb6-2406">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2406">Az.AnalysisServices</span></span>
* <span data-ttu-id="4ffb6-2407">Az AddAzureASAccount parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2407">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4ffb6-2408">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2408">Az.Automation</span></span>
* <span data-ttu-id="4ffb6-2409">Az Import-AzAutomationDscNodeConfiguration súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2409">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="4ffb6-2410">A konfigurációnév-ellenőrzés hozzáadva az Import-AzAutomationDscConfiguration parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2410">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="4ffb6-2411">Továbbfejlesztett hibakezelés az Import-AzAutomationDscConfiguration parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2411">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4ffb6-2412">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2412">Az.CognitiveServices</span></span>
* <span data-ttu-id="4ffb6-2413">A CustomSubdomainName új választható paraméterként hozzáadva a New-AzCognitiveServicesAccount parancsmaghoz, amellyel altartomány adható meg az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2413">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4ffb6-2414">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2414">Az.Compute</span></span>
* <span data-ttu-id="4ffb6-2415">Kijavítva az azonosító paraméterkészleteivel kapcsolatos probléma</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2415">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="4ffb6-2416">Frissült a Get-AzVMExtension parancsmag, hogy az összes telepített bővítményt listázza, ha a Name paraméter nincs megadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2416">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="4ffb6-2417">A Tag és a ResourceId paraméterek hozzáadva az Update-AzImage parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2417">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="4ffb6-2418">A Get-AzVmssVM példányazonosító nélkül, az InstanceView használatával példánynézetben listázni tudja a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2418">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4ffb6-2419">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2419">Az.DataLakeStore</span></span>
* <span data-ttu-id="4ffb6-2420">Parancsmagok hozzáadása a törölt ADL-elemek enumerálásához és visszaállításához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2420">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4ffb6-2421">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2421">Az.EventHub</span></span>
* <span data-ttu-id="4ffb6-2422">Új SkipEmptyArchives logikai tulajdonság hozzáadva az üres archívumok kihagyásához az Eventhub CaptureDescription osztályában</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2422">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4ffb6-2423">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2423">Az.KeyVault</span></span>
* <span data-ttu-id="4ffb6-2424">A Set-AzKeyVaultSecret címkézésének kijavítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2424">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4ffb6-2425">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2425">Az.LogicApp</span></span>
* <span data-ttu-id="4ffb6-2426">Hozzáadva az integrációs fiókok alapszintű termékváltozatában</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2426">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="4ffb6-2427">Hozzáadva az XSLT 2.0-ban, az XSLT 3.0-ban és a Liquid leképezéstípusok esetén</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2427">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="4ffb6-2428">Új parancsmagok az integrációs fiók szerelvényeihez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2428">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="4ffb6-2429">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2429">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="4ffb6-2430">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2430">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="4ffb6-2431">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2431">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="4ffb6-2432">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2432">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="4ffb6-2433">Új parancsmagok az integrációs fiók kötegkonfigurációjához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2433">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="4ffb6-2434">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2434">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="4ffb6-2435">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2435">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="4ffb6-2436">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2436">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="4ffb6-2437">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2437">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="4ffb6-2438">A Logic Apps SDK frissítése a 4.1.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2438">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4ffb6-2439">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2439">Az.Monitor</span></span>
* <span data-ttu-id="4ffb6-2440">A Get-AzMetric súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2440">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4ffb6-2441">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2441">Az.Network</span></span>
* <span data-ttu-id="4ffb6-2442">Az Add-AzApplicationGatewayCustomError súgójában lévő példa frissítése</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2442">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4ffb6-2443">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2443">Az.OperationalInsights</span></span>
* <span data-ttu-id="4ffb6-2444">Kibővített támogatás a New és a Get ApplicationInsights adatforráshoz.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2444">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="4ffb6-2445">Új „ApplicationInsights” altípus hozzáadva az adott munkaterület Get specific és Get all Application Insights-adatforrásainak támogatásához.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2445">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="4ffb6-2446">A New-AzOperationalInsightsApplicationInsightsDataSource parancsmag hozzáadva adatforrás létrehozásához a következő Application Insights-erőforrásparaméterekkel: subscriptionId, resourceGroupName és name.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2446">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4ffb6-2447">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2447">Az.Resources</span></span>
* <span data-ttu-id="4ffb6-2448">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2448">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="4ffb6-2449">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2449">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="4ffb6-2450">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2450">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="4ffb6-2451">Ki lett javítva a KeyCredentials ismételt létrehozását megakadályozó hiba</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2451">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="4ffb6-2452">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2452">Az.Sql</span></span>
* <span data-ttu-id="4ffb6-2453">Rugalmas SQL DB-skálázási szint támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2453">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="4ffb6-2454">Ki lett javítva az a hiba, hogy a visszaállítási kérésben szereplő szükségtelen tulajdonságok megadása miatt a visszaállítás esetenként meghiúsult</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2454">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4ffb6-2455">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2455">Az.Websites</span></span>
* <span data-ttu-id="4ffb6-2456">A Get-AzWebAppSlotMetrics példájának javítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2456">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="4ffb6-2457">1.3.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2457">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4ffb6-2458">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2458">Az.Accounts</span></span>
* <span data-ttu-id="4ffb6-2459">Frissítés a ClientRuntime legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2459">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4ffb6-2460">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2460">Az.AnalysisServices</span></span>
<span data-ttu-id="4ffb6-2461">Az Az.AnalysisServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2461">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4ffb6-2462">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2462">Az.Compute</span></span>
* <span data-ttu-id="4ffb6-2463">AEM-bővítmény: Mostantól az UltraSSD, valamint a P60, P70 és P80 lemezek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2463">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="4ffb6-2464">A Set-AzVMBootDiagnostics súgóleírása frissült.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2464">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="4ffb6-2465">Az Update-AzImage súgóleírása és példája frissült.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2465">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4ffb6-2466">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2466">Az.RecoveryServices</span></span>
<span data-ttu-id="4ffb6-2467">Az Az.RecoveryServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2467">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4ffb6-2468">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2468">Az.Resources</span></span>
* <span data-ttu-id="4ffb6-2469">Az erőforráscsoportok címkézése ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2469">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="4ffb6-2470">További információ: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2470">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="4ffb6-2471">Ki lett javítva az a hiba, amikor a `Get-AzureRmRoleAssignment` nem vette figyelembe az -ErrorAction paramétert.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2471">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="4ffb6-2472">További információ: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2472">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="4ffb6-2473">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2473">Az.Sql</span></span>
* <span data-ttu-id="4ffb6-2474">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2474">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="4ffb6-2475">Ki lett javítva az a hiba, amikor az Azure-fiókba való bejelentkezés hiánya nullref kivételt eredményezett az SQL-parancsmagok végrehajtásakor.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2475">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="4ffb6-2476">A nullref kivétel ki lett javítva a Get-AzSqlCapabilityben.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2476">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="4ffb6-2477">1.2.1 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2477">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4ffb6-2478">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2478">Az.Accounts</span></span>
* <span data-ttu-id="4ffb6-2479">A hitelesítés megfelelő verziójával rendelkező kiadás</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2479">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4ffb6-2480">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2480">Az.AnalysisServices</span></span>
* <span data-ttu-id="4ffb6-2481">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2481">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4ffb6-2482">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2482">Az.RecoveryServices</span></span>
* <span data-ttu-id="4ffb6-2483">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2483">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="4ffb6-2484">1.2.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2484">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4ffb6-2485">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2485">Az.Accounts</span></span>
* <span data-ttu-id="4ffb6-2486">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2486">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="4ffb6-2487">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2487">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4ffb6-2488">Az Uninstall-AzureRm figyelmeztető üzenete hozzáadva a PS Core-ban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2488">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="4ffb6-2489">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2489">Az.Aks</span></span>
* <span data-ttu-id="4ffb6-2490">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2490">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4ffb6-2491">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2491">Az.Automation</span></span>
* <span data-ttu-id="4ffb6-2492">Mostantól támogatottak a Python 2-runbookok.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2492">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="4ffb6-2493">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2493">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4ffb6-2494">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2494">Az.Cdn</span></span>
* <span data-ttu-id="4ffb6-2495">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2495">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4ffb6-2496">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2496">Az.Compute</span></span>
* <span data-ttu-id="4ffb6-2497">Az Invoke-AzVMReimage parancsmag hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2497">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="4ffb6-2498">A TempDisk paraméter hozzá lett adva a Set-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2498">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="4ffb6-2499">A New-AzVM figyelmeztető üzenete ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2499">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="4ffb6-2500">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2500">Az.ContainerRegistry</span></span>
* <span data-ttu-id="4ffb6-2501">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2501">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4ffb6-2502">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2502">Az.DataFactory</span></span>
* <span data-ttu-id="4ffb6-2503">Az ADF .Net SDK verziója 3.0.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2503">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4ffb6-2504">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2504">Az.DataLakeStore</span></span>
* <span data-ttu-id="4ffb6-2505">Ki lett javítva az ADLS-végponttal kapcsolatos probléma az MSI használatakor.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2505">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="4ffb6-2506">További információ: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2506">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="4ffb6-2507">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2507">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4ffb6-2508">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2508">Az.IotHub</span></span>
* <span data-ttu-id="4ffb6-2509">Az Encoding formátum hozzá lett adva az Add-IotHubRoutingEndpoint parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2509">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4ffb6-2510">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2510">Az.KeyVault</span></span>
* <span data-ttu-id="4ffb6-2511">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2511">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4ffb6-2512">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2512">Az.Network</span></span>
* <span data-ttu-id="4ffb6-2513">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2513">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="4ffb6-2514">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2514">Az.Resources</span></span>
* <span data-ttu-id="4ffb6-2515">A helytelen példák ki lettek javítva a New-AzADAppCredential és a New-AzADSpCredential referenciadokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2515">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="4ffb6-2516">Ki lett javítva az a hiba, amikor a -TemplateFile paraméter nem lett feloldva az erőforráscsoportokat üzembe helyező parancsmagok végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2516">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="4ffb6-2517">Az.Resources: A New-AzureRmPolicyDefinition -Mode alapértelmezett értékének dokumentációja ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2517">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="4ffb6-2518">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2518">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="4ffb6-2519">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2519">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="4ffb6-2520">Ki lett javítva a „PSResourceGroupDeployment” objektum formázásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2520">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="4ffb6-2521">További információ: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2521">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4ffb6-2522">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2522">Az.ServiceFabric</span></span>
* <span data-ttu-id="4ffb6-2523">Visszaállítás a VMSS-modell tanúsítványának hozzáadásakor bekövetkező kivétel-visszaadás esetén; javított hiba: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2523">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="4ffb6-2524">Bizonyos hibaüzenetek ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2524">Fix some error messages.</span></span>
* <span data-ttu-id="4ffb6-2525">Ki lett javítva az alapértelmezett ARM-sablonnal való fürtlétrehozás a New-AzServiceFabriCluster esetében, amely nem működött az Az-ba történő migrálással.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2525">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="4ffb6-2526">Ki lett javítva a fürt-/alkalmazástanúsítvány létrehozása, így mostantól csak a fürtnek megfelelő virtuálisgép-méretezési csoportokhoz (Virtual Machine Scale Sets) lesznek hozzáadva, a fürtazonosító bővítményben való ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2526">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="4ffb6-2527">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2527">Az.SignalR</span></span>
* <span data-ttu-id="4ffb6-2528">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2528">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="4ffb6-2529">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2529">Az.Sql</span></span>
* <span data-ttu-id="4ffb6-2530">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2530">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4ffb6-2531">A LicenseType paraméter paraméterleírása frissítve lett a lehetséges értékekkel.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2531">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="4ffb6-2532">Ki lett javítva az a hiba, amikor egy felügyelt példány identitásának frissítése nem működött, ha az volt az egyetlen frissített tulajdonság.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2532">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="4ffb6-2533">Egyéni rendezések támogatása a felügyelt példányokon</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2533">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4ffb6-2534">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2534">Az.Storage</span></span>
* <span data-ttu-id="4ffb6-2535">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2535">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4ffb6-2536">Részletes hibaüzenet megjelenítése klasszikus naplózás/metrika get/set műveletei esetében a prémium szintű Storage-fiókon, mivel a prémium szintű Storage-fiók nem támogatja a klasszikus naplózást/metrikát.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2536">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="4ffb6-2537">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2537">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="4ffb6-2538">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2538">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="4ffb6-2539">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2539">Az.TrafficManager</span></span>
* <span data-ttu-id="4ffb6-2540">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2540">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4ffb6-2541">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2541">Az.Websites</span></span>
* <span data-ttu-id="4ffb6-2542">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2542">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4ffb6-2543">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól a megfelelő erőforráscsoportba és helyre tölti fel a tanúsítványt, ha az alkalmazás ASE-n üzemel.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2543">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="4ffb6-2544">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól nem írja felül a címkéket SSL-tanúsítvány alkalmazáshoz való kötésekor.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2544">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="4ffb6-2545">1.1.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2545">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4ffb6-2546">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2546">Az.Accounts</span></span>
* <span data-ttu-id="4ffb6-2547">A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2547">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4ffb6-2548">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2548">Az.Compute</span></span>
* <span data-ttu-id="4ffb6-2549">A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2549">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="4ffb6-2550">Frissült az azonosító leírása a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2550">Updated the description of ID in help files</span></span>
* <span data-ttu-id="4ffb6-2551">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2551">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4ffb6-2552">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2552">Az.DataLakeStore</span></span>
* <span data-ttu-id="4ffb6-2553">A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2553">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="4ffb6-2554">A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2554">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="4ffb6-2555">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2555">Az.EventGrid</span></span>
* <span data-ttu-id="4ffb6-2556">Frissítve a 2019-01-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2556">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="4ffb6-2557">A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2557">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="4ffb6-2558">New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2558">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="4ffb6-2559">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2559">Event Time-To-Live,</span></span>
        - <span data-ttu-id="4ffb6-2560">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2560">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="4ffb6-2561">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2561">Dead letter endpoint.</span></span>
    - <span data-ttu-id="4ffb6-2562">Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2562">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="4ffb6-2563">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2563">Event Time-To-Live,</span></span>
        - <span data-ttu-id="4ffb6-2564">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2564">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="4ffb6-2565">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2565">Dead letter endpoint.</span></span>
* <span data-ttu-id="4ffb6-2566">Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2566">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="4ffb6-2567">Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2567">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4ffb6-2568">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2568">Az.IotHub</span></span>
* <span data-ttu-id="4ffb6-2569">Frissítve az IoT Hub SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2569">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4ffb6-2570">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2570">Az.LogicApp</span></span>
* <span data-ttu-id="4ffb6-2571">A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2571">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="4ffb6-2572">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2572">Az.Resources</span></span>
* <span data-ttu-id="4ffb6-2573">Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2573">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="4ffb6-2574">További információ: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2574">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="4ffb6-2575">Ki lett javítva a -Custom paraméter kezelése a New/Set-AzPolicyDefinition parancsban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2575">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="4ffb6-2576">Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2576">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="4ffb6-2577">A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2577">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="4ffb6-2578">További információ: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2578">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="4ffb6-2579">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2579">Az.SignalR</span></span>
* <span data-ttu-id="4ffb6-2580">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2580">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="4ffb6-2581">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2581">Az.Sql</span></span>
* <span data-ttu-id="4ffb6-2582">A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2582">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4ffb6-2583">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2583">Az.Storage</span></span>
* <span data-ttu-id="4ffb6-2584">A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2584">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="4ffb6-2585">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2585">New-AzStorageContext</span></span>
* <span data-ttu-id="4ffb6-2586">A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2586">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="4ffb6-2587">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2587">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4ffb6-2588">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2588">Az.Websites</span></span>
* <span data-ttu-id="4ffb6-2589">Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2589">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="4ffb6-2590">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2590">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="4ffb6-2591">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2591">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="4ffb6-2592">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2592">General</span></span>

- <span data-ttu-id="4ffb6-2593">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2593">General Availability of Az Module</span></span>
- <span data-ttu-id="4ffb6-2594">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2594">Online help for each module</span></span>
- <span data-ttu-id="4ffb6-2595">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2595">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="4ffb6-2596">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2596">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="4ffb6-2597">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2597">Az.Accounts</span></span>
- <span data-ttu-id="4ffb6-2598">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2598">Changed from Az.Profile</span></span>
- <span data-ttu-id="4ffb6-2599">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2599">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="4ffb6-2600">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2600">Az.ApiManagement</span></span>
- <span data-ttu-id="4ffb6-2601">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2601">Fixes for #7002</span></span>
- <span data-ttu-id="4ffb6-2602">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2602">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="4ffb6-2603">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2603">Az.Batch</span></span>
- <span data-ttu-id="4ffb6-2604">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2604">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="4ffb6-2605">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2605">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="4ffb6-2606">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2606">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="4ffb6-2607">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2607">Az.Billing</span></span>
- <span data-ttu-id="4ffb6-2608">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2608">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="4ffb6-2609">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2609">Az.CognitivServices</span></span>
- <span data-ttu-id="4ffb6-2610">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2610">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="4ffb6-2611">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2611">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="4ffb6-2612">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2612">Az.ContainerInstance</span></span>
- <span data-ttu-id="4ffb6-2613">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2613">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="4ffb6-2614">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2614">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="4ffb6-2615">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2615">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="4ffb6-2616">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2616">Az.DataLakeStore</span></span>
- <span data-ttu-id="4ffb6-2617">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2617">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="4ffb6-2618">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2618">Az.Monitor</span></span>
- <span data-ttu-id="4ffb6-2619">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2619">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="4ffb6-2620">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2620">Az.KeyVault</span></span>
- <span data-ttu-id="4ffb6-2621">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2621">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="4ffb6-2622">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2622">Az.MachineLearning</span></span>
- <span data-ttu-id="4ffb6-2623">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2623">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="4ffb6-2624">Az.Media</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2624">Az.Media</span></span>
- <span data-ttu-id="4ffb6-2625">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2625">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="4ffb6-2626">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2626">Az.Network</span></span>
<span data-ttu-id="4ffb6-2627">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2627">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="4ffb6-2628">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2628">New cmdlets added:</span></span>
        - <span data-ttu-id="4ffb6-2629">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2629">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4ffb6-2630">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2630">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4ffb6-2631">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2631">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4ffb6-2632">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2632">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4ffb6-2633">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2633">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4ffb6-2634">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2634">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="4ffb6-2635">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2635">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="4ffb6-2636">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2636">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="4ffb6-2637">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2637">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="4ffb6-2638">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2638">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="4ffb6-2639">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2639">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="4ffb6-2640">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2640">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="4ffb6-2641">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2641">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="4ffb6-2642">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2642">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="4ffb6-2643">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2643">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="4ffb6-2644">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2644">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="4ffb6-2645">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2645">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="4ffb6-2646">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2646">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="4ffb6-2647">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2647">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="4ffb6-2648">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2648">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="4ffb6-2649">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2649">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="4ffb6-2650">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2650">Az.OperationalInsights</span></span>
- <span data-ttu-id="4ffb6-2651">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2651">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="4ffb6-2652">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2652">Az.Profile</span></span>
- <span data-ttu-id="4ffb6-2653">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2653">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="4ffb6-2654">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2654">Az.RecoveryServices</span></span>
- <span data-ttu-id="4ffb6-2655">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2655">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="4ffb6-2656">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2656">Az.Resources</span></span>
- <span data-ttu-id="4ffb6-2657">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2657">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="4ffb6-2658">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2658">Az.ServiceFabric</span></span>
- <span data-ttu-id="4ffb6-2659">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2659">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="4ffb6-2660">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2660">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="4ffb6-2661">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2661">Az.SIgnalR</span></span>
- <span data-ttu-id="4ffb6-2662">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2662">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="4ffb6-2663">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2663">Az.Sql</span></span>
- <span data-ttu-id="4ffb6-2664">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2664">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="4ffb6-2665">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2665">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="4ffb6-2666">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2666">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="4ffb6-2667">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2667">Az.Storage</span></span>
- <span data-ttu-id="4ffb6-2668">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2668">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="4ffb6-2669">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2669">Az.Websites</span></span>
- <span data-ttu-id="4ffb6-2670">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2670">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="4ffb6-2671">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2671">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="4ffb6-2672">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2672">General</span></span>

* <span data-ttu-id="4ffb6-2673">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2673">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="4ffb6-2674">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2674">Az.Compute</span></span>

* <span data-ttu-id="4ffb6-2675">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2675">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="4ffb6-2676">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2676">Az.DataLakeStore</span></span>

* <span data-ttu-id="4ffb6-2677">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2677">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="4ffb6-2678">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2678">Az.FrontDoor</span></span>

* <span data-ttu-id="4ffb6-2679">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2679">Fixed some broken links</span></span>
    - <span data-ttu-id="4ffb6-2680">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2680">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="4ffb6-2681">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2681">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="4ffb6-2682">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2682">Az.RecoveryServices</span></span>

* <span data-ttu-id="4ffb6-2683">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2683">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="4ffb6-2684">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2684">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="4ffb6-2685">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2685">Az.Resources</span></span>

* <span data-ttu-id="4ffb6-2686">[https://github.com/Azure/azure-powershell/issues/7679](https://github.com/Azure/azure-powershell/issues/7679 ) javítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2686">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="4ffb6-2687">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2687">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="4ffb6-2688">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2688">Az.Sql</span></span>

* <span data-ttu-id="4ffb6-2689">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2689">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="4ffb6-2690">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2690">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="4ffb6-2691">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2691">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="4ffb6-2692">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2692">Az.Storage</span></span>

* <span data-ttu-id="4ffb6-2693">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2693">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="4ffb6-2694">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2694">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="4ffb6-2695">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2695">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="4ffb6-2696">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2696">Support Static Website configuration</span></span>
    - <span data-ttu-id="4ffb6-2697">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2697">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="4ffb6-2698">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2698">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="4ffb6-2699">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2699">Az.Websites</span></span>

* <span data-ttu-id="4ffb6-2700">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2700">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="4ffb6-2701">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2701">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="4ffb6-2702">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2702">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="4ffb6-2703">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2703">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="4ffb6-2704">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2704">Az.ApiManagement</span></span>
* <span data-ttu-id="4ffb6-2705">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2705">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="4ffb6-2706">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2706">Az.Automation</span></span>
* <span data-ttu-id="4ffb6-2707">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2707">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="4ffb6-2708">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2708">Added Update Management cmdlets</span></span>
* <span data-ttu-id="4ffb6-2709">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2709">Added Source Control cmdlets</span></span>
* <span data-ttu-id="4ffb6-2710">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2710">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="4ffb6-2711">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2711">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="4ffb6-2712">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2712">Az.Compute</span></span>
* <span data-ttu-id="4ffb6-2713">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2713">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="4ffb6-2714">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2714">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="4ffb6-2715">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2715">Az.ContainerInstance</span></span>
* <span data-ttu-id="4ffb6-2716">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2716">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="4ffb6-2717">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2717">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="4ffb6-2718">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2718">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="4ffb6-2719">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2719">Az.Network</span></span>
* <span data-ttu-id="4ffb6-2720">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2720">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="4ffb6-2721">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2721">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="4ffb6-2722">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2722">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="4ffb6-2723">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2723">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="4ffb6-2724">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2724">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="4ffb6-2725">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2725">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="4ffb6-2726">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2726">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="4ffb6-2727">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2727">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="4ffb6-2728">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2728">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="4ffb6-2729">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2729">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="4ffb6-2730">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2730">Az.Relay</span></span>
* <span data-ttu-id="4ffb6-2731">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2731">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="4ffb6-2732">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2732">Az.Resources</span></span>
* <span data-ttu-id="4ffb6-2733">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2733">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="4ffb6-2734">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2734">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="4ffb6-2735">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2735">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="4ffb6-2736">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2736">Az.ServiceFabric</span></span>
* <span data-ttu-id="4ffb6-2737">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2737">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="4ffb6-2738">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2738">Az.Sql</span></span>
* <span data-ttu-id="4ffb6-2739">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2739">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="4ffb6-2740">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2740">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4ffb6-2741">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2741">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4ffb6-2742">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2742">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4ffb6-2743">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2743">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4ffb6-2744">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2744">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="4ffb6-2745">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2745">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="4ffb6-2746">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2746">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="4ffb6-2747">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2747">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="4ffb6-2748">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2748">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="4ffb6-2749">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2749">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="4ffb6-2750">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2750">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="4ffb6-2751">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2751">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="4ffb6-2752">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2752">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="4ffb6-2753">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2753">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="4ffb6-2754">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2754">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="4ffb6-2755">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2755">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="4ffb6-2756">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2756">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="4ffb6-2757">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2757">General</span></span>
* <span data-ttu-id="4ffb6-2758">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2758">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="4ffb6-2759">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2759">Az.Profile</span></span>
* <span data-ttu-id="4ffb6-2760">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2760">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="4ffb6-2761">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2761">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="4ffb6-2762">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2762">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="4ffb6-2763">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2763">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="4ffb6-2764">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2764">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="4ffb6-2765">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2765">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="4ffb6-2766">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2766">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="4ffb6-2767">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2767">Az.CognitiveServices</span></span>
* <span data-ttu-id="4ffb6-2768">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2768">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4ffb6-2769">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2769">Az.Compute</span></span>
* <span data-ttu-id="4ffb6-2770">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2770">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="4ffb6-2771">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2771">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="4ffb6-2772">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2772">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4ffb6-2773">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2773">Az.DataLakeStore</span></span>
* <span data-ttu-id="4ffb6-2774">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2774">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="4ffb6-2775">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2775">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="4ffb6-2776">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2776">Az.Insights</span></span>
* <span data-ttu-id="4ffb6-2777">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2777">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="4ffb6-2778">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2778">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="4ffb6-2779">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2779">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="4ffb6-2780">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2780">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4ffb6-2781">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2781">Az.Network</span></span>
* <span data-ttu-id="4ffb6-2782">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2782">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="4ffb6-2783">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2783">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="4ffb6-2784">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2784">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="4ffb6-2785">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2785">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="4ffb6-2786">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2786">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="4ffb6-2787">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2787">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="4ffb6-2788">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2788">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4ffb6-2789">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2789">Az.PolicyInsights</span></span>
* <span data-ttu-id="4ffb6-2790">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2790">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="4ffb6-2791">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2791">Az.Resources</span></span>
* <span data-ttu-id="4ffb6-2792">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402 ) javítása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2792">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="4ffb6-2793">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2793">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4ffb6-2794">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2794">Az.ServiceBus</span></span>
* <span data-ttu-id="4ffb6-2795">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2795">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4ffb6-2796">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2796">Az.ServiceFabric</span></span>
* <span data-ttu-id="4ffb6-2797">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2797">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="4ffb6-2798">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2798">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="4ffb6-2799">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2799">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="4ffb6-2800">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2800">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="4ffb6-2801">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2801">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="4ffb6-2802">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2802">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="4ffb6-2803">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2803">Az.Profile</span></span>
* <span data-ttu-id="4ffb6-2804">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2804">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="4ffb6-2805">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2805">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4ffb6-2806">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2806">Az.Compute</span></span>
* <span data-ttu-id="4ffb6-2807">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2807">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="4ffb6-2808">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2808">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4ffb6-2809">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2809">Az.DataLakeStore</span></span>
* <span data-ttu-id="4ffb6-2810">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2810">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="4ffb6-2811">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2811">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="4ffb6-2812">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2812">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="4ffb6-2813">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2813">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="4ffb6-2814">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2814">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4ffb6-2815">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2815">Az.Network</span></span>
* <span data-ttu-id="4ffb6-2816">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2816">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="4ffb6-2817">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2817">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4ffb6-2818">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2818">Az.Resources</span></span>
* <span data-ttu-id="4ffb6-2819">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2819">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="4ffb6-2820">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2820">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="4ffb6-2821">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2821">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="4ffb6-2822">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2822">Azure.Storage</span></span>
* <span data-ttu-id="4ffb6-2823">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2823">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="4ffb6-2824">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2824">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="4ffb6-2825">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2825">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="4ffb6-2826">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2826">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="4ffb6-2827">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2827">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4ffb6-2828">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2828">Az.CognitiveServices</span></span>
* <span data-ttu-id="4ffb6-2829">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2829">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4ffb6-2830">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2830">Az.Compute</span></span>
* <span data-ttu-id="4ffb6-2831">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2831">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="4ffb6-2832">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2832">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="4ffb6-2833">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2833">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="4ffb6-2834">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2834">Az.DataFactoryV2</span></span>
* <span data-ttu-id="4ffb6-2835">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2835">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4ffb6-2836">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2836">Az.Network</span></span>
* <span data-ttu-id="4ffb6-2837">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2837">Added NetworkProfile functionality.</span></span> <span data-ttu-id="4ffb6-2838">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2838">new cmdlets added</span></span>
    - <span data-ttu-id="4ffb6-2839">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2839">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="4ffb6-2840">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2840">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="4ffb6-2841">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2841">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="4ffb6-2842">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2842">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="4ffb6-2843">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2843">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="4ffb6-2844">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2844">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="4ffb6-2845">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2845">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="4ffb6-2846">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2846">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="4ffb6-2847">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2847">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="4ffb6-2848">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2848">Az.RedisCache</span></span>
* <span data-ttu-id="4ffb6-2849">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2849">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="4ffb6-2850">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2850">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="4ffb6-2851">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2851">Az.Resources</span></span>
* <span data-ttu-id="4ffb6-2852">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2852">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="4ffb6-2853">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2853">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="4ffb6-2854">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2854">Az.Sql</span></span>
* <span data-ttu-id="4ffb6-2855">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2855">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4ffb6-2856">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2856">Az.Websites</span></span>
* <span data-ttu-id="4ffb6-2857">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2857">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="4ffb6-2858">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2858">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="4ffb6-2859">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2859">0.2.0 - September 2018</span></span>
 <span data-ttu-id="4ffb6-2860">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="4ffb6-2860">Initial Release</span></span>
