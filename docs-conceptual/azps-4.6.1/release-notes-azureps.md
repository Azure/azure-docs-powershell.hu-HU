---
title: Az Azure PowerShell kibocsátási megjegyzései
description: Megismerheti az Azure PowerShell-modulok legújabb frissítéseit.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 04e85c32b1af0bbdfb622973e0900724b8e3c8e3
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/01/2020
ms.locfileid: "89244228"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="3ef75-103">Az Azure PowerShell kibocsátási megjegyzései</span><span class="sxs-lookup"><span data-stu-id="3ef75-103">Azure PowerShell release notes</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="3ef75-104">4.6.1 – 2020. augusztus</span><span class="sxs-lookup"><span data-stu-id="3ef75-104">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="3ef75-105">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-105">Az.Compute</span></span>
* <span data-ttu-id="3ef75-106">A New-AzVm -EncryptionAtHost paraméterének javítása az alapértelmezett False érték eltávolításához [#12776]</span><span class="sxs-lookup"><span data-stu-id="3ef75-106">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="3ef75-107">4.6.0 – 2020. augusztus</span><span class="sxs-lookup"><span data-stu-id="3ef75-107">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3ef75-108">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3ef75-108">Az.Accounts</span></span>
* <span data-ttu-id="3ef75-109">Az összes nyilvános felhőkörnyezet betöltődik, ha a felderítési végpont nem ad vissza alapértelmezett AzureCloud- vagy más nyilvános környezetet [#12633]</span><span class="sxs-lookup"><span data-stu-id="3ef75-109">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="3ef75-110">A SubscriptionPolicies elérhetővé lett téve a 'Get-AzSubscription' parancsmagban [#12551]</span><span class="sxs-lookup"><span data-stu-id="3ef75-110">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3ef75-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3ef75-111">Az.Automation</span></span>
* <span data-ttu-id="3ef75-112">A '-RunOn' paraméterek hozzá lettek adva a 'Set-AzAutomationWebhook' parancsmaghoz hibridfeldolgozó-csoport megadásához</span><span class="sxs-lookup"><span data-stu-id="3ef75-112">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3ef75-113">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-113">Az.Compute</span></span>
* <span data-ttu-id="3ef75-114">Az '-EncryptionAtHost' paraméter hozzá lett adva a 'New-AzVm', a 'New-AzVmss', a 'New-AzVMConfig', a 'New-AzVmssConfig', az 'Update-AzVM' és az 'Update-AzVmss' parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-114">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="3ef75-115">A 'SecurityProfile' hozzá lett adva a 'Get-AzVm' és a 'Get-AzVmssVM' visszaadott objektumhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-115">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="3ef75-116">Az '-InstanceView' kapcsoló hozzá lett adva választható paraméterként a 'Get-AzHostGroup' parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-116">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="3ef75-117">Hozzá lett adva az új 'Invoke-AzVmPatchAssessment' parancsmag</span><span class="sxs-lookup"><span data-stu-id="3ef75-117">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3ef75-118">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3ef75-118">Az.DataFactory</span></span>
* <span data-ttu-id="3ef75-119">A hiányzó tulajdonságok hozzá lettek adva a PSPipelineRun osztályhoz.</span><span class="sxs-lookup"><span data-stu-id="3ef75-119">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="3ef75-120">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3ef75-120">Az.HDInsight</span></span>
* <span data-ttu-id="3ef75-121">Támogatottá vált a fürtlétrehozás a gazdagépen végzett titkosítási funkcióval.</span><span class="sxs-lookup"><span data-stu-id="3ef75-121">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3ef75-122">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3ef75-122">Az.KeyVault</span></span>
* <span data-ttu-id="3ef75-123">Figyelmeztető üzenetek lettek hozzáadva a helyreállítható törlés letiltásának tervezésekor</span><span class="sxs-lookup"><span data-stu-id="3ef75-123">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="3ef75-124">Figyelmeztető üzenetek lettek hozzáadva a SecretValueText attribútum eltávolításának tervezésekor</span><span class="sxs-lookup"><span data-stu-id="3ef75-124">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="3ef75-125">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="3ef75-125">Az.Maintenance</span></span>
* <span data-ttu-id="3ef75-126">Opcionális ütemezéssel kapcsolatos mezők lettek hozzáadva a 'New-AzMaintenanceConfiguration' parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-126">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="3ef75-127">Új parancsmag lett hozzáadva a 'Get-AzMaintenancePublicConfiguration' használatához</span><span class="sxs-lookup"><span data-stu-id="3ef75-127">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="3ef75-128">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-128">Az.ManagedServices</span></span>
* <span data-ttu-id="3ef75-129">Kompatibilitástörő változásra figyelmeztető üzenetek lettek hozzáadva a felügyelt szolgáltatások hozzárendeléséhez és definíciójához tartozó parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-129">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3ef75-130">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3ef75-130">Az.Monitor</span></span>
* <span data-ttu-id="3ef75-131">A 'set-AzDiagnosticSetting' paraméterkészlete ki lett bővítve a naplók és metrikák engedélyezésének szétválasztása érdekében [#12482]</span><span class="sxs-lookup"><span data-stu-id="3ef75-131">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="3ef75-132">Ki lett javítva az 'Add-AzMetricAlertRuleV2' folyamatból érkező metrikariasztáskor jelentkező hibája</span><span class="sxs-lookup"><span data-stu-id="3ef75-132">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="3ef75-133">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-133">Az.Resources</span></span>
* <span data-ttu-id="3ef75-134">Frissült a 'Get-AzPolicyAlias'-válasz, amely mostantól információt tartalmaz arról, hogy az alias módosítható-e az Azure Policyval.</span><span class="sxs-lookup"><span data-stu-id="3ef75-134">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="3ef75-135">Létre lett hozva az új 'Set-AzRoleAssignment' parancsmag</span><span class="sxs-lookup"><span data-stu-id="3ef75-135">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="3ef75-136">Hozzá lett adva a 'Get-AzDeploymentManagementGroupWhatIfResult' az ARM-sablon What-If típusú eredményeinek a felügyeleti csoport hatókörében történő lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-136">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="3ef75-137">Hozzá lett adva az új 'Get-AzTenantWhatIfResult' parancsmag az ARM-sablonok What-If típusú eredményeinek bérlői hatókörben történő lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-137">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="3ef75-138">A '-WhatIf' és a '-Confirm' felül lett bírálva a 'New-AzManagementGroupDeployment' és a 'New-AzTenantDeployment' esetében az ARM-sablon What-If típusú eredményeinek használata érdekében</span><span class="sxs-lookup"><span data-stu-id="3ef75-138">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="3ef75-139">Ki lett javítva a '-WhatIf' és a '-Confirm' viselkedése az új üzembehelyezési parancsmagok esetében, hogy megfeleljenek a hamis és</span><span class="sxs-lookup"><span data-stu-id="3ef75-139">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="3ef75-140">Ki lett javítva a szerializálási hiba a '-TemplateObject' és a 'TemplateParameterObject' esetében [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="3ef75-140">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="3ef75-141">Kompatibilitástörő változást okozó attribútum lett hozzáadva a 'Get-AzResourceGroupDeploymentOperation' parancsmaghoz a kimenet típusának közelgő változása miatt</span><span class="sxs-lookup"><span data-stu-id="3ef75-141">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="3ef75-142">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="3ef75-142">Az.SignalR</span></span>
* <span data-ttu-id="3ef75-143">Ki lettek javítva a 'Restart-AzSignalR' és az 'Update-AzSignalR' súgófájljainak hibái</span><span class="sxs-lookup"><span data-stu-id="3ef75-143">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="3ef75-144">Hozzá lett adva az 'Update-AzSignalRNetworkAcl' és a 'Set-AzSignalRUpstream' parancsmag</span><span class="sxs-lookup"><span data-stu-id="3ef75-144">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3ef75-145">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3ef75-145">Az.Storage</span></span>
* <span data-ttu-id="3ef75-146">A blobok lekérdezésgyorsítása támogatottá vált</span><span class="sxs-lookup"><span data-stu-id="3ef75-146">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="3ef75-147">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="3ef75-147">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="3ef75-148">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="3ef75-148">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="3ef75-149">Frissült a súgófájl, több leírás lett hozzáadva, és javítva lett egy elírás</span><span class="sxs-lookup"><span data-stu-id="3ef75-149">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="3ef75-150">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="3ef75-150">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="3ef75-151">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="3ef75-151">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="3ef75-152">Ki lett javítva a hiba, amely során meghiúsult a blobletöltés, ha a megfelelő alkönyvtár nem létezett [#12592]</span><span class="sxs-lookup"><span data-stu-id="3ef75-152">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="3ef75-153">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3ef75-153">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="3ef75-154">Támogatottá vált a Storage-fiókok objektumreplikációs szabályzatának lekérése/beállítása/eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-154">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="3ef75-155">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="3ef75-155">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="3ef75-156">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="3ef75-156">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="3ef75-157">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="3ef75-157">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="3ef75-158">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="3ef75-158">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="3ef75-159">Támogatottá vált a Blob szolgáltatásbeli változáscsatorna engedélyezése/letiltása a Storage-fiókoknál</span><span class="sxs-lookup"><span data-stu-id="3ef75-159">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="3ef75-160">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="3ef75-160">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="3ef75-161">4.5.0 – 2020. augusztus</span><span class="sxs-lookup"><span data-stu-id="3ef75-161">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3ef75-162">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3ef75-162">Az.Accounts</span></span>
* <span data-ttu-id="3ef75-163">„Connect-AzAccount” parancsmag frissítve a „MaxContextPopulation” paraméter elfogadására [#9865]</span><span class="sxs-lookup"><span data-stu-id="3ef75-163">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="3ef75-164">A SubscriptionClient-verzió frissítve a 2019. 06. 01. verzióra és a bérlői tartományok megjelenítése [#9838]</span><span class="sxs-lookup"><span data-stu-id="3ef75-164">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="3ef75-165">Az előfizetés támogatott otthoni bérlői és managedBy bérlői információi</span><span class="sxs-lookup"><span data-stu-id="3ef75-165">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="3ef75-166">A modul neve és a verzió adatai javítva a telemetriai adatokban</span><span class="sxs-lookup"><span data-stu-id="3ef75-166">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="3ef75-167">Korrigált SqlDatabaseDnsSuffix és ServiceManagementUrl, ha a környezeti metaadatok végpontja inkompatibilis értéket ad vissza</span><span class="sxs-lookup"><span data-stu-id="3ef75-167">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="3ef75-168">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="3ef75-168">Az.Aks</span></span>
* <span data-ttu-id="3ef75-169">A „ClientIdAndSecret” eltávolítva és lecserélve a ServicePrincipalIdAndSecret parancsmagra, és „ClientIdAndSecret” beállítva aliasként [#12381].</span><span class="sxs-lookup"><span data-stu-id="3ef75-169">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="3ef75-170">A „Get-AzAks”/„New-AzAks”/„Remove-AzAks”/„Set-AzAks” eltávolítva és lecserélve a „Get-AzAksCluster”/„New-AzAksCluster”/„Remove-AzAksCluster”/„Set-AzAksCluster” parancsmagra, és az eredetiek beállítva aliasként [#12373].</span><span class="sxs-lookup"><span data-stu-id="3ef75-170">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="3ef75-171">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3ef75-171">Az.ApiManagement</span></span>
* <span data-ttu-id="3ef75-172">Új 'Add-AzApiManagementApiToGateway' parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-172">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="3ef75-173">Új „Get-AzApiManagementGateway” parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-173">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="3ef75-174">Új „Get-AzApiManagementGatewayHostnameConfiguration” parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-174">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="3ef75-175">Új „Get-AzApiManagementGatewayKey” parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-175">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="3ef75-176">Új „New-AzApiManagementGateway” parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-176">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="3ef75-177">Új „New-AzApiManagementGatewayHostnameConfiguration” parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-177">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="3ef75-178">Új „New-AzApiManagementResourceLocationObject” parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-178">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="3ef75-179">Új „Remove-AzApiManagementApiFromGateway” parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-179">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="3ef75-180">Új „Remove-AzApiManagementGateway” parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-180">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="3ef75-181">Új „Remove-AzApiManagementGatewayHostnameConfiguration” parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-181">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="3ef75-182">Új „Update-AzApiManagementGateway” parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-182">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="3ef75-183">Új választható [-GatewayId] paramétert hozzáadva a „Get-AzApiManagementApi” parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="3ef75-183">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3ef75-184">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-184">Az.CognitiveServices</span></span>
* <span data-ttu-id="3ef75-185">A „Deny” utasítás kifejezetten a NetworkRules alapértelmezett műveleteként lett használva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-185">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="3ef75-186">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3ef75-186">Az.FrontDoor</span></span>
* <span data-ttu-id="3ef75-187">Kijavítottunk egy hibát, ahol kivétel történt, amikor az Enum.Parse null értéket próbált kényszeríteni egy engedélyezett vagy letiltott enumerálási értékre [#12344]</span><span class="sxs-lookup"><span data-stu-id="3ef75-187">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="3ef75-188">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3ef75-188">Az.HDInsight</span></span>
* <span data-ttu-id="3ef75-189">Támogatott a fürtlétrehozás az átvitel közbeni titkosítási funkcióval.</span><span class="sxs-lookup"><span data-stu-id="3ef75-189">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="3ef75-190">Új „EncryptionInTransit” paraméter hozzáadva a „New-AzHDInsightCluster” parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-190">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="3ef75-191">Új „EncryptionInTransit” paraméter hozzáadva a „New-AzHDInsightClusterConfig” parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-191">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="3ef75-192">Támogatotta a fürtlétrehozás a privát kapcsolat funkcióval:</span><span class="sxs-lookup"><span data-stu-id="3ef75-192">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="3ef75-193">Új „PublicNetworkAccessType” és az „OutboundPublicNetworkAccessType” paraméterek hozzáadva a „New-AzHDInsightCluster” parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-193">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="3ef75-194">Új „PublicNetworkAccessType” és az „OutboundPublicNetworkAccessType” paraméterek hozzáadva a „New-AzHDInsightClusterConfig” parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-194">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="3ef75-195">Virtuális hálózati adatok visszaadása a „New-AzHDInsightCluster” vagy a „Get-AzHDInsightCluster” meghívásakor</span><span class="sxs-lookup"><span data-stu-id="3ef75-195">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3ef75-196">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-196">Az.Network</span></span>
* <span data-ttu-id="3ef75-197">Az AddressPrefixType paraméter mostantól támogatott a Remove-AzExpressRouteCircuitConnectionConfig esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-197">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="3ef75-198">Hozzáadott nem kompatibilitástörő változások: PeerAddressType funkció a privát társviszony-létesítéshez a „Remove-AzExpressRouteCircutPeeringConfig” parancsmagban.</span><span class="sxs-lookup"><span data-stu-id="3ef75-198">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="3ef75-199">A kód úgy lett módosítva, hogy figyelmen kívül hagyja az AddressPrefixType és a PeerAddressType paramétert.</span><span class="sxs-lookup"><span data-stu-id="3ef75-199">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="3ef75-200">A „New-AzLoadBalancerFrontendIpConfig”, „New-AzPublicIpAddress” és „New-AzPublicIpPrefix” figyelmeztető üzenete módosult.</span><span class="sxs-lookup"><span data-stu-id="3ef75-200">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3ef75-201">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3ef75-201">Az.OperationalInsights</span></span>
* <span data-ttu-id="3ef75-202">A „-ForceDelete” kapcsoló hozzáadva a „Remove-AzOperationalInsightsworkspace” parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-202">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="3ef75-203">Új „Get-AzOperationalInsightsDeletedWorkspace” parancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-203">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="3ef75-204">Új „Restore-AzOperationalInsightsWorkspace” parancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-204">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3ef75-205">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-205">Az.RecoveryServices</span></span>
* <span data-ttu-id="3ef75-206">Az Azure Backup tároló-/elemfelderítési funkciója továbbfejlesztve.</span><span class="sxs-lookup"><span data-stu-id="3ef75-206">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3ef75-207">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-207">Az.Resources</span></span>
* <span data-ttu-id="3ef75-208">A „Condition”, a „ConditionVersion” és a „Description” tulajdonság hozzáadva a „New-AzRoleAssignment” parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-208">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="3ef75-209">Ebbe beletartozik az adatmodellek összes kapcsolódó változása</span><span class="sxs-lookup"><span data-stu-id="3ef75-209">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="3ef75-210">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-210">Az.Sql</span></span>
* <span data-ttu-id="3ef75-211">Ki lett javítva a „New-AzSqlServer” és a „set-AzSqlServer” esetében a kiszolgálónevekben a kis- és nagybetűk meg nem különböztetését eredményező hiba</span><span class="sxs-lookup"><span data-stu-id="3ef75-211">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="3ef75-212">A „New-AzSqlDatabaseSecondary” parancsmagban egy meglévő adatbázishiba miatt helytelen adatbázisnevet visszaadó hiba javítva lett</span><span class="sxs-lookup"><span data-stu-id="3ef75-212">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3ef75-213">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3ef75-213">Az.Storage</span></span>
* <span data-ttu-id="3ef75-214">A tároló/blob SAS-jogkivonat létrehozása támogatott az új x,t engedéllyel</span><span class="sxs-lookup"><span data-stu-id="3ef75-214">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="3ef75-215">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="3ef75-215">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="3ef75-216">„New-AzStorageContainerSASToken”</span><span class="sxs-lookup"><span data-stu-id="3ef75-216">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="3ef75-217">A fiók SAS-jogkivonat létrehozása támogatott az új x,t,f engedéllyel</span><span class="sxs-lookup"><span data-stu-id="3ef75-217">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="3ef75-218">„New-AzStorageAccountSASToken”</span><span class="sxs-lookup"><span data-stu-id="3ef75-218">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="3ef75-219">Az egyetlen fájlmegosztás használatának lekérése támogatott</span><span class="sxs-lookup"><span data-stu-id="3ef75-219">Supported get single file share usage</span></span>
    - <span data-ttu-id="3ef75-220">„Get-AzRmStorageShare”</span><span class="sxs-lookup"><span data-stu-id="3ef75-220">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="3ef75-221">4.4.0 – 2020. július</span><span class="sxs-lookup"><span data-stu-id="3ef75-221">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3ef75-222">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3ef75-222">Az.Accounts</span></span>
* <span data-ttu-id="3ef75-223">Invoke-AzRestMethod új parancsmag hozzáadása</span><span class="sxs-lookup"><span data-stu-id="3ef75-223">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="3ef75-224">Kijavítottunk egy olyan problémát, amely hitelesítési hibákat okozhat az olyan többfolyamatos forgatókönyvekben, mint például több Azure PowerShell parancsmag futtatása a Start-Job paranccsal [#9448]</span><span class="sxs-lookup"><span data-stu-id="3ef75-224">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="3ef75-225">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="3ef75-225">Az.Aks</span></span>
* <span data-ttu-id="3ef75-226">Ki lett javítva az a hiba, amely miatt a Get-AzAks nem kér le minden fürtöt [#12296]</span><span class="sxs-lookup"><span data-stu-id="3ef75-226">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="3ef75-227">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-227">Az.AnalysisServices</span></span>
* <span data-ttu-id="3ef75-228">A hitelesítés projekthivatkozása eltávolítva</span><span class="sxs-lookup"><span data-stu-id="3ef75-228">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3ef75-229">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3ef75-229">Az.Automation</span></span>
* <span data-ttu-id="3ef75-230">Ki lett javítva az a hiba, amely miatt a feloldójeleket tartalmazó sztringek nem alakíthatók át JSON-objektummá.</span><span class="sxs-lookup"><span data-stu-id="3ef75-230">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3ef75-231">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-231">Az.Compute</span></span>
* <span data-ttu-id="3ef75-232">Figyelmeztetés jelenik meg a New-AzVmss a „latest” rendszerképverzió nélküli használatakor</span><span class="sxs-lookup"><span data-stu-id="3ef75-232">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3ef75-233">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3ef75-233">Az.DataFactory</span></span>
* <span data-ttu-id="3ef75-234">Globális paraméterek hozzáadva a Data Factoryhez.</span><span class="sxs-lookup"><span data-stu-id="3ef75-234">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="3ef75-235">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3ef75-235">Az.EventGrid</span></span>
* <span data-ttu-id="3ef75-236">Frissítve a 2020-06-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="3ef75-236">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="3ef75-237">Új funkciók hozzáadva:</span><span class="sxs-lookup"><span data-stu-id="3ef75-237">Added new features:</span></span>
    - <span data-ttu-id="3ef75-238">Bemenetleképezés</span><span class="sxs-lookup"><span data-stu-id="3ef75-238">Input mapping</span></span>
    - <span data-ttu-id="3ef75-239">Eseménykézbesítési séma</span><span class="sxs-lookup"><span data-stu-id="3ef75-239">Event Delivery Schema</span></span>
    - <span data-ttu-id="3ef75-240">Privát kapcsolat</span><span class="sxs-lookup"><span data-stu-id="3ef75-240">Private Link</span></span>
    - <span data-ttu-id="3ef75-241">V10 felhő-eseményséma</span><span class="sxs-lookup"><span data-stu-id="3ef75-241">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="3ef75-242">Service Bus-témakör célértékként</span><span class="sxs-lookup"><span data-stu-id="3ef75-242">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="3ef75-243">Azure-függvény célértékként</span><span class="sxs-lookup"><span data-stu-id="3ef75-243">Azure Function As Destination</span></span>
    - <span data-ttu-id="3ef75-244">Webhookkötegelés</span><span class="sxs-lookup"><span data-stu-id="3ef75-244">WebHook Batching</span></span>
    - <span data-ttu-id="3ef75-245">Biztonságos webhook (AAD-támogatás)</span><span class="sxs-lookup"><span data-stu-id="3ef75-245">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="3ef75-246">IP-szűrés</span><span class="sxs-lookup"><span data-stu-id="3ef75-246">IpFiltering</span></span>
* <span data-ttu-id="3ef75-247">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="3ef75-247">Updated cmdlets:</span></span>
    - <span data-ttu-id="3ef75-248">New-AzEventGridSubscription/Update-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="3ef75-248">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="3ef75-249">Új választható paraméterek lettek hozzáadva a webhookkötegelés támogatásáért.</span><span class="sxs-lookup"><span data-stu-id="3ef75-249">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="3ef75-250">Új választható paraméterek lettek hozzáadva a biztonságos webhook AAD-vel való használatának támogatásáért.</span><span class="sxs-lookup"><span data-stu-id="3ef75-250">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="3ef75-251">Új felsorolási érték lett hozzáadva az EndpointType paraméterhez az Azure-függvény és a Service Bus-témakör új célértékként való támogatásáért.</span><span class="sxs-lookup"><span data-stu-id="3ef75-251">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="3ef75-252">Új választható paraméter lett hozzáadva a kézbesítési sémához.</span><span class="sxs-lookup"><span data-stu-id="3ef75-252">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="3ef75-253">New-AzEventGridTopic/Update-AzEventGridTopic és New-AzEventGridDomain/Update-AzEventGridDomain:</span><span class="sxs-lookup"><span data-stu-id="3ef75-253">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="3ef75-254">Új választható paraméterek lettek hozzáadva az IP-szűrés támogatásáért.</span><span class="sxs-lookup"><span data-stu-id="3ef75-254">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="3ef75-255">New-AzEventGridTopic/New-AzEventGridDomain:</span><span class="sxs-lookup"><span data-stu-id="3ef75-255">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="3ef75-256">Új választható paraméterek lettek hozzáadva a bemenetleképezés támogatásáért.</span><span class="sxs-lookup"><span data-stu-id="3ef75-256">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="3ef75-257">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3ef75-257">Az.FrontDoor</span></span>
* <span data-ttu-id="3ef75-258">Modul frissítve a 2020-05-01-es API-verzió használatára</span><span class="sxs-lookup"><span data-stu-id="3ef75-258">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="3ef75-259">Privátkapcsolat-támogatás hozzáadva a Storage-, KeyVault- és Web App Service-erőforrásokhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-259">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="3ef75-260">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3ef75-260">Az.HDInsight</span></span>
* <span data-ttu-id="3ef75-261">ADLSGen1/2-tárolóval rendelkező fürt országos felhőkben való létrehozásának támogatása.</span><span class="sxs-lookup"><span data-stu-id="3ef75-261">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3ef75-262">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3ef75-262">Az.Monitor</span></span>
* <span data-ttu-id="3ef75-263">Ki lett javítva a Get-AzDiagnosticSetting hibája, amely miatt a metrikák vagy naplók null értékűek [#12272]</span><span class="sxs-lookup"><span data-stu-id="3ef75-263">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3ef75-264">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-264">Az.Network</span></span>
* <span data-ttu-id="3ef75-265">A paraméterek felcserélése ki lett javítva a VWan–HubVnet kapcsolatban</span><span class="sxs-lookup"><span data-stu-id="3ef75-265">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="3ef75-266">Új parancsmagok lettek hozzáadva az Azure hálózati virtuális berendezések helyéhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-266">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="3ef75-267">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="3ef75-267">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="3ef75-268">New-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="3ef75-268">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="3ef75-269">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="3ef75-269">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="3ef75-270">Update-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="3ef75-270">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="3ef75-271">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="3ef75-271">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="3ef75-272">Új parancsmagok lettek hozzáadva az Azure hálózati virtuális berendezésekhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-272">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="3ef75-273">Get-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="3ef75-273">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="3ef75-274">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="3ef75-274">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="3ef75-275">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="3ef75-275">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="3ef75-276">Update-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="3ef75-276">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="3ef75-277">Get-AzNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="3ef75-277">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="3ef75-278">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="3ef75-278">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="3ef75-279">Application Gateway előkészítve a Private Link gyakori parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-279">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="3ef75-280">StorageSync előkészítve a Private Link gyakori parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-280">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="3ef75-281">SignalR előkészítve a Private Link gyakori parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-281">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3ef75-282">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-282">Az.RecoveryServices</span></span>
* <span data-ttu-id="3ef75-283">A hitelesítés projekthivatkozása eltávolítva</span><span class="sxs-lookup"><span data-stu-id="3ef75-283">Removed project reference to Authentication</span></span>
* <span data-ttu-id="3ef75-284">Azure Backup-parancsmagok finomhangolása a pontosabb szövegért.</span><span class="sxs-lookup"><span data-stu-id="3ef75-284">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="3ef75-285">Az Azure Backup mostantól támogatott az MAB-ügynökfeladatok beolvasásához a Get-AzRecoveryServicesBackupJob parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="3ef75-285">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3ef75-286">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-286">Az.Resources</span></span>
* <span data-ttu-id="3ef75-287">A Save-AzResourceGroupDeploymentTemplate frissítése az SDK használatához.</span><span class="sxs-lookup"><span data-stu-id="3ef75-287">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="3ef75-288">Unregister-AzResourceProvider parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-288">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="3ef75-289">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-289">Az.Sql</span></span>
* <span data-ttu-id="3ef75-290">Szolgáltatásnév és vendégfelhasználók támogatása hozzáadva a Set-AzSqlInstanceActiveDirectoryAdministrator parancsmagban</span><span class="sxs-lookup"><span data-stu-id="3ef75-290">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="3ef75-291">Ki lett javítva egy hiba az adatbesorolási parancsmagokban.</span><span class="sxs-lookup"><span data-stu-id="3ef75-291">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="3ef75-292">A felügyelt Azure SQL-példány feladatátvétele mostantól támogatott: Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="3ef75-292">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3ef75-293">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3ef75-293">Az.Storage</span></span>
* <span data-ttu-id="3ef75-294">Ki lett javítva az a probléma, amely miatt a UserAgent nem adható hozzá egyes adatsíkparancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="3ef75-294">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="3ef75-295">Storage-fiók létrehozásának/frissítésének támogatása a MinimumTlsVersion és az AllowBlobPublicAccess használatával</span><span class="sxs-lookup"><span data-stu-id="3ef75-295">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="3ef75-296">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3ef75-296">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="3ef75-297">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3ef75-297">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="3ef75-298">A Storage-fiókok Blob service-beli verziószámozása engedélyezésének/letiltásának támogatása</span><span class="sxs-lookup"><span data-stu-id="3ef75-298">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="3ef75-299">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="3ef75-299">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="3ef75-300">Blobok blobverziókkal való listázásának támogatása</span><span class="sxs-lookup"><span data-stu-id="3ef75-300">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="3ef75-301">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="3ef75-301">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="3ef75-302">Egyetlen blobpillanatkép vagy blobverzió lekérésének/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="3ef75-302">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="3ef75-303">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="3ef75-303">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="3ef75-304">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="3ef75-304">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="3ef75-305">Az Azure.Storage.Blobs 12-es verziójában létrehozott blobobjektum folyamatának támogatása</span><span class="sxs-lookup"><span data-stu-id="3ef75-305">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="3ef75-306">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3ef75-306">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="3ef75-307">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="3ef75-307">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="3ef75-308">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="3ef75-308">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="3ef75-309">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3ef75-309">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="3ef75-310">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="3ef75-310">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="3ef75-311">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="3ef75-311">Az.StorageSync</span></span>
* <span data-ttu-id="3ef75-312">A 2020-03-01-es API-verziót célzó StorageSync SDK új verziója hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-312">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="3ef75-313">Tárolószinkronizálási szolgáltatás frissítési parancsmagja hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-313">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="3ef75-314">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="3ef75-314">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="3ef75-315">IncomingTrafficPolicy és PrivateEndpointConnections hozzáadva a StorageSyncService parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="3ef75-315">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3ef75-316">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3ef75-316">Az.Websites</span></span>
* <span data-ttu-id="3ef75-317">Támogatás hozzáadva az olyan Pontok műveleteinek elvégzéséhez, amelyek nem abban az erőforráscsoportban vannak, amelyben az App Service-csomag</span><span class="sxs-lookup"><span data-stu-id="3ef75-317">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="3ef75-318">4.3.0 – 2020. június</span><span class="sxs-lookup"><span data-stu-id="3ef75-318">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3ef75-319">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3ef75-319">Az.Accounts</span></span>
* <span data-ttu-id="3ef75-320">A környezetfelderítés beállítása és a környezet hozzáadása az Add-AzEnvironment használatával alapértelmezés szerint támogatott</span><span class="sxs-lookup"><span data-stu-id="3ef75-320">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="3ef75-321">Előre betöltött szerelvények frissítése [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="3ef75-321">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="3ef75-322">Az Azure.Core szerelvény frissült</span><span class="sxs-lookup"><span data-stu-id="3ef75-322">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="3ef75-323">Ki lett javítva egy probléma, amely a Connect-AzAccount meghiúsulását okozhatta többszálas végrehajtás esetében [#11201]</span><span class="sxs-lookup"><span data-stu-id="3ef75-323">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="3ef75-324">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="3ef75-324">Az.Aks</span></span>
* <span data-ttu-id="3ef75-325">A régi [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) használata helyébe a [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) és a [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) API-k meghívása lépett</span><span class="sxs-lookup"><span data-stu-id="3ef75-325">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="3ef75-326">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3ef75-326">Az.Batch</span></span>
* <span data-ttu-id="3ef75-327">Frissítve lett az Az.Batch a Microsoft.Azure.Management.Batch SDK 11.0.0-s verziójának használatára</span><span class="sxs-lookup"><span data-stu-id="3ef75-327">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="3ef75-328">Hozzá lett adva a BatchAccount identitás beállításának lehetősége a New-AzBatchAccount parancsmagban</span><span class="sxs-lookup"><span data-stu-id="3ef75-328">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3ef75-329">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-329">Az.CognitiveServices</span></span>
* <span data-ttu-id="3ef75-330">A fiók képességeinek megjelenítése támogatott.</span><span class="sxs-lookup"><span data-stu-id="3ef75-330">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="3ef75-331">Támogatott a PublicNetworkAccess paraméter módosítása.</span><span class="sxs-lookup"><span data-stu-id="3ef75-331">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3ef75-332">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-332">Az.Compute</span></span>
* <span data-ttu-id="3ef75-333">A SimulateEviction paraméter hozzá lett adva a Set-AzVm és a Set-AzVmssVM parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="3ef75-333">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="3ef75-334">A Premium_LRS hozzá lett adva a StorageAccountType paraméter argumentumbefejezőjéhez a New-AzGalleryImageVersion parancsmagban.</span><span class="sxs-lookup"><span data-stu-id="3ef75-334">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="3ef75-335">Alállapotok lettek hozzáadva a VMCustomScriptExtension bővítményhez [#11297]</span><span class="sxs-lookup"><span data-stu-id="3ef75-335">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="3ef75-336">A Törlés lehetőség hozzá lett adva az EvictionPolicy paraméter argumentumbefejezőjéhez a New-AzVM és a New-AzVMConfig parancsmagokban.</span><span class="sxs-lookup"><span data-stu-id="3ef75-336">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="3ef75-337">Az új virtuálisgép-bővítmény neve ki lett javítva az SAP esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-337">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3ef75-338">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3ef75-338">Az.DataFactory</span></span>
* <span data-ttu-id="3ef75-339">Az ADF .Net SDK a 4.9.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="3ef75-339">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3ef75-340">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3ef75-340">Az.EventHub</span></span>
* <span data-ttu-id="3ef75-341">Managed Identity-paraméterek lettek hozzáadva a New-AzEventHubNamespace és a Set-AzEventHubNamespace parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-341">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="3ef75-342">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="3ef75-342">Az.Functions</span></span>
* <span data-ttu-id="3ef75-343">A PowerShell 7.0- és a Java 11-függvényalkalmazások létrehozása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="3ef75-343">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="3ef75-344">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3ef75-344">Az.HDInsight</span></span>
* <span data-ttu-id="3ef75-345">Támogatott a gazdagépek listázása és a HDInsight-fürt adott gazdagépeinek újraindítása.</span><span class="sxs-lookup"><span data-stu-id="3ef75-345">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="3ef75-346">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="3ef75-346">Az.HealthcareApis</span></span>
* <span data-ttu-id="3ef75-347">Az SDK a 1.1.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="3ef75-347">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="3ef75-348">Az exportálási beállítások és a Managed Identity mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="3ef75-348">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3ef75-349">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3ef75-349">Az.Monitor</span></span>
* <span data-ttu-id="3ef75-350">Ki lett javítva a bemeneti objektumparaméter a Set-AzActivityLogAlert parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-350">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="3ef75-351">Ki lett javítva az InputObject paraméter a Set-AzActionGroup parancsmag esetében [#10868]</span><span class="sxs-lookup"><span data-stu-id="3ef75-351">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3ef75-352">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-352">Az.Network</span></span>
* <span data-ttu-id="3ef75-353">Az AddressPrefixType paraméter mostantól támogatott a Remove-AzExpressRouteCircuitConnectionConfig esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-353">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="3ef75-354">Új parancsmagok lettek hozzáadva az Azure FirewallPolicy szabályzathoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-354">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="3ef75-355">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="3ef75-355">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="3ef75-356">A tűzfalszabályzathoz tartozó hálózati szabályok céltartományneveinek támogatása</span><span class="sxs-lookup"><span data-stu-id="3ef75-356">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="3ef75-357">A háttércímkészlet műveletei mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="3ef75-357">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="3ef75-358">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="3ef75-358">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="3ef75-359">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3ef75-359">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="3ef75-360">Set-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3ef75-360">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="3ef75-361">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3ef75-361">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="3ef75-362">Get-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3ef75-362">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="3ef75-363">A New-AzIpGroup névérvényesítése hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-363">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="3ef75-364">Új parancsmagok lettek hozzáadva az Azure FirewallPolicy szabályzathoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-364">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="3ef75-365">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="3ef75-365">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="3ef75-366">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: Egyéni DNS-kiszolgálók beállítása/eltávolítása a VirtualWan-P2SVpnGateway átjárón.</span><span class="sxs-lookup"><span data-stu-id="3ef75-366">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="3ef75-367">Frissült a New-AzP2sVpnGateway: A -CustomDnsServer opcionális paraméter hozzá lett adva az ügyfelek számára, hogy megadhassák a P2SVpnGateway átjárón beállítani kívánt DNS-kiszolgálókat (ezeket pont–hely ügyfelek is használhatják).</span><span class="sxs-lookup"><span data-stu-id="3ef75-367">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="3ef75-368">Frissült az AzP2sVpnGateway: A -CustomDnsServer opcionális paraméter hozzá lett adva az ügyfelek számára, hogy megadhassák a P2SVpnGateway átjárón beállítani kívánt DNS-kiszolgálókat (ezeket pont–hely ügyfelek is használhatják).</span><span class="sxs-lookup"><span data-stu-id="3ef75-368">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="3ef75-369">Frissült az Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="3ef75-369">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="3ef75-370">A -BgpPeeringAddress opcionális paraméter hozzá lett adva az ügyfelek számára a VPN Gateway átjárón beállítani kívánt egyéni bgps megadásához.</span><span class="sxs-lookup"><span data-stu-id="3ef75-370">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="3ef75-371">Új parancsmag lett hozzáadva a VirtualHub-erőforrás útválasztási állapota visszaállításának támogatásához:</span><span class="sxs-lookup"><span data-stu-id="3ef75-371">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="3ef75-372">Reset-AzHubRouter</span><span class="sxs-lookup"><span data-stu-id="3ef75-372">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="3ef75-373">A tűzfalszabályzat legutóbbi Swagger-módosításának megfelelően frissültek az alábbi tételek</span><span class="sxs-lookup"><span data-stu-id="3ef75-373">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="3ef75-374">A RuleGroup, a RuleCollectionGroup és a RuleType neve megváltozott</span><span class="sxs-lookup"><span data-stu-id="3ef75-374">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="3ef75-375">Mostantól támogatott a tűzfalszabályzat NAT-szabálygyűjteménye esetében több NAT-szabálygyűjtemény használata</span><span class="sxs-lookup"><span data-stu-id="3ef75-375">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="3ef75-376">[Kompatibilitástörő változás] Kötelező SourceIpGroup paraméter lett hozzáadva a New-AzFirewallPolicyApplicationRule és a New-AzFirewallPolicyNetworkRule esetében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-376">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="3ef75-377">[Kompatibilitástörő változás] A New-AzFirewallPolicyApplicationRule ki lett javítva, a SourceAddress paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="3ef75-377">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="3ef75-378">[Kompatibilitástörő változás] A New-AzFirewallPolicyApplicationRule ki lett javítva, a SourceAddress paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="3ef75-378">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="3ef75-379">[Kompatibilitástörő változás] Eltávolított kötelező paraméterek: TranslatedAddress, TranslatedPort a New-AzFirewallPolicyNatRuleCollection esetében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-379">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="3ef75-380">Új parancsmagok lettek hozzáadva a PrivateLink támogatásához az Application Gatewayen</span><span class="sxs-lookup"><span data-stu-id="3ef75-380">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="3ef75-381">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ef75-381">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="3ef75-382">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ef75-382">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="3ef75-383">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ef75-383">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="3ef75-384">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ef75-384">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="3ef75-385">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ef75-385">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="3ef75-386">New-AzApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ef75-386">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="3ef75-387">Új parancsmagok lettek hozzáadva a VirtualHub HubRouteTables gyermekerőforrásai esetében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-387">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="3ef75-388">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="3ef75-388">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="3ef75-389">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="3ef75-389">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="3ef75-390">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="3ef75-390">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="3ef75-391">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="3ef75-391">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="3ef75-392">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="3ef75-392">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="3ef75-393">Frissültek a meglévő parancsmagok az opcionális RoutingConfiguration bemeneti paraméter támogatásához az egyéni útválasztás esetében a VirtualWanban.</span><span class="sxs-lookup"><span data-stu-id="3ef75-393">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="3ef75-394">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="3ef75-394">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="3ef75-395">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="3ef75-395">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="3ef75-396">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="3ef75-396">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="3ef75-397">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="3ef75-397">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="3ef75-398">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="3ef75-398">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="3ef75-399">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="3ef75-399">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="3ef75-400">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="3ef75-400">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="3ef75-401">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="3ef75-401">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3ef75-402">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3ef75-402">Az.OperationalInsights</span></span>
* <span data-ttu-id="3ef75-403">Ki lett javítva az a PSWorkspace-hiba, amely miatt meghiúsult az IOperationalInsightsWorkspace implementálása [#12135]</span><span class="sxs-lookup"><span data-stu-id="3ef75-403">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="3ef75-404">A pergb2018 hozzá lett adva az SKU paraméter érvényes értékéhez a Set-AzOperationalInsightsWorkspace esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-404">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="3ef75-405">A FunctionParameters alias hozzá lett adva a FunctionParameter paraméterhez a következők esetében:</span><span class="sxs-lookup"><span data-stu-id="3ef75-405">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="3ef75-406">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="3ef75-406">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="3ef75-407">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="3ef75-407">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3ef75-408">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-408">Az.RecoveryServices</span></span>
* <span data-ttu-id="3ef75-409">Az Azure Backup mostantól támogatott az MAB-elemek beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="3ef75-409">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="3ef75-410">Az Azure Site Recovery támogatja a StandardSSD_LRS lemeztípust</span><span class="sxs-lookup"><span data-stu-id="3ef75-410">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="3ef75-411">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-411">Az.Resources</span></span>
* <span data-ttu-id="3ef75-412">A UsageLocation, GivenName, Surname, AccountEnabled, MailNickname, Mail paraméterek hozzá lettek adva a PSADUser esetében [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="3ef75-412">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="3ef75-413">Ki lett javítva az a hiba, hogy a -Mail nem működött a Get-AzADUser esetében [#11981]</span><span class="sxs-lookup"><span data-stu-id="3ef75-413">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="3ef75-414">Az -ExcludeChangeType paraméter hozzá lett adva a következőkhöz: Get-AzDeploymentWhatIfResult és Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="3ef75-414">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="3ef75-415">A -WhatIfExcludeChangeType paraméter hozzá lett adva a következőkhöz: New-AzDeployment és New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3ef75-415">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="3ef75-416">A Test-Az\*Deployment parancsmagok frissültek a megfelelőbb hibaüzenetek megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-416">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="3ef75-417">Ki lett javítva az üzemelő példány -Name paraméterének súgóüzenete a create és a What-If parancsmagok esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-417">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="3ef75-418">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-418">Az.Sql</span></span>
* <span data-ttu-id="3ef75-419">Szolgáltatásnév támogatása hozzáadva a Set SQL Server Azure Active Directory Admin parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-419">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="3ef75-420">Ki lett javítva a szinkronizálási probléma az adatbesorolási parancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-420">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="3ef75-421">Támogatott az e-mail-cím alapján történő felhasználókeresés a következő esetében: Set-AzSqlServerActiveDirectoryAdministrator [#12192]</span><span class="sxs-lookup"><span data-stu-id="3ef75-421">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3ef75-422">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3ef75-422">Az.Storage</span></span>
* <span data-ttu-id="3ef75-423">Támogatott a tárfiók RequireInfrastructureEncryption használatával való létrehozása</span><span class="sxs-lookup"><span data-stu-id="3ef75-423">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="3ef75-424">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3ef75-424">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="3ef75-425">Át lett helyezve az Azure.Core betöltési logikája Az.Accounts modulba</span><span class="sxs-lookup"><span data-stu-id="3ef75-425">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3ef75-426">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3ef75-426">Az.Websites</span></span>
* <span data-ttu-id="3ef75-427">Hozzáadott védelem a létrehozott webalkalmazás törléséhez, ha a visszaállítás nem sikerült a Restore-AzDeletedWebApp esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-427">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="3ef75-428">A SourceWebApp.Location paraméter hozzá lett adva a New-AzWebApp és a New-AzWebAppSlot esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-428">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="3ef75-429">Ki lett javítva az a hiba, amely megakadályozta a tárolóbeállítások módosítását a Set-AzWebApp és a Set-AzWebAppSlot esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-429">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="3ef75-430">Ki lett javítva a SiteConfig lekérésének hibája, ha a -Name nem lett megadva a Get-AzWebApp esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-430">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="3ef75-431">Támogatás hozzáadva ASP létráhozásához Linux-alkalmazások esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-431">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="3ef75-432">Kivételek hozzáadva az erőforráscsoportok közötti klónozás esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-432">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="3ef75-433">4.2.0 – 2020. június</span><span class="sxs-lookup"><span data-stu-id="3ef75-433">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3ef75-434">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3ef75-434">Az.Accounts</span></span>
* <span data-ttu-id="3ef75-435">Kijavítottunk egy problémát, amely miatt az Az Azure Automation-naplókat vagy PowerShell-feladatokat hagyott ki [#11492]</span><span class="sxs-lookup"><span data-stu-id="3ef75-435">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="3ef75-436">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-436">Az.AnalysisServices</span></span>
* <span data-ttu-id="3ef75-437">Frissítettük az adatsík parancsmagjainak szerelvényverzióját</span><span class="sxs-lookup"><span data-stu-id="3ef75-437">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="3ef75-438">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3ef75-438">Az.ApiManagement</span></span>
* <span data-ttu-id="3ef75-439">Frissítettük a szolgáltatásfelügyeleti parancsmagok szerelvényverzióját</span><span class="sxs-lookup"><span data-stu-id="3ef75-439">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="3ef75-440">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="3ef75-440">Az.Billing</span></span>
* <span data-ttu-id="3ef75-441">Frissítettük a felhasználási parancsmagok szerelvényverzióját</span><span class="sxs-lookup"><span data-stu-id="3ef75-441">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3ef75-442">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-442">Az.CognitiveServices</span></span>
* <span data-ttu-id="3ef75-443">A PrivateEndpoint és a PublicNetworkAccess vezérlők támogatása.</span><span class="sxs-lookup"><span data-stu-id="3ef75-443">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="3ef75-444">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3ef75-444">Az.DataFactory</span></span>
* <span data-ttu-id="3ef75-445">Frissítettük a Data Factory V2 parancsmagjainak szerelvényverzióját</span><span class="sxs-lookup"><span data-stu-id="3ef75-445">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="3ef75-446">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="3ef75-446">Az.DataShare</span></span>
* <span data-ttu-id="3ef75-447">Az Az.DataShare modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="3ef75-447">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="3ef75-448">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="3ef75-448">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="3ef75-449">Az „Az.DesktopVirtualization” modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="3ef75-449">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3ef75-450">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3ef75-450">Az.OperationalInsights</span></span>
* <span data-ttu-id="3ef75-451">SDK frissítve a 0.21.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="3ef75-451">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="3ef75-452">Választható paraméterek hozzáadva a következőkhöz:</span><span class="sxs-lookup"><span data-stu-id="3ef75-452">Added optional parameters to</span></span> 
    - <span data-ttu-id="3ef75-453">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="3ef75-453">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="3ef75-454">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="3ef75-454">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3ef75-455">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3ef75-455">Az.PolicyInsights</span></span>
* <span data-ttu-id="3ef75-456">Javítottuk a Start-AzPolicyComplianceScan 3. példáját</span><span class="sxs-lookup"><span data-stu-id="3ef75-456">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="3ef75-457">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="3ef75-457">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="3ef75-458">Frissítettük a PowerBI-parancsmagok szerelvényverzióját</span><span class="sxs-lookup"><span data-stu-id="3ef75-458">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="3ef75-459">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="3ef75-459">Az.PrivateDns</span></span>
* <span data-ttu-id="3ef75-460">Javítottuk a Remove-AzPrivateDnsRecordSet kimeneti sztringjének formázását</span><span class="sxs-lookup"><span data-stu-id="3ef75-460">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3ef75-461">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-461">Az.RecoveryServices</span></span>
* <span data-ttu-id="3ef75-462">Azure Site Recovery-támogatás helyreállítási terv létrehozásához az xml-bemenetből kezdeményezett, zónák közötti replikáció esetében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-462">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="3ef75-463">Frissítettük a SiteRecovery és a Backup parancsmagok szerelvényverzióját</span><span class="sxs-lookup"><span data-stu-id="3ef75-463">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="3ef75-464">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-464">Az.Resources</span></span>
* <span data-ttu-id="3ef75-465">Szélsőérték paraméter hozzáadva a Get-AzDeploymentScriptLog és a Save-AzDeploymentScriptLog parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-465">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="3ef75-466">Kimeneti tulajdonság formázása és megjelenítése a Get-AzDeploymentScript parancsmag kimenetén</span><span class="sxs-lookup"><span data-stu-id="3ef75-466">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="3ef75-467">A -DeploymentScriptInputObject paraméter új neve -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="3ef75-467">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="3ef75-468">Javítottuk a parancsmagüzenetek hiányzó fájl-/célnevét.</span><span class="sxs-lookup"><span data-stu-id="3ef75-468">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="3ef75-469">Frissítettük a Resource Manager és a címkék parancsmagjainak szerelvényverzióját</span><span class="sxs-lookup"><span data-stu-id="3ef75-469">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="3ef75-470">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-470">Az.Sql</span></span>
* <span data-ttu-id="3ef75-471">UsePrivateLinkConnection hozzáadva a következőkhöz: New-AzSqlSyncGroup, Update-AzSqlSyncGroup, New-AzSqlSyncMember és Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="3ef75-471">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="3ef75-472">SyncMemberAzureDatabaseResourceId hozzáadva a következőkhöz: New-AzSqlSyncMember és Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="3ef75-472">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="3ef75-473">Vendégfelhasználó-keresés támogatása hozzáadva a Set SQL Server Azure Active Directory Admin parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-473">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3ef75-474">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3ef75-474">Az.Storage</span></span>
* <span data-ttu-id="3ef75-475">Frissítettük az adatsík parancsmagjainak szerelvényverzióját</span><span class="sxs-lookup"><span data-stu-id="3ef75-475">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="3ef75-476">4.1.0 – 2020. május</span><span class="sxs-lookup"><span data-stu-id="3ef75-476">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="3ef75-477">A legutóbbi kiadás óta bevezetett újdonságok</span><span class="sxs-lookup"><span data-stu-id="3ef75-477">Highlights since the last release</span></span>
* <span data-ttu-id="3ef75-478">Támogatott PowerShell-verziók: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="3ef75-478">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="3ef75-479">Az Az.Functions általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="3ef75-479">General availability of Az.Functions</span></span> 
* <span data-ttu-id="3ef75-480">A következők rendelkeznek nagyobb kiadással: Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources és Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3ef75-480">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3ef75-481">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3ef75-481">Az.Accounts</span></span>
* <span data-ttu-id="3ef75-482">Frissítve lett az Add-AzEnvironment és a Set-AzEnvironment parancsmag, amelyek mostantól elfogadják az AzureSynapseAnalyticsEndpointResourceId és az AzureSynapseAnalyticsEndpointSuffix paramétereket</span><span class="sxs-lookup"><span data-stu-id="3ef75-482">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="3ef75-483">Hozzá lettek adva az Azure.Core-hoz kapcsolódó szerelvények az Az.Accounts-hoz, a támogatott platformok a Windows PowerShell 5.1, a PowerShell Core 6.2.4 és a PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="3ef75-483">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="3ef75-484">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="3ef75-484">Az.Aks</span></span>
* <span data-ttu-id="3ef75-485">Az API-verzió frissítve lett a 2019-10-01-es verzióra</span><span class="sxs-lookup"><span data-stu-id="3ef75-485">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="3ef75-486">Az AKS Windows-tárolókkal történő létrehozásának támogatása</span><span class="sxs-lookup"><span data-stu-id="3ef75-486">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="3ef75-487">Elérhető új parancsmagok: New-AzAksNodePool, Update-AzAksNodePool, Remove-AzAksNodePool,        Get-AzAksNodePool, Install-AzAksKubectl, Get-AzAksVersion</span><span class="sxs-lookup"><span data-stu-id="3ef75-487">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="3ef75-488">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3ef75-488">Az.ApiManagement</span></span>
* <span data-ttu-id="3ef75-489">New-AzApiManagement és Set-AzApiManagement: az [-AssignIdentity] paraméter új neve [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="3ef75-489">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="3ef75-490">New-AzApiManagement és Set-AzApiManagement: Új paraméter lett hozzáadva: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="3ef75-490">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="3ef75-491">A Get-AzApiManagementProperty át lett nevezve a következőre: Get-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="3ef75-491">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="3ef75-492">A PropertyId paraméter át lett nevezve a következőre: NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="3ef75-492">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="3ef75-493">A New-AzApiManagementProperty át lett nevezve a következőre: New-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="3ef75-493">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="3ef75-494">A PropertyId paraméter át lett nevezve a következőre: NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="3ef75-494">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="3ef75-495">A Set-AzApiManagementProperty át lett nevezve a következőre: Set-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="3ef75-495">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="3ef75-496">A PropertyId paraméter át lett nevezve a következőre: NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="3ef75-496">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="3ef75-497">A Remove-AzApiManagementProperty át lett nevezve a következőre: Remove-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="3ef75-497">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="3ef75-498">A PropertyId paraméter át lett nevezve a következőre: NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="3ef75-498">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="3ef75-499">Hozzá lett adva az új Get-AzApiManagementAuthorizationServerClientSecret parancsmag, valamint a Get-AzApiManagementAuthorizationServer már nem ad vissza titkos ügyfélkulcsot.</span><span class="sxs-lookup"><span data-stu-id="3ef75-499">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="3ef75-500">Hozzá lett adva az új Get-AzApiManagementNamedValueSecretValue parancsmag, és a Get-AzApiManagementNamedValue nem ad vissza titkos kulcsot.</span><span class="sxs-lookup"><span data-stu-id="3ef75-500">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="3ef75-501">Hozzá lett adva az új Get-AzApiManagementOpenIdConnectProviderClientSecret parancsmag, valamint a Get-AzApiManagementOpenIdConnectProvider már nem ad vissza titkos ügyfélkulcsot.</span><span class="sxs-lookup"><span data-stu-id="3ef75-501">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="3ef75-502">Hozzá lett adva az új Get-AzApiManagementSubscriptionKey parancsmag, és a Get-AzApiManagementSubscription már nem ad vissza előfizetési azonosítót.</span><span class="sxs-lookup"><span data-stu-id="3ef75-502">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="3ef75-503">Hozzá lett adva az új Get-AzApiManagementTenantAccessSecret parancsmag, és a Get-AzApiManagementTenantAccess már nem ad vissza kulcsot.</span><span class="sxs-lookup"><span data-stu-id="3ef75-503">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="3ef75-504">Hozzá lett adva az új Get-AzApiManagementTenantGitAccessSecret parancsmag, és a Get-AzApiManagementTenantGitAccess már nem ad vissza kulcsot.</span><span class="sxs-lookup"><span data-stu-id="3ef75-504">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="3ef75-505">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="3ef75-505">Az.ApplicationInsights</span></span>
* <span data-ttu-id="3ef75-506">Hozzáadott paraméterek: A New-AzApplicationInsights esetében: RetentionInDays, PublicNetworkAccessForIngestion, PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="3ef75-506">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="3ef75-507">Létre lett hozva az Update-AzApplicationInsights parancsmag</span><span class="sxs-lookup"><span data-stu-id="3ef75-507">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="3ef75-508">Parancsmagok lettek létrehozva a társított tárfiókhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-508">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="3ef75-509">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3ef75-509">Az.Batch</span></span>
* <span data-ttu-id="3ef75-510">Frissítve lett az Az.Batch a Microsoft.Azure.Batch SDK 13.0.0.-s verziójának és a Microsoft.Azure.Management.Batch SDK 9.0.0-s verziójának használatára.</span><span class="sxs-lookup"><span data-stu-id="3ef75-510">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="3ef75-511">Kiválaszthatóvá vált a hozzáadni kívánt tanúsítvány típusa a New-AzBatchCertificate új -CertificateKind paraméterének használatával.</span><span class="sxs-lookup"><span data-stu-id="3ef75-511">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="3ef75-512">El lett távolítva az ApplicationPackages tulajdonság a PSApplicationből, amelynek típusa eddig mindig '' volt.</span><span class="sxs-lookup"><span data-stu-id="3ef75-512">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="3ef75-513">Most már lekérhetők az alkalmazásokon belüli adott csomagok a Get-AzBatchApplicationPackage használatával.</span><span class="sxs-lookup"><span data-stu-id="3ef75-513">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="3ef75-514">Például: Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication.</span><span class="sxs-lookup"><span data-stu-id="3ef75-514">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="3ef75-515">Egy készlet New-AzBatchPool használatával történő létrehozásakor a PSImageReference VirtualMachineImageId tulajdonsága már csak a Shared Image Gallery-ben található rendszerképre hivatkozhat.</span><span class="sxs-lookup"><span data-stu-id="3ef75-515">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="3ef75-516">Egy készlet New-AzBatchPool használatával történő létrehozásakor a készlet nyilvános IP-cím nélkül is létrehozható a PSNetworkConfiguration új PublicIPAddressConfiguration tulajdonságával.</span><span class="sxs-lookup"><span data-stu-id="3ef75-516">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="3ef75-517">A PSNetworkConfiguration PublicIPs tulajdonsága a PSPublicIPAddressConfiguration esetében is elérhető.</span><span class="sxs-lookup"><span data-stu-id="3ef75-517">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="3ef75-518">Ez a tulajdonság csak akkor adható meg, ha az IPAddressProvisioningType UserManaged típusú.</span><span class="sxs-lookup"><span data-stu-id="3ef75-518">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3ef75-519">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-519">Az.Compute</span></span>
* <span data-ttu-id="3ef75-520">A HostId paraméter hozzá lett adva az Update-AzVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-520">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="3ef75-521">Frissültek a New-AzVMConfig, New-AzVmssConfig, Update-AzVmss, Set-AzVMOperatingSystem és Set-AzVmssOsProfile parancsmagok súgódokumentumai.</span><span class="sxs-lookup"><span data-stu-id="3ef75-521">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="3ef75-522">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="3ef75-522">Breaking changes</span></span>
    - <span data-ttu-id="3ef75-523">A FilterExpression paraméter el lett távolítva a Get-AzVMImage parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="3ef75-523">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="3ef75-524">Az AssignIdentity paraméter el lett távolítva a New-AzVmssConfig, New-AzVMConfig és Update-AzVM parancsmagokból.</span><span class="sxs-lookup"><span data-stu-id="3ef75-524">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="3ef75-525">Az AutomaticRepairMaxInstanceRepairsPercent paraméter el lett távolítva a New-AzVmssConfig és az Update-AzVmss parancsmagokból.</span><span class="sxs-lookup"><span data-stu-id="3ef75-525">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="3ef75-526">Az AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus és VirtualMachineScaleSetsColocationStatus tulajdonságok el lettek távolítva a ProximityPlacementGroup paraméterből.</span><span class="sxs-lookup"><span data-stu-id="3ef75-526">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="3ef75-527">A MaxInstanceRepairsPercent tulajdonság el lett távolítva a következőből: AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="3ef75-527">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="3ef75-528">Az AvailabilitySets, VirtualMachines és VirtualMachineScaleSets típusa IList<SubResource> helyett mostantól IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="3ef75-528">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="3ef75-529">Frissült a Get-AzVM parancsmag leírása, hogy pontosabban ismertesse a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="3ef75-529">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="3ef75-530">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3ef75-530">Az.DataFactory</span></span>
* <span data-ttu-id="3ef75-531">Adatfolyam futtatókörnyezeti tulajdonságaihoz tartozó CRUD támogatása a felügyelt IR-ben.</span><span class="sxs-lookup"><span data-stu-id="3ef75-531">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="3ef75-532">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3ef75-532">Az.FrontDoor</span></span>
* <span data-ttu-id="3ef75-533">Új parancsmagok lettek hozzáadva a Front Door szabálymotor-objektumának létrehozására, frissítésére, lekérésére és törlésére.</span><span class="sxs-lookup"><span data-stu-id="3ef75-533">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="3ef75-534">Hozzá lettek adva segítő parancsmagok a Front Door szabálymotor-objektumának létrehozásához</span><span class="sxs-lookup"><span data-stu-id="3ef75-534">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="3ef75-535">Hozzá lett adva a szabálymotor-referencia a Front Door útválasztásiszabály-objektumához.</span><span class="sxs-lookup"><span data-stu-id="3ef75-535">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="3ef75-536">Hozzá lettek adva privát kapcsolati paraméterek a Front Door háttérobjektumához</span><span class="sxs-lookup"><span data-stu-id="3ef75-536">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="3ef75-537">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="3ef75-537">Az.Functions</span></span>
* <span data-ttu-id="3ef75-538">Az Az.Functions modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="3ef75-538">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="3ef75-539">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3ef75-539">Az.HDInsight</span></span>
* <span data-ttu-id="3ef75-540">Az ügyfél által felügyelt kulcson alapuló lemeztitkosítás mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="3ef75-540">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="3ef75-541">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="3ef75-541">Az.HealthcareApis</span></span>
* <span data-ttu-id="3ef75-542">A hozzáférési szabályzatok már nem tartoznak alapértelmezés szerint az aktuális rendszerbiztonsági taghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-542">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3ef75-543">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3ef75-543">Az.IotHub</span></span>
* <span data-ttu-id="3ef75-544">Hozzá lett adva egy parancsmag, amellyel egy SQL-szerű nyelv használatával végzett, információkat lekérő lekérdezés indítható el az IoT Hubban.</span><span class="sxs-lookup"><span data-stu-id="3ef75-544">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="3ef75-545">Javítva a hiba, amely miatt az Add-AzIotHubDevice gyermekeszköz nélkül nem tudott Edge-kompatibilis eszközt létrehozni [#11597]</span><span class="sxs-lookup"><span data-stu-id="3ef75-545">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="3ef75-546">Hozzá lett adva egy parancsmag egy SAS-token létrehozásához az IoT Hub, eszköz vagy modul számára.</span><span class="sxs-lookup"><span data-stu-id="3ef75-546">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="3ef75-547">Hozzá lett adva egy parancsmag a konfiguráció-metrikák lekérdezésének meghívásához.</span><span class="sxs-lookup"><span data-stu-id="3ef75-547">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="3ef75-548">Az IoT Edge nagy léptékű automatikus üzembe helyezésének kezelése.</span><span class="sxs-lookup"><span data-stu-id="3ef75-548">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="3ef75-549">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="3ef75-549">New cmdlets are:</span></span>
    - <span data-ttu-id="3ef75-550">Add-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="3ef75-550">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="3ef75-551">Get-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="3ef75-551">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="3ef75-552">Remove-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="3ef75-552">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="3ef75-553">Set-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="3ef75-553">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="3ef75-554">Hozzá lett adva egy parancsmag, amellyel az IoT Edge üzembehelyezési metrikáit lekérő lekérdezést hívható meg.</span><span class="sxs-lookup"><span data-stu-id="3ef75-554">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="3ef75-555">Hozzá lett adva egy parancsmag a konfiguráció tartalmának egy adott Edge-eszközre történő alkalmazásához.</span><span class="sxs-lookup"><span data-stu-id="3ef75-555">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3ef75-556">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3ef75-556">Az.KeyVault</span></span>
* <span data-ttu-id="3ef75-557">A következő két alias el lett távolítva: New-AzKeyVaultCertificateAdministratorDetails és New-AzKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="3ef75-557">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="3ef75-558">Alapértelmezés szerint engedélyezve lett a helyreállítható törlés egy kulcstartó létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="3ef75-558">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="3ef75-559">Kulcstartó létrehozásakor a hálózati szabályok beállíthatók a megadott hálózati helyekről való hozzáférés szabályozására</span><span class="sxs-lookup"><span data-stu-id="3ef75-559">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="3ef75-560">A saját kulcs használata (BYOK) már támogatott</span><span class="sxs-lookup"><span data-stu-id="3ef75-560">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="3ef75-561">Az Add-AzKeyVaultKey támogatja a kulcscserekulcsok létrehozását</span><span class="sxs-lookup"><span data-stu-id="3ef75-561">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="3ef75-562">A Get-AzKeyVaultKey támogatja a nyilvános kulcsok PEM formátumban való letöltését</span><span class="sxs-lookup"><span data-stu-id="3ef75-562">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="3ef75-563">Frissült az Add-AzKeyVaultKey súgódokumentációjának KeyOps része</span><span class="sxs-lookup"><span data-stu-id="3ef75-563">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3ef75-564">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3ef75-564">Az.Monitor</span></span>
* <span data-ttu-id="3ef75-565">Javítva a Set-AzDiagnosticSettings hibája, amely miatt a megtartási szabályzat nem vonatkozott minden kategóriára [#11589]</span><span class="sxs-lookup"><span data-stu-id="3ef75-565">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="3ef75-566">A WebTest rendelkezésre állási feltételeinek támogatása a 2-es verziójú metrikariasztás esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-566">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="3ef75-567">New-AzMetricAlertRuleV2Criteria: mostantól megadhatók a webteszt rendelkezésre állási feltételei</span><span class="sxs-lookup"><span data-stu-id="3ef75-567">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="3ef75-568">Add-AzMetricAlertRuleV2: támogatja a webteszt új rendelkezésre állási feltételeit</span><span class="sxs-lookup"><span data-stu-id="3ef75-568">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="3ef75-569">El lett távolítva a RetentionPolicy redundáns definíciója a PSLogProfile-ból [#7608]</span><span class="sxs-lookup"><span data-stu-id="3ef75-569">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="3ef75-570">El lettek távolítva a PSEventData objektumban meghatározott redundáns tulajdonságok [#11353]</span><span class="sxs-lookup"><span data-stu-id="3ef75-570">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="3ef75-571">A Get-Azlog át lett nevezve a következőre: Get-AzActivityLog</span><span class="sxs-lookup"><span data-stu-id="3ef75-571">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3ef75-572">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-572">Az.Network</span></span>
* <span data-ttu-id="3ef75-573">Kompatibilitástörő változást okozó attribútum lett hozzáadva, amely figyelmeztet a Zone alapértelmezett viselkedésének változásáról</span><span class="sxs-lookup"><span data-stu-id="3ef75-573">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="3ef75-574">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3ef75-574">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="3ef75-575">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3ef75-575">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="3ef75-576">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3ef75-576">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="3ef75-577">Hozzá lett adva az új, SecurityPartnerProvider legfelsőbb szintű erőforrás támogatása</span><span class="sxs-lookup"><span data-stu-id="3ef75-577">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="3ef75-578">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="3ef75-578">New cmdlets added:</span></span>
        - <span data-ttu-id="3ef75-579">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3ef75-579">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="3ef75-580">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3ef75-580">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="3ef75-581">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3ef75-581">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="3ef75-582">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3ef75-582">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="3ef75-583">Hozzá lett adva a RequiredZoneNames tulajdonság a PSPrivateLinkResource esetében, és a GroupId a PSPrivateEndpointConnection esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-583">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="3ef75-584">Kijavítva a SuccessThresholdRoundTripTimeMs paraméter típusa a New-AzNetworkWatcherConnectionMonitorTestConfigurationObject esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-584">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="3ef75-585">Frissítve lettek a VirtualWan parancsmagok az AllowVnetToVnetTraffic argumentum True értékre való állításához.</span><span class="sxs-lookup"><span data-stu-id="3ef75-585">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="3ef75-586">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="3ef75-586">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="3ef75-587">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="3ef75-587">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="3ef75-588">Új parancsmagok lettek hozzáadva a privát végpontok DNS-zónacsoportjainak támogatásához</span><span class="sxs-lookup"><span data-stu-id="3ef75-588">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="3ef75-589">New-AzPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="3ef75-589">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="3ef75-590">Get-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="3ef75-590">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="3ef75-591">New-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="3ef75-591">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="3ef75-592">Set-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="3ef75-592">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="3ef75-593">Remove-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="3ef75-593">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="3ef75-594">Hozzá lett adva a DNSEnableProxy, a DNSRequireProxyForNetworkRules és a DNSServers paraméter az AzureFirewall-hoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-594">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="3ef75-595">Hozzá lett adva az EnableDnsProxy, a DnsProxyNotRequiredForNetworkRule és a DnsServer paraméter az AzureFirewall-hoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-595">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="3ef75-596">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="3ef75-596">Updated cmdlet:</span></span>
        - <span data-ttu-id="3ef75-597">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="3ef75-597">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3ef75-598">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3ef75-598">Az.OperationalInsights</span></span>
* <span data-ttu-id="3ef75-599">Frissítve lett a régi kód az újonnan létrehozott SDK alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="3ef75-599">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="3ef75-600">Az elavult API-k miatt törölt parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3ef75-600">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="3ef75-601">Get-AzOperationalInsightsSavedSearchResult (alias: Get-AzOperationalInsightsSavedSearchResults)</span><span class="sxs-lookup"><span data-stu-id="3ef75-601">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="3ef75-602">Get-AzOperationalInsightsSearchResult (alias: Get-AzOperationalInsightsSearchResults)</span><span class="sxs-lookup"><span data-stu-id="3ef75-602">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="3ef75-603">Get-AzOperationalInsightsLinkTarget (alias: Get-AzOperationalInsightsLinkTargets)</span><span class="sxs-lookup"><span data-stu-id="3ef75-603">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="3ef75-604">Paraméterek lettek hozzáadva a Set-AzOperationalInsightsWorkspace és New-AzOperationalInsightsWorkspace parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-604">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="3ef75-605">Parancsmagok lettek létrehozva a társított tárfiókhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-605">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="3ef75-606">Parancsmagok lettek létrehozva a fürtökhöz és a társított szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-606">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3ef75-607">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-607">Az.RecoveryServices</span></span>
* <span data-ttu-id="3ef75-608">Hozzá lett adva az Azure Site Recovery-támogatás a közelségi elhelyezési csoportokban lévő virtuális gépek védelme érdekében, az Azure–Azure szolgáltatók esetében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-608">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="3ef75-609">Hozzá lett adva az Azure Site Recovery-támogatás a zónák közötti replikáció esetében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-609">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="3ef75-610">Az Azure Backup már támogatja a hosszú távú megőrzést az Azure FileShare helyreállítási pontok esetében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-610">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="3ef75-611">Hozzá lettek adva az Azure Backup lemezkizárási tulajdonságok a Get-AzRecoveryServicesBackupItem parancsmag kimenetéhez.</span><span class="sxs-lookup"><span data-stu-id="3ef75-611">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="3ef75-612">Hozzá lett adva a privát végpont a Vault hitelesítési fájljaihoz a Site Recovery szolgáltatás esetében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-612">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3ef75-613">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-613">Az.Resources</span></span>
* <span data-ttu-id="3ef75-614">Hozzá lett adva a megtekintés késéséről figyelmeztető üzenet az új szerepkör-definíció létrehozása során</span><span class="sxs-lookup"><span data-stu-id="3ef75-614">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="3ef75-615">Módosítva lettek a szabályzat-parancsmagok a szigorú típusmegadású objektumok megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-615">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="3ef75-616">El lett távolítva a Get-AzResourceLock parancsmaghoz használt -TenantLevel paraméter [#11335]</span><span class="sxs-lookup"><span data-stu-id="3ef75-616">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="3ef75-617">Javítva a Remove-AzResourceGroup -Id ResourceId parancsmag [#9882]</span><span class="sxs-lookup"><span data-stu-id="3ef75-617">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="3ef75-618">Hozzá lett adva egy új parancsmag az ARM-sablon What-If típusú eredményeinek lekéréséhez az erőforráscsoport hatókörében: Get-AzDeploymentResourceGroupWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="3ef75-618">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="3ef75-619">Hozzá lett adva egy új parancsmag az ARM-sablonok What-If típusú eredményeinek lekéréséhez az előfizetés hatókörében: Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="3ef75-619">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="3ef75-620">Alias: Get-AzSubscriptionDeploymentWhatIf</span><span class="sxs-lookup"><span data-stu-id="3ef75-620">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="3ef75-621">A -WhatIf és a -Confirm paraméter felül lett írva a New-AzDeployment és a New-AzResourceGroupDeployment parancsmagok esetében az ARM-sablon What-If típusú eredményeinek használata érdekében</span><span class="sxs-lookup"><span data-stu-id="3ef75-621">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="3ef75-622">Hozzá lett adva az elavulási üzenet az ApiVersion paraméterhez az üzembehelyezési parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="3ef75-622">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="3ef75-623">Hozzá lett adva egy képesség, amely lehetővé teszi, hogy fejlettebb hibaüzenetek jelenjenek meg az üzembehelyezési hibák esetén</span><span class="sxs-lookup"><span data-stu-id="3ef75-623">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="3ef75-624">Hozzá lett adva a correlationId-naplózása az üzembehelyezési hibák esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-624">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="3ef75-625">Hozzá lett adva az error tulajdonság az üzembehelyezési szkript kimenetéhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-625">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="3ef75-626">A Microsoft.Azure.Management.ResourceManager NuGet frissítve lett a 3.7.1-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="3ef75-626">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="3ef75-627">El lettek távolítva adott tesztesetek, mivel a DeploymentValidateResult Error tulajdonsága csak olvasható állapotúra változott a NuGet 3.7.1-preview verziójától kezdődően</span><span class="sxs-lookup"><span data-stu-id="3ef75-627">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="3ef75-628">A GenericResourceExpanded át lett hozva a ResourceManager SDK 3.7.1-preview verziójából</span><span class="sxs-lookup"><span data-stu-id="3ef75-628">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="3ef75-629">Hozzá lett adva a címketámogatás az összes, üzembe helyezéshez használt Get parancsmaghoz, valamint a következőkhöz:</span><span class="sxs-lookup"><span data-stu-id="3ef75-629">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="3ef75-630">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="3ef75-630">'New-AzDeployment'</span></span>
    - <span data-ttu-id="3ef75-631">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3ef75-631">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="3ef75-632">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3ef75-632">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="3ef75-633">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="3ef75-633">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3ef75-634">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3ef75-634">Az.ServiceFabric</span></span>
* <span data-ttu-id="3ef75-635">Javítva a hiba, amely hibás tanúsítvány-ujjlenyomatot kért le a tanúsítvány --SecretIdentifier használatával történő hozzáadásakor</span><span class="sxs-lookup"><span data-stu-id="3ef75-635">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="3ef75-636">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-636">Az.Sql</span></span>
* <span data-ttu-id="3ef75-637">Javult a következők teljesítménye:</span><span class="sxs-lookup"><span data-stu-id="3ef75-637">Enhance performance of:</span></span>
    - <span data-ttu-id="3ef75-638">Set-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="3ef75-638">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="3ef75-639">Set-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="3ef75-639">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="3ef75-640">Remove-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="3ef75-640">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="3ef75-641">Remove-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="3ef75-641">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="3ef75-642">Enable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="3ef75-642">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="3ef75-643">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="3ef75-643">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="3ef75-644">Disable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="3ef75-644">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="3ef75-645">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="3ef75-645">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="3ef75-646">El lett távolítva a RetentionDays paraméter ügyféloldali érvényesítése a Set-AzSqlDatabaseBackupShortTermRetentionPolicy parancsmagból</span><span class="sxs-lookup"><span data-stu-id="3ef75-646">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="3ef75-647">A Vnet-ben található tárfiók naplózása, javítva a Storage Blob-adatok közreműködői szerepkörének létrehozásakor fellépő hiba.</span><span class="sxs-lookup"><span data-stu-id="3ef75-647">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3ef75-648">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3ef75-648">Az.Storage</span></span>
* <span data-ttu-id="3ef75-649">Hozzá lett adva az -AsJob a fiók Get-AzStorageAccount parancsmagjának lekéréséhez vagy listázásához</span><span class="sxs-lookup"><span data-stu-id="3ef75-649">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="3ef75-650">A KeyVersion választható lett a Storage-fiók KeyvaultEncryption használatával történő frissítésekor a kulcs automatikus rotálásának támogatásához</span><span class="sxs-lookup"><span data-stu-id="3ef75-650">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="3ef75-651">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3ef75-651">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="3ef75-652">Javítva a hiba, amely során az Azure File Directory eltávolítása egy folyamattal meghiúsult</span><span class="sxs-lookup"><span data-stu-id="3ef75-652">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="3ef75-653">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="3ef75-653">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="3ef75-654">[#9880] javítva: Módosítva lett a NetWorkRule DefaultAction értékdefiníciója, hogy megfeleljen a Swaggernek.</span><span class="sxs-lookup"><span data-stu-id="3ef75-654">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="3ef75-655">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="3ef75-655">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="3ef75-656">Get-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="3ef75-656">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="3ef75-657">[#11624] javítva: Duplikált szabályok kihagyása NetworkRules hozzáadásakor a kiszolgáló meghibásodásának elkerülése érdekében</span><span class="sxs-lookup"><span data-stu-id="3ef75-657">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="3ef75-658">Add-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3ef75-658">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="3ef75-659">A Microsoft.Azure.Cosmos.Table SDK verziója 1.0.7-re frissült</span><span class="sxs-lookup"><span data-stu-id="3ef75-659">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="3ef75-660">Hozzá lett adva egy figyelmeztető üzenet, amely emlékezteti a felhasználót, hogy listázzon újra a ContinuationToken használatával, ha csak részleges elemeket ad vissza a rendszer a Data Lake Gen2 elemek listáján</span><span class="sxs-lookup"><span data-stu-id="3ef75-660">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="3ef75-661">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="3ef75-661">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="3ef75-662">Storage-fiók létrehozásának és frissítésének támogatása Azure Files Active Directory Domain Service-hitelesítéssel</span><span class="sxs-lookup"><span data-stu-id="3ef75-662">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="3ef75-663">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3ef75-663">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="3ef75-664">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3ef75-664">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="3ef75-665">Storage-fiók Kerberos-kulcsai listázásának vagy új Kerberos-kulcsok létrehozásának támogatása</span><span class="sxs-lookup"><span data-stu-id="3ef75-665">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="3ef75-666">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="3ef75-666">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="3ef75-667">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="3ef75-667">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="3ef75-668">Feladatátvételi Storage-fiók támogatása</span><span class="sxs-lookup"><span data-stu-id="3ef75-668">Supported failover Storage account</span></span>
    - <span data-ttu-id="3ef75-669">Invoke-AzStorageAccountFailover</span><span class="sxs-lookup"><span data-stu-id="3ef75-669">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="3ef75-670">Frissítve a Get-AzStorageBlobCopyState súgója</span><span class="sxs-lookup"><span data-stu-id="3ef75-670">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="3ef75-671">Frissítve a Get-AzStorageFileCopyState és a Start-AzStorageBlobCopy súgója</span><span class="sxs-lookup"><span data-stu-id="3ef75-671">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="3ef75-672">A Storage-ügyfélkódtár 12-es verziója integrálva lett a Queue és a File parancsmagokba</span><span class="sxs-lookup"><span data-stu-id="3ef75-672">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="3ef75-673">A kimenet típusa CloudFile helyett mostantól AzureStorageFile, az eredeti kimenet az új kimenet gyermektulajdonsága lesz</span><span class="sxs-lookup"><span data-stu-id="3ef75-673">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="3ef75-674">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="3ef75-674">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="3ef75-675">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="3ef75-675">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="3ef75-676">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3ef75-676">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="3ef75-677">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3ef75-677">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="3ef75-678">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="3ef75-678">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="3ef75-679">A kimenet típusa CloudFileDirectory helyett mostantól AzureStorageFileDirectory, az eredeti kimenet az új kimenet gyermektulajdonsága lesz</span><span class="sxs-lookup"><span data-stu-id="3ef75-679">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="3ef75-680">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="3ef75-680">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="3ef75-681">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="3ef75-681">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="3ef75-682">A kimenet típusa CloudFileShare helyett mostantól AzureStorageFileShare, az eredeti kimenet az új kimenet gyermektulajdonsága lesz</span><span class="sxs-lookup"><span data-stu-id="3ef75-682">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="3ef75-683">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="3ef75-683">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="3ef75-684">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="3ef75-684">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="3ef75-685">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="3ef75-685">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="3ef75-686">A kimenet típusa FileShareProperties helyett mostantól AzureStorageFileShare, az eredeti kimenet az új kimenet gyermek-altulajdonsága lesz</span><span class="sxs-lookup"><span data-stu-id="3ef75-686">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="3ef75-687">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="3ef75-687">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="3ef75-688">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="3ef75-688">Az.TrafficManager</span></span>
* <span data-ttu-id="3ef75-689">Javítva a hibás profilnév a DisableAzureTrafficManagerEndpoint részletes kimenetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-689">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3ef75-690">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3ef75-690">Az.Websites</span></span>
* <span data-ttu-id="3ef75-691">Javítva az elgépelés az Update-AzWebAppAccessRestrictionConfig súgójában.</span><span class="sxs-lookup"><span data-stu-id="3ef75-691">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="3ef75-692">3.8.0 – 2020. április</span><span class="sxs-lookup"><span data-stu-id="3ef75-692">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="3ef75-693">A legutóbbi kiadás óta bevezetett újdonságok</span><span class="sxs-lookup"><span data-stu-id="3ef75-693">Highlights since the last release</span></span>
* <span data-ttu-id="3ef75-694">Az Az.Storage által támogatott PowerShell-verziók: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="3ef75-694">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3ef75-695">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3ef75-695">Az.Accounts</span></span>
* <span data-ttu-id="3ef75-696">Frissítve lett az Azure PowerShell-felmérés URL-címe a következő helyen: Resolve-AzError [#11507]</span><span class="sxs-lookup"><span data-stu-id="3ef75-696">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="3ef75-697">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3ef75-697">Az.ApiManagement</span></span>
* <span data-ttu-id="3ef75-698">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó értesítés az Azure File parancsmagok kimenetére vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="3ef75-698">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="3ef75-699">Set-AzApiManagementGroup – Frissítve lett a dokumentáció a GroupId paraméter meghatározása érdekében</span><span class="sxs-lookup"><span data-stu-id="3ef75-699">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="3ef75-700">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3ef75-700">Az.Cdn</span></span>
* <span data-ttu-id="3ef75-701">Ki lett javítva a díjszabási termékváltozat megjelenítése a ChinaCDN kapcsán</span><span class="sxs-lookup"><span data-stu-id="3ef75-701">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3ef75-702">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-702">Az.CognitiveServices</span></span>
* <span data-ttu-id="3ef75-703">Támogatott identitás, Titkosítás, UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="3ef75-703">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3ef75-704">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-704">Az.Compute</span></span>
* <span data-ttu-id="3ef75-705">Hozzá lett adva a Set-AzVmssOrchestrationServiceState parancsmag.</span><span class="sxs-lookup"><span data-stu-id="3ef75-705">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="3ef75-706">A Get-AzVmss az InstanceView használatával az OrchestrationService állapotait mutatja.</span><span class="sxs-lookup"><span data-stu-id="3ef75-706">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3ef75-707">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3ef75-707">Az.IotHub</span></span>
* <span data-ttu-id="3ef75-708">Az IoT-ikereszköz konfigurációjának kezelése, Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="3ef75-708">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="3ef75-709">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="3ef75-709">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="3ef75-710">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="3ef75-710">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="3ef75-711">Hozzá lett adva egy parancsmag a közvetlen metódusok az IoT Hubban lévő eszközökön való meghívásához.</span><span class="sxs-lookup"><span data-stu-id="3ef75-711">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="3ef75-712">Az IoT-ikereszköz modulja konfigurációjának kezelése, Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="3ef75-712">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="3ef75-713">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="3ef75-713">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="3ef75-714">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="3ef75-714">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="3ef75-715">Nagy méretekben történő automatikus IoT-eszközfelügyelet konfigurációjának kezelése.</span><span class="sxs-lookup"><span data-stu-id="3ef75-715">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="3ef75-716">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="3ef75-716">New cmdlets are:</span></span>
    - <span data-ttu-id="3ef75-717">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ef75-717">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="3ef75-718">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ef75-718">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="3ef75-719">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ef75-719">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="3ef75-720">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ef75-720">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="3ef75-721">Hozzá lett adva egy parancsmag az Edge-modul metódusok az IoT Hubban való meghívásához.</span><span class="sxs-lookup"><span data-stu-id="3ef75-721">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3ef75-722">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3ef75-722">Az.KeyVault</span></span>
* <span data-ttu-id="3ef75-723">Hozzá lett adva egy új Update-AzKeyVault parancsmag a helyreállító törlés és végleges törlés elleni védelem tárolón való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-723">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="3ef75-724">Támogatás a következőhöz: Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="3ef75-724">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="3ef75-725">Ki lettek javítva a Remove-AzKeyVaultManagedStorageSasDefinition [#11479] példáinak hibái</span><span class="sxs-lookup"><span data-stu-id="3ef75-725">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="3ef75-726">Támogatás a privát végponthoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-726">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="3ef75-727">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="3ef75-727">Az.Maintenance</span></span>
* <span data-ttu-id="3ef75-728">Karbantartási parancsmagok végleges verziójának közzététele az általánosan elérhető kiadás számára</span><span class="sxs-lookup"><span data-stu-id="3ef75-728">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3ef75-729">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3ef75-729">Az.Monitor</span></span>
* <span data-ttu-id="3ef75-730">Parancsmagok hozzáadva a privát kapcsolat hatóköréhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-730">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="3ef75-731">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="3ef75-731">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="3ef75-732">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="3ef75-732">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="3ef75-733">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="3ef75-733">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="3ef75-734">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="3ef75-734">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="3ef75-735">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="3ef75-735">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="3ef75-736">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="3ef75-736">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="3ef75-737">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="3ef75-737">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3ef75-738">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-738">Az.Network</span></span>
* <span data-ttu-id="3ef75-739">Frissítve lettek a parancsmagok a virtuális hálózati átjáróhoz való csatlakozás engedélyezéséhez magánhálózati IP-cím esetében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-739">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="3ef75-740">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3ef75-740">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="3ef75-741">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3ef75-741">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="3ef75-742">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3ef75-742">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="3ef75-743">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3ef75-743">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="3ef75-744">Frissítve lettek a parancsmagok az FQDN-alapú LocalNetworkGateways és VpnSites engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-744">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="3ef75-745">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3ef75-745">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="3ef75-746">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="3ef75-746">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="3ef75-747">Az IPv6-címcsalád támogatása a következőben: ExpressRouteCircuitConnectionConfig (Global Reach)</span><span class="sxs-lookup"><span data-stu-id="3ef75-747">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="3ef75-748">Hozzá lett adva a Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="3ef75-748">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="3ef75-749">lehetővé teszi az összes meglévő tulajdonság beállítását, beleértve a következőt is: IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="3ef75-749">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="3ef75-750">Frissítve lett az Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="3ef75-750">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="3ef75-751">Hozzá lett adva egy másik opcionális AddressPrefixType paraméter a címelőtag címcsaládjának meghatározásához</span><span class="sxs-lookup"><span data-stu-id="3ef75-751">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="3ef75-752">Frissítve lettek a parancsmagok a DPD-időtúllépés beállításának engedélyezéséhez a virtuális hálózati átjáró kapcsolatain.</span><span class="sxs-lookup"><span data-stu-id="3ef75-752">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="3ef75-753">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3ef75-753">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="3ef75-754">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3ef75-754">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3ef75-755">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3ef75-755">Az.PolicyInsights</span></span>
* <span data-ttu-id="3ef75-756">Hozzá lett adva a Start-AzPolicyComplianceScan parancsmag a szabályzatok megfelelőségi vizsgálatának elindításához</span><span class="sxs-lookup"><span data-stu-id="3ef75-756">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="3ef75-757">Szabályzatdefiníció, készletdefiníció és hozzárendelési verziók hozzáadva a Get-AzPolicyState kimenetéhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-757">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3ef75-758">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3ef75-758">Az.ServiceFabric</span></span>
* <span data-ttu-id="3ef75-759">Tovább lett fejlesztve a kódok formázása és a használhatóság a New-AzServiceFabricCluster példái esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-759">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="3ef75-760">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-760">Az.Sql</span></span>
* <span data-ttu-id="3ef75-761">Hozzá lettek adva a Get-AzSqlInstanceOperation és a Stop-AzSqlInstanceOperation parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3ef75-761">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="3ef75-762">Naplózás támogatása egy VNet-ben található tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="3ef75-762">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3ef75-763">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3ef75-763">Az.Storage</span></span>
* <span data-ttu-id="3ef75-764">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó értesítés az Azure File parancsmagok kimenetére vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="3ef75-764">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="3ef75-765">Támogatott új SkuName StandardGZRS, StandardRAGZRS a Storage-fiók létrehozása/frissítése során</span><span class="sxs-lookup"><span data-stu-id="3ef75-765">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="3ef75-766">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3ef75-766">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="3ef75-767">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3ef75-767">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="3ef75-768">Támogatott Data Lake Gen2</span><span class="sxs-lookup"><span data-stu-id="3ef75-768">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="3ef75-769">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="3ef75-769">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="3ef75-770">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="3ef75-770">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="3ef75-771">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="3ef75-771">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="3ef75-772">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="3ef75-772">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="3ef75-773">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="3ef75-773">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="3ef75-774">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="3ef75-774">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="3ef75-775">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="3ef75-775">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="3ef75-776">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="3ef75-776">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="3ef75-777">0.10.0-s előzetes verzió – 2020. április</span><span class="sxs-lookup"><span data-stu-id="3ef75-777">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="3ef75-778">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="3ef75-778">General</span></span>
* <span data-ttu-id="3ef75-779">Az Az modulok előzetes verziója mostantól elérhető az Azure Stack Hubon.</span><span class="sxs-lookup"><span data-stu-id="3ef75-779">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="3ef75-780">Ez lehetővé teszi a platformok közötti kompatibilitást a Linux és a macOs rendszerekkel.</span><span class="sxs-lookup"><span data-stu-id="3ef75-780">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="3ef75-781">A Azure Stack Hub mostantól támogatja a PowerShell Core-t az Az modulokkal, további információt [itt](https://aka.ms/az4AzureStack) talál</span><span class="sxs-lookup"><span data-stu-id="3ef75-781">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="3ef75-782">Az Az modulok támogatják a 2019-03-01-hybrid profilt:</span><span class="sxs-lookup"><span data-stu-id="3ef75-782">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="3ef75-783">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="3ef75-783">Az.Billing</span></span>
  - <span data-ttu-id="3ef75-784">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-784">Az.Compute</span></span>
  - <span data-ttu-id="3ef75-785">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="3ef75-785">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="3ef75-786">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3ef75-786">Az.EventHub</span></span>
  - <span data-ttu-id="3ef75-787">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3ef75-787">Az.IotHub</span></span>
  - <span data-ttu-id="3ef75-788">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3ef75-788">Az.KeyVault</span></span>
  - <span data-ttu-id="3ef75-789">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3ef75-789">Az.Monitor</span></span>
  - <span data-ttu-id="3ef75-790">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-790">Az.Network</span></span>
  - <span data-ttu-id="3ef75-791">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-791">Az.Resources</span></span>
  - <span data-ttu-id="3ef75-792">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3ef75-792">Az.Storage</span></span>
  - <span data-ttu-id="3ef75-793">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3ef75-793">Az.Websites</span></span>
* <span data-ttu-id="3ef75-794">A következő három új PowerShell-modul lett bevezetve, amelyek használhatók az Azure Stack Hubbal: Az.Databox, Az.IotHub és Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3ef75-794">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="3ef75-795">A parancsok viszonylag változatlanok maradnak, kisebb módosításokkal. Például az Az helyébe az AzureRM lép.</span><span class="sxs-lookup"><span data-stu-id="3ef75-795">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="3ef75-796">Az Azure Stack Hubhoz kapcsolódó PowerShell-dokumentáció frissített hivatkozását [itt](https://aka.ms/InstallASHPowerShell) találja</span><span class="sxs-lookup"><span data-stu-id="3ef75-796">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="3ef75-797">3.7.0 – 2020. március</span><span class="sxs-lookup"><span data-stu-id="3ef75-797">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3ef75-798">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3ef75-798">Az.Accounts</span></span>
* <span data-ttu-id="3ef75-799">Ki lett javítva az a hiba, hogy a Get-AzTenant/Get-AzDefault/Set-AzDefault parancs NullReferenceException hibát ad vissza kijelentkezett állapotban [#10292]</span><span class="sxs-lookup"><span data-stu-id="3ef75-799">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3ef75-800">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-800">Az.Compute</span></span>
* <span data-ttu-id="3ef75-801">A következő paraméterek lettek hozzáadva a New-AzDiskConfig parancsmaghoz:</span><span class="sxs-lookup"><span data-stu-id="3ef75-801">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="3ef75-802">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="3ef75-802">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="3ef75-803">Engedélyezve lett a New-AzGalleryImageVersion parancsmag célparaméterének titkosítási tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="3ef75-803">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="3ef75-804">Ki lett javítva a tempDisk hibája a Set-AzVmss -Reimage és az Invoke-AzVMReimage parancsmag esetében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-804">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="3ef75-805">[#11354]</span><span class="sxs-lookup"><span data-stu-id="3ef75-805">[#11354]</span></span>
* <span data-ttu-id="3ef75-806">Az alábbi parancsmagok mostantól támogatottak az új SAP-bővítmény esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-806">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="3ef75-807">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="3ef75-807">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="3ef75-808">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="3ef75-808">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="3ef75-809">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="3ef75-809">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="3ef75-810">Update-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="3ef75-810">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="3ef75-811">Ki lettek javítva a súgódokumentáció példáinak hibái</span><span class="sxs-lookup"><span data-stu-id="3ef75-811">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="3ef75-812">Táblázatos formátumban jelenítette meg a sztring pontos értékét a PowerState virtuális gép esetében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-812">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="3ef75-813">New-AzVmssConfig: ki lett javítva az AutomaticRepairs tulajdonság szerializálása a SinglePlacementGroup letiltott állapota esetén.</span><span class="sxs-lookup"><span data-stu-id="3ef75-813">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="3ef75-814">[#11257]</span><span class="sxs-lookup"><span data-stu-id="3ef75-814">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3ef75-815">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3ef75-815">Az.DataFactory</span></span>
* <span data-ttu-id="3ef75-816">Az ADF .Net SDK a 4.8.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="3ef75-816">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="3ef75-817">Opcionális paraméterek lettek hozzáadva az Invoke-AzDataFactoryV2Pipeline parancshoz az újrafuttatás támogatásához</span><span class="sxs-lookup"><span data-stu-id="3ef75-817">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3ef75-818">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3ef75-818">Az.DataLakeStore</span></span>
* <span data-ttu-id="3ef75-819">Hozzá lett adva a kompatibilitástörő változás leírása az Export-AzDataLakeStoreItem és az Import-AzDataLakeStoreItem parancsok esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-819">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="3ef75-820">A bájtkódolási lehetőség hozzá lett adva a New-AzDataLakeStoreItem, az Add-AzDAtaLakeStoreItemContent és a Get-AzDAtaLakeStoreItemContent parancsok esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-820">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="3ef75-821">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3ef75-821">Az.HDInsight</span></span>
* <span data-ttu-id="3ef75-822">Fürt létrehozásakor a minimálisan támogatott TLS-verzió megadása támogatott.</span><span class="sxs-lookup"><span data-stu-id="3ef75-822">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3ef75-823">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3ef75-823">Az.IotHub</span></span>
* <span data-ttu-id="3ef75-824">Hozzá lett adva az elosztott beállítások eszközönkénti felügyeletének támogatása.</span><span class="sxs-lookup"><span data-stu-id="3ef75-824">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="3ef75-825">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="3ef75-825">New Cmdlets are:</span></span>
    - <span data-ttu-id="3ef75-826">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="3ef75-826">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="3ef75-827">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="3ef75-827">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3ef75-828">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3ef75-828">Az.KeyVault</span></span>
* <span data-ttu-id="3ef75-829">Kompatibilitástörő változást okozó attribútumok lettek hozzáadva a New-AzKeyVault parancshoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-829">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3ef75-830">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3ef75-830">Az.Monitor</span></span>
* <span data-ttu-id="3ef75-831">Frissült a New-AzScheduledQueryRuleLogMetricTrigger dokumentációja</span><span class="sxs-lookup"><span data-stu-id="3ef75-831">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3ef75-832">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-832">Az.Network</span></span>
* <span data-ttu-id="3ef75-833">Frissültek a parancsmagok a több-bérlős VirtualHubVnetConnections engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-833">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="3ef75-834">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="3ef75-834">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="3ef75-835">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="3ef75-835">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="3ef75-836">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3ef75-836">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="3ef75-837">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3ef75-837">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="3ef75-838">Az SQL Management SDK-függőség el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="3ef75-838">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3ef75-839">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3ef75-839">Az.PolicyInsights</span></span>
* <span data-ttu-id="3ef75-840">Továbbfejlesztett hibaüzenetek</span><span class="sxs-lookup"><span data-stu-id="3ef75-840">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3ef75-841">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-841">Az.RecoveryServices</span></span>
* <span data-ttu-id="3ef75-842">Hozzá lett adva az Azure Site Recovery-támogatás az Azure Diskkel titkosított virtuális gépek védelmének újbóli beállítása és frissített virtuálisgép-tulajdonságai esetében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-842">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="3ef75-843">Hozzá lett adva az Azure Site Recovery VmwareToAzure tulajdonságainak vészhelyreállítási monitorozása</span><span class="sxs-lookup"><span data-stu-id="3ef75-843">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="3ef75-844">Hozzá lett adva az Azure Backup-támogatás a sikertelen elemekre vonatkozó szabályzatfrissítés újbóli végrehajtása esetében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-844">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="3ef75-845">Hozzá lett adva az Azure Backup-támogatás a lemezkizárási beállításokhoz a biztonsági mentés és a visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="3ef75-845">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="3ef75-846">Hozzá lett adva az Azure Backup-támogatás több fájl/mappa visszaállításához az AzureFileShare-ben</span><span class="sxs-lookup"><span data-stu-id="3ef75-846">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="3ef75-847">Hozzá lett adva az Azure Backup-támogatás a felhasználó által megadott erőforráscsoport támogatásához az IaasVM-szabályzat frissítésekor</span><span class="sxs-lookup"><span data-stu-id="3ef75-847">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="3ef75-848">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-848">Az.Resources</span></span>
* <span data-ttu-id="3ef75-849">Ki lett javítva a Get-AzResource-ResourceGroupName-Name-ExpandProperties-ResourceType parancs, hogy ezentúl az erőforrások aktuális API-verzióját használja az alapértelmezett verzió helyett [#11267]</span><span class="sxs-lookup"><span data-stu-id="3ef75-849">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="3ef75-850">Hozzá lett adva a CorrelationId-naplózás a hibaforgatókönyvek esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-850">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="3ef75-851">A Get-AzResourceLock dokumentációjában kisebb módosítás történt.</span><span class="sxs-lookup"><span data-stu-id="3ef75-851">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="3ef75-852">Példa hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-852">Added example.</span></span>
* <span data-ttu-id="3ef75-853">A szimpla idézőjel fel lett oldva a Get-AzADUser paraméterértékében [#11317]</span><span class="sxs-lookup"><span data-stu-id="3ef75-853">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="3ef75-854">Új parancsmagok lettek hozzáadva az üzembehelyezési szkriptekhez (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript)</span><span class="sxs-lookup"><span data-stu-id="3ef75-854">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="3ef75-855">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-855">Az.Sql</span></span>
* <span data-ttu-id="3ef75-856">Olvasható másodlagos paraméter lett hozzáadva az Invoke-AzSqlDatabaseFailover parancshoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-856">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="3ef75-857">A Disable-AzSqlServerActiveDirectoryOnlyAuthentication parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="3ef75-857">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="3ef75-858">Az érzékenységi besorolás mentése megtörténik az adatbázis oszlopainak osztályozásakor.</span><span class="sxs-lookup"><span data-stu-id="3ef75-858">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="3ef75-859">Az.Support</span><span class="sxs-lookup"><span data-stu-id="3ef75-859">Az.Support</span></span>
* <span data-ttu-id="3ef75-860">Az Az.Support modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="3ef75-860">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3ef75-861">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3ef75-861">Az.Websites</span></span>
* <span data-ttu-id="3ef75-862">Mostantól támogatott a webalkalmazások forgalom-útválasztási szabályainak az alábbi új parancsmagokkal történő használata</span><span class="sxs-lookup"><span data-stu-id="3ef75-862">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="3ef75-863">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="3ef75-863">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="3ef75-864">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="3ef75-864">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="3ef75-865">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="3ef75-865">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="3ef75-866">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="3ef75-866">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="3ef75-867">3.6.1 – 2020. március</span><span class="sxs-lookup"><span data-stu-id="3ef75-867">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3ef75-868">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3ef75-868">Az.Accounts</span></span>
* <span data-ttu-id="3ef75-869">Azure PowerShell felmérési oldal megnyitása itt: Send-Feedback [#11020]</span><span class="sxs-lookup"><span data-stu-id="3ef75-869">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="3ef75-870">Azure PowerShell-felmérés URL-címének megjelenítése itt: Resolve-Error [#11021]</span><span class="sxs-lookup"><span data-stu-id="3ef75-870">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="3ef75-871">Az-verzió hozzáadva az UserAgenthez</span><span class="sxs-lookup"><span data-stu-id="3ef75-871">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="3ef75-872">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3ef75-872">Az.ApiManagement</span></span>
* <span data-ttu-id="3ef75-873">Mostantól támogatott az egyéni tartomány lekérése és konfigurálása a DeveloperPortal végpontján [#11007]</span><span class="sxs-lookup"><span data-stu-id="3ef75-873">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="3ef75-874">Export-AzApiManagementAPi – Mostantól támogatott az Api-definíció Json formátumban való letöltése [#9987]</span><span class="sxs-lookup"><span data-stu-id="3ef75-874">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="3ef75-875">Import-AzApiManagementApi – Az OpenAPI 3.0-definíció Json-dokumentumokból való importálása mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="3ef75-875">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="3ef75-876">New-AzApiManagementIdentityProvider és Set-AzApiManagementIdentityProvider – A Signin Tenant konfigurálása az AAD B2C-szolgáltató esetében mostantól támogatott. [#9784]</span><span class="sxs-lookup"><span data-stu-id="3ef75-876">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3ef75-877">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3ef75-877">Az.DataLakeStore</span></span>
* <span data-ttu-id="3ef75-878">A System.Buffershez hivatkozásának explicit hozzáadása a következőkben: csproj és psd1</span><span class="sxs-lookup"><span data-stu-id="3ef75-878">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3ef75-879">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3ef75-879">Az.IotHub</span></span>
* <span data-ttu-id="3ef75-880">Az eszközök az IoT Hubban való kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="3ef75-880">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="3ef75-881">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="3ef75-881">New Cmdlets are:</span></span>
    - <span data-ttu-id="3ef75-882">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="3ef75-882">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="3ef75-883">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="3ef75-883">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="3ef75-884">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="3ef75-884">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="3ef75-885">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="3ef75-885">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="3ef75-886">A cél IoT-eszközökön lévő modulok IoT Hubban való kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="3ef75-886">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="3ef75-887">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="3ef75-887">New Cmdlets are:</span></span>
    - <span data-ttu-id="3ef75-888">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="3ef75-888">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="3ef75-889">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="3ef75-889">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="3ef75-890">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="3ef75-890">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="3ef75-891">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="3ef75-891">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="3ef75-892">Parancsmag hozzáadva egy IoT Hubban lévő cél IoT-eszköz kapcsolati sztringjének lekéréséhez.</span><span class="sxs-lookup"><span data-stu-id="3ef75-892">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="3ef75-893">Parancsmag hozzáadva egy IoT Hubban lévő cél IoT-eszköz modulja kapcsolati sztringjének lekéréséhez.</span><span class="sxs-lookup"><span data-stu-id="3ef75-893">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="3ef75-894">Az IoT-eszközök szülő eszközének lekérése/beállítása mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="3ef75-894">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="3ef75-895">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="3ef75-895">New Cmdlets are:</span></span>
    - <span data-ttu-id="3ef75-896">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="3ef75-896">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="3ef75-897">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="3ef75-897">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="3ef75-898">Az eszközök szülő-gyermek kapcsolatainak kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="3ef75-898">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3ef75-899">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3ef75-899">Az.Monitor</span></span>
* <span data-ttu-id="3ef75-900">A Get-AzMetricDefinition kimeneti értéke javítva [#9714]</span><span class="sxs-lookup"><span data-stu-id="3ef75-900">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3ef75-901">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-901">Az.Network</span></span>
* <span data-ttu-id="3ef75-902">SQL Management SDK frissítve.</span><span class="sxs-lookup"><span data-stu-id="3ef75-902">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="3ef75-903">Kijavítottuk a PrivateLinkServiceConnectionState osztály eltérő elnevezéssel kapcsolatos hibáját.</span><span class="sxs-lookup"><span data-stu-id="3ef75-903">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="3ef75-904">Az ActionsRequired mező leképezése a követezőre: ActionRequired</span><span class="sxs-lookup"><span data-stu-id="3ef75-904">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="3ef75-905">PublicNetworkAccess hozzáadva a következőhöz: New-AzSqlServer és Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="3ef75-905">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="3ef75-906">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-906">Az.Resources</span></span>
* <span data-ttu-id="3ef75-907">A Get-AzRoleAssignment null értékű hivatkozásra vonatkozó hibája javítva</span><span class="sxs-lookup"><span data-stu-id="3ef75-907">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="3ef75-908">A -Force és a -PassThru kapcsoló nem kötelezőként lett megjelölve a Remove-AzADGroup esetében [#10849]</span><span class="sxs-lookup"><span data-stu-id="3ef75-908">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="3ef75-909">Javítva a hiba, amely miatt a MailNickname nem lett visszaadva Remove-AzADGroup esetében [#11167]</span><span class="sxs-lookup"><span data-stu-id="3ef75-909">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="3ef75-910">A Remove-AzADGroup folyamatművelet működési hibája kijavítva [#11171]</span><span class="sxs-lookup"><span data-stu-id="3ef75-910">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="3ef75-911">A GetAzureRoleAssignmentCommand null értékű hivatkozásra vonatkozó hibája javítva</span><span class="sxs-lookup"><span data-stu-id="3ef75-911">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="3ef75-912">Kompatibilitástörő változás hozzáadva a szabályzati parancsmagok soron következő változásaihoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-912">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="3ef75-913">Frissült a Get-AzResourceGroup az erőforráscsoport-címke kiszolgálóoldali szűrésének elvégzéséhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-913">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="3ef75-914">A címkeparancsmagok kiterjesztése a -ResourceID elfogadása érdekében</span><span class="sxs-lookup"><span data-stu-id="3ef75-914">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="3ef75-915">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ef75-915">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="3ef75-916">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ef75-916">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="3ef75-917">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ef75-917">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="3ef75-918">Új címkeparancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-918">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="3ef75-919">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ef75-919">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="3ef75-920">A ScopedDeployment áthozva az SDK 3.3.0-ból</span><span class="sxs-lookup"><span data-stu-id="3ef75-920">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="3ef75-921">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-921">Az.Sql</span></span>
* <span data-ttu-id="3ef75-922">PublicNetworkAccess hozzáadva a következőhöz: New-AzSqlServer és Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="3ef75-922">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="3ef75-923">Támogatás hozzáadva a biztonsági másolatok hosszú távú megőrzési konfigurációjához a felügyelt adatbázisok esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-923">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="3ef75-924">LTR-szabályzat lekérése/beállítása felügyelt adatbázison</span><span class="sxs-lookup"><span data-stu-id="3ef75-924">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="3ef75-925">LTR biztonsági másolat(ok) lekérése felügyelt adatbázis, felügyelt példány vagy hely szerint</span><span class="sxs-lookup"><span data-stu-id="3ef75-925">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="3ef75-926">LTR biztonsági másolat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-926">Remove an LTR backup</span></span>
    - <span data-ttu-id="3ef75-927">LTR biztonsági másolat visszaállítása új felügyelt adatbázis létrehozásához</span><span class="sxs-lookup"><span data-stu-id="3ef75-927">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="3ef75-928">MinimalTlsVersion hozzáadva a következőkhöz: New-AzSqlServer és Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="3ef75-928">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="3ef75-929">MinimalTlsVersion hozzáadva a következőkhöz: New-AzSqlInstance és Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3ef75-929">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="3ef75-930">Az SQL SDK-verzió felléptetése a következőhöz: AZ.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-930">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3ef75-931">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3ef75-931">Az.Storage</span></span>
* <span data-ttu-id="3ef75-932">Támogatott AllowProtectedAppendWrite a következőben: ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="3ef75-932">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="3ef75-933">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="3ef75-933">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="3ef75-934">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó figyelmeztető üzenet az AzureStorageTable típusának módosítására vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="3ef75-934">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="3ef75-935">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="3ef75-935">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="3ef75-936">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="3ef75-936">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3ef75-937">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3ef75-937">Az.Websites</span></span>
* <span data-ttu-id="3ef75-938">Címke paraméter hozzáadva a következőkhöz: New-AzAppServicePlan és Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3ef75-938">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="3ef75-939">A parancsmag végrehajtásának leállítása, ha egy egyéni tartomány webhelyhez történő hozzáadásakor a rendszer kivételt ad vissza</span><span class="sxs-lookup"><span data-stu-id="3ef75-939">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="3ef75-940">Támogatás hozzáadva az olyan App Services műveletek elvégzéséhez, amelyek nem abban az erőforráscsoportban vannak, amelyben az App Service-csomag</span><span class="sxs-lookup"><span data-stu-id="3ef75-940">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="3ef75-941">Hozzáférési korlátozás alkalmazva a különböző erőforráscsoportokban lévő webalkalmazásokra/függvényekre</span><span class="sxs-lookup"><span data-stu-id="3ef75-941">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="3ef75-942">Az egyéni WebAppSlots-gazdanevek beállítására vonatkozó hiba kijavítva</span><span class="sxs-lookup"><span data-stu-id="3ef75-942">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="3ef75-943">3.5.0 – 2020. február</span><span class="sxs-lookup"><span data-stu-id="3ef75-943">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="3ef75-944">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="3ef75-944">Highlights since the last major release</span></span>
* <span data-ttu-id="3ef75-945">Frissült az ügyféloldali telemetria.</span><span class="sxs-lookup"><span data-stu-id="3ef75-945">Updated client side telemetry.</span></span>
* <span data-ttu-id="3ef75-946">Az.IotHub: parancsmagok hozzáadva az eszközkezelés támogatásához.</span><span class="sxs-lookup"><span data-stu-id="3ef75-946">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="3ef75-947">Az.SqlVirtualMachine: parancsmagok hozzáadva a rendelkezésreállási csoport figyelőjéhez.</span><span class="sxs-lookup"><span data-stu-id="3ef75-947">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3ef75-948">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3ef75-948">Az.Accounts</span></span>
* <span data-ttu-id="3ef75-949">A SubscriptionId, a TenantId és a végrehajtási idő hozzáadva az ügyféloldali telemetria adataihoz.</span><span class="sxs-lookup"><span data-stu-id="3ef75-949">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3ef75-950">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3ef75-950">Az.Automation</span></span>
* <span data-ttu-id="3ef75-951">Ki lett javítva a „New-AzAutomationSoftwareUpdateConfiguration” referenciadokumentációjának 1. példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="3ef75-951">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3ef75-952">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-952">Az.CognitiveServices</span></span>
* <span data-ttu-id="3ef75-953">Az SDK a 7.0-ás verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="3ef75-953">Updated SDK to 7.0</span></span>
* <span data-ttu-id="3ef75-954">Tovább lett fejlesztve a hibaüzenet, amely akkor jelenik meg, ha a kiszolgáló üres törzset ad vissza válaszként</span><span class="sxs-lookup"><span data-stu-id="3ef75-954">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3ef75-955">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-955">Az.Compute</span></span>
* <span data-ttu-id="3ef75-956">A ProximityPlacementGroupId mostantól üres értékkel is rendelkezhet a frissítés során</span><span class="sxs-lookup"><span data-stu-id="3ef75-956">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="3ef75-957">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3ef75-957">Az.FrontDoor</span></span>
* <span data-ttu-id="3ef75-958">Új parancsmag hozzáadva a WAF-ban használható felügyelt szabálydefiníciók lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-958">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3ef75-959">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3ef75-959">Az.IotHub</span></span>
* <span data-ttu-id="3ef75-960">Az eszközök az IoT Hubban való kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="3ef75-960">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="3ef75-961">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="3ef75-961">New Cmdlets are:</span></span>
    - <span data-ttu-id="3ef75-962">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="3ef75-962">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="3ef75-963">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="3ef75-963">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="3ef75-964">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="3ef75-964">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="3ef75-965">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="3ef75-965">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3ef75-966">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3ef75-966">Az.KeyVault</span></span>
* <span data-ttu-id="3ef75-967">Ki lett javítva az Add-AzKeyVaultKey.md duplikált szövege</span><span class="sxs-lookup"><span data-stu-id="3ef75-967">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3ef75-968">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3ef75-968">Az.Monitor</span></span>
* <span data-ttu-id="3ef75-969">Ki lett javítva a Get-AzLog parancsmag leírása.</span><span class="sxs-lookup"><span data-stu-id="3ef75-969">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="3ef75-970">Egy új, ActionGroupId nevű paraméter lett hozzáadva a „New-AzMetricAlertRuleV2” parancshoz.</span><span class="sxs-lookup"><span data-stu-id="3ef75-970">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="3ef75-971">A felhasználó a következőket adhatja meg: ActionGroupId(string) vagy ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="3ef75-971">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3ef75-972">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-972">Az.Network</span></span>
* <span data-ttu-id="3ef75-973">Hozzá lett adva egy extra paramétermegjegyzés a „New-AzPrivateLinkService” parancsmag „-EnableProxyProtocol” paraméteréhez.</span><span class="sxs-lookup"><span data-stu-id="3ef75-973">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="3ef75-974">A Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és a Start-AzVirtualnetworkGatewayPacketCapture.md FilterData kapcsolójának példái ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-974">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="3ef75-975">Hozzá lett adva egy csomagrögzítési példa a Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és Start-AzVirtualnetworkGatewayPacketCapture.md minden belső és külső csomagjának rögzítéséhez.</span><span class="sxs-lookup"><span data-stu-id="3ef75-975">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="3ef75-976">Az Azure Firewall-szabályzat mostantól támogatott a Vnet-tűzfalakon</span><span class="sxs-lookup"><span data-stu-id="3ef75-976">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="3ef75-977">Nem lettek hozzáadva új parancsmagok.</span><span class="sxs-lookup"><span data-stu-id="3ef75-977">No new cmdlets are added.</span></span> <span data-ttu-id="3ef75-978">Enyhítve lettek a tűzfalszabályzat korlátozásai a Vnet-tűzfalak esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-978">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3ef75-979">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-979">Az.RecoveryServices</span></span>
* <span data-ttu-id="3ef75-980">A fájlokként történő visszaállítás mostantól támogatott az SQL-adatbázisok esetében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-980">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3ef75-981">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-981">Az.Resources</span></span>
* <span data-ttu-id="3ef75-982">Újra lettek tervezve a sablonalapú üzembehelyezési parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3ef75-982">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="3ef75-983">Új parancsmagok lettek hozzáadva a felügyeleti csoportban való üzembe helyezés kezeléséhez: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3ef75-983">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="3ef75-984">Új parancsmagok lettek hozzáadva a bérlői hatókörben való üzembe helyezés kezeléséhez: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="3ef75-984">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="3ef75-985">Az \*-AzDeployment parancsmagok kifejezetten az előfizetési hatókörben való működéshez lettek újratervezve</span><span class="sxs-lookup"><span data-stu-id="3ef75-985">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="3ef75-986">Az \*-AzSubscriptionDeployment aliasok lettek létrehozva az \*-AzDeployment parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-986">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="3ef75-987">Ki lett javítva az „Update-AzADApplication” nem beállított „AvailableToOtherTenants” paraméter esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-987">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="3ef75-988">Az ApplicationObjectWithoutCredentialParameterSet el lett távolítva az AmbiguousParameterSetException elkerülése érdekében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-988">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="3ef75-989">A súgófájlok újra létre lettek hozva</span><span class="sxs-lookup"><span data-stu-id="3ef75-989">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="3ef75-990">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-990">Az.Sql</span></span>
* <span data-ttu-id="3ef75-991">Az előfizetések közötti időponthoz kötött visszaállítás mostantól támogatott a felügyelt példányokon.</span><span class="sxs-lookup"><span data-stu-id="3ef75-991">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="3ef75-992">A már meglévő felügyelt SQL-példány hardvergenerációjának módosítása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="3ef75-992">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="3ef75-993">Ki lettek javítva az „Update-AzSqlServerVulnerabilityAssessmentSetting” súgópéldái: paraméter/tulajdonságkimenet – EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="3ef75-993">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="3ef75-994">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3ef75-994">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="3ef75-995">Parancsmagokat hozzáadva a rendelkezésreállási csoport figyelőjéhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-995">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="3ef75-996">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="3ef75-996">Az.StorageSync</span></span>
* <span data-ttu-id="3ef75-997">Frissültek az „Invoke-AzStorageSyncCompatibilityCheck” támogatott karakterkészletei.</span><span class="sxs-lookup"><span data-stu-id="3ef75-997">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="3ef75-998">3.4.0 – 2020. február</span><span class="sxs-lookup"><span data-stu-id="3ef75-998">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="3ef75-999">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="3ef75-999">Highlights since the last major release</span></span>
* <span data-ttu-id="3ef75-1000">Megjelent az Az.CosmosDB 0.1.0-s kezdeti verziója</span><span class="sxs-lookup"><span data-stu-id="3ef75-1000">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="3ef75-1001">Az.Network ConnectionMonitor V2 támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1001">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3ef75-1002">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3ef75-1002">Az.Accounts</span></span>
* <span data-ttu-id="3ef75-1003">A környezet automatikus mentésének letiltása, ha az AzureRmContext.json nem érhető el</span><span class="sxs-lookup"><span data-stu-id="3ef75-1003">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="3ef75-1004">Az Azure Powershell Common referenciájának frissítése 1.3.5-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="3ef75-1004">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="3ef75-1005">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3ef75-1005">Az.ApiManagement</span></span>
* <span data-ttu-id="3ef75-1006">**Get-AzApiManagementApiSchema** Az API-val társított Open-API séma kijavítása   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="3ef75-1006">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="3ef75-1007">**New-AzApiManagementProduct**\* és **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="3ef75-1007">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="3ef75-1008">https://github.com/Azure/azure-powershell/issues/10472 dokumentációja kijavítva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1008">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="3ef75-1009">**Set-AzApiManagementApi** A ServiceUrl parancsmaggal való frissítését bemutató példa hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1009">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3ef75-1010">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-1010">Az.Compute</span></span>
* <span data-ttu-id="3ef75-1011">A virtuális gép állapotának korlátozása 100 értékre, hogy ne legyen szabályozás, ha a Get-AzVM -Status a virtuális gép neve nélkül lett végrehajtva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1011">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="3ef75-1012">Update-AzDiskEncryptionSet parancsmagok hozzáadása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1012">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="3ef75-1013">Az EncryptionType és a DiskEncryptionSetId paraméterek hozzáadása a következő parancsmagokhoz:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1013">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="3ef75-1014">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="3ef75-1014">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="3ef75-1015">A ColocationStatus paraméter hozzáadva a Get-AzProximityPlacementGroup parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1015">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3ef75-1016">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3ef75-1016">Az.DataFactory</span></span>
* <span data-ttu-id="3ef75-1017">Az ADF .Net SDK frissítve lett a 4.7.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="3ef75-1017">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="3ef75-1018">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="3ef75-1018">Az.DeploymentManager</span></span>
* <span data-ttu-id="3ef75-1019">LIST műveletek hozzáadása az erőforrásokhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1019">Adds LIST operations for resources</span></span>
* <span data-ttu-id="3ef75-1020">Műveletek végrehajtásának lehetősége az állapotellenőrzés lépésein</span><span class="sxs-lookup"><span data-stu-id="3ef75-1020">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="3ef75-1021">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3ef75-1021">Az.HDInsight</span></span>
* <span data-ttu-id="3ef75-1022">A New-AzHDInsightCluster dokumentációs hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1022">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3ef75-1023">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3ef75-1023">Az.KeyVault</span></span>
* <span data-ttu-id="3ef75-1024">Name alias hozzáadása a VaultName attribútumhoz, hogy a Remove-AzureKeyVault konzisztens legyen a New-AzureKeyVault paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1024">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3ef75-1025">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-1025">Az.Network</span></span>
* <span data-ttu-id="3ef75-1026">Új példa hozzáadva a Set-AzNetworkWatcherConfigFlowLog.md fájlhoz a Traffic Analytics-letiltási forgatókönyv szemléltetésére.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1026">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="3ef75-1027">Felügyeleti IP-konfiguráció támogatás hozzáadva az Azure Firewallhoz – egy dedikált alhálózat és nyilvános IP-cím, amelyet a tűzfal a forgalom felügyeléséhez használni fog</span><span class="sxs-lookup"><span data-stu-id="3ef75-1027">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="3ef75-1028">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1028">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="3ef75-1029">Hozzá lett adva a (nem kötelező) -PublicIpAddress-ManagementPublicIpAddress paraméter, amely egy nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="3ef75-1029">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="3ef75-1030">Hozzá lett adva a SetManagementIpConfiguration metódus a tűzfalobjektumok esetében – nyilvános IP-cím-objektumokat fogad el bemeneti adatként – az alhálózat nevének AzureFirewallManagementSubnet értéknek kell lennie</span><span class="sxs-lookup"><span data-stu-id="3ef75-1030">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="3ef75-1031">A Get-AzNetworkSecurityGroup példái javítva, hogy hálózati biztonsági csoportok példáit tartalmazzák hálózati adapterek helyett.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1031">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="3ef75-1032">Javítottunk egy elírást a New-AzVpnSite parancsban, amely megakadályozta, hogy az erőforrásazonosító-kiegészítő kiegészítsen egy paramétert.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1032">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="3ef75-1033">Az Application Gateway szabály-újraírási műveletkészletének URL-konfigurálása mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1033">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="3ef75-1034">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1034">New cmdlets added:</span></span>
        - <span data-ttu-id="3ef75-1035">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ef75-1035">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="3ef75-1036">A parancsmagok frissültek a nem kötelező UrlConfiguration paraméterrel</span><span class="sxs-lookup"><span data-stu-id="3ef75-1036">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="3ef75-1037">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="3ef75-1037">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="3ef75-1038">A Network Watcher Connection Monitor 2-es verziójú erőforrások támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1038">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3ef75-1039">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3ef75-1039">Az.PolicyInsights</span></span>
* <span data-ttu-id="3ef75-1040">A javítandó erőforrások azonosítása előtti megfelelőségértékelés támogatása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1040">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="3ef75-1041">-ResourceDiscoverMode paraméter hozzáadása a Start-AzPolicyRemediation parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1041">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="3ef75-1042">A szabályzatok metaadat-erőforrásainak elérésére szolgáló Get-AzPolicyMetadata parancsmag hozzáadása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1042">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="3ef75-1043">A Get-AzPolicyState és a Get-AzPolicyStateSummary frissült a 2019-10-01 API-verzióhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1043">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3ef75-1044">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-1044">Az.RecoveryServices</span></span>
* <span data-ttu-id="3ef75-1045">Azure Site Recovery-támogatás a replikált lemezek eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1045">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="3ef75-1046">Hozzáadott Azure Backup-támogatás a helyreállítási tárak létrehozása közbeni címkehozzáadáshoz.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1046">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3ef75-1047">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-1047">Az.Resources</span></span>
* <span data-ttu-id="3ef75-1048">A -Scope választható a \*-AzPolicyAssignment parancsmagokban; az alapértelmezett érték a környezeti előfizetés</span><span class="sxs-lookup"><span data-stu-id="3ef75-1048">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="3ef75-1049">Az ADServicePrincipal jelszó és kulcs típusú hitelesítő adatokkal való létrehozását szemléltető példák hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1049">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="3ef75-1050">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-1050">Az.Sql</span></span>
<span data-ttu-id="3ef75-1051">A New-AzSqlDatabaseSecondary parancsmag javítva, hogy a PartnerDatabaseName létezését ellenőrizze a DatabaseName létezése helyett.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1051">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3ef75-1052">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3ef75-1052">Az.Storage</span></span>
* <span data-ttu-id="3ef75-1053">A Table/Queue Encryption Keytype készlet beállításának támogatása Storage-fiók létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="3ef75-1053">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="3ef75-1054">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3ef75-1054">New-AzStorageAccount</span></span>
* <span data-ttu-id="3ef75-1055">RequestId megjelenítése, ha a StorageException nem rendelkezik ExtendedErrorInformation paraméterrel</span><span class="sxs-lookup"><span data-stu-id="3ef75-1055">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="3ef75-1056">A Start-AzStorageBlobCopy parancsmag 6. példájának kijavítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1056">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3ef75-1057">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3ef75-1057">Az.Websites</span></span>
* <span data-ttu-id="3ef75-1058">A Set-AzWebapp és a Set-AzWebappSlot támogatja az AlwaysOn, a MinTls és a FtpsState tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="3ef75-1058">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="3ef75-1059">Javítva a hiba, amely miatt a HttpsOnly és az AppservicePlan Set-AzWebApp paranccsal történő egyidejű módosításakor a HttpsOnly paraméter alaphelyzetbe állt.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1059">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="3ef75-1060">3.3.0 – 2020. január</span><span class="sxs-lookup"><span data-stu-id="3ef75-1060">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3ef75-1061">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3ef75-1061">Az.Accounts</span></span>
* <span data-ttu-id="3ef75-1062">Frissítve lettek az Add-AzEnvironment és Set-AzEnvironment parancsmagok, amelyek mostantól elfogadják az AzureAttestationServiceEndpointResourceId és AzureAttestationServiceEndpointSuffix paramétereket</span><span class="sxs-lookup"><span data-stu-id="3ef75-1062">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="3ef75-1063">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3ef75-1063">Az.Cdn</span></span>
* <span data-ttu-id="3ef75-1064">A hibaválasz részleteinek láthatóvá tétele a New-AzCdnEndpoint parancsmagban</span><span class="sxs-lookup"><span data-stu-id="3ef75-1064">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3ef75-1065">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-1065">Az.Compute</span></span>
* <span data-ttu-id="3ef75-1066">Javítva lett a Set-AzVMCustomScriptExtension parancsmag az olyan virtuális gépek esetében, amelyek felügyelt operációsrendszer-lemeze nem rendelkezik operációsrendszer-profillal.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1066">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="3ef75-1067">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3ef75-1067">Az.ContainerInstance</span></span>
* <span data-ttu-id="3ef75-1068">Javítva lettek a New-AzContainerGroup parancsmagpélda által használt paraméternevek</span><span class="sxs-lookup"><span data-stu-id="3ef75-1068">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="3ef75-1069">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="3ef75-1069">Az.DataBoxEdge</span></span>
* <span data-ttu-id="3ef75-1070">Hozzá lett adva a Get-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="3ef75-1070">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="3ef75-1071">Az Edge Storage-tároló lekérése</span><span class="sxs-lookup"><span data-stu-id="3ef75-1071">Get the Edge Storage Container</span></span>
* <span data-ttu-id="3ef75-1072">Hozzá lett adva a New-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="3ef75-1072">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="3ef75-1073">Új Edge Storage-tároló létrehozása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1073">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="3ef75-1074">Hozzá lett adva a Remove-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="3ef75-1074">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="3ef75-1075">Az Edge Storage-tároló eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1075">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="3ef75-1076">Hozzá lett adva az Invoke-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="3ef75-1076">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="3ef75-1077">Meghívási művelet az Edge Storage-tárolóban lévő adatok frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-1077">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="3ef75-1078">Hozzá lett adva a Get-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="3ef75-1078">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="3ef75-1079">Az Edge Storage-fiók lekérése</span><span class="sxs-lookup"><span data-stu-id="3ef75-1079">Get the Edge Storage Account</span></span>
* <span data-ttu-id="3ef75-1080">Hozzá lett adva a New-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="3ef75-1080">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="3ef75-1081">Új Edge Storage-fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1081">Create new Edge Storage Account</span></span>
* <span data-ttu-id="3ef75-1082">Hozzá lett adva a Remove-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="3ef75-1082">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="3ef75-1083">Az Edge Storage-fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1083">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="3ef75-1084">Hozzá lett adva az Invoke-AzDataBoxEdgeShare parancsmag</span><span class="sxs-lookup"><span data-stu-id="3ef75-1084">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="3ef75-1085">Meghívási művelet a megosztott adatok frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-1085">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="3ef75-1086">Hozzá lett adva a Set-AzDataBoxEdgeStorageAccountCredential parancsmag</span><span class="sxs-lookup"><span data-stu-id="3ef75-1086">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="3ef75-1087">Az Az.DataBoxEdge tárfiók hitelesítő adatainak beállítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1087">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3ef75-1088">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3ef75-1088">Az.DataFactory</span></span>
* <span data-ttu-id="3ef75-1089">Hozzá lettek adva az AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId és VersionStatus tulajdonságok a Get-AzDataFactoryV2IntegrationRuntime parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1089">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="3ef75-1090">Az ADF .Net SDK frissítve lett a 4.6.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="3ef75-1090">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="3ef75-1091">A PublicIPs paraméter hozzá lett adva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz statikus nyilvános IP-címekkel rendelkező Azure-SSIS IR létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1091">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="3ef75-1092">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="3ef75-1092">Az.DevTestLabs</span></span>
* <span data-ttu-id="3ef75-1093">A hibás hivatkozás el lett távolítva a Get-AzDtlAllowedVMSizesPolicy.md parancsmagból</span><span class="sxs-lookup"><span data-stu-id="3ef75-1093">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3ef75-1094">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3ef75-1094">Az.EventHub</span></span>
* <span data-ttu-id="3ef75-1095">A 10634-es hiba javítása: Ki lett javítva a nullértékű objektumhivatkozás a remove eventhubnamespace esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-1095">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="3ef75-1096">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3ef75-1096">Az.HDInsight</span></span>
* <span data-ttu-id="3ef75-1097">Ki lett javítva az Invoke-AzHDInsightHiveJob.md hibája.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1097">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="3ef75-1098">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="3ef75-1098">Az.MachineLearning</span></span>
* <span data-ttu-id="3ef75-1099">El lettek távolítva az alábbi parancsmagok, mivel a MachineLearningCompute már nem érhető el</span><span class="sxs-lookup"><span data-stu-id="3ef75-1099">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="3ef75-1100">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="3ef75-1100">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="3ef75-1101">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="3ef75-1101">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="3ef75-1102">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="3ef75-1102">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="3ef75-1103">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="3ef75-1103">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="3ef75-1104">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="3ef75-1104">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="3ef75-1105">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="3ef75-1105">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="3ef75-1106">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="3ef75-1106">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3ef75-1107">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-1107">Az.Network</span></span>
* <span data-ttu-id="3ef75-1108">Frissítve lett a Microsoft.Azure.Management.Sql függősége: 1.36-preview helyett 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="3ef75-1108">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3ef75-1109">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-1109">Az.RecoveryServices</span></span>
* <span data-ttu-id="3ef75-1110">Módosított Azure Site Recovery-támogatás azon felügyelt lemezeken található, inaktív állapotban titkosított virtuális gépeknél, amelyekhez felhasználó által kezelt kulcsok tartoznak a következő esetében: Azure – Azure-szolgáltató.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1110">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="3ef75-1111">Azure Site Recovery-támogatás a lemeztitkosítási csoportazonosító megadásának opcionálissá tételéhez a védelem engedélyezése során a következő esetében: VMware – Azure.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1111">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="3ef75-1112">Azure Site Recovery-támogatás a lemeztitkosítási csoportazonosító megadásának opcionálissá tételéhez a lemez szintjén a védelem engedélyezéséhez a következő esetében: VMware – Azure.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1112">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="3ef75-1113">Azure Site Recovery-támogatás a Replikációval védett, lemeztitkosítási csoportleképezéssel ellátott elemek frissítéséhez a következő esetében: HyperV – Azure.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1113">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3ef75-1114">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-1114">Az.Resources</span></span>
* <span data-ttu-id="3ef75-1115">Javítva lett egy hiba a Remove-AzTag súgódokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1115">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="3ef75-1116">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-1116">Az.Sql</span></span>
* <span data-ttu-id="3ef75-1117">Javítva lett a sebezhetőségi felmérés csoportszintű alapkonfigurációs parancsmagjainak működése: az Azure-adatbázis főadatbázisában használható, a felügyelt példányok rendszeradatbázisaiban korlátozott.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1117">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="3ef75-1118">Ki lett javítva egy hiba az SQL-példányok feladatátvételi csoportjainak létrehozása esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-1118">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="3ef75-1119">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3ef75-1119">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="3ef75-1120">Hozzá lett adva a DR, mint új érvényes licenctípus</span><span class="sxs-lookup"><span data-stu-id="3ef75-1120">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3ef75-1121">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3ef75-1121">Az.Storage</span></span>
* <span data-ttu-id="3ef75-1122">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó figyelmeztető üzenet a DefaultAction értékének módosítására vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="3ef75-1122">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="3ef75-1123">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="3ef75-1123">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="3ef75-1124">Támogatott a tárfiók legutóbbi szinkronizálási időpontjának lekérése a get-AzureRMStorageAccount parancsmag -IncludeGeoReplicationStats paraméterrel való futtatásával</span><span class="sxs-lookup"><span data-stu-id="3ef75-1124">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="3ef75-1125">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3ef75-1125">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="3ef75-1126">3.2.0 – 2019. december</span><span class="sxs-lookup"><span data-stu-id="3ef75-1126">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="3ef75-1127">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="3ef75-1127">General</span></span>
* <span data-ttu-id="3ef75-1128">A .psd1 hivatkozásai frissítve, hogy minden modulhoz a relatív elérési utat használják</span><span class="sxs-lookup"><span data-stu-id="3ef75-1128">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3ef75-1129">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3ef75-1129">Az.Accounts</span></span>
* <span data-ttu-id="3ef75-1130">A megfelelő felhasználói ügynök beállítva az ügyféloldali telemetriához az Az 4.0 előzetes verziójában</span><span class="sxs-lookup"><span data-stu-id="3ef75-1130">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="3ef75-1131">Felhasználóbarát hibaüzenet megjelenítése, ha az Az 4.0 előzetes verziójában a környezet null értékű</span><span class="sxs-lookup"><span data-stu-id="3ef75-1131">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="3ef75-1132">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3ef75-1132">Az.Batch</span></span>
* <span data-ttu-id="3ef75-1133">Ki lett javítva a [10602-es](https://github.com/Azure/azure-powershell/issues/10602) számú hiba, amely miatt a **New-AzBatchPool** nem megfelelően küldte el a „VirtualMachineConfiguration.ContainerConfiguration” és a „VirtualMachineConfiguration.DataDisks” paramétereket a kiszolgálónak.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1133">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3ef75-1134">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3ef75-1134">Az.DataFactory</span></span>
* <span data-ttu-id="3ef75-1135">Az ADF .Net SDK a 4.5.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="3ef75-1135">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="3ef75-1136">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3ef75-1136">Az.FrontDoor</span></span>
* <span data-ttu-id="3ef75-1137">A WAF felügyeleti szabályok kizárása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="3ef75-1137">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="3ef75-1138">Hozzá lett adva a SocketAddr automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="3ef75-1138">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="3ef75-1139">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="3ef75-1139">Az.HealthcareApis</span></span>
* <span data-ttu-id="3ef75-1140">Kivételkezelés</span><span class="sxs-lookup"><span data-stu-id="3ef75-1140">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3ef75-1141">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3ef75-1141">Az.KeyVault</span></span>
* <span data-ttu-id="3ef75-1142">Ki lett javítva az esetleg nem beállított értékek hozzáférésével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="3ef75-1142">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="3ef75-1143">Az elliptikus görbéjű titkosítási tanúsítványok kezelése</span><span class="sxs-lookup"><span data-stu-id="3ef75-1143">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="3ef75-1144">A görbe tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1144">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3ef75-1145">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3ef75-1145">Az.Monitor</span></span>
* <span data-ttu-id="3ef75-1146">Opcionális argumentum hozzáadva a Diagnosztikai beállítások hozzáadása parancshoz.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1146">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="3ef75-1147">Ez egy kapcsoló argumentum, amely megléte esetén azt jelzi, hogy a Log Analyticsbe történő exportálást egy rögzített séma (más néven</span><span class="sxs-lookup"><span data-stu-id="3ef75-1147">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="3ef75-1148">dedikált adattípus) szerint kell végrehajtani</span><span class="sxs-lookup"><span data-stu-id="3ef75-1148">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3ef75-1149">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-1149">Az.Network</span></span>
* <span data-ttu-id="3ef75-1150">Támogatás az Ip-csoportok számára az AzureFirewall alkalmazás, valamint a Nat- és a hálózati szabályok esetében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1150">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3ef75-1151">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-1151">Az.Resources</span></span>
* <span data-ttu-id="3ef75-1152">Ki lett javítva az a hiba, amely miatt a sablonalapú üzembe helyezés során a sablonparamétert nem lehet olvasni, ha a sablonparaméter és egy beépített paraméter neve között névütközés áll fenn.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1152">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="3ef75-1153">Frissültek a szabályzat parancsmagjai a 2019. 09. 01. dátumú új API-verzió használatára, amely bevezeti a szabályzatkészlet-definíciókon belüli csoportos támogatást.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1153">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="3ef75-1154">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-1154">Az.Sql</span></span>
* <span data-ttu-id="3ef75-1155">Frissítve lett a sebezhetőségi felmérés automatikus engedélyezéséhez szükséges tárterület létrehozása a Storagev2-ben</span><span class="sxs-lookup"><span data-stu-id="3ef75-1155">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3ef75-1156">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3ef75-1156">Az.Storage</span></span>
* <span data-ttu-id="3ef75-1157">A blob-/tárolóidentitás-alapú SAS-token Oauth-hitelesítésen alapuló Storage-környezettel való létrehozásának támogatása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1157">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="3ef75-1158">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="3ef75-1158">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="3ef75-1159">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="3ef75-1159">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="3ef75-1160">Támogatott lett a tárfiókhoz tartozó felhasználódelegálási kulcsok visszavonása, így minden identitásalapú SAS-token visszavonható</span><span class="sxs-lookup"><span data-stu-id="3ef75-1160">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="3ef75-1161">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="3ef75-1161">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="3ef75-1162">Frissítés a Microsoft.Azure.Management.Storage 14.2.0-s verziójára az új API-verzió (2019. 06. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1162">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="3ef75-1163">A QuotaGiB (gigabájtban megadott megosztási kvóta) esetében támogatottak az 5120-nál nagyobb értékek a fájlmegosztási parancsmagok felügyeleti síkján, és hozzá lett adva a Quota paraméteralias a QuotaGiB paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1163">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="3ef75-1164">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="3ef75-1164">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="3ef75-1165">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="3ef75-1165">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="3ef75-1166">A „QuotaGiB” paraméteralias hozzáadva a „kvóta” paraméterhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-1166">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="3ef75-1167">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="3ef75-1167">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="3ef75-1168">Ki lett javítva az a hiba, amely miatt a Set-AzStorageContainerAcl parancsmag el tudta távolítani a tárolt hozzáférési szabályzatot</span><span class="sxs-lookup"><span data-stu-id="3ef75-1168">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="3ef75-1169">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="3ef75-1169">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="3ef75-1170">3.1.0 – 2019. november</span><span class="sxs-lookup"><span data-stu-id="3ef75-1170">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="3ef75-1171">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="3ef75-1171">Highlights since the last major release</span></span>
* <span data-ttu-id="3ef75-1172">Az.DataBoxEdge 1.0.0 kiadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1172">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="3ef75-1173">Az.SqlVirtualMachine 1.0.0 kiadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1173">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3ef75-1174">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-1174">Az.Compute</span></span>
* <span data-ttu-id="3ef75-1175">A virtuális gépek Reapply funkciója</span><span class="sxs-lookup"><span data-stu-id="3ef75-1175">VM Reapply feature</span></span>
    - <span data-ttu-id="3ef75-1176">A Reapply paraméter hozzá lett adva a Set-AzVM parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1176">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="3ef75-1177">A virtuálisgép-méretezési csoportok AutomaticRepairs funkciója:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1177">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="3ef75-1178">Az EnableAutomaticRepair, az AutomaticRepairGracePeriod és az AutomaticRepairMaxInstanceRepairsPercent paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3ef75-1178">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="3ef75-1179">Több-bérlős katalógus-rendszerkép támogatása a New-AzVM parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-1179">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="3ef75-1180">A Spot hozzá lett adva a New-AzVM, a New-AzVMConfig és a New-AzVmss parancsmag Priority paraméterének argumentumbefejezőjéhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-1180">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="3ef75-1181">A DiskIOPSReadWrite és a DiskMBpsReadWrite paraméter hozzá lett adva az Add-AzVmssDataDisk parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1181">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="3ef75-1182">A New-AzGalleryImageVersion parancsmag SourceImageId paramétere mostantól nem kötelező</span><span class="sxs-lookup"><span data-stu-id="3ef75-1182">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="3ef75-1183">A New-AzGalleryImageVersion parancsmag az OSDiskImage és a DataDiskImage paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="3ef75-1183">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="3ef75-1184">A HyperVGeneration paraméter mostantól elérhető a New-AzGalleryImageDefinition parancsmagban</span><span class="sxs-lookup"><span data-stu-id="3ef75-1184">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="3ef75-1185">A SkipExtensionsOnOverprovisionedVMs paraméter hozzá lett adva a New-AzVmss, a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1185">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="3ef75-1186">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="3ef75-1186">Az.DataBoxEdge</span></span>
* <span data-ttu-id="3ef75-1187">A(z) `Get-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1187">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="3ef75-1188">Megrendelés lekérése</span><span class="sxs-lookup"><span data-stu-id="3ef75-1188">Get the Order</span></span>
* <span data-ttu-id="3ef75-1189">A(z) `New-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1189">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="3ef75-1190">Új megrendelés létrehozása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1190">Create new Order</span></span>
* <span data-ttu-id="3ef75-1191">A(z) `Remove-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1191">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="3ef75-1192">Megrendelés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1192">Remove the Order</span></span>
* <span data-ttu-id="3ef75-1193">`New-AzDataBoxEdgeShare` parancsmag módosítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1193">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="3ef75-1194">Mostantól helyi megosztást hoz létre</span><span class="sxs-lookup"><span data-stu-id="3ef75-1194">Now creates Local Share</span></span>
* <span data-ttu-id="3ef75-1195">A(z) `Set-AzDataBoxEdgeRole` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1195">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="3ef75-1196">Mostantól az IotRole leképezhető a Share-re</span><span class="sxs-lookup"><span data-stu-id="3ef75-1196">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="3ef75-1197">A(z) `Invoke-AzDataBoxEdgeDevice` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1197">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="3ef75-1198">Frissítések keresésének, letöltésének, telepítésének indítása az eszközön</span><span class="sxs-lookup"><span data-stu-id="3ef75-1198">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="3ef75-1199">A(z) `Get-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1199">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="3ef75-1200">Triggerek információinak lekérdezése</span><span class="sxs-lookup"><span data-stu-id="3ef75-1200">Gets the information about Triggers</span></span>
* <span data-ttu-id="3ef75-1201">A(z) `New-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1201">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="3ef75-1202">Új triggerek létrehozása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1202">Create new Triggers</span></span>
* <span data-ttu-id="3ef75-1203">A(z) `Remove-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1203">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="3ef75-1204">Triggerek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1204">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3ef75-1205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3ef75-1205">Az.DataFactory</span></span>
* <span data-ttu-id="3ef75-1206">Az ADF .Net SDK a 4.4.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="3ef75-1206">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="3ef75-1207">Az ExpressCustomSetup paraméter hozzá lett adva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz a beállítási konfigurációk és külső összetevők egyéni beállítási szkript nélkül történő engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1207">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3ef75-1208">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3ef75-1208">Az.DataLakeStore</span></span>
* <span data-ttu-id="3ef75-1209">Frissült a Get-AzDataLakeStoreDeletedItem és a Restore-AzDataLakeStoreDeletedItem dokumentációja</span><span class="sxs-lookup"><span data-stu-id="3ef75-1209">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3ef75-1210">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3ef75-1210">Az.EventHub</span></span>
* <span data-ttu-id="3ef75-1211">A 10301-es hiba javítása: Az SAS-token dátumformátumának javítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1211">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="3ef75-1212">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3ef75-1212">Az.FrontDoor</span></span>
* <span data-ttu-id="3ef75-1213">Az Enable-AzFrontDoorCustomDomainHttps és a New-AzFrontDoorFrontendEndpointObject a MinimumTlsVersion paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="3ef75-1213">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="3ef75-1214">A New-AzFrontDoorHealthProbeSettingObject a HealthProbeMethod és az EnabledState paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="3ef75-1214">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="3ef75-1215">Új parancsmag érhető el a Front Door létrehozásakor/frissítésekor megadandó BackendPoolsSettings objektum létrehozásához</span><span class="sxs-lookup"><span data-stu-id="3ef75-1215">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="3ef75-1216">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="3ef75-1216">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3ef75-1217">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-1217">Az.Network</span></span>
* <span data-ttu-id="3ef75-1218">A Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és a Start-AzVirtualnetworkGatewayPacketCapture.md FilterData kapcsolójának példái módosultak.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1218">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="3ef75-1219">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="3ef75-1219">Az.PrivateDns</span></span>
* <span data-ttu-id="3ef75-1220">A PrivateDns .net sdk frissült az 1.0.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="3ef75-1220">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3ef75-1221">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-1221">Az.RecoveryServices</span></span>
* <span data-ttu-id="3ef75-1222">Mostantól Azure Site Recovery-támogatás érhető el a lemeztípus kiválasztásához a védelem engedélyezésekor.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1222">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="3ef75-1223">Azure Site Recovery-hibajavítás a visszaállítási terv műveletének szerkesztéséhez.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1223">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="3ef75-1224">SQL-visszaállítási támogatás az Azure Backuphoz a fájlstream-adatbázisok elfogadása érdekében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1224">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="3ef75-1225">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="3ef75-1225">Az.RedisCache</span></span>
* <span data-ttu-id="3ef75-1226">A MinimumTlsVersion paraméter hozzá lett adva a New-AzRedisCache és a Set-AzRedisCache parancsmagban.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1226">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="3ef75-1227">Emellett a MinimumTlsVersion hozzá lett adva a Get-AzRedisCache parancsmag kimenetéhez.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1227">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="3ef75-1228">Mostantól elérhető a -Size paraméter érvényesítése a Set-AzRedisCache és a New-AzRedisCache parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1228">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="3ef75-1229">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-1229">Az.Resources</span></span>
- <span data-ttu-id="3ef75-1230">Frissültek a szabályzat parancsmagjai a 2019. 06. 01. dátumú új API-verzió használatára, amely tartalmazza az új EnforcementMode tulajdonságot a szabályzat-hozzárendelésekben.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1230">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="3ef75-1231">Frissült a létrehozási szabályzat definíciójának súgóbeli példája</span><span class="sxs-lookup"><span data-stu-id="3ef75-1231">Updated create policy definition help example</span></span>
- <span data-ttu-id="3ef75-1232">Kijavítottuk azt a hibát, amikor a Remove-AZADServicePrincipal -ServicePrincipalName null értékű hivatkozást ad vissza, ha az egyszerű szolgáltatásnév nem található.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1232">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="3ef75-1233">Kijavítottuk azt a hibát, amikor a New-AZADServicePrincipal null értékű hivatkozást ad vissza, ha a bérlőnek nincs előfizetése.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1233">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="3ef75-1234">A New-AzAdServicePrincipal módosult, és már csak a társított alkalmazáshoz ad hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1234">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="3ef75-1235">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-1235">Az.Sql</span></span>
* <span data-ttu-id="3ef75-1236">Az adatbázisbeli ReadReplicaCount mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1236">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="3ef75-1237">A Set-AzSqlDatabase ki lett javítva nem beállított zónaredundancia esetén</span><span class="sxs-lookup"><span data-stu-id="3ef75-1237">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="3ef75-1238">3.0.0 – 2019. november</span><span class="sxs-lookup"><span data-stu-id="3ef75-1238">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="3ef75-1239">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="3ef75-1239">General</span></span>
* <span data-ttu-id="3ef75-1240">Megjelent az Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="3ef75-1240">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3ef75-1241">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3ef75-1241">Az.Accounts</span></span>
* <span data-ttu-id="3ef75-1242">A Resolve-Error aliast érintő elavulási üzenet hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1242">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="3ef75-1243">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="3ef75-1243">Az.Advisor</span></span>
* <span data-ttu-id="3ef75-1244">Új Működésbeli kiválóság kategória hozzáadva a Get-AzAdvisorRecommendation parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1244">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="3ef75-1245">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3ef75-1245">Az.Batch</span></span>
* <span data-ttu-id="3ef75-1246">A `CoreQuota` átnevezve `BatchAccountContext` értékre a következőn: `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1246">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="3ef75-1247">Emellett egy új `LowPriorityCoreQuota` elem is található.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1247">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="3ef75-1248">Ez hatással van a következőre: **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1248">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="3ef75-1249">A **New-AzBatchTask** `-ResourceFile` paraméter most már `PSResourceFile` objektumok gyűjteményét használja, amely az új **New-AzBatchResourceFile** parancsmaggal hozható létre.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1249">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="3ef75-1250">Új **New-AzBatchResourceFile** parancsfájl a szükséges `PSResourceFile` objektumok létrehozásának elősegítéséhez.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1250">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="3ef75-1251">Ezek az **New-AzBatchTask**`-ResourceFile` paraméterénél adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1251">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="3ef75-1252">Ez két új típusú erőforrásfájlt támogat a meglévő `HttpUrl` mód mellett:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1252">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="3ef75-1253">Az `AutoStorageContainerName`-alapú erőforrásfájlok egy teljes automatikus tárolót töltenek le a Batch-csomópontra.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1253">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="3ef75-1254">A `StorageContainerUrl`-alapú erőforrásfájlok az URL-címben megadott tárolót töltik le a Batch-csomópontra.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1254">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="3ef75-1255">A `PSApplication`**Get-AzBatchApplication** által visszaadott `ApplicationPackages` tulajdonsága eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1255">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="3ef75-1256">Most már lekérhetők az alkalmazásokon belüli adott csomagok a **Get-AzBatchApplicationPackage** használatával.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1256">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="3ef75-1257">Például: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1257">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="3ef75-1258">Az `ApplicationId` átnevezve `ApplicationName` értékre a **Get-AzBatchApplicationPackage**, a **New-AzBatchApplicationPackage**, a **Remove-AzBatchApplicationPackage**, a **Get-AzBatchApplication**, a **New-AzBatchApplication**, a **Remove-AzBatchApplication** és a **Set-AzBatchApplication** esetében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1258">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="3ef75-1259">Az `ApplicationId` mostantól az `ApplicationName` aliasa.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1259">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="3ef75-1260">Az új `PSWindowsUserConfiguration` tulajdonság hozzáadva a következőhöz: `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1260">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="3ef75-1261">A `Version` átnevezve `Name` értékre a `PSApplicationPackage` esetében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1261">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="3ef75-1262">A `BlobSource` átnevezve `HttpUrl` értékre a `PSResourceFile` esetében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1262">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="3ef75-1263">Az `OSDisk` tulajdonság eltávolítva a következőből: `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1263">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="3ef75-1264">A **Set-AzBatchPoolOSVersion** eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1264">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="3ef75-1265">Ez a művelet már nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1265">This operation is no longer supported.</span></span>
* <span data-ttu-id="3ef75-1266">`PSCloudServiceConfiguration``TargetOSVersion` eleme eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1266">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="3ef75-1267">A `CurrentOSVersion` átnevezve `OSVersion` értékre a `PSCloudServiceConfiguration` esetében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1267">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="3ef75-1268">`DataEgressGiB` és `DataIngressGiB` eltávolítva a következőből: `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1268">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="3ef75-1269">A **Get-AzBatchNodeAgentSku** eltávolítva és a **Get-AzBatchSupportedImage** parancsmaggal helyettesítve.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1269">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="3ef75-1270">A **Get-AzBatchSupportedImage** ugyanazokat az adatokat jeleníti meg, mint a **Get-AzBatchNodeAgentSku**, csak egyszerűbb formátumban.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1270">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="3ef75-1271">Most már új, nem ellenőrzött rendszerképeket is visszaad a rendszer.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1271">New non-verified images are also now returned.</span></span> <span data-ttu-id="3ef75-1272">Minden rendszerképről további, `Capabilities` és `BatchSupportEndOfLife` típusú információk is szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1272">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="3ef75-1273">Lehetőség arra, hogy távoli fájlrendszereket lehessen csatlakoztatni egy készlet minden csomópontjára a **New-AzBatchPool** új `MountConfiguration` paraméterével.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1273">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="3ef75-1274">Most már támogatja a hálózati biztonsági szabályokat, amelyek a letiltják a készletekhez való hozzáférést a forgalom forrásportja alapján.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1274">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="3ef75-1275">Ez a `PSNetworkSecurityGroupRule``SourcePortRanges` tulajdonsága alapján történik.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1275">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="3ef75-1276">Tároló futtatásakor a Batch támogatja a feladat végrehajtását a tároló munkakönyvtárában vagy a Batch-feladat munkakönyvtárában.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1276">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="3ef75-1277">Ezt a `PSTaskContainerSettings``WorkingDirectory` tulajdonsága szabályozza.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1277">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="3ef75-1278">Új lehetőség nyilvános IP-gyűjtemény megadására az érintett `PSNetworkConfiguration` elemen az új `PublicIPs` tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1278">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="3ef75-1279">Ez garantálja, hogy a készletben található csomópontok rendelkeznek majd IP-címmel a felhasználó által megadott IP-listáról.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1279">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="3ef75-1280">Ha nincs megadva, a `PSSTartTask` alapértelmezett `WaitForSuccess` értéke `$True` (korábban `$False` volt).</span><span class="sxs-lookup"><span data-stu-id="3ef75-1280">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="3ef75-1281">Ha nincs megadva, a `PSAutoUserSpecification` alapértelmezett `Scope` értéke `Pool` (korábban Windowson `Task`, Linuxon pedig `Pool` volt).</span><span class="sxs-lookup"><span data-stu-id="3ef75-1281">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="3ef75-1282">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3ef75-1282">Az.Cdn</span></span>
* <span data-ttu-id="3ef75-1283">A RulesEngine tartalmazza az új UrlRewriteAction és a CacheKeyQueryStringAction műveleteket.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1283">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="3ef75-1284">Javítva számos olyan hiba, mint a New-AzDeliveryRuleCondition parancsmag hiányzó Selector bemenete.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1284">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3ef75-1285">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-1285">Az.Compute</span></span>
* <span data-ttu-id="3ef75-1286">Lemeztitkosítási készlet funkció</span><span class="sxs-lookup"><span data-stu-id="3ef75-1286">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="3ef75-1287">Új parancsmagok:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="3ef75-1287">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="3ef75-1288">A DiskEncryptionSetId paraméter hozzá lett adva a következő parancsmagokhoz:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="3ef75-1288">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="3ef75-1289">A DiskEncryptionSetId és az EncryptionType paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="3ef75-1289">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="3ef75-1290">A PublicIPAddressVersion paraméter hozzá lett adva a New-AzVmssIPConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1290">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="3ef75-1291">Egyéni szkriptbővítmény FileUris tulajdonságának módosítása nyilvánosról védett beállításra</span><span class="sxs-lookup"><span data-stu-id="3ef75-1291">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="3ef75-1292">ScaleInPolicy hozzáadva a New-AzVmss, New-AzVmssConfig és Update-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1292">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="3ef75-1293">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="3ef75-1293">Breaking changes</span></span>
    - <span data-ttu-id="3ef75-1294">A New-AzDiskConfig esetében a DiskSizeGB helyett az UploadSizeInBytes paramétert kell használni, ha a CreateOption értéke Upload</span><span class="sxs-lookup"><span data-stu-id="3ef75-1294">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="3ef75-1295">A PublishingProfile.Source.ManagedImage.Id elemet a StorageProfile.Source.Id helyettesíti a GalleryImageVersion objektumban</span><span class="sxs-lookup"><span data-stu-id="3ef75-1295">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3ef75-1296">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3ef75-1296">Az.DataFactory</span></span>
* <span data-ttu-id="3ef75-1297">Az ADF .Net SDK a 4.3.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="3ef75-1297">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3ef75-1298">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3ef75-1298">Az.DataLakeStore</span></span>
* <span data-ttu-id="3ef75-1299">Az ADLS SDK-verziójának frissítése (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) , a következő javításokkal</span><span class="sxs-lookup"><span data-stu-id="3ef75-1299">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="3ef75-1300">Kivétel jelzésének elkerülése, amikor a lomtár vagy a könyvtár bejegyzésének CreationTime tulajdonsága nem deszerializálható.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1300">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="3ef75-1301">Beállítás megjelenítése minden kérelem-időtúllépés esetén az adlsclient objektumban</span><span class="sxs-lookup"><span data-stu-id="3ef75-1301">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="3ef75-1302">Az eredeti syncflag átadásának javítása a badoffset helyreállításához</span><span class="sxs-lookup"><span data-stu-id="3ef75-1302">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="3ef75-1303">Az EnumerateDirectory javítása a folytatási token válaszellenőrzés utáni lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-1303">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="3ef75-1304">Concat-hiba javítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1304">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="3ef75-1305">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3ef75-1305">Az.FrontDoor</span></span>
* <span data-ttu-id="3ef75-1306">Különféle elgépelések kijavítva a modulban</span><span class="sxs-lookup"><span data-stu-id="3ef75-1306">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="3ef75-1307">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3ef75-1307">Az.HDInsight</span></span>
* <span data-ttu-id="3ef75-1308">Kijavítva az a hiba, amely miatt az ügyfél a Nem érvényes Base-64-sztring hibát kapta, amikor a Get-AzHDInsightCluster használatával próbálta lekérni a fürtöt az ADLSGen1 tároló esetében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1308">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="3ef75-1309">Új, ApplicationId nevű paraméter hozzáadva az Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig és New-AzHDInsightCluster nevű három parancsmaghoz, hogy az ügyfél megadhassa a szolgáltatásnév alkalmazásazonosítóját az Azure Data Lake eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1309">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="3ef75-1310">A Microsoft.Azure.Management.HDInsight 2.1.0 módosítva a következőre: 5.1.0</span><span class="sxs-lookup"><span data-stu-id="3ef75-1310">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="3ef75-1311">Öt parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1311">Removed five cmdlets:</span></span>
    - <span data-ttu-id="3ef75-1312">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="3ef75-1312">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="3ef75-1313">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="3ef75-1313">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="3ef75-1314">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="3ef75-1314">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="3ef75-1315">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="3ef75-1315">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="3ef75-1316">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="3ef75-1316">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="3ef75-1317">Három parancsmag hozzáadva:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1317">Added three cmdlets:</span></span>
    - <span data-ttu-id="3ef75-1318">Get-AzHDInsightMonitoring a Get-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1318">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="3ef75-1319">Enable-AzHDInsightMonitoring az Enable-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1319">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="3ef75-1320">Disable-AzHDInsightMonitoring a Disable-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1320">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="3ef75-1321">A Get-AzHDInsightProperties javítva, hogy támogassa a képességinformációk adott helyről történő beszerzését.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1321">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="3ef75-1322">Paraméterkészletek (Spark1, Spark2) eltávolítva a következőből: Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1322">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="3ef75-1323">Az Add-AzHDInsightSecurityProfile parancsmag súgódokumentumai példákkal bővültek.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1323">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="3ef75-1324">A következő parancsmagok kimeneti típusa megváltozott:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1324">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="3ef75-1325">A Get-AzHDInsightProperties kimeneti típusa CapabilitiesResponse értékről AzureHDInsightCapabilities értékre változott.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1325">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="3ef75-1326">A Remove-AzHDInsightCluster kimeneti típusa ClusterGetResponse értékről logikai értékre változott.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1326">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="3ef75-1327">A Set-AzHDInsightGatewaySettings HttpConnectivitySettings kimeneti típusa GatewaySettings értékre változott.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1327">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="3ef75-1328">Néhány forgatókönyvi teszteset hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1328">Added some scenario test cases.</span></span>
* <span data-ttu-id="3ef75-1329">Néhány alias eltávolítva: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1329">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3ef75-1330">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3ef75-1330">Az.IotHub</span></span>
* <span data-ttu-id="3ef75-1331">Kompatibilitástörő változások:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1331">Breaking changes:</span></span>
    - <span data-ttu-id="3ef75-1332">Az Add-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1332">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="3ef75-1333">Az Add-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1333">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="3ef75-1334">A Get-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1334">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="3ef75-1335">A Get-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1335">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="3ef75-1336">A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1336">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="3ef75-1337">A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1337">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="3ef75-1338">A New-AzIotHubExportDevice parancsmag már nem támogatja a New-AzIotHubExportDevices aliast.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1338">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="3ef75-1339">A New-AzIotHubImportDevice parancsmag már nem támogatja a New-AzIotHubImportDevices aliast.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1339">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="3ef75-1340">A Remove-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1340">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="3ef75-1341">A Remove-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1341">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="3ef75-1342">A Set-AzIotHub parancsmag a továbbiakban nem támogatja az OperationsMonitoringProperties paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1342">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="3ef75-1343">A Set-AzIotHub parancsmaghoz tartozó UpdateOperationsMonitoringProperties paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1343">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3ef75-1344">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-1344">Az.RecoveryServices</span></span>
* <span data-ttu-id="3ef75-1345">Azure Site Recovery-támogatás az olyan hálózati erőforrások konfigurálásához, mint a hálózati biztonsági csoportok, a nyilvános IP-címek és az Azure–Azure belső terheléselosztók.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1345">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="3ef75-1346">Azure Site Recovery-támogatás felügyelt lemezekre történő íráshoz VMware-ről az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1346">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="3ef75-1347">Azure Site Recovery-támogatás hálózati adapter csökkentéséhez VMware-ről az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1347">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="3ef75-1348">Azure Site Recovery-támogatás a hálózat felgyorsításához Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1348">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="3ef75-1349">Azure Site Recovery-támogatás az automatikus frissítési ügynök biztosításához Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1349">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="3ef75-1350">Azure Site Recovery-támogatás standard SSD-meghajtóhoz Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1350">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="3ef75-1351">Azure Site Recovery-támogatás az Azure Disk Encryption kétlépéses hitelesítéséhez Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1351">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="3ef75-1352">Azure Site Recovery-támogatás az újonnan hozzáadott lemez védelméhez Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1352">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="3ef75-1353">SoftDelete funkció hozzáadva a virtuális géphez, továbbá a softdelete-hez hozzáadott tesztek</span><span class="sxs-lookup"><span data-stu-id="3ef75-1353">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="3ef75-1354">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-1354">Az.Resources</span></span>
* <span data-ttu-id="3ef75-1355">A Microsoft.Extensions.Caching.Memory függőségi szerelvény frissítése 1.1.1-esről 2.2-es verzióra</span><span class="sxs-lookup"><span data-stu-id="3ef75-1355">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3ef75-1356">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-1356">Az.Network</span></span>
* <span data-ttu-id="3ef75-1357">A PrivateEndpointConnection összes parancsmagjának módosítása az általános szolgáltató támogatásához.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1357">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="3ef75-1358">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1358">Updated cmdlet:</span></span>
        - <span data-ttu-id="3ef75-1359">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3ef75-1359">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="3ef75-1360">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3ef75-1360">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="3ef75-1361">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3ef75-1361">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="3ef75-1362">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3ef75-1362">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="3ef75-1363">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3ef75-1363">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="3ef75-1364">Új parancsmag hozzáadása a PrivateLinkResource-hoz, valamint az általános szolgáltató támogatása.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1364">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="3ef75-1365">Új parancsmag:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1365">New cmdlet:</span></span>
        - <span data-ttu-id="3ef75-1366">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="3ef75-1366">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="3ef75-1367">Új mezőket és paramétereket ad a Proxy Protocol V2 funkcióhoz.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1367">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="3ef75-1368">Hozzáadja az EnableProxyProtocol tulajdonságot a PrivateLinkService osztályban</span><span class="sxs-lookup"><span data-stu-id="3ef75-1368">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="3ef75-1369">Hozzáadja a LinkIdentifier tulajdonságot a PrivateEndpointConnection osztályban</span><span class="sxs-lookup"><span data-stu-id="3ef75-1369">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="3ef75-1370">New-AzPrivateLinkService frissítve az új, választható EnableProxyProtocol paraméter hozzáadásával.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1370">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="3ef75-1371">Ki lett javítva a New-AzApplicationGatewaySku referenciadokumentációjában található helytelen paraméterleírás</span><span class="sxs-lookup"><span data-stu-id="3ef75-1371">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="3ef75-1372">Új parancsmagok az Azure Firewall-szabályzat támogatásához</span><span class="sxs-lookup"><span data-stu-id="3ef75-1372">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="3ef75-1373">A VirtualHub RouteTables gyermekerőforrásának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1373">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="3ef75-1374">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1374">New cmdlets added:</span></span>
        - <span data-ttu-id="3ef75-1375">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="3ef75-1375">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="3ef75-1376">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="3ef75-1376">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="3ef75-1377">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="3ef75-1377">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="3ef75-1378">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="3ef75-1378">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="3ef75-1379">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3ef75-1379">Set-AzVirtualHub</span></span>
* <span data-ttu-id="3ef75-1380">Az új termékváltozat és VirtualWANType tulajdonság támogatásának hozzáadása a VirtualHub, illetve a VirtualWan esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-1380">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="3ef75-1381">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1381">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="3ef75-1382">New-AzVirtualHub: Sku paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1382">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="3ef75-1383">Update-AzVirtualHub: Sku paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1383">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="3ef75-1384">New-AzVirtualWan: VirtualWANType paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1384">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="3ef75-1385">Update-AzVirtualWan: VirtualWANType paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1385">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="3ef75-1386">Az EnableInternetSecurity tulajdonság támogatásának hozzáadása a HubVnetConnection, a VpnConnection és az ExpressRouteConnection esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-1386">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="3ef75-1387">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1387">New cmdlets added:</span></span>
        - <span data-ttu-id="3ef75-1388">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="3ef75-1388">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="3ef75-1389">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1389">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="3ef75-1390">New-AzureRmVirtualHubVnetConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1390">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="3ef75-1391">New-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1391">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="3ef75-1392">Update-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1392">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="3ef75-1393">New-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1393">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="3ef75-1394">Set-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1394">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="3ef75-1395">TopLevel WebApplicationFirewall-szabályzat beállításának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1395">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="3ef75-1396">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1396">New cmdlets added:</span></span>
        - <span data-ttu-id="3ef75-1397">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="3ef75-1397">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="3ef75-1398">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="3ef75-1398">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="3ef75-1399">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="3ef75-1399">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="3ef75-1400">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="3ef75-1400">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="3ef75-1401">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="3ef75-1401">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="3ef75-1402">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="3ef75-1402">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="3ef75-1403">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1403">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="3ef75-1404">New-AzApplicationGatewayFirewallPolicy: PolicySetting, ManagedRule paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1404">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="3ef75-1405">A CustomRule Geo-Match operátorának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1405">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="3ef75-1406">A GeoMatch hozzáadva a FirewallCondition operátorához</span><span class="sxs-lookup"><span data-stu-id="3ef75-1406">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="3ef75-1407">perListener és a perSite tűzfalszabályzat támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1407">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="3ef75-1408">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1408">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="3ef75-1409">New-AzApplicationGatewayHttpListener: FirewallPolicy, FirewallPolicyId paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1409">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="3ef75-1410">New-AzApplicationGatewayPathRuleConfig: FirewallPolicy, FirewallPolicyId paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1410">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="3ef75-1411">Javítva: a PSBastion esetében a szükséges AzureBastionSubnet alhálózat nevében nem kell megkülönböztetni a kis- és nagybetűket</span><span class="sxs-lookup"><span data-stu-id="3ef75-1411">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="3ef75-1412">A hálózati szabályok céltartományneveinek és a NAT-szabályok lefordított tartományneveinek támogatása az Azure Firewallban</span><span class="sxs-lookup"><span data-stu-id="3ef75-1412">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="3ef75-1413">Az IpGroup legfelsőbb szintű RouteTables erőforrásának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1413">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="3ef75-1414">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1414">New cmdlets added:</span></span>
        - <span data-ttu-id="3ef75-1415">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="3ef75-1415">New-AzIpGroup</span></span>
        - <span data-ttu-id="3ef75-1416">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="3ef75-1416">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="3ef75-1417">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="3ef75-1417">Get-AzIpGroup</span></span>
        - <span data-ttu-id="3ef75-1418">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="3ef75-1418">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3ef75-1419">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3ef75-1419">Az.ServiceFabric</span></span>
* <span data-ttu-id="3ef75-1420">Az Add-AzServiceFabricApplicationCertificate parancsmag el lett távolítva, mivel az Add-AzVmssSecret lefedi ezt a forgatókönyvet.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1420">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="3ef75-1421">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-1421">Az.Sql</span></span>
* <span data-ttu-id="3ef75-1422">Törölt adatbázisok visszaállításának támogatása hozzáadva a felügyelt példányokon.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1422">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="3ef75-1423">A régi naplózási parancsmagok elavulttá váltak a kódban.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1423">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="3ef75-1424">A következő elavult aliasok el lettek távolítva:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1424">Removed deprecated aliases:</span></span>
* <span data-ttu-id="3ef75-1425">Get-AzSqlDatabaseIndexRecommendations (a Get-AzSqlDatabaseIndexRecommendation használata javasolt helyette)</span><span class="sxs-lookup"><span data-stu-id="3ef75-1425">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="3ef75-1426">Get-AzSqlDatabaseRestorePoints (a Get-AzSqlDatabaseRestorePoint használata javasolt helyette)</span><span class="sxs-lookup"><span data-stu-id="3ef75-1426">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="3ef75-1427">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag eltávolítva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1427">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="3ef75-1428">Az elavult sebezhetőség-felmérési beállítások parancsmagjainak aliasai eltávolítva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1428">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="3ef75-1429">A fejlett fenyegetésészlelési beállítások parancsmagjai elavulttá váltak</span><span class="sxs-lookup"><span data-stu-id="3ef75-1429">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="3ef75-1430">Parancsmagok hozzáadása egy adatbázis oszlopait érintő érzékenységi javaslatok letiltása és engedélyezése céljából.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1430">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3ef75-1431">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3ef75-1431">Az.Storage</span></span>
* <span data-ttu-id="3ef75-1432">Nagy fájlok megosztásának engedélyezése Storage-fiók létrehozása vagy frissítése esetén</span><span class="sxs-lookup"><span data-stu-id="3ef75-1432">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="3ef75-1433">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3ef75-1433">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="3ef75-1434">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3ef75-1434">Set-AzStorageAccount</span></span>
* <span data-ttu-id="3ef75-1435">Fájlkezelő bezárása/lekérése esetén a fájlkönyvtár vagy fájl bemeneti elérési út ellenőrzése kimarad, hogy a DeletePending állapotban lévő objektum ne okozhasson hibát</span><span class="sxs-lookup"><span data-stu-id="3ef75-1435">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="3ef75-1436">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="3ef75-1436">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="3ef75-1437">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="3ef75-1437">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="3ef75-1438">2.8.0 – 2019. október</span><span class="sxs-lookup"><span data-stu-id="3ef75-1438">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="3ef75-1439">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="3ef75-1439">General</span></span>
* <span data-ttu-id="3ef75-1440">Az.HealthcareApis 1.0.0-s kiadás</span><span class="sxs-lookup"><span data-stu-id="3ef75-1440">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3ef75-1441">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3ef75-1441">Az.Accounts</span></span>
* <span data-ttu-id="3ef75-1442">A telemetria és az URL-címek újraírásának frissítése a létrehozott modulok esetében, a Windows-egységek tesztelésének javítása.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1442">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="3ef75-1443">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3ef75-1443">Az.ApiManagement</span></span>
* <span data-ttu-id="3ef75-1444">**Set-AzApiManagementApi** – Az API a következőre való frissítésének támogatása: ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="3ef75-1444">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="3ef75-1445">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="3ef75-1445">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3ef75-1446">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3ef75-1446">Az.Automation</span></span>
* <span data-ttu-id="3ef75-1447">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag a Linux újraindítási beállítási paramétere kapcsán.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1447">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="3ef75-1448">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3ef75-1448">Az.Batch</span></span>
* <span data-ttu-id="3ef75-1449">A **Get-AzBatchNodeAgentSku** elavult, így a 2.0.0-ás verziótól a **Get-AzBatchSupportImage** váltja fel.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1449">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3ef75-1450">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-1450">Az.Compute</span></span>
* <span data-ttu-id="3ef75-1451">A Priority, EvictionPolicy és MaxPrice paraméterek hozzáadása a New-AzVM és a New-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1451">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="3ef75-1452">Az Add-AzVMAdditionalUnattendContent és az Add-AzVMSshPublicKey parancsmagok figyelmeztető üzenetének és súgójának kijavítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1452">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="3ef75-1453">A -skipVmBackup kivétel kijavítása felügyelt lemezekkel rendelkező Linux rendszerű virtuális gépek esetében a Set-AzVMDiskEncryptionExtension kapcsán.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1453">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="3ef75-1454">A titkosítási beállítások frissítési hibájának kijavítása a Set-AzVMDiskEncryptionExtension kétmenetes forgatókönyvében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1454">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3ef75-1455">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3ef75-1455">Az.DataFactory</span></span>
* <span data-ttu-id="3ef75-1456">CRUD-parancsok lettek hozzáadva az ADF V2-adatfolyamhoz: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow és Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1456">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="3ef75-1457">Műveleti parancsok lettek hozzáadva az ADF V2-adatfolyam hibakeresési munkamenetéhez: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand és Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1457">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="3ef75-1458">Az ADF .Net SDK a 4.2.0-ás verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="3ef75-1458">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3ef75-1459">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3ef75-1459">Az.DataLakeStore</span></span>
* <span data-ttu-id="3ef75-1460">A fiókérvényesítés javítása, hogy a "-" jelölésű fiókok tartomány nélkül is továbbíthatók legyenek</span><span class="sxs-lookup"><span data-stu-id="3ef75-1460">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="3ef75-1461">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="3ef75-1461">Az.HealthcareApis</span></span>
* <span data-ttu-id="3ef75-1462">A PowerShell az 1.0.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="3ef75-1462">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="3ef75-1463">Az SDK a 1.0.2-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="3ef75-1463">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="3ef75-1464">Frissítés a tesztekben az új SDK-verzióra való hivatkozáshoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1464">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="3ef75-1465">A kimeneti struktúra beágyazottról simítottra frissült.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1465">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3ef75-1466">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3ef75-1466">Az.IotHub</span></span>
* <span data-ttu-id="3ef75-1467">Új útválasztási forrás hozzáadása: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="3ef75-1467">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="3ef75-1468">Kisebb hibajavítás: A Get-AzIothub nem adja vissza a következőt: subscriptionId</span><span class="sxs-lookup"><span data-stu-id="3ef75-1468">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3ef75-1469">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3ef75-1469">Az.Monitor</span></span>
* <span data-ttu-id="3ef75-1470">Új műveleticsoport-fogadók hozzáadva a következő műveleti csoporthoz:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="3ef75-1470">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="3ef75-1471">Az általános riasztási séma használata engedélyezve a fogadók számára.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1471">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="3ef75-1472">Ez nem vonatkozik az SMS, az Azure App leküldéses üzenetei, az ITSM és a Voice fogadóira.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1472">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="3ef75-1473">A webhookok mostantól az Azure Active Directory-hitelesítés használatát is támogatják.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1473">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3ef75-1474">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-1474">Az.Network</span></span>
* <span data-ttu-id="3ef75-1475">Új Get-AzAvailableServiceAlias parancsmag hozzáadva, amely a szolgáltatásvégpont-szabályzatokhoz használható aliasok beszerzéséhez hívható meg.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1475">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="3ef75-1476">Forgalomválasztók hozzáadásának támogatása a virtuális hálózati átjáró kapcsolataihoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1476">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="3ef75-1477">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1477">New cmdlets added:</span></span>
        - <span data-ttu-id="3ef75-1478">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="3ef75-1478">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="3ef75-1479">Parancsmagok frissítve választható paraméterekkel -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3ef75-1479">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="3ef75-1480">Az ESP és AH protokollok támogatása a hálózati biztonsági szabályzati konfigurációkban</span><span class="sxs-lookup"><span data-stu-id="3ef75-1480">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="3ef75-1481">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1481">Updated cmdlets:</span></span>
        - <span data-ttu-id="3ef75-1482">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3ef75-1482">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="3ef75-1483">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3ef75-1483">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="3ef75-1484">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3ef75-1484">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="3ef75-1485">Tovább javult a Cortex-parancsmagok kivételeinek kezelése</span><span class="sxs-lookup"><span data-stu-id="3ef75-1485">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="3ef75-1486">A VirtualNetworkGateways új generációi és termékváltozatai</span><span class="sxs-lookup"><span data-stu-id="3ef75-1486">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="3ef75-1487">A VirtualNetworkGateways új generációinak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1487">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="3ef75-1488">A VirtualNetworkGateways új, nagy átviteli sebességű termékváltozatainak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1488">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="3ef75-1489">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="3ef75-1489">Az.RedisCache</span></span>
* <span data-ttu-id="3ef75-1490">Frissült a Set-AzRedisCache referenciadokumentációja, amely most már tartalmazza a -Size paraméter hiányzó értékeit.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1490">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="3ef75-1491">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-1491">Az.Sql</span></span>
* <span data-ttu-id="3ef75-1492">Az Active Directory-rendszergazda a felügyelt példányon való beállításának támogatása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1492">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3ef75-1493">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3ef75-1493">Az.Storage</span></span>
* <span data-ttu-id="3ef75-1494">Az Storage-ügyfélkódtár a 11.1.0-s verzióra frissült.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1494">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="3ef75-1495">A Management plane API-val rendelkező tárolók listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="3ef75-1495">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="3ef75-1496">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3ef75-1496">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="3ef75-1497">A tárfiókok előfizetésből történő listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="3ef75-1497">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="3ef75-1498">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3ef75-1498">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="3ef75-1499">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="3ef75-1499">Az.StorageSync</span></span>
* <span data-ttu-id="3ef75-1500">A Reset-AzStorageSyncServerCertificate 9810-es hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1500">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3ef75-1501">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3ef75-1501">Az.Websites</span></span>
* <span data-ttu-id="3ef75-1502">Egy alkalmazáshoz tartozó ASP Set-AzWebApp általi frissítése sikertelen volt</span><span class="sxs-lookup"><span data-stu-id="3ef75-1502">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="3ef75-1503">2.7.0 – 2019. szeptember</span><span class="sxs-lookup"><span data-stu-id="3ef75-1503">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="3ef75-1504">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3ef75-1504">Az.ApiManagement</span></span>
* <span data-ttu-id="3ef75-1505">Frissítve lett a „-Format” paraméter leírása a „Set-AzApiManagementPolicy” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="3ef75-1505">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="3ef75-1506">El lettek távolítva az elavult „Update-AzApiManagementDeployment” parancsmag referenciái a referenciadokumentációból.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1506">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="3ef75-1507">A „Set-AzApiManagement” használható helyette.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1507">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3ef75-1508">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3ef75-1508">Az.Automation</span></span>
* <span data-ttu-id="3ef75-1509">Ki lett javítva a „Register-AzAutomationDscNode” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="3ef75-1509">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="3ef75-1510">Hozzá lett adva az operációs rendszerrel kapcsolatos korlátozások pontosítása a Register-AzAutomationDSCNode parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1510">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="3ef75-1511">Ki lett javítva a Start-AzAutomationRunbook parancsmag null értékű hivatkozás okozta kivétele a -Wait paraméter esetén.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1511">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3ef75-1512">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-1512">Az.Compute</span></span>
* <span data-ttu-id="3ef75-1513">Hozzá lett adva az UploadSizeInBytes paraméter a New-AzDiskConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1513">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="3ef75-1514">Hozzá lett adva az Incremental paraméter a New-AzSnapshotConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1514">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="3ef75-1515">Alacsony prioritású virtuálisgép-funkció hozzáadása:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1515">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="3ef75-1516">Hozzá lett adva a MaxPrice, az EvictionPolicy és a Priority paraméter a New-AzVMConfig parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1516">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="3ef75-1517">Hozzá lett adva a MaxPrice paraméter a New-AzVmssConfig, az Update-AzVM és az Update-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1517">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="3ef75-1518">Ki lett javítva a Get-AzAvailabilitySet parancsmag virtuálisgép-hivatkozással kapcsolatos hibája, amely miatt a parancsmag az előfizetésben található összes rendelkezésreállási csoportot listázta.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1518">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="3ef75-1519">Ki lett javítva a Get-AzRemoteDesktopFile parancsmag esetében jelentkező null kivétel.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1519">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="3ef75-1520">Ki lett javítva virtuális merevlemezek Seek metódusa a végrelatív pozíció esetében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1520">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="3ef75-1521">Ki lett javítva az UltraSSD hibája a New-AzVM és az Update-AzVM parancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1521">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3ef75-1522">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3ef75-1522">Az.DataFactory</span></span>
* <span data-ttu-id="3ef75-1523">Hozzá lett adva 3 új parancs (az Add-AzDataFactoryV2TriggerSubscription, a Remove-AzDataFactoryV2TriggerSubscription és a Get-AzDataFactoryV2TriggerSubscriptionStatus) az ADF V2-höz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1523">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="3ef75-1524">Az ADF .Net SDK a 4.1.3-as verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="3ef75-1524">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="3ef75-1525">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3ef75-1525">Az.HDInsight</span></span>
* <span data-ttu-id="3ef75-1526">Kompatibilitástörő változások a meghívással kapcsolatban</span><span class="sxs-lookup"><span data-stu-id="3ef75-1526">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3ef75-1527">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3ef75-1527">Az.IotHub</span></span>
* <span data-ttu-id="3ef75-1528">Hozzá lett adva az IoTHubok földrajzilag párosított vészhelyreállítási régiójába történő feladatátvétel meghívásának támogatása.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1528">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="3ef75-1529">Hozzá lett adva az IoTHubok üzenetbővítés-kezelésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1529">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="3ef75-1530">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1530">New cmdlets are:</span></span>
    - <span data-ttu-id="3ef75-1531">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="3ef75-1531">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="3ef75-1532">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="3ef75-1532">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="3ef75-1533">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="3ef75-1533">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="3ef75-1534">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="3ef75-1534">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3ef75-1535">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3ef75-1535">Az.Monitor</span></span>
* <span data-ttu-id="3ef75-1536">A legújabb Monitor SDK-ra mutat, azaz a 0.24.1-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="3ef75-1536">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="3ef75-1537">Nem kompatibilitástörő változásokkal bővíti a Metrics parancsmagokat, így az egységek számbavétele számos új értéket támogat.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1537">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="3ef75-1538">Ezek írásvédett parancsmagok, ezért a parancsmagok bemenetében nem történik változás.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1538">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="3ef75-1539">Az **ActionGroups**-kérések api-version értéke mostantól **2019-06-01**, korábban **2018-03-01** volt.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1539">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="3ef75-1540">A forgatókönyvtesztek frissültek, így igazodnak a változáshoz.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1540">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="3ef75-1541">Az **EmailReceiver** és a **WebhookReceiver** osztályok konstruktoraihoz hozzá lett adva egy új kötelező argumentum, a **useCommonAlertSchema** nevű logikai érték.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1541">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="3ef75-1542">A kompatibilitástörő változás parancsmagok elől való elrejtése érdekében a rögzített érték jelenleg a **false** (hamis).</span><span class="sxs-lookup"><span data-stu-id="3ef75-1542">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="3ef75-1543">**MEGJEGYZÉS**: Ez egy átmeneti módosítás, amelyet a Riasztások csapatnak érvényesítenie kell.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1543">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="3ef75-1544">A **Source** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1544">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="3ef75-1545">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1545">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="3ef75-1546">Az **AlertingAction** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1546">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="3ef75-1547">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1547">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="3ef75-1548">A dinamikus küszöbérték kritériumainak támogatása a 2-es verziójú metrikariasztás esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-1548">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="3ef75-1549">New-AzMetricAlertRuleV2Criteria: mostantól a dinamikus küszöbértékek kritériumait is létrehozza</span><span class="sxs-lookup"><span data-stu-id="3ef75-1549">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="3ef75-1550">Add-AzMetricAlertRuleV2: mostantól a dinamikus küszöbértékek kritériumait is elfogadja</span><span class="sxs-lookup"><span data-stu-id="3ef75-1550">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="3ef75-1551">Az ütemezett lekérdezési szabályok parancsmagjainak (SQR) fejlesztései</span><span class="sxs-lookup"><span data-stu-id="3ef75-1551">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="3ef75-1552">A parancsmagok a „Location” paraméter mindkét formátumát elfogadják: a helyet (például eastus) és a hely megjelenített nevét is (például USA keleti régiója)</span><span class="sxs-lookup"><span data-stu-id="3ef75-1552">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="3ef75-1553">Megfelelően ábrázolva lett az „Enabled” paraméter a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="3ef75-1553">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="3ef75-1554">Példák lettek hozzáadva az „ActionGroup” opcionális paraméterhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-1554">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="3ef75-1555">Általánosan továbbfejlesztett súgófájlok</span><span class="sxs-lookup"><span data-stu-id="3ef75-1555">Overall improved help files</span></span>
* <span data-ttu-id="3ef75-1556">Ki lett javítva a „Set-AzActionRule” hatókörtípusának meghatározásával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="3ef75-1556">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3ef75-1557">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-1557">Az.Network</span></span>
* <span data-ttu-id="3ef75-1558">Ki lett javítva a „New-AzApplicationGateway” referenciadokumentációjában található helytelen példa</span><span class="sxs-lookup"><span data-stu-id="3ef75-1558">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="3ef75-1559">Hozzá lett adva egy csomagrögzítés összes tulajdonságának lekérésével kapcsolatos megjegyzés a „Get-AzNetworkWatcherPacketCapture” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="3ef75-1559">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="3ef75-1560">Ki lett javítva a „Test-AzNetworkWatcherIPFlow” referenciadokumentációjában található példa a hálózati adapterek megfelelő számbavétele érdekében</span><span class="sxs-lookup"><span data-stu-id="3ef75-1560">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="3ef75-1561">Tovább lett fejlesztve a felhőkivétel-elemzés az esetleges további részletek megjelenítése érdekében</span><span class="sxs-lookup"><span data-stu-id="3ef75-1561">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="3ef75-1562">Tovább lett fejlesztve a felhőkivétel-elemzés az SDK-kivételek további típusainak kezelése érdekében</span><span class="sxs-lookup"><span data-stu-id="3ef75-1562">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="3ef75-1563">Ki lett javítva a biztonságiszabály-modellek helytelen leképezése</span><span class="sxs-lookup"><span data-stu-id="3ef75-1563">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="3ef75-1564">Hozzá lettek adva a privát IP-cím funkcióval kapcsolatos tulajdonságok a hálózati adapterhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-1564">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="3ef75-1565">Hozzá lett adva a „PrivateEndpoint” tulajdonság PSResourceId típusúként a PSNetworkInterface osztályhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1565">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="3ef75-1566">Hozzá lett adva a „PrivateLinkConnectionProperties” tulajdonság PSIpConfigurationConnectivityInformation típusúként a PSNetworkInterfaceIPConfiguration osztályhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1566">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="3ef75-1567">Hozzá lett adva a PSIpConfigurationConnectivityInformation nevű új modellosztály</span><span class="sxs-lookup"><span data-stu-id="3ef75-1567">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="3ef75-1568">Hozzá lett adva az új ApplicationRuleProtocolType „mssql” az Azure Firewall-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1568">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="3ef75-1569">MultiLink-támogatás a Virtuális WAN-ben</span><span class="sxs-lookup"><span data-stu-id="3ef75-1569">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="3ef75-1570">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3ef75-1570">New cmdlets</span></span>
        - <span data-ttu-id="3ef75-1571">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="3ef75-1571">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="3ef75-1572">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="3ef75-1572">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="3ef75-1573">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1573">Updated cmdlet:</span></span>
        - <span data-ttu-id="3ef75-1574">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="3ef75-1574">New-VpnSite</span></span>
        - <span data-ttu-id="3ef75-1575">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="3ef75-1575">Update-VpnSite</span></span>
        - <span data-ttu-id="3ef75-1576">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="3ef75-1576">New-VpnConnection</span></span>
        - <span data-ttu-id="3ef75-1577">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="3ef75-1577">Update-VpnConnection</span></span>
* <span data-ttu-id="3ef75-1578">Ki lettek javítva bizonyos PowerShell-példák dokumentumai, hogy az AzureRM-parancsmagok helyett az Az-parancsmagokat használják</span><span class="sxs-lookup"><span data-stu-id="3ef75-1578">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3ef75-1579">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-1579">Az.RecoveryServices</span></span>
* <span data-ttu-id="3ef75-1580">Frissítve lett az AzureVMpolicy objektum a ProtectedItemsCount attribútummal</span><span class="sxs-lookup"><span data-stu-id="3ef75-1580">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="3ef75-1581">Tesztek lettek hozzáadva a virtuális gép szabályzatához és az eredeti Storage-fiók visszaállításához</span><span class="sxs-lookup"><span data-stu-id="3ef75-1581">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="3ef75-1582">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-1582">Az.Resources</span></span>
* <span data-ttu-id="3ef75-1583">Ki lett javítva a hiba, amely miatt a New-AzRoleAssignment parancsot nem lehetett meghívni a Scope paraméter nélkül.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1583">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3ef75-1584">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3ef75-1584">Az.ServiceFabric</span></span>
* <span data-ttu-id="3ef75-1585">Ki lett javítva az „Update-AzServiceFabricReliability” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="3ef75-1585">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="3ef75-1586">Új parancsmagok lettek hozzáadva az alkalmazás és a szolgáltatások felügyeletéhez:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1586">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="3ef75-1587">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="3ef75-1587">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="3ef75-1588">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="3ef75-1588">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="3ef75-1589">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="3ef75-1589">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="3ef75-1590">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="3ef75-1590">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="3ef75-1591">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="3ef75-1591">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="3ef75-1592">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="3ef75-1592">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="3ef75-1593">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="3ef75-1593">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="3ef75-1594">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="3ef75-1594">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="3ef75-1595">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="3ef75-1595">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="3ef75-1596">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="3ef75-1596">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="3ef75-1597">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="3ef75-1597">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="3ef75-1598">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="3ef75-1598">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="3ef75-1599">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="3ef75-1599">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="3ef75-1600">A Service Fabric SDK az 1.2.0-s verzióra frissült, amely a Service Fabric erőforrás-szolgáltató 2019-03-01 api-versionjét használja.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1600">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="3ef75-1601">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="3ef75-1601">Az.SignalR</span></span>
* <span data-ttu-id="3ef75-1602">Hozzá lettek adva az Update, Restart, CheckNameAvailability és GetUsage parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3ef75-1602">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="3ef75-1603">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-1603">Az.Sql</span></span>
* <span data-ttu-id="3ef75-1604">Frissítve lett a „Get-AzSqlElasticPool” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="3ef75-1604">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="3ef75-1605">Hozzá lett adva egy rugalmas készlet létrehozását bemutató virtuálismag-példa (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="3ef75-1605">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="3ef75-1606">El lett távolítva az EmailAddresses érvényesítése és annak ellenőrzése, hogy az EmailAdmins értéke hamis-e abban az esetben, ha az EmailAddresses üres a Set-AzSqlServerAdvancedThreatProtectionPolicy és a Set-AzSqlDatabaseAdvancedThreatProtectionPolicy parancsmagban</span><span class="sxs-lookup"><span data-stu-id="3ef75-1606">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="3ef75-1607">Engedélyezve lettek a kiszolgáló-/adatbázis-naplózási beállítások abban az esetben, ha több olyan diagnosztikai beállítás létezik, amelyek engedélyezik a naplózási kategóriát.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1607">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="3ef75-1608">Ki lett javítva az e-mail-címek ellenőrzése több, SQL-sebezhetőségi felméréshez használt parancsmagban (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting és Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="3ef75-1608">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3ef75-1609">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3ef75-1609">Az.Storage</span></span>
* <span data-ttu-id="3ef75-1610">Frissítve lett a „Get-AzStorageAccountKey” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="3ef75-1610">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="3ef75-1611">A forrásfájl SMB-tulajdonságai (fájlattribútumok, fájl létrehozásának ideje, fájl utolsó írásának ideje) célfájlban történő megtartásának támogatása az Azure File-beli feltöltés/letöltés esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-1611">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="3ef75-1612">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3ef75-1612">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="3ef75-1613">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3ef75-1613">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="3ef75-1614">Ki lett javítva a tulajdonság-/metaadathibával meghiúsuló blokkblobfeltöltés a tárolóképes ImmutabilityPolicy esetében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1614">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="3ef75-1615">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3ef75-1615">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="3ef75-1616">Az Azure File-megosztások Management plane API-val történő kezelésének támogatása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1616">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="3ef75-1617">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="3ef75-1617">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="3ef75-1618">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="3ef75-1618">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="3ef75-1619">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="3ef75-1619">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="3ef75-1620">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="3ef75-1620">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3ef75-1621">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3ef75-1621">Az.Websites</span></span>
* <span data-ttu-id="3ef75-1622">Ki lett javítva az a probléma, amely miatt a webalkalmazás Címkéi törölve lettek az alkalmazás új ASP-be történő migrálásakor</span><span class="sxs-lookup"><span data-stu-id="3ef75-1622">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="3ef75-1623">Ki lett javítva a Publish-AzureWebapp parancs a Linux és Windows rendszeren történő működés érdekében</span><span class="sxs-lookup"><span data-stu-id="3ef75-1623">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="3ef75-1624">Frissítve lett a „Get-AzWebAppPublishingProfile” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="3ef75-1624">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="3ef75-1625">2.6.0 – 2019. augusztus</span><span class="sxs-lookup"><span data-stu-id="3ef75-1625">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="3ef75-1626">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="3ef75-1626">General</span></span>
* <span data-ttu-id="3ef75-1627">Különféle elgépelések kijavítva több modulban</span><span class="sxs-lookup"><span data-stu-id="3ef75-1627">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3ef75-1628">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3ef75-1628">Az.Accounts</span></span>
* <span data-ttu-id="3ef75-1629">Felhasználó által hozzárendelt MSI támogatása az Azure Functions-hitelesítésben (#9479)</span><span class="sxs-lookup"><span data-stu-id="3ef75-1629">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="3ef75-1630">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="3ef75-1630">Az.Aks</span></span>
* <span data-ttu-id="3ef75-1631">A Get-AzAks kimenetével kapcsolatos probléma ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1631">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="3ef75-1632">További információ: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="3ef75-1632">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="3ef75-1633">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3ef75-1633">Az.ApiManagement</span></span>
* <span data-ttu-id="3ef75-1634">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="3ef75-1634">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="3ef75-1635">Frissült a .net nuget verziója, amely nem kényszeríti ki a productId, az apiId, a groupId és a userId korlátozásait</span><span class="sxs-lookup"><span data-stu-id="3ef75-1635">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="3ef75-1636">**Get-AzApiManagementProduct** – A termékek API-val történő lekérdezése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1636">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="3ef75-1637">**New-AzApiManagementApiRevision** – Ki lett javítva az a probléma, amely miatt az ApiRevisionDescription nem lett beállítva az új API-változat létrehozásakor https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="3ef75-1637">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="3ef75-1638">Ki lett javítva a PsApiManagementOAuth2AuthrozationServer modell elírása PsApiManagementOAuth2AuthorizationServer értékre</span><span class="sxs-lookup"><span data-stu-id="3ef75-1638">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="3ef75-1639">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3ef75-1639">Az.Batch</span></span>
* <span data-ttu-id="3ef75-1640">Ki lett javítva a súgóüzenetben és a dokumentációban található elgépelés, nagy kezdőbetűs Windows értékre</span><span class="sxs-lookup"><span data-stu-id="3ef75-1640">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="3ef75-1641">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3ef75-1641">Az.Cdn</span></span>
* <span data-ttu-id="3ef75-1642">Ki lett javítva egy elgépelés CDN modulátalakító segédben</span><span class="sxs-lookup"><span data-stu-id="3ef75-1642">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3ef75-1643">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-1643">Az.Compute</span></span>
* <span data-ttu-id="3ef75-1644">Új VmssId a New-AzVMConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1644">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="3ef75-1645">Új TerminateScheduledEvents és a TerminateScheduledEventNotBeforeTimeoutInMinutes paraméterek a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1645">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="3ef75-1646">Új HyperVGeneration tulajdonság a VM-rendszerképobjektumhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1646">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="3ef75-1647">Új Host és HostGroup jellemzők</span><span class="sxs-lookup"><span data-stu-id="3ef75-1647">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="3ef75-1648">Új parancsmagok:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="3ef75-1648">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="3ef75-1649">Új HostId paraméter a New-AzVMConfig és a New-AzVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1649">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="3ef75-1650">Az Invoke-AzVMRunCommand dokumentációjában található példa frissítve lett a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="3ef75-1650">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="3ef75-1651">A -VolumeType leírása frissítve lett a set-AzVMDiskEncryptionExtension és a set-AzVmssDiskEncryptionExtension referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="3ef75-1651">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3ef75-1652">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3ef75-1652">Az.DataFactory</span></span>
* <span data-ttu-id="3ef75-1653">A New-AzDataFactoryEncryptValue dokumentációjában a Windows szó nagy kezdőbetűsre lett javítva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1653">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="3ef75-1654">Az ADF .Net SDK a 4.1.2-es verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="3ef75-1654">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="3ef75-1655">Új DataProxyIntegrationRuntimeName, DataProxyIntegrationRuntimeName és DataProxyStagingPath paraméterek lettek hozzáadva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz, lehetővé téve a helyi integrációs modul SSIS integrációs modul proxyjaként való beállítását</span><span class="sxs-lookup"><span data-stu-id="3ef75-1655">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="3ef75-1656">Frissítve lett a PSTriggerRun, hogy megjelenítse az aktivált folyamatokat, üzeneteket és tulajdonságokat, illetve a PSActivityRun, hogy megjelenítse a tevékenységtípust</span><span class="sxs-lookup"><span data-stu-id="3ef75-1656">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3ef75-1657">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3ef75-1657">Az.DataLakeStore</span></span>
* <span data-ttu-id="3ef75-1658">Ki lett javítva a Get-DataLakeStoreDeletedItem lefagyása hibák vagy távoli kivételek esetén.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1658">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3ef75-1659">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3ef75-1659">Az.EventHub</span></span>
* <span data-ttu-id="3ef75-1660">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNteworkRule paraméter a Set-AzEventHubNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="3ef75-1660">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="3ef75-1661">Ki lett javítva a 9558-as számú hiba: Set-AzEventHubNamespace a PUT helyett a PATCH kérést használta</span><span class="sxs-lookup"><span data-stu-id="3ef75-1661">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="3ef75-1662">új EnableKafka paraméter a Set-AzEventHubNamespace parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1662">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="3ef75-1663">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="3ef75-1663">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="3ef75-1664">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="3ef75-1664">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="3ef75-1665">Ki lett javítva egy elgépelés a dokumentációban, ahol az Azure csupa kisbetűvel szerepelt</span><span class="sxs-lookup"><span data-stu-id="3ef75-1665">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3ef75-1666">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3ef75-1666">Az.Monitor</span></span>
* <span data-ttu-id="3ef75-1667">Hibás paraméternév lett kijavítva a súgódokumentációban</span><span class="sxs-lookup"><span data-stu-id="3ef75-1667">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3ef75-1668">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-1668">Az.Network</span></span>
* <span data-ttu-id="3ef75-1669">Frissítve lett a New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3ef75-1669">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="3ef75-1670">A PublicIpAddress elavult, mert a kiszolgálóoldalon nem használatos.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1670">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="3ef75-1671">Hozzá lett adva egy opcionális Primary paraméter, amely azt jelzi, hogy a jelenlegi IP-konfiguráció elsődleges-e.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1671">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="3ef75-1672">Javítva lett az SDK kérelemhiba-kivételének kezelése – kijavítja azt a problémát, amely miatt az SDK-kivételek kezelése korábban nem volt megfelelő, és a fontos hibarészletek nem jelentek meg</span><span class="sxs-lookup"><span data-stu-id="3ef75-1672">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="3ef75-1673">Be lett állítva, hogy az IPv6 IP-előtag ellenőrzési logikája ellenőrizze az IPv6-előtag hosszának megfelelőségét.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1673">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="3ef75-1674">Frissült a Get-AzVirtualNetworkSubnetConfig: Új paraméterkészlet lett hozzáadva az alhálózat erőforrás-azonosítója szerinti lekéréshez.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1674">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="3ef75-1675">Frissült az AzNetworkServiceTag Location paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1675">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3ef75-1676">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3ef75-1676">Az.OperationalInsights</span></span>
* <span data-ttu-id="3ef75-1677">Frissült a New-AzOperationalInsightsLinuxSyslogDataSource dokumentációja</span><span class="sxs-lookup"><span data-stu-id="3ef75-1677">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="3ef75-1678">Példa hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1678">Added example</span></span>
    - <span data-ttu-id="3ef75-1679">A -Name paraméter leírása frissítve lett</span><span class="sxs-lookup"><span data-stu-id="3ef75-1679">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="3ef75-1680">Új példa lett hozzáadva a New-AzOperationalInsightsWindowsEventDataSource parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1680">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="3ef75-1681">Módosult a New-AzOperationalInsightsWindowsEventDataSource -Name paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1681">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3ef75-1682">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-1682">Az.RecoveryServices</span></span>
* <span data-ttu-id="3ef75-1683">Frissült a Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="3ef75-1683">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="3ef75-1684">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-1684">Az.Resources</span></span>
* <span data-ttu-id="3ef75-1685">A Microsoft.Resource mostantól támogatja a 2019-05-10-es új api-verziót</span><span class="sxs-lookup"><span data-stu-id="3ef75-1685">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="3ef75-1686">Mostantól támogatott a copy.count = 0 a változók, erőforrások és tulajdonságok esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-1686">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="3ef75-1687">A condition = false vagy copy.count = 0 tulajdonságú erőforrások teljes módban törölve lesznek</span><span class="sxs-lookup"><span data-stu-id="3ef75-1687">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="3ef75-1688">A súgódokumentációhoz hozzá lett adva egy példa a szabályzatok előfizetési szinten történő hozzárendeléséhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-1688">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3ef75-1689">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3ef75-1689">Az.ServiceBus</span></span>
* <span data-ttu-id="3ef75-1690">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNetworkRule paraméter a Set-AzServiceBusNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="3ef75-1690">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="3ef75-1691">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="3ef75-1691">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="3ef75-1692">Új Test-AzServiceBusNameAvailability parancs lett hozzáadva annak ellenőrzésére, hogy az üzenetsor és a témakör neve elérhető-e</span><span class="sxs-lookup"><span data-stu-id="3ef75-1692">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3ef75-1693">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3ef75-1693">Az.ServiceFabric</span></span>
* <span data-ttu-id="3ef75-1694">Ki lettek javítva a csomóponttípus-hozzáadási parancsmag hibái:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1694">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="3ef75-1695">NullReferenceException hiba történt, ha az erőforráscsoport más, a Service Fabric-fürthöz nem kapcsolódó VMSS-sel rendelkezett.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1695">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="3ef75-1696">Kijavított hiba: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="3ef75-1696">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="3ef75-1697">Ki lett javítva egy hiba, amely miatt a parancsmag futása meghiúsult, ha a virtualNetwork a fürttől eltérő erőforráscsoportban volt.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1697">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="3ef75-1698">kijavított hiba: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="3ef75-1698">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="3ef75-1699">Az Add-AzServiceFabricApplicationCertificate parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="3ef75-1699">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="3ef75-1700">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-1700">Az.Sql</span></span>
* <span data-ttu-id="3ef75-1701">Frissült a régi naplózási parancsmagok dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1701">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3ef75-1702">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3ef75-1702">Az.Storage</span></span>
* <span data-ttu-id="3ef75-1703">A Get/Close-AzStorageFileHandle súgója további parancsmagpélda-forgatókönyvek hozzáadásával és a paraméterek leírásának frissítésével változott</span><span class="sxs-lookup"><span data-stu-id="3ef75-1703">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="3ef75-1704">A StandardBlobTier mostantól támogatott a blobfeltöltési és -másolási műveletekhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-1704">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="3ef75-1705">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3ef75-1705">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="3ef75-1706">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="3ef75-1706">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="3ef75-1707">A rehidratálás prioritása mostantól támogatott a blobmásoláskor</span><span class="sxs-lookup"><span data-stu-id="3ef75-1707">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="3ef75-1708">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="3ef75-1708">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3ef75-1709">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3ef75-1709">Az.Websites</span></span>
* <span data-ttu-id="3ef75-1710">Magyarázat hozzáadva a Set-AzWebApp és a Set-AzWebAppSlot parancsmagok -AppSettings paraméteréhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-1710">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="3ef75-1711">2.5.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="3ef75-1711">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3ef75-1712">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3ef75-1712">Az.Accounts</span></span>
* <span data-ttu-id="3ef75-1713">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1713">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="3ef75-1714">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="3ef75-1714">Az.ApplicationInsights</span></span>
* <span data-ttu-id="3ef75-1715">A Remove-AzApplicationInsightsApiKey dokumentáció példájában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1715">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3ef75-1716">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3ef75-1716">Az.Automation</span></span>
* <span data-ttu-id="3ef75-1717">Az erőforrássztringben található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1717">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3ef75-1718">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-1718">Az.CognitiveServices</span></span>
* <span data-ttu-id="3ef75-1719">NetworkRuleSet támogatás hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1719">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3ef75-1720">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-1720">Az.Compute</span></span>
* <span data-ttu-id="3ef75-1721">A virtuálisgép-példány nézetobjektumaiból hiányzó tulajdonságok (ComputerName, OsName, OsVersion és HyperVGeneration) hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1721">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="3ef75-1722">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3ef75-1722">Az.ContainerRegistry</span></span>
* <span data-ttu-id="3ef75-1723">A Remove-AzContainerRegistryReplication Replikáció paraméterében lévő elírás javítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1723">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="3ef75-1724">További információ: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="3ef75-1724">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3ef75-1725">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3ef75-1725">Az.DataFactory</span></span>
* <span data-ttu-id="3ef75-1726">Az ADF .Net SDK a 4.1.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="3ef75-1726">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="3ef75-1727">A Get-AzDataFactoryV2PipelineRun dokumentációjában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1727">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3ef75-1728">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3ef75-1728">Az.EventHub</span></span>
* <span data-ttu-id="3ef75-1729">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="3ef75-1729">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="3ef75-1730">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="3ef75-1730">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3ef75-1731">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3ef75-1731">Az.KeyVault</span></span>
* <span data-ttu-id="3ef75-1732">A KeySize tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1732">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="3ef75-1733">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3ef75-1733">Az.LogicApp</span></span>
* <span data-ttu-id="3ef75-1734">A Get-AzIntegrationAccountMap javítása, hogy minden leképezéstípust listázzon</span><span class="sxs-lookup"><span data-stu-id="3ef75-1734">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="3ef75-1735">Új MapType paraméter hozzáadva a szűréshez</span><span class="sxs-lookup"><span data-stu-id="3ef75-1735">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="3ef75-1736">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-1736">Az.ManagedServices</span></span>
* <span data-ttu-id="3ef75-1737">Az API 2019. 06. 01-én kiadott (GA) verziójának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1737">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3ef75-1738">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-1738">Az.Network</span></span>
* <span data-ttu-id="3ef75-1739">A privát végpont és privát kapcsolatszolgáltatás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1739">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="3ef75-1740">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3ef75-1740">New cmdlets</span></span>
        - <span data-ttu-id="3ef75-1741">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="3ef75-1741">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="3ef75-1742">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3ef75-1742">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="3ef75-1743">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3ef75-1743">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="3ef75-1744">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3ef75-1744">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="3ef75-1745">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3ef75-1745">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="3ef75-1746">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3ef75-1746">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="3ef75-1747">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="3ef75-1747">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="3ef75-1748">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3ef75-1748">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="3ef75-1749">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies jelző a VirtualNetwork alhálózatban</span><span class="sxs-lookup"><span data-stu-id="3ef75-1749">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="3ef75-1750">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig frissítve</span><span class="sxs-lookup"><span data-stu-id="3ef75-1750">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="3ef75-1751">Hozzá lett adva a -PrivateEndpointNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát végpont esetében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1751">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="3ef75-1752">Hozzá lett adva a -PrivateLinkServiceNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát kapcsolati szolgáltatás esetében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1752">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="3ef75-1753">Az AzPrivateLinkService parancsmag ServiceName paramétere átnevezve a Name névre a ServiceName aliasszal a visszamenőleges kompatibilitás érdekében</span><span class="sxs-lookup"><span data-stu-id="3ef75-1753">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="3ef75-1754">ICMP-protokoll engedélyezése a hálózati biztonsági szabályzati konfigurációkhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1754">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="3ef75-1755">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3ef75-1755">Updated cmdlets</span></span>
        - <span data-ttu-id="3ef75-1756">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3ef75-1756">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="3ef75-1757">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3ef75-1757">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="3ef75-1758">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3ef75-1758">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="3ef75-1759">A ConnectionProtocolType (Ikev1/Ikev2) hozzáadva a New-AzVirtualNetworkGatewayConnection konfigurálható paramétereként</span><span class="sxs-lookup"><span data-stu-id="3ef75-1759">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="3ef75-1760">PrivateIpAddressVersion hozzáadva a LoadBalancerFrontendIpConfigurationhöz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1760">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="3ef75-1761">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1761">Updated cmdlet:</span></span>
        - <span data-ttu-id="3ef75-1762">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3ef75-1762">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="3ef75-1763">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3ef75-1763">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="3ef75-1764">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3ef75-1764">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="3ef75-1765">Application Gateway New-AzApplicationGatewayProbeConfig parancs frissítése a mintavétel egyéni portjának támogatásához</span><span class="sxs-lookup"><span data-stu-id="3ef75-1765">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="3ef75-1766">Frissített New-AzApplicationGatewayProbeConfig: A Port opcionális paraméter hozzáadva, amelyet a rendszer a háttérrendszer-kiszolgáló mintavételére használ.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1766">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="3ef75-1767">Ez a paraméter a Standard_V2 és WAF_V2 termékváltozatokban használható.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1767">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3ef75-1768">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3ef75-1768">Az.OperationalInsights</span></span>
* <span data-ttu-id="3ef75-1769">A mentett keresések alapértelmezett verziója 1 értékre frissítve.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1769">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="3ef75-1770">Null reguláris kifejezések kezelése javítva az egyéni naplókban</span><span class="sxs-lookup"><span data-stu-id="3ef75-1770">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3ef75-1771">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-1771">Az.RecoveryServices</span></span>
* <span data-ttu-id="3ef75-1772">A Get-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="3ef75-1772">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="3ef75-1773">A Get-AzRecoveryServicesBackupContainer.md frissítése</span><span class="sxs-lookup"><span data-stu-id="3ef75-1773">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="3ef75-1774">A Get-AzRecoveryServicesVault.md frissítése</span><span class="sxs-lookup"><span data-stu-id="3ef75-1774">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="3ef75-1775">A Wait-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="3ef75-1775">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="3ef75-1776">A Set-AzRecoveryServicesVaultContext.md frissítése</span><span class="sxs-lookup"><span data-stu-id="3ef75-1776">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="3ef75-1777">A Get-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="3ef75-1777">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="3ef75-1778">A Get-AzRecoveryServicesBackupRecoveryPoint.md frissítése</span><span class="sxs-lookup"><span data-stu-id="3ef75-1778">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="3ef75-1779">A Restore-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="3ef75-1779">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="3ef75-1780">A tároló Azure-fájlmegosztásban való regisztrációjának törlésére szolgáló szolgáltatáshívás frissítése</span><span class="sxs-lookup"><span data-stu-id="3ef75-1780">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="3ef75-1781">A Set-AzRecoveryServicesAsrAlertSetting.md frissítése</span><span class="sxs-lookup"><span data-stu-id="3ef75-1781">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="3ef75-1782">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-1782">Az.Resources</span></span>
- <span data-ttu-id="3ef75-1783">A New-AzResourceGroupDeployment dokumentációban hivatkozott hiányzó parancsmag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1783">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="3ef75-1784">A szabályzat parancsmagjai frissítve a 2019. 01. 01. dátumú új API-verzió használatára</span><span class="sxs-lookup"><span data-stu-id="3ef75-1784">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3ef75-1785">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3ef75-1785">Az.ServiceBus</span></span>
* <span data-ttu-id="3ef75-1786">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="3ef75-1786">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="3ef75-1787">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="3ef75-1787">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="3ef75-1788">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-1788">Az.Sql</span></span>
* <span data-ttu-id="3ef75-1789">A Set-AzSqlDatabaseSecondary parancsmag hiányzó példáinak javítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1789">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="3ef75-1790">A biztonságirés-felmérés e-mail-cím megadása nélkül beállított ismétlődő vizsgálatának javítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1790">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="3ef75-1791">Egy kis elírás javítása egy figyelmeztető üzenetben.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1791">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3ef75-1792">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3ef75-1792">Az.Storage</span></span>
* <span data-ttu-id="3ef75-1793">A Get-AzStorageAccount hivatkozási dokumentációjában található példa frissítése a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="3ef75-1793">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="3ef75-1794">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="3ef75-1794">Az.StorageSync</span></span>
* <span data-ttu-id="3ef75-1795">Az Invoke-AzStorageSyncChangeDetection parancsmag hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1795">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="3ef75-1796">A 9551-es hiba javítása a TierFilesOlderThanDays betartásához</span><span class="sxs-lookup"><span data-stu-id="3ef75-1796">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3ef75-1797">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3ef75-1797">Az.Websites</span></span>
* <span data-ttu-id="3ef75-1798">A hiba elhárítása, amely miatt a Get-AzWebApp és a Set-AzWebApp nem adott vissza egyes SiteConfig tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="3ef75-1798">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="3ef75-1799">Egy új Location paraméter hozzáadása a Get-AzDeletedWebApp és a Restore-AzDeletedWebApp parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1799">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="3ef75-1800">A webalkalmazás-tárhelyek New-AzWebApp -IncludeSourceWebAppSlots használatával történő klónozásakor jelentkező hiba javítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1800">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="3ef75-1801">2.4.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="3ef75-1801">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3ef75-1802">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3ef75-1802">Az.Accounts</span></span>
* <span data-ttu-id="3ef75-1803">Profilparancsmagok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1803">Add support for profile cmdlets</span></span>
* <span data-ttu-id="3ef75-1804">A létrehozott parancsmagokban lévő környezetek és adatsíkok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1804">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="3ef75-1805">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen végpontot használt az adatsík parancsmagjaihoz Windows PowerShellben</span><span class="sxs-lookup"><span data-stu-id="3ef75-1805">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="3ef75-1806">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="3ef75-1806">Az.Advisor</span></span>
* <span data-ttu-id="3ef75-1807">Az Az.Advisor GA-kiadása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1807">GA release of Az.Advisor</span></span>
* <span data-ttu-id="3ef75-1808">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="3ef75-1808">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="3ef75-1809">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3ef75-1809">Az.ApiManagement</span></span>
* <span data-ttu-id="3ef75-1810">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="3ef75-1810">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="3ef75-1811">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="3ef75-1811">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="3ef75-1812">Előfizetések felhasználó és termék szerinti lekérdezésének támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1812">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="3ef75-1813">„/”, „/apis”, „/apis/echo-api” hatókör használatával történő lekérdezés támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1813">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="3ef75-1814">A következő hibák ki lettek javítva: https://github.com/Azure/azure-powershell/issues/9307 és https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="3ef75-1814">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="3ef75-1815">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="3ef75-1815">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="3ef75-1816">Az „ApiVersion” és az „ApiVersionSetId” megadhatóvá vált az API-k importálásakor</span><span class="sxs-lookup"><span data-stu-id="3ef75-1816">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3ef75-1817">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3ef75-1817">Az.Automation</span></span>
* <span data-ttu-id="3ef75-1818">A Set-AzAutomationConnectionFieldValue parancsmag sztringértékek kezelése esetén fellépő hibája javítva lett.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1818">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3ef75-1819">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-1819">Az.Compute</span></span>
* <span data-ttu-id="3ef75-1820">A HyperVGeneration paraméter hozzáadása a New-AzImageConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1820">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3ef75-1821">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3ef75-1821">Az.DataFactory</span></span>
* <span data-ttu-id="3ef75-1822">A tevékenység-, folyamat- és eseményindító-futtatási kimenetek lekérdezési ADF-parancsmagjainak frissítése a Select-Object folyamat támogatásához.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1822">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="3ef75-1823">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3ef75-1823">Az.EventGrid</span></span>
* <span data-ttu-id="3ef75-1824">Az elgépelés ki lett javítva a New-AzEventGridSubscription dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="3ef75-1824">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3ef75-1825">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3ef75-1825">Az.IotHub</span></span>
* <span data-ttu-id="3ef75-1826">Az engedélyezési szabályzati kulcsok újragenerálásának támogatása hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1826">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3ef75-1827">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-1827">Az.Network</span></span>
* <span data-ttu-id="3ef75-1828">A „RoutingPreference” hozzáadva a nyilvános IP-címkékhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-1828">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="3ef75-1829">Javítottuk a példákat a „Get-AzNetworkServiceTag” referenciadokumentációban</span><span class="sxs-lookup"><span data-stu-id="3ef75-1829">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3ef75-1830">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3ef75-1830">Az.PolicyInsights</span></span>
* <span data-ttu-id="3ef75-1831">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyState parancsmagban</span><span class="sxs-lookup"><span data-stu-id="3ef75-1831">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="3ef75-1832">További információ: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="3ef75-1832">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3ef75-1833">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3ef75-1833">Az.OperationalInsights</span></span>
* <span data-ttu-id="3ef75-1834">Javítottuk a Get-AzOperationalInsightsDataSource parancsmagban visszaadott CustomLog adatforrásmodellt</span><span class="sxs-lookup"><span data-stu-id="3ef75-1834">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3ef75-1835">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-1835">Az.RecoveryServices</span></span>
* <span data-ttu-id="3ef75-1836">Az IaaSVMs get-policy parancsának javítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1836">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="3ef75-1837">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-1837">Az.Resources</span></span>
    - <span data-ttu-id="3ef75-1838">A Get-AzPolicyState -Top paraméter súgószövegének javítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1838">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="3ef75-1839">Ügyféloldali lapozás támogatásának hozzáadása a Get-AzPolicyAlias parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1839">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="3ef75-1840">Új (-PolicyParameters és -PolicyParametersObject) paraméterek hozzáadása a Set-AzPolicyAssignment parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1840">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="3ef75-1841">A Policy-parancsmagok néhány dokumentumának és példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="3ef75-1841">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3ef75-1842">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3ef75-1842">Az.ServiceBus</span></span>
* <span data-ttu-id="3ef75-1843">A 4938-as hiba javítása – A New-AzureRmServiceBusQueue parancsmag BadRequest értéket ad vissza a MaxSizeInMegabytes megadásakor</span><span class="sxs-lookup"><span data-stu-id="3ef75-1843">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="3ef75-1844">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-1844">Az.Sql</span></span>
* <span data-ttu-id="3ef75-1845">A példány-feladatátvételi csoportok parancsmagjainak hozzáadása az előzetes kiadásból a nyilvános kiadáshoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1845">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="3ef75-1846">Az Azure SQL Server\Database Auditing támogatása új parancsmagokkal.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1846">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="3ef75-1847">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="3ef75-1847">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="3ef75-1848">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="3ef75-1848">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="3ef75-1849">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="3ef75-1849">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="3ef75-1850">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="3ef75-1850">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="3ef75-1851">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="3ef75-1851">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="3ef75-1852">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="3ef75-1852">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="3ef75-1853">E-mailes korlátozások eltávolítása a sebezhetőségi felmérés beállításaiból</span><span class="sxs-lookup"><span data-stu-id="3ef75-1853">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3ef75-1854">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3ef75-1854">Az.Storage</span></span>
* <span data-ttu-id="3ef75-1855">Az „-IndexDocument” és „-ErrorDocument404Path” paraméter módosítása kötelezőről opcionálisra a következő parancsmagban:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1855">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="3ef75-1856">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="3ef75-1856">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="3ef75-1857">A Get-AzStorageBlobContent súgójának frissítése egy példa hozzáadásával</span><span class="sxs-lookup"><span data-stu-id="3ef75-1857">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="3ef75-1858">További hibaadatok megjelenítése, ha a parancsmag futtatása StorageException miatt meghiúsul</span><span class="sxs-lookup"><span data-stu-id="3ef75-1858">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="3ef75-1859">Storage-fiók létrehozásának és frissítésének támogatása Azure Files AAD DS-hitelesítéssel</span><span class="sxs-lookup"><span data-stu-id="3ef75-1859">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="3ef75-1860">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3ef75-1860">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="3ef75-1861">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3ef75-1861">Set-AzStorageAccount</span></span>
* <span data-ttu-id="3ef75-1862">Támogatás a fájlmegosztások, fájlkönyvtárak vagy fájlok fájlleíróinak listázásához vagy bezárásához</span><span class="sxs-lookup"><span data-stu-id="3ef75-1862">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="3ef75-1863">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="3ef75-1863">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="3ef75-1864">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="3ef75-1864">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="3ef75-1865">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="3ef75-1865">Az.StorageSync</span></span>
* <span data-ttu-id="3ef75-1866">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="3ef75-1866">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="3ef75-1867">2.3.2 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="3ef75-1867">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3ef75-1868">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3ef75-1868">Az.Accounts</span></span>
* <span data-ttu-id="3ef75-1869">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen URL-címeket használt a Functions-hívásokhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1869">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="3ef75-1870">További információ: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="3ef75-1870">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="3ef75-1871">Javítva lett az aliasok hibája az AzureRM–Az parancsmagok közötti átvitel esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-1871">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="3ef75-1872">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="3ef75-1872">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="3ef75-1873">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="3ef75-1873">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3ef75-1874">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-1874">Az.Compute</span></span>
* <span data-ttu-id="3ef75-1875">A „New-AzVm” és „New-AzVmss” egyszerű paraméterkészletek mostantól elfogadják a „ProximityPlacementGroup” paramétert.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1875">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="3ef75-1876">Az elgépelés ki lett javítva a „New-AzVM” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="3ef75-1876">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="3ef75-1877">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="3ef75-1877">Az.Dns</span></span>
* <span data-ttu-id="3ef75-1878">Az elgépelés ki lett javítva a „Set-AzDnsZone” súgópéldáinál.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1878">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="3ef75-1879">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3ef75-1879">Az.EventGrid</span></span>
* <span data-ttu-id="3ef75-1880">Frissítve a 2019-06-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1880">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="3ef75-1881">Új parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1881">New cmdlets:</span></span>
    - <span data-ttu-id="3ef75-1882">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="3ef75-1882">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="3ef75-1883">Létrehoz egy új Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1883">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="3ef75-1884">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="3ef75-1884">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="3ef75-1885">Lekéri egy Event Grid-tartomány részleteit, vagy az aktuális Azure-előfizetéshez tartozó összes Event Grid-tartomány listáját.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1885">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="3ef75-1886">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="3ef75-1886">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="3ef75-1887">Eltávolít egy Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1887">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="3ef75-1888">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="3ef75-1888">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="3ef75-1889">Újra létrehozza a megosztott hozzáférési kulcsot az Azure Event Grid-tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1889">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="3ef75-1890">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="3ef75-1890">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="3ef75-1891">Lekéri az Event Grid-tartományban való esemény-közzétételhez használt megosztott hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1891">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="3ef75-1892">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1892">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="3ef75-1893">Új Azure Event Grid-tartományi témakört hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1893">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="3ef75-1894">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="3ef75-1894">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="3ef75-1895">Lekéri egy Event Grid-tartományi témakör részleteit, vagy az aktuális Azure-előfizetés adott Event Grid-tartományához tartozó Event Grid-tartományi témakörök listáját</span><span class="sxs-lookup"><span data-stu-id="3ef75-1895">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="3ef75-1896">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1896">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="3ef75-1897">Eltávolít egy meglévő Azure Event Grid-tartományi témakört.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1897">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="3ef75-1898">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1898">Updated cmdlets:</span></span>
    - <span data-ttu-id="3ef75-1899">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1899">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="3ef75-1900">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1900">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="3ef75-1901">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1901">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="3ef75-1902">Új paraméterkészletek lettek hozzáadva tartományok és tartományi témakörök esetében, lehetővé téve a meglévő paraméterek (például EndPointType, SubjectBeginsWith stb.) újbóli felhasználását.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1902">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="3ef75-1903">Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1903">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="3ef75-1904">Esemény-előfizetés lejárati dátuma,</span><span class="sxs-lookup"><span data-stu-id="3ef75-1904">Event subscription expiration date,</span></span>
            - <span data-ttu-id="3ef75-1905">Speciális szűrési paraméterek.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1905">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="3ef75-1906">Új felsorolási érték lett hozzáadva a servicebusqueue elem célértékeként.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1906">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="3ef75-1907">Nem engedélyezett az -IncludedEventType beállításnál az „All” érték használata és a következővel való helyettesítése:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1907">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="3ef75-1908">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1908">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="3ef75-1909">Új opcionális paraméterek (Top, ODataQuery és NextLink) az eredmények tördelésének és szűrésének támogatásához.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1909">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="3ef75-1910">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="3ef75-1910">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="3ef75-1911">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1911">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="3ef75-1912">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1912">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="3ef75-1913">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3ef75-1913">Az.FrontDoor</span></span>
* <span data-ttu-id="3ef75-1914">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="3ef75-1914">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="3ef75-1915">Hozzá lett adva az átalakítások támogatása és az új operátorértékek automatikus kitöltése (RegEx)</span><span class="sxs-lookup"><span data-stu-id="3ef75-1915">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="3ef75-1916">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="3ef75-1916">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="3ef75-1917">Hozzá lett adva az új értékek automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="3ef75-1917">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3ef75-1918">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-1918">Az.Network</span></span>
* <span data-ttu-id="3ef75-1919">Virtuális hálózati átjárók erőforrás-támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1919">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="3ef75-1920">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3ef75-1920">New cmdlets</span></span>
        - <span data-ttu-id="3ef75-1921">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="3ef75-1921">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="3ef75-1922">AvailablePrivateEndpointType hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1922">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="3ef75-1923">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3ef75-1923">New cmdlets</span></span>
        - <span data-ttu-id="3ef75-1924">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="3ef75-1924">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="3ef75-1925">PrivatePrivateLinkService hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1925">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="3ef75-1926">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3ef75-1926">New cmdlets</span></span>
        - <span data-ttu-id="3ef75-1927">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3ef75-1927">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="3ef75-1928">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3ef75-1928">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="3ef75-1929">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3ef75-1929">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="3ef75-1930">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3ef75-1930">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="3ef75-1931">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3ef75-1931">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="3ef75-1932">PrivateEndpoint hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-1932">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="3ef75-1933">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3ef75-1933">New cmdlets</span></span>
        - <span data-ttu-id="3ef75-1934">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="3ef75-1934">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="3ef75-1935">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="3ef75-1935">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="3ef75-1936">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="3ef75-1936">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="3ef75-1937">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="3ef75-1937">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="3ef75-1938">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: UseLocalAzureIpAddress jelző a VpnConnection elemen</span><span class="sxs-lookup"><span data-stu-id="3ef75-1938">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="3ef75-1939">Frissítve lett a New-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1939">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="3ef75-1940">Frissítve lett a Set-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1940">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="3ef75-1941">Hozzá lett adva az írásvédett PeeredConnections mező az ExpressRoute-társhálózatlétesítések esetében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1941">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="3ef75-1942">Hozzá lett adva az írásvédett GlobalReachEnabled mező az ExpressRoute esetében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1942">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="3ef75-1943">Kompatibilitástörő változást okozó attribútum lett hozzáadva, amely jelzi az AllowGlobalReach mező elavulását az ExpressRouteCircuit-modellben</span><span class="sxs-lookup"><span data-stu-id="3ef75-1943">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="3ef75-1944">Javítva lett a 8756-os hiba a TargetListenerID AzApplicationGatewayRedirectConfiguration-parancsmagokkal való használata során</span><span class="sxs-lookup"><span data-stu-id="3ef75-1944">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="3ef75-1945">Javítva lett a hiba a New-AzApplicationGatewayPathRuleConfig parancsmagban, amely megakadályozta az átírási szabálykészlet beállítását.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1945">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="3ef75-1946">Javítva lett a VirtualNetworkTaps megjelenítése a NetworkInterfaceIpConfiguration esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-1946">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="3ef75-1947">Javítva lettek a Cortex Get-parancsmagok az összes rész felsorolásához</span><span class="sxs-lookup"><span data-stu-id="3ef75-1947">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="3ef75-1948">Javítva lett a VirtualHub-hivatkozás létrehozása az ExpressRouteGateways, VpnGateway esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-1948">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="3ef75-1949">Hozzá lett adva a rendelkezésreállási zónák támogatása az AzureFirewall és a NatGateway esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-1949">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="3ef75-1950">Hozzá lett adva a Get-AzNetworkServiceTag parancsmag</span><span class="sxs-lookup"><span data-stu-id="3ef75-1950">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="3ef75-1951">Hozzá lett adva a több nyilvános IP-cím támogatása az Azure Firewall esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-1951">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="3ef75-1952">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="3ef75-1952">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="3ef75-1953">Hozzá lett adva a -PublicIpAddress paraméter, amely egy vagy több nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="3ef75-1953">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="3ef75-1954">Hozzá lett adva a -VirtualNetwork paraméter, amely virtuális hálózati objektumokat fogad el</span><span class="sxs-lookup"><span data-stu-id="3ef75-1954">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="3ef75-1955">Hozzá lett adva az AddPublicIpAddress és RemovePublicIpAddress metódus a tűzfalobjektumok esetében, és nyilvános IP-cím-objektumokat fogadnak el bemeneti adatként</span><span class="sxs-lookup"><span data-stu-id="3ef75-1955">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="3ef75-1956">Elavult a -PublicIpName és a -VirtualNetworkName paraméter</span><span class="sxs-lookup"><span data-stu-id="3ef75-1956">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="3ef75-1957">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: VpnClient AAD-alapú hitelesítési beállítások megadása a virtuális hálózati átjárók erőforrásaihoz.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1957">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="3ef75-1958">Frissült a New-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1958">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="3ef75-1959">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1959">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="3ef75-1960">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva a RemoveAadAuthentication opcionális kapcsolóparaméter a VpnClient AAD-alapú hitelesítési beállítások eltávolításához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1960">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3ef75-1961">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3ef75-1961">Az.OperationalInsights</span></span>
* <span data-ttu-id="3ef75-1962">Engedélyezve lett a **pergb2018** tarifacsomag a „New-AzureRmOperationalInsightsWorkspace” parancs esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-1962">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="3ef75-1963">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-1963">Az.Resources</span></span>
* <span data-ttu-id="3ef75-1964">További sablonexportálási beállítások támogatása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1964">Support for additional Template Export options</span></span>
    - <span data-ttu-id="3ef75-1965">Hozzá lett adva a „-SkipResourceNameParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-1965">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="3ef75-1966">Hozzá lett adva a „-SkipAllParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-1966">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="3ef75-1967">Hozzá lett adva a „-Resource” paraméter az Export-AzResourceGroup esetében az exportált erőforrások szűréséhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-1967">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3ef75-1968">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3ef75-1968">Az.ServiceFabric</span></span>
* <span data-ttu-id="3ef75-1969">Ki lett javítva az a hiba, hogy a ByExistingKeyVault tanúsítvány hozzáadása bizonyos esetekben helytelen ujjlenyomatot kért le</span><span class="sxs-lookup"><span data-stu-id="3ef75-1969">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="3ef75-1970">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-1970">Az.Sql</span></span>
* <span data-ttu-id="3ef75-1971">Javítva lett az Advanced Threat Protection Storage-végpontjának utótagja</span><span class="sxs-lookup"><span data-stu-id="3ef75-1971">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="3ef75-1972">Javítva lett, hogy az Advanced Data Security engedélyezése felülbírálja az Advanced Threat Protection-szabályzatot</span><span class="sxs-lookup"><span data-stu-id="3ef75-1972">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="3ef75-1973">Új parancsmagok lettek hozzáadva a Management.Sql esetében, amelyek lehetővé teszik az ügyfelek számára TDE-kulcsok hozzáadását és TDE-védő beállítását a felügyelt példányokhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1973">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="3ef75-1974">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3ef75-1974">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="3ef75-1975">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3ef75-1975">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="3ef75-1976">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3ef75-1976">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="3ef75-1977">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="3ef75-1977">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="3ef75-1978">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="3ef75-1978">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3ef75-1979">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3ef75-1979">Az.Storage</span></span>
* <span data-ttu-id="3ef75-1980">A FileStorage és az SkuName Premium_ZRS altípus támogatása Storage-fiókok létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="3ef75-1980">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="3ef75-1981">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3ef75-1981">New-AzStorageAccount</span></span>
* <span data-ttu-id="3ef75-1982">Egyértelműsítve lett a blobmódosíthatatlansági parancsmag leírása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1982">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="3ef75-1983">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="3ef75-1983">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3ef75-1984">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3ef75-1984">Az.Websites</span></span>
* <span data-ttu-id="3ef75-1985">Optimalizálva lett a Get-AzWebAppCertificate parancsmag, hogy erőforráscsoport szerint szűrjön a kiszolgálón, ne ügyfél szerint</span><span class="sxs-lookup"><span data-stu-id="3ef75-1985">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="3ef75-1986">Hozzá lett adva a -UseDisasterRecovery kapcsolóparaméter a Get-AzWebAppSnapshot parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-1986">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="3ef75-1987">2.2.0 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="3ef75-1987">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="3ef75-1988">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3ef75-1988">Az.Cdn</span></span>
* <span data-ttu-id="3ef75-1989">Frissített parancsmagok a rulesEngine szolgáltatás támogatásához a 2019. 04. 15. API-verzión</span><span class="sxs-lookup"><span data-stu-id="3ef75-1989">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3ef75-1990">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-1990">Az.Compute</span></span>
* <span data-ttu-id="3ef75-1991">A `NoWait` paraméter hozzáadása, amely elindítja a műveletet, és azonnal visszatér, még a művelet befejezése előtt.</span><span class="sxs-lookup"><span data-stu-id="3ef75-1991">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="3ef75-1992">Frissített parancsmagok:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="3ef75-1992">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3ef75-1993">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3ef75-1993">Az.EventHub</span></span>
* <span data-ttu-id="3ef75-1994">A 9231-es hiba javítása – a Get-AzEventHubNamespace nem ad vissza címkéket</span><span class="sxs-lookup"><span data-stu-id="3ef75-1994">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="3ef75-1995">A 9230-as hiba javítása – a Get-AzEventHubNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="3ef75-1995">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3ef75-1996">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-1996">Az.Network</span></span>
* <span data-ttu-id="3ef75-1997">ResourceID és InputObject frissítése a Nat-átjárón</span><span class="sxs-lookup"><span data-stu-id="3ef75-1997">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="3ef75-1998">ResourceID és InputObject aliasának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="3ef75-1998">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3ef75-1999">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3ef75-1999">Az.PolicyInsights</span></span>
* <span data-ttu-id="3ef75-2000">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyEvent parancsmagban</span><span class="sxs-lookup"><span data-stu-id="3ef75-2000">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3ef75-2001">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-2001">Az.RecoveryServices</span></span>
* <span data-ttu-id="3ef75-2002">Az IaaSVM szabályzat minimális megőrzési ideje 7 napról 1-re módosult</span><span class="sxs-lookup"><span data-stu-id="3ef75-2002">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3ef75-2003">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3ef75-2003">Az.ServiceBus</span></span>
* <span data-ttu-id="3ef75-2004">A 9182-es hiba javítása – a Get-AzServiceBusNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="3ef75-2004">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3ef75-2005">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3ef75-2005">Az.ServiceFabric</span></span>
* <span data-ttu-id="3ef75-2006">Az Update-AzServiceFabricReliability hibaüzenetében lévő gépelési hiba kijavítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-2006">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="3ef75-2007">A Service Fabric parancssorok hiányzó karakterének pótlása</span><span class="sxs-lookup"><span data-stu-id="3ef75-2007">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="3ef75-2008">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-2008">Az.Sql</span></span>
* <span data-ttu-id="3ef75-2009">A DnsZonePartner paraméter hozzáadása a New-AzureSqlInstance parancsmaghoz az AutoDr képesség a felügyelt példányon való támogatásához.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2009">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="3ef75-2010">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag kivezetése</span><span class="sxs-lookup"><span data-stu-id="3ef75-2010">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="3ef75-2011">Threat Detection parancsmagok átnevezése Advanced Threat Protection névre</span><span class="sxs-lookup"><span data-stu-id="3ef75-2011">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="3ef75-2012">A New-AzSqlInstance, - StorageSizeInGB és - LicenseType paraméterek mostantól nem kötelezőek.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2012">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3ef75-2013">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3ef75-2013">Az.Websites</span></span>
* <span data-ttu-id="3ef75-2014">javítja azt a hibát, amely miatt a Set-AzWebApp és a Set-AzWebAppSlot a -WebApp tulajdonsággal való használata eltávolította a címkéket</span><span class="sxs-lookup"><span data-stu-id="3ef75-2014">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="3ef75-2015">2.1.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="3ef75-2015">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="3ef75-2016">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3ef75-2016">Az.ApiManagement</span></span>
* <span data-ttu-id="3ef75-2017">Új parancsmagok a globális és API-szintű diagnosztika kezeléshez</span><span class="sxs-lookup"><span data-stu-id="3ef75-2017">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="3ef75-2018">**Get-AzApiManagementDiagnostic** – A globális vagy API hatókörre konfigurált diagnosztika beolvasása</span><span class="sxs-lookup"><span data-stu-id="3ef75-2018">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="3ef75-2019">**New-AzApiManagementDiagnostic** – Új diagnosztika létrehozása a globális vagy API szintű hatókörhöz</span><span class="sxs-lookup"><span data-stu-id="3ef75-2019">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="3ef75-2020">**New-AzApiManagementHttpMessageDiagnostic** – Diagnosztikai beállítás létrehozása arra vonatkozóan, hogy mely fejléceknél naplózzon a rendszer, és mekkora legyen a törzs mérete bájtban</span><span class="sxs-lookup"><span data-stu-id="3ef75-2020">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="3ef75-2021">**New-AzApiManagementPipelineDiagnosticSetting** – Diagnosztikai beállítások létrehozása az átjáróra érkező és onnan induló HTTP-üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2021">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="3ef75-2022">**New-AzApiManagementSamplingSetting** – Mintavételezési beállítások létrehozása diagnosztikai kérésekhez/válaszokhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-2022">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="3ef75-2023">**Remove-AzApiManagementDiagnostic** – Diagnosztikai entitás eltávolítása globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="3ef75-2023">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="3ef75-2024">**Set-AzApiManagementDiagnostic** – Diagnosztikai entitás frissítése globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="3ef75-2024">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="3ef75-2025">Új parancsmagok az ApiManagement szolgáltatás gyorsítótárának kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-2025">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="3ef75-2026">**Get-AzApiManagementCache** – Az azonosító által megadott vagy az összes gyorsítótár részleteinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="3ef75-2026">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="3ef75-2027">**New-AzApiManagementCache** – Új alapértelmezett gyorsítótár létrehozása vagy gyorsítótár létrehozása adott Azure-régióban</span><span class="sxs-lookup"><span data-stu-id="3ef75-2027">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="3ef75-2028">**Remove-AzApiManagementCache** – Gyorsítótár eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-2028">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="3ef75-2029">**Update-AzApiManagementCache** – Gyorsítótár frissítése</span><span class="sxs-lookup"><span data-stu-id="3ef75-2029">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="3ef75-2030">Új parancsmagok az API-séma kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-2030">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="3ef75-2031">**New-AzApiManagementSchema** – Új séma létrehozása egy API-hoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-2031">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="3ef75-2032">**Get-AzApiManagementSchema** – Az API-ban konfigurált sémák beolvasása</span><span class="sxs-lookup"><span data-stu-id="3ef75-2032">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="3ef75-2033">**Remove-AzApiManagementSchema** – Az API-ban konfigurált sémák eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-2033">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="3ef75-2034">**Set-AzApiManagementSchema** – Az API-ban konfigurált séma frissítése</span><span class="sxs-lookup"><span data-stu-id="3ef75-2034">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="3ef75-2035">Új parancsmag a felhasználói jogkivonat létrehozásához</span><span class="sxs-lookup"><span data-stu-id="3ef75-2035">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="3ef75-2036">**New-AzApiManagementUserToken** – Új, alapértelmezés szerint 8 órán át érvényes felhasználói jogkivonat létrehozása. Ezen parancsmag használatával lehet a „GIT” felhasználó számára jogkivonatot létrehozni.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2036">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="3ef75-2037">Új parancsmag a hálózat állapotának lekérdezéséhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-2037">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="3ef75-2038">**Get-AzApiManagementNetworkStatus** – Azon erőforrások hálózati állapotának beolvasása, amelyektől az API Management szolgáltatás függ.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2038">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="3ef75-2039">Ez hasznos lehet, ha az ApiManagement szolgáltatást virtuális hálózatra telepíti, és ellenőrizni kell, hogy rendben működnek-e a függőségek.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2039">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="3ef75-2040">A **New-AzApiManagement** parancsmag frissítése az ApiManagement szolgáltatás kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-2040">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="3ef75-2041">Mostantól az új „Consumption” SKU is támogatott</span><span class="sxs-lookup"><span data-stu-id="3ef75-2041">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="3ef75-2042">Mostantól az „EnableClientCertificate” jelző a „Consumption” SKU-hoz is bekapcsolható</span><span class="sxs-lookup"><span data-stu-id="3ef75-2042">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="3ef75-2043">Az új **New-AzApiManagementSslSetting** parancsmag lehetővé teszi a „TLS/SSL” beállítás konfigurálását a „Háttér” és „Előtér” esetén is.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2043">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="3ef75-2044">Ez egy ApiManagement szolgáltatás előterén a titkosítások, mint például a 3DES, valamint a szerverprotokollok, mint például a Http2 konfigurálására is alkalmas.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2044">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="3ef75-2045">Mostantól támogatott a „DeveloperPortal” gazdanév ApiManagement szolgáltatáson történő konfigurálása.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2045">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="3ef75-2046">A **Get-AzApiManagementSsoToken** parancsmagok frissítése a „PsApiManagement” objektum bemenetként való használatához</span><span class="sxs-lookup"><span data-stu-id="3ef75-2046">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="3ef75-2047">A parancsmag frissítése a hibaüzenetek beágyazott megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-2047">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="3ef75-2048">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hibakód: ValidationError Hibaüzenet: Egy vagy több mező hibás értéket tartalmaz: Hiba részletei:    [Kód=ValidationError, Üzenet=Hiba a log-to-eventhub elemben, 3. sor, 10. oszlop: A naplózó nem található, Cél=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="3ef75-2048">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="3ef75-2049">Az **Export-AzApiManagementApi** parancsmag frissítse az API-k OpenApi 3.0 formátumban való exportálásához</span><span class="sxs-lookup"><span data-stu-id="3ef75-2049">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="3ef75-2050">Az **Import-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="3ef75-2050">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="3ef75-2051">API importálása az OpenApi 3.0 dokumentumspecifikációból</span><span class="sxs-lookup"><span data-stu-id="3ef75-2051">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="3ef75-2052">A bármely (Swagger, Wadl, Wsdl, OpenAPI) dokumentumban megadott PsApiManagementSchema tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="3ef75-2052">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="3ef75-2053">A bármely dokumentumban megadott ServiceUrl tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="3ef75-2053">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="3ef75-2054">A **Get-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) való visszaadásához</span><span class="sxs-lookup"><span data-stu-id="3ef75-2054">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="3ef75-2055">A **Set-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) és XML-nek megfelelő feloldójeles formátumban (xml használatával) való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="3ef75-2055">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="3ef75-2056">A **New-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="3ef75-2056">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="3ef75-2057">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="3ef75-2057">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="3ef75-2058">API létrehozása ApiVersionSet tulajdonságban</span><span class="sxs-lookup"><span data-stu-id="3ef75-2058">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="3ef75-2059">API klónozása SourceApiId és SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="3ef75-2059">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="3ef75-2060">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="3ef75-2060">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="3ef75-2061">A **Set-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="3ef75-2061">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="3ef75-2062">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="3ef75-2062">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="3ef75-2063">API frissítése ApiVersionSet tulajdonságba</span><span class="sxs-lookup"><span data-stu-id="3ef75-2063">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="3ef75-2064">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="3ef75-2064">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="3ef75-2065">A **New-AzApiManagementRevision** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="3ef75-2065">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="3ef75-2066">Létező változat klónozása (címkék, termékek, műveletek és szabályzatok másolása) a SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="3ef75-2066">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="3ef75-2067">Az új változat a szülő ApiId értékét veszi át</span><span class="sxs-lookup"><span data-stu-id="3ef75-2067">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="3ef75-2068">ApiRevisionDescription biztosítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-2068">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="3ef75-2069">A „ServiceUrl” felülírása API klónozáskor</span><span class="sxs-lookup"><span data-stu-id="3ef75-2069">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="3ef75-2070">A **New-AzApiManagementIdentityProvider** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="3ef75-2070">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="3ef75-2071">AAD vagy AADB2C konfigurálása hitelesítésszolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="3ef75-2071">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="3ef75-2072">SignupPolicy, SigninPolicy, ProfileEditingPolicy és PasswordResetPolicy beállítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-2072">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="3ef75-2073">A **New-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="3ef75-2073">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="3ef75-2074">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-2074">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="3ef75-2075">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-2075">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="3ef75-2076">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-2076">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="3ef75-2077">A **Set-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="3ef75-2077">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="3ef75-2078">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-2078">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="3ef75-2079">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-2079">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="3ef75-2080">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-2080">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="3ef75-2081">Az alábbi parancsmagok frissültek a ResourceID bemenetként való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="3ef75-2081">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="3ef75-2082">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3ef75-2082">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="3ef75-2083">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="3ef75-2083">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="3ef75-2084">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="3ef75-2084">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="3ef75-2085">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="3ef75-2085">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="3ef75-2086">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="3ef75-2086">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="3ef75-2087">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="3ef75-2087">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="3ef75-2088">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="3ef75-2088">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="3ef75-2089">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3ef75-2089">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="3ef75-2090">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="3ef75-2090">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="3ef75-2091">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="3ef75-2091">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="3ef75-2092">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="3ef75-2092">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="3ef75-2093">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="3ef75-2093">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3ef75-2094">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3ef75-2094">Az.Automation</span></span>
* <span data-ttu-id="3ef75-2095">A Get-AzAutomationJobOutputRecord frissítése a JSON- és a szövegrekordértékek kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-2095">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="3ef75-2096">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="3ef75-2096">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="3ef75-2097">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="3ef75-2097">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="3ef75-2098">A Start-AzAutomationDscCompilationJob viselkedésének módosítása a munka elindítására a befejezésre való várakozás helyett</span><span class="sxs-lookup"><span data-stu-id="3ef75-2098">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="3ef75-2099">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="3ef75-2099">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="3ef75-2100">A Get-AzAutomationDscNode azon hibájának javítása, amely miatt a -Name használatakor az összes csomópontot visszaadta.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2100">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="3ef75-2101">Most már csak az egyező csomópontot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2101">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3ef75-2102">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-2102">Az.Compute</span></span>
* <span data-ttu-id="3ef75-2103">A ProtectFromScaleIn és a ProtectFromScaleSetAction paraméterek hozzáadása az Update-AzVmssVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-2103">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="3ef75-2104">A New-azvm fedőparaméter-készlet mostantól alapértelmezetten egy elérhető helyet használ, ha az USA keleti régiója nem támogatott</span><span class="sxs-lookup"><span data-stu-id="3ef75-2104">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3ef75-2105">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3ef75-2105">Az.DataLakeStore</span></span>
* <span data-ttu-id="3ef75-2106">Az ADLS SDK frissítése a httpclient használatához, integrált adatsíkteszteléssel az Azure-keretrendszerben</span><span class="sxs-lookup"><span data-stu-id="3ef75-2106">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3ef75-2107">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3ef75-2107">Az.Monitor</span></span>
* <span data-ttu-id="3ef75-2108">A hibás paraméternevek kijavítása a súgópéldákban</span><span class="sxs-lookup"><span data-stu-id="3ef75-2108">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3ef75-2109">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-2109">Az.Network</span></span>
* <span data-ttu-id="3ef75-2110">DisableBgpRoutePropagation jelölő hozzáadása az érvényes útválasztási táblázathoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-2110">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="3ef75-2111">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="3ef75-2111">Updated cmdlet:</span></span>
        - <span data-ttu-id="3ef75-2112">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="3ef75-2112">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="3ef75-2113">A dupla kötőjel kijavítása a New-AzApplicationGatewayTrustedRootCertificate dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="3ef75-2113">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="3ef75-2114">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-2114">Az.Resources</span></span>
* <span data-ttu-id="3ef75-2115">Új Get-AzureRmDenyAssignment parancsmag hozzáadása a megtagadási hozzárendelések lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-2115">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="3ef75-2116">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-2116">Az.Sql</span></span>
* <span data-ttu-id="3ef75-2117">Advanced Threat Protection parancsmagok átnevezése Advanced Data Security névre és a sebezhetőségi felmérés alapértelmezett engedélyezése</span><span class="sxs-lookup"><span data-stu-id="3ef75-2117">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="3ef75-2118">2.0.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="3ef75-2118">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3ef75-2119">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3ef75-2119">Az.Accounts</span></span>
* <span data-ttu-id="3ef75-2120">Az Authentication Library frissítése a felhasználóneves/jelszavas hitelesítéssel kapcsolatos ADFS-problémák kijavításához</span><span class="sxs-lookup"><span data-stu-id="3ef75-2120">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3ef75-2121">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-2121">Az.CognitiveServices</span></span>
* <span data-ttu-id="3ef75-2122">Csak a Bing jogi nyilatkozat jelenik meg a Bing Search-szolgáltatásoknál.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2122">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="3ef75-2123">A sikertelen fióklétrehozás hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2123">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3ef75-2124">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-2124">Az.Compute</span></span>
* <span data-ttu-id="3ef75-2125">Közelségi elhelyezési csoport szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2125">Proximity placement group feature.</span></span>
    - <span data-ttu-id="3ef75-2126">A következő új parancsmagok lettek hozzáadva:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="3ef75-2126">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="3ef75-2127">Az új ProximityPlacementGroupId paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="3ef75-2127">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="3ef75-2128">A StorageAccountType paraméter hozzá lett adva a New-AzGalleryImageVersion parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2128">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="3ef75-2129">A New-AzGalleryImageVersion TargetRegion paramétere tartalmazhatja a következőt: StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2129">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="3ef75-2130">A SkipShutdown kapcsolóparaméter hozzá lett adva a Stop-AzVM és Stop-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-2130">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="3ef75-2131">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="3ef75-2131">Breaking changes</span></span>
    - <span data-ttu-id="3ef75-2132">A Set-AzVMBootDiagnostics parancsmag új neve: Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2132">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="3ef75-2133">Az Export-AzLogAnalyticThrottledRequests parancsmag új neve: Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2133">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="3ef75-2134">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="3ef75-2134">Az.DeploymentManager</span></span>
* <span data-ttu-id="3ef75-2135">Az Azure Deployment Manager-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="3ef75-2135">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="3ef75-2136">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="3ef75-2136">Az.Dns</span></span>
* <span data-ttu-id="3ef75-2137">Automatikus DNS NameServer-delegálás</span><span class="sxs-lookup"><span data-stu-id="3ef75-2137">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="3ef75-2138">A DNS-zóna létrehozási parancsmag további opcionális paraméterként elfogadja a szülőzóna nevét.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2138">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="3ef75-2139">Névkiszolgálói rekordokat ad hozzá a szülőzónában az újonnan létrehozott gyermekzóna számára.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2139">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="3ef75-2140">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3ef75-2140">Az.FrontDoor</span></span>
* <span data-ttu-id="3ef75-2141">Az Azure FrontDoor-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="3ef75-2141">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="3ef75-2142">A WAF-parancsmagok új neve tartalmazza a „Waf” sztringet</span><span class="sxs-lookup"><span data-stu-id="3ef75-2142">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="3ef75-2143">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3ef75-2143">Az.HDInsight</span></span>
* <span data-ttu-id="3ef75-2144">A következő két parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="3ef75-2144">Removed two cmdlets:</span></span>
    - <span data-ttu-id="3ef75-2145">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="3ef75-2145">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="3ef75-2146">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="3ef75-2146">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="3ef75-2147">Egy új, Set-AzHDInsightGatewayCredential nevű parancsmag lett hozzáadva a Grant-AzHDInsightHttpServicesAccess helyett</span><span class="sxs-lookup"><span data-stu-id="3ef75-2147">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="3ef75-2148">A Get-AzHDInsightJobOutput parancsmag frissítve lett, hogy különbséget tegyen az olvasói és a HDInsight-operátori szerepkör között:</span><span class="sxs-lookup"><span data-stu-id="3ef75-2148">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="3ef75-2149">Az olvasói szerepkörrel rendelkező felhasználóknak explicit módon meg kell adniuk a DefaultStorageAccountKey paramétert, ellenkező esetben hiba történik.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2149">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="3ef75-2150">A HDInsight-operátori szerepkörrel rendelkező felhasználókat ez nem érinti.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2150">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3ef75-2151">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3ef75-2151">Az.Monitor</span></span>
* <span data-ttu-id="3ef75-2152">Az SQR API (ütemezett lekérdezési szabály) új parancsmagjai</span><span class="sxs-lookup"><span data-stu-id="3ef75-2152">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="3ef75-2153">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="3ef75-2153">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="3ef75-2154">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="3ef75-2154">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="3ef75-2155">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="3ef75-2155">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="3ef75-2156">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="3ef75-2156">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="3ef75-2157">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="3ef75-2157">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="3ef75-2158">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="3ef75-2158">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="3ef75-2159">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3ef75-2159">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="3ef75-2160">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3ef75-2160">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="3ef75-2161">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3ef75-2161">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="3ef75-2162">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3ef75-2162">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="3ef75-2163">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3ef75-2163">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="3ef75-2164">[További](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) információk az SQR API-ról</span><span class="sxs-lookup"><span data-stu-id="3ef75-2164">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="3ef75-2165">A frissített Az.Monitor.md tartalmazza a GenV2 (nem klasszikus) metrikaalapú riasztási szabály parancsmagjait</span><span class="sxs-lookup"><span data-stu-id="3ef75-2165">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3ef75-2166">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-2166">Az.Network</span></span>
* <span data-ttu-id="3ef75-2167">A NAT-átjáró erőforrás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-2167">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="3ef75-2168">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3ef75-2168">New cmdlets</span></span>
        - <span data-ttu-id="3ef75-2169">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="3ef75-2169">New-AzNatGateway</span></span>
        - <span data-ttu-id="3ef75-2170">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="3ef75-2170">Get-AzNatGateway</span></span>
        - <span data-ttu-id="3ef75-2171">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="3ef75-2171">Set-AzNatGateway</span></span>
        - <span data-ttu-id="3ef75-2172">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="3ef75-2172">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="3ef75-2173">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3ef75-2173">Updated cmdlets</span></span>
        - <span data-ttu-id="3ef75-2174">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="3ef75-2174">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="3ef75-2175">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="3ef75-2175">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="3ef75-2176">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: Egyéni útvonalak beállítása/eltávolítása a Brooklyn Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2176">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="3ef75-2177">Frissült a New-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2177">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="3ef75-2178">Frissült a Set-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2178">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3ef75-2179">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3ef75-2179">Az.PolicyInsights</span></span>
* <span data-ttu-id="3ef75-2180">A szabályzat-kiértékelési adatok lekérdezésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2180">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="3ef75-2181">Az -Expand paraméter hozzá lett adva a Get-AzPolicyState parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2181">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="3ef75-2182">Az -Expand PolicyEvaluationDetails támogatása.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2182">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3ef75-2183">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-2183">Az.RecoveryServices</span></span>
* <span data-ttu-id="3ef75-2184">Az előfizetések közötti Azure–Azure Site Recovery átvitel támogatása.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2184">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="3ef75-2185">Az Azure Site Recovery jövőbeni kompatibilitástörő változásainak jelölése.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2185">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="3ef75-2186">Ki lett javítva az Azure Site Recovery helyreállítási és műveletterve.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2186">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="3ef75-2187">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure hálózatleképezés.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2187">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="3ef75-2188">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure védelemirány felügyelt lemezek esetében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2188">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="3ef75-2189">További kisebb javítások.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2189">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="3ef75-2190">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="3ef75-2190">Az.Relay</span></span>
* <span data-ttu-id="3ef75-2191">Az elgépelések ki lettek javítva az ügyféloldali üzenetekben</span><span class="sxs-lookup"><span data-stu-id="3ef75-2191">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3ef75-2192">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3ef75-2192">Az.ServiceBus</span></span>
* <span data-ttu-id="3ef75-2193">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="3ef75-2193">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3ef75-2194">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3ef75-2194">Az.Storage</span></span>
* <span data-ttu-id="3ef75-2195">A Storage ügyféloldali kódtárának frissítése a 10.0.1-es verziójára (az SDK összes objektuma esetében módosul a névtér a Microsoft.WindowsAzure.Storage. *névtérről a Microsoft.Azure.Storage.* névtérre)</span><span class="sxs-lookup"><span data-stu-id="3ef75-2195">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="3ef75-2196">Frissítés a Microsoft.Azure.Management.Storage 11.0.0-s verziójára az új API-verzió (2019. 04. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2196">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="3ef75-2197">A Tárfiók létrehozása parancs esetében az alapértelmezett Storage-fiókaltípus a Storage helyett mostantól a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2197">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="3ef75-2198">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3ef75-2198">New-AzStorageAccount</span></span>
* <span data-ttu-id="3ef75-2199">A Storage-fiók Sku.Name parancsmagkimenete módosul, hogy igazodjon a bemeneti SkuName paraméterhez, egy aláhúzásjel („_”) hozzáadásával – például a StandardLRS a Standard_LRS névre módosul</span><span class="sxs-lookup"><span data-stu-id="3ef75-2199">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="3ef75-2200">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3ef75-2200">New-AzStorageAccount</span></span>
    - <span data-ttu-id="3ef75-2201">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3ef75-2201">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="3ef75-2202">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3ef75-2202">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3ef75-2203">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3ef75-2203">Az.Websites</span></span>
* <span data-ttu-id="3ef75-2204">Az Altípus tulajdonság mostantól meg lesz adva a Get-AzWebApp által visszaadott PSSite objektumokhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-2204">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="3ef75-2205">A Get-AzWebApp\*Metrics és a Get-AzAppServicePlanMetrics megjelölve elavultként</span><span class="sxs-lookup"><span data-stu-id="3ef75-2205">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="3ef75-2206">1.8.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="3ef75-2206">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="3ef75-2207">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="3ef75-2207">Highlights since the last major release</span></span>
* <span data-ttu-id="3ef75-2208">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="3ef75-2208">General availability of `Az` module</span></span>
* <span data-ttu-id="3ef75-2209">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="3ef75-2209">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="3ef75-2210">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="3ef75-2210">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="3ef75-2211">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-2211">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="3ef75-2212">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-2212">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="3ef75-2213">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-2213">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="3ef75-2214">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-2214">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3ef75-2215">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3ef75-2215">Az.Accounts</span></span>
* <span data-ttu-id="3ef75-2216">Eltávolítás-AzureRm megfelelően törölni a Mac modulok frissítése</span><span class="sxs-lookup"><span data-stu-id="3ef75-2216">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="3ef75-2217">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3ef75-2217">Az.Batch</span></span>
* <span data-ttu-id="3ef75-2218">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2218">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="3ef75-2219">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3ef75-2219">Az.Cdn</span></span>
* <span data-ttu-id="3ef75-2220">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2220">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3ef75-2221">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-2221">Az.CognitiveServices</span></span>
* <span data-ttu-id="3ef75-2222">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2222">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3ef75-2223">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-2223">Az.Compute</span></span>
* <span data-ttu-id="3ef75-2224">Az AEM telepítési kapcsolatos problémák megoldásához, ha a lemezek erőforrás-azonosítók kisbetűs resourcegroups volt az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="3ef75-2224">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="3ef75-2225">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2225">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3ef75-2226">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="3ef75-2226">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3ef75-2227">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3ef75-2227">Az.DataFactory</span></span>
* <span data-ttu-id="3ef75-2228">Adjon hozzá SsisProperties, ha a NodeCount felügyelt integrációs modul nem null értékű.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2228">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3ef75-2229">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3ef75-2229">Az.DataLakeStore</span></span>
* <span data-ttu-id="3ef75-2230">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2230">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="3ef75-2231">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3ef75-2231">Az.EventGrid</span></span>
* <span data-ttu-id="3ef75-2232">A Súgó szöveg jelzi, hogy erőforrásokat kell létrehozni a create/update eseményt előfizetés parancsmagok használata előtt végpont frissítése.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2232">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3ef75-2233">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3ef75-2233">Az.EventHub</span></span>
* <span data-ttu-id="3ef75-2234">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="3ef75-2234">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="3ef75-2235">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3ef75-2235">Az.HDInsight</span></span>
* <span data-ttu-id="3ef75-2236">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2236">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3ef75-2237">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3ef75-2237">Az.IotHub</span></span>
* <span data-ttu-id="3ef75-2238">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2238">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3ef75-2239">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3ef75-2239">Az.KeyVault</span></span>
* <span data-ttu-id="3ef75-2240">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2240">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3ef75-2241">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="3ef75-2241">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="3ef75-2242">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="3ef75-2242">Az.MachineLearning</span></span>
* <span data-ttu-id="3ef75-2243">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2243">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="3ef75-2244">Az.Media</span><span class="sxs-lookup"><span data-stu-id="3ef75-2244">Az.Media</span></span>
* <span data-ttu-id="3ef75-2245">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2245">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3ef75-2246">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3ef75-2246">Az.Monitor</span></span>
  * <span data-ttu-id="3ef75-2247">Riasztási szabály (nem klasszikus) GenV2 mérőszám-alapú új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3ef75-2247">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="3ef75-2248">Új AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="3ef75-2248">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="3ef75-2249">Új AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="3ef75-2249">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="3ef75-2250">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="3ef75-2250">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="3ef75-2251">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="3ef75-2251">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="3ef75-2252">Adjon hozzá AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="3ef75-2252">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="3ef75-2253">Frissített verzió 0.22.0-preview figyelő SDK</span><span class="sxs-lookup"><span data-stu-id="3ef75-2253">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3ef75-2254">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-2254">Az.Network</span></span>
* <span data-ttu-id="3ef75-2255">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2255">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3ef75-2256">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="3ef75-2256">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="3ef75-2257">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="3ef75-2257">Az.NotificationHubs</span></span>
* <span data-ttu-id="3ef75-2258">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2258">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3ef75-2259">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3ef75-2259">Az.OperationalInsights</span></span>
* <span data-ttu-id="3ef75-2260">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2260">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="3ef75-2261">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="3ef75-2261">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="3ef75-2262">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2262">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3ef75-2263">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-2263">Az.RecoveryServices</span></span>
* <span data-ttu-id="3ef75-2264">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2264">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3ef75-2265">Frissített táblázatos formában az SQL azure-beli virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="3ef75-2265">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="3ef75-2266">A hozzáadott alternatív módszert AzureFileShare hely beolvasása</span><span class="sxs-lookup"><span data-stu-id="3ef75-2266">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="3ef75-2267">Frissített ScheduleRunDays SchedulePolicy objektumban időzóna szerint</span><span class="sxs-lookup"><span data-stu-id="3ef75-2267">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="3ef75-2268">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="3ef75-2268">Az.RedisCache</span></span>
* <span data-ttu-id="3ef75-2269">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2269">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3ef75-2270">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-2270">Az.Resources</span></span>
* <span data-ttu-id="3ef75-2271">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="3ef75-2271">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="3ef75-2272">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-2272">Az.Sql</span></span>
* <span data-ttu-id="3ef75-2273">Cserélje le a függőségi figyelő SDK közös kód</span><span class="sxs-lookup"><span data-stu-id="3ef75-2273">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="3ef75-2274">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2274">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3ef75-2275">Továbbfejlesztett folyamat, amely több oszlop osztályozási.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2275">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="3ef75-2276">Termékváltozat tulajdonságok (termékváltozat neve, családi, kapacitás) válasz a Get-AzSqlServerServiceObjective és formátum táblaként alapértelmezés szerint tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2276">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="3ef75-2277">Lehetővé teszi a Get-AzSqlServerServiceObjective anélkül, hogy a régióban egy már létező kiszolgáló hely alapján.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2277">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="3ef75-2278">Hozzon létre felügyelt példányt az időzóna-paraméter támogatása.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2278">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="3ef75-2279">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="3ef75-2279">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3ef75-2280">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3ef75-2280">Az.Websites</span></span>
* <span data-ttu-id="3ef75-2281">a Set-AzWebApp és a Set-AzWebAppSlot távolítja el a címkék a végrehajtási javítások</span><span class="sxs-lookup"><span data-stu-id="3ef75-2281">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="3ef75-2282">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2282">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3ef75-2283">A webhelyek SDK frissítése.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2283">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="3ef75-2284">A AdminSiteName tulajdonság PSAppServicePlan eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2284">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="3ef75-2285">1.7.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="3ef75-2285">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="3ef75-2286">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="3ef75-2286">Highlights since the last major release</span></span>
* <span data-ttu-id="3ef75-2287">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="3ef75-2287">General availability of `Az` module</span></span>
* <span data-ttu-id="3ef75-2288">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="3ef75-2288">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="3ef75-2289">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="3ef75-2289">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="3ef75-2290">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-2290">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="3ef75-2291">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-2291">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="3ef75-2292">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-2292">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="3ef75-2293">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-2293">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3ef75-2294">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3ef75-2294">Az.Accounts</span></span>
* <span data-ttu-id="3ef75-2295">Frissített Add-AzEnvironment és Set-AzEnvironment parancsmag az AzureAnalysisServicesEndpointResourceId paraméter elfogadásához</span><span class="sxs-lookup"><span data-stu-id="3ef75-2295">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="3ef75-2296">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-2296">Az.AnalysisServices</span></span>
* <span data-ttu-id="3ef75-2297">ServiceClient használata DataPlane-parancsmagokban és az eredeti hitelesítési logika eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-2297">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="3ef75-2298">Az Add-AzureASAccount burkolóként való megadása a Connect-AzAccount számára a kompatibilitástörő változás elkerüléséhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-2298">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3ef75-2299">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3ef75-2299">Az.Automation</span></span>
* <span data-ttu-id="3ef75-2300">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag belefoglalásokat érintő hibája.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2300">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="3ef75-2301">Az IncludedKbNumber és az IncludedPackageNameMask paraméter mostantól működőképes.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2301">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="3ef75-2302">Hibajavítás az Azure Automation frissítéskezelési dinamikus csoportja esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-2302">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3ef75-2303">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-2303">Az.Compute</span></span>
* <span data-ttu-id="3ef75-2304">HyperVGeneration paraméter hozzáadása a New-AzDiskConfig és a New-AzSnapshotConfig parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-2304">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="3ef75-2305">Virtuális gépek más bérlők katalógus-rendszerképével való létrehozásának engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2305">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="3ef75-2306">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3ef75-2306">Az.ContainerInstance</span></span>
* <span data-ttu-id="3ef75-2307">Ki lett javítva a New-AzContainerGroup üres záró argumentumot hozzáadó -Command paraméterével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="3ef75-2307">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3ef75-2308">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3ef75-2308">Az.DataFactory</span></span>
* <span data-ttu-id="3ef75-2309">Az ADF .Net SDK verziója 3.0.2-re frissült.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2309">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="3ef75-2310">A Set-AzDataFactoryV2 parancsmag a RepoConfiguration beállításaihoz tartozó kiegészítő paraméterekkel lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2310">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3ef75-2311">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-2311">Az.Resources</span></span>
* <span data-ttu-id="3ef75-2312">Továbbfejlesztett szolgáltatókezelés a Get-AzResource esetében, -ResourceId vagy -ResourceGroupName, -Name és -ResourceType paraméterek megadásakor</span><span class="sxs-lookup"><span data-stu-id="3ef75-2312">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="3ef75-2313">Továbbfejlesztett hibakezelés a Test-AzDeployment és a Test-AzResourceGroupDeployment esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-2313">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="3ef75-2314">A hibákat nem a telepítés ellenőrzése során kezeli, hanem a parancs kimenetébe foglalja bele</span><span class="sxs-lookup"><span data-stu-id="3ef75-2314">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="3ef75-2315">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="3ef75-2315">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="3ef75-2316">-IgnoreDynamicParameters kapcsolóparaméter hozzáadása telepítési parancsmagokhoz a rendszer által feltett kérdések szkriptekben és feladatokban való mellőzéséhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-2316">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="3ef75-2317">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="3ef75-2317">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="3ef75-2318">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-2318">Az.Sql</span></span>
* <span data-ttu-id="3ef75-2319">Adatbázisadat-besorolás támogatása.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2319">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3ef75-2320">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3ef75-2320">Az.Storage</span></span>
* <span data-ttu-id="3ef75-2321">Részletes hibaüzenet megjelenítése Storage-környezet -UseConnectedAccount paraméterrel történő létrehozásakor az Azure-fiókba való bejelentkezés nélkül</span><span class="sxs-lookup"><span data-stu-id="3ef75-2321">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="3ef75-2322">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3ef75-2322">New-AzStorageContext</span></span>
* <span data-ttu-id="3ef75-2323">Adott Storage-fiók Blob service-tulajdonságai kezelésének támogatása Management plane API-val</span><span class="sxs-lookup"><span data-stu-id="3ef75-2323">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="3ef75-2324">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="3ef75-2324">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="3ef75-2325">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="3ef75-2325">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="3ef75-2326">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3ef75-2326">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="3ef75-2327">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3ef75-2327">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="3ef75-2328">Az -AsJob támogatása blobok és fájlok feltöltéséhez, valamint parancsmagok letöltéséhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-2328">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="3ef75-2329">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3ef75-2329">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="3ef75-2330">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3ef75-2330">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="3ef75-2331">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3ef75-2331">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="3ef75-2332">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3ef75-2332">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="3ef75-2333">1.6.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="3ef75-2333">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="3ef75-2334">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="3ef75-2334">Highlights since the last major release</span></span>
* <span data-ttu-id="3ef75-2335">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="3ef75-2335">General availability of `Az` module</span></span>
* <span data-ttu-id="3ef75-2336">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="3ef75-2336">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="3ef75-2337">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="3ef75-2337">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="3ef75-2338">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-2338">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="3ef75-2339">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-2339">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="3ef75-2340">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-2340">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="3ef75-2341">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-2341">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3ef75-2342">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3ef75-2342">Az.Automation</span></span>
* <span data-ttu-id="3ef75-2343">Az Azure Automation frissítéskezelése módosult, hogy támogassa az alábbi új funkciókat:</span><span class="sxs-lookup"><span data-stu-id="3ef75-2343">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="3ef75-2344">Dinamikus csoportosítás</span><span class="sxs-lookup"><span data-stu-id="3ef75-2344">Dynamic grouping</span></span>
    * <span data-ttu-id="3ef75-2345">Előzetesen és utólagosan futtatandó szkriptek</span><span class="sxs-lookup"><span data-stu-id="3ef75-2345">Pre-Post script</span></span>
    * <span data-ttu-id="3ef75-2346">Újraindítási beállítás</span><span class="sxs-lookup"><span data-stu-id="3ef75-2346">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3ef75-2347">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-2347">Az.Compute</span></span>
* <span data-ttu-id="3ef75-2348">Ki lett javítva az elérési útvonal feloldásával kapcsolatos hiba a Get-AzVmBootDiagnosticsData esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-2348">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="3ef75-2349">A Compute ügyfélkódtár frissült a 25.0.0 verzióra</span><span class="sxs-lookup"><span data-stu-id="3ef75-2349">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3ef75-2350">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3ef75-2350">Az.KeyVault</span></span>
* <span data-ttu-id="3ef75-2351">Helyettesítő karakterek támogatásának hozzáadása a KeyVault-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-2351">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3ef75-2352">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-2352">Az.Network</span></span>
* <span data-ttu-id="3ef75-2353">Az Intelligens veszélyforrás-felderítés támogatásának hozzáadása az Azure Firewallhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-2353">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="3ef75-2354">Az Application Gateway-tűzfalszabályzat legfelső szintű erőforrása és egyéni szabályok hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-2354">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3ef75-2355">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-2355">Az.RecoveryServices</span></span>
* <span data-ttu-id="3ef75-2356">A SnapshotRetentionInDays hozzáadása az Azure-beli virtuális gépek szabályzatához az azonnali RP támogatása érdekében</span><span class="sxs-lookup"><span data-stu-id="3ef75-2356">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="3ef75-2357">Folyamat támogatásának hozzáadása a regisztrációtörlési tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-2357">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="3ef75-2358">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-2358">Az.Resources</span></span>
* <span data-ttu-id="3ef75-2359">Helyettesítő karakterek támogatásának hozzáadása a Get-AzResource és Get-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-2359">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="3ef75-2360">Az ARM általános hívása esetén használt hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="3ef75-2360">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="3ef75-2361">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-2361">Az.Sql</span></span>
* <span data-ttu-id="3ef75-2362">A Fenyegetésészlelés parancsmagjainak paramétere (ExcludeDetectionType) a DetectionType helyett string[] lett, hogy a jövőben is használható legyen az új DetectionType-ok hozzáadásakor, valamint az automatikus kitöltés támogatása érdekében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2362">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3ef75-2363">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3ef75-2363">Az.Storage</span></span>
* <span data-ttu-id="3ef75-2364">Tárfiók felügyeleti szabályzata lekérésének/beállításának/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="3ef75-2364">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="3ef75-2365">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="3ef75-2365">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="3ef75-2366">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="3ef75-2366">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="3ef75-2367">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="3ef75-2367">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="3ef75-2368">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="3ef75-2368">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="3ef75-2369">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="3ef75-2369">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="3ef75-2370">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="3ef75-2370">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3ef75-2371">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3ef75-2371">Az.Websites</span></span>
* <span data-ttu-id="3ef75-2372">Ki lett javítva az ARM-sablon azon hibája, amely miatt meghiúsul az összes tárolóhely a New-AzWebApp - IncludeSourceWebAppSlots használatával történő klónozása</span><span class="sxs-lookup"><span data-stu-id="3ef75-2372">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="3ef75-2373">1.5.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="3ef75-2373">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3ef75-2374">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3ef75-2374">Az.Accounts</span></span>
* <span data-ttu-id="3ef75-2375">A Register-AzModule parancs hozzáadása az AutoRest által létrehozott parancsmagok támogatásához</span><span class="sxs-lookup"><span data-stu-id="3ef75-2375">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="3ef75-2376">A Connect-AzAccount példáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="3ef75-2376">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3ef75-2377">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3ef75-2377">Az.Automation</span></span>
* <span data-ttu-id="3ef75-2378">A bizonyos havi ütemezések lekérésekor jelentkező hiba kijavítva számos Azure Automation-parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-2378">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="3ef75-2379">Ki lett javítva a hiba, amely miatt a Get-AzAutomationDscNode csak az első 20 csomópontot adta vissza.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2379">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="3ef75-2380">Most már az összes csomópontot visszaadja</span><span class="sxs-lookup"><span data-stu-id="3ef75-2380">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="3ef75-2381">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3ef75-2381">Az.Cdn</span></span>
* <span data-ttu-id="3ef75-2382">Új Powershell-parancsmagok hozzáadva az Egyéni tartományi Https engedélyezése/letiltása szolgáltatáshoz, a régiek elavultak</span><span class="sxs-lookup"><span data-stu-id="3ef75-2382">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3ef75-2383">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-2383">Az.Compute</span></span>
* <span data-ttu-id="3ef75-2384">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-2384">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3ef75-2385">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3ef75-2385">Az.DataFactory</span></span>
* <span data-ttu-id="3ef75-2386">Az ADF .Net SDK verziója 3.0.1-re frissült</span><span class="sxs-lookup"><span data-stu-id="3ef75-2386">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="3ef75-2387">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3ef75-2387">Az.LogicApp</span></span>
* <span data-ttu-id="3ef75-2388">Ki lett javítva a hiba, amely miatt a ListWorkflows csak az eredmények első oldalát kérte le</span><span class="sxs-lookup"><span data-stu-id="3ef75-2388">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3ef75-2389">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-2389">Az.Network</span></span>
* <span data-ttu-id="3ef75-2390">Helyettesítő karakterek támogatásának hozzáadása a Network-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-2390">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3ef75-2391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-2391">Az.RecoveryServices</span></span>
* <span data-ttu-id="3ef75-2392">Azure-beli virtuális gépen futtatott SQL Server támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="3ef75-2392">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="3ef75-2393">SDK-frissítés</span><span class="sxs-lookup"><span data-stu-id="3ef75-2393">SDK Update</span></span>
* <span data-ttu-id="3ef75-2394">VMappContainer ellenőrzés eltávolítva a Get-ProtectableItem parancsmagból</span><span class="sxs-lookup"><span data-stu-id="3ef75-2394">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="3ef75-2395">Name és ServerName paraméterek hozzáadva a Get-ProtectableItem parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-2395">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="3ef75-2396">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-2396">Az.Resources</span></span>
* <span data-ttu-id="3ef75-2397">`-TemplateObject` paraméter hozzáadva az üzembe helyező parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-2397">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="3ef75-2398">További információ: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="3ef75-2398">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="3ef75-2399">Ki lett javítva a hiba, amely akkor jelentkezett, amikor a(z) `Get-AzResource` eredménye át lett irányítva a következőbe: `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="3ef75-2399">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="3ef75-2400">További információ: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="3ef75-2400">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="3ef75-2401">Ki lett javítva a JSON-adattípus módosításával kapcsolatos probléma, amely a(z) `Set-AzResource` futtatásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="3ef75-2401">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="3ef75-2402">További információ: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="3ef75-2402">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="3ef75-2403">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-2403">Az.Sql</span></span>
* <span data-ttu-id="3ef75-2404">Az AuditingEndpointsCommunicator frissítése.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2404">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="3ef75-2405">Ki lett javítva az új diagnosztikai beállítások létrehozásakor jelentkező ritka eset viselkedése.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2405">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3ef75-2406">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3ef75-2406">Az.Storage</span></span>
* <span data-ttu-id="3ef75-2407">A BlockBlobStorage altípus támogatása a Storage-fiók létrehozásakor      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3ef75-2407">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="3ef75-2408">1.4.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="3ef75-2408">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="3ef75-2409">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-2409">Az.AnalysisServices</span></span>
* <span data-ttu-id="3ef75-2410">Az AddAzureASAccount parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="3ef75-2410">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3ef75-2411">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3ef75-2411">Az.Automation</span></span>
* <span data-ttu-id="3ef75-2412">Az Import-AzAutomationDscNodeConfiguration súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="3ef75-2412">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="3ef75-2413">A konfigurációnév-ellenőrzés hozzáadva az Import-AzAutomationDscConfiguration parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-2413">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="3ef75-2414">Továbbfejlesztett hibakezelés az Import-AzAutomationDscConfiguration parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-2414">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3ef75-2415">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-2415">Az.CognitiveServices</span></span>
* <span data-ttu-id="3ef75-2416">A CustomSubdomainName új választható paraméterként hozzáadva a New-AzCognitiveServicesAccount parancsmaghoz, amellyel altartomány adható meg az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2416">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3ef75-2417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-2417">Az.Compute</span></span>
* <span data-ttu-id="3ef75-2418">Kijavítva az azonosító paraméterkészleteivel kapcsolatos probléma</span><span class="sxs-lookup"><span data-stu-id="3ef75-2418">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="3ef75-2419">Frissült a Get-AzVMExtension parancsmag, hogy az összes telepített bővítményt listázza, ha a Name paraméter nincs megadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-2419">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="3ef75-2420">A Tag és a ResourceId paraméterek hozzáadva az Update-AzImage parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-2420">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="3ef75-2421">A Get-AzVmssVM példányazonosító nélkül, az InstanceView használatával példánynézetben listázni tudja a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2421">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3ef75-2422">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3ef75-2422">Az.DataLakeStore</span></span>
* <span data-ttu-id="3ef75-2423">Parancsmagok hozzáadása a törölt ADL-elemek enumerálásához és visszaállításához</span><span class="sxs-lookup"><span data-stu-id="3ef75-2423">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3ef75-2424">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3ef75-2424">Az.EventHub</span></span>
* <span data-ttu-id="3ef75-2425">Új SkipEmptyArchives logikai tulajdonság hozzáadva az üres archívumok kihagyásához az Eventhub CaptureDescription osztályában</span><span class="sxs-lookup"><span data-stu-id="3ef75-2425">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3ef75-2426">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3ef75-2426">Az.KeyVault</span></span>
* <span data-ttu-id="3ef75-2427">A Set-AzKeyVaultSecret címkézésének kijavítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-2427">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="3ef75-2428">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3ef75-2428">Az.LogicApp</span></span>
* <span data-ttu-id="3ef75-2429">Hozzáadva az integrációs fiókok alapszintű termékváltozatában</span><span class="sxs-lookup"><span data-stu-id="3ef75-2429">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="3ef75-2430">Hozzáadva az XSLT 2.0-ban, az XSLT 3.0-ban és a Liquid leképezéstípusok esetén</span><span class="sxs-lookup"><span data-stu-id="3ef75-2430">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="3ef75-2431">Új parancsmagok az integrációs fiók szerelvényeihez</span><span class="sxs-lookup"><span data-stu-id="3ef75-2431">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="3ef75-2432">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="3ef75-2432">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="3ef75-2433">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="3ef75-2433">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="3ef75-2434">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="3ef75-2434">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="3ef75-2435">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="3ef75-2435">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="3ef75-2436">Új parancsmagok az integrációs fiók kötegkonfigurációjához</span><span class="sxs-lookup"><span data-stu-id="3ef75-2436">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="3ef75-2437">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ef75-2437">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="3ef75-2438">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ef75-2438">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="3ef75-2439">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ef75-2439">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="3ef75-2440">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ef75-2440">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="3ef75-2441">A Logic Apps SDK frissítése a 4.1.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="3ef75-2441">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3ef75-2442">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3ef75-2442">Az.Monitor</span></span>
* <span data-ttu-id="3ef75-2443">A Get-AzMetric súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="3ef75-2443">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3ef75-2444">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-2444">Az.Network</span></span>
* <span data-ttu-id="3ef75-2445">Az Add-AzApplicationGatewayCustomError súgójában lévő példa frissítése</span><span class="sxs-lookup"><span data-stu-id="3ef75-2445">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3ef75-2446">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3ef75-2446">Az.OperationalInsights</span></span>
* <span data-ttu-id="3ef75-2447">Kibővített támogatás a New és a Get ApplicationInsights adatforráshoz.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2447">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="3ef75-2448">Új „ApplicationInsights” altípus hozzáadva az adott munkaterület Get specific és Get all Application Insights-adatforrásainak támogatásához.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2448">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="3ef75-2449">A New-AzOperationalInsightsApplicationInsightsDataSource parancsmag hozzáadva adatforrás létrehozásához a következő Application Insights-erőforrásparaméterekkel: subscriptionId, resourceGroupName és name.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2449">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3ef75-2450">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-2450">Az.Resources</span></span>
* <span data-ttu-id="3ef75-2451">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="3ef75-2451">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="3ef75-2452">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="3ef75-2452">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="3ef75-2453">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="3ef75-2453">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="3ef75-2454">Ki lett javítva a KeyCredentials ismételt létrehozását megakadályozó hiba</span><span class="sxs-lookup"><span data-stu-id="3ef75-2454">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="3ef75-2455">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-2455">Az.Sql</span></span>
* <span data-ttu-id="3ef75-2456">Rugalmas SQL DB-skálázási szint támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-2456">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="3ef75-2457">Ki lett javítva az a hiba, hogy a visszaállítási kérésben szereplő szükségtelen tulajdonságok megadása miatt a visszaállítás esetenként meghiúsult</span><span class="sxs-lookup"><span data-stu-id="3ef75-2457">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3ef75-2458">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3ef75-2458">Az.Websites</span></span>
* <span data-ttu-id="3ef75-2459">A Get-AzWebAppSlotMetrics példájának javítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-2459">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="3ef75-2460">1.3.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="3ef75-2460">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3ef75-2461">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3ef75-2461">Az.Accounts</span></span>
* <span data-ttu-id="3ef75-2462">Frissítés a ClientRuntime legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="3ef75-2462">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="3ef75-2463">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-2463">Az.AnalysisServices</span></span>
<span data-ttu-id="3ef75-2464">Az Az.AnalysisServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2464">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3ef75-2465">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-2465">Az.Compute</span></span>
* <span data-ttu-id="3ef75-2466">AEM-bővítmény: Mostantól az UltraSSD, valamint a P60, P70 és P80 lemezek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2466">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="3ef75-2467">A Set-AzVMBootDiagnostics súgóleírása frissült.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2467">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="3ef75-2468">Az Update-AzImage súgóleírása és példája frissült.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2468">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3ef75-2469">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-2469">Az.RecoveryServices</span></span>
<span data-ttu-id="3ef75-2470">Az Az.RecoveryServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2470">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3ef75-2471">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-2471">Az.Resources</span></span>
* <span data-ttu-id="3ef75-2472">Az erőforráscsoportok címkézése ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2472">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="3ef75-2473">További információ: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="3ef75-2473">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="3ef75-2474">Ki lett javítva az a hiba, amikor a `Get-AzureRmRoleAssignment` nem vette figyelembe az -ErrorAction paramétert.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2474">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="3ef75-2475">További információ: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="3ef75-2475">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="3ef75-2476">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-2476">Az.Sql</span></span>
* <span data-ttu-id="3ef75-2477">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-2477">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="3ef75-2478">Ki lett javítva az a hiba, amikor az Azure-fiókba való bejelentkezés hiánya nullref kivételt eredményezett az SQL-parancsmagok végrehajtásakor.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2478">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="3ef75-2479">A nullref kivétel ki lett javítva a Get-AzSqlCapabilityben.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2479">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="3ef75-2480">1.2.1 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="3ef75-2480">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3ef75-2481">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3ef75-2481">Az.Accounts</span></span>
* <span data-ttu-id="3ef75-2482">A hitelesítés megfelelő verziójával rendelkező kiadás</span><span class="sxs-lookup"><span data-stu-id="3ef75-2482">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="3ef75-2483">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-2483">Az.AnalysisServices</span></span>
* <span data-ttu-id="3ef75-2484">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="3ef75-2484">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3ef75-2485">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-2485">Az.RecoveryServices</span></span>
* <span data-ttu-id="3ef75-2486">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="3ef75-2486">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="3ef75-2487">1.2.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="3ef75-2487">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3ef75-2488">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3ef75-2488">Az.Accounts</span></span>
* <span data-ttu-id="3ef75-2489">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-2489">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="3ef75-2490">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2490">Update incorrect online help URLs</span></span>
* <span data-ttu-id="3ef75-2491">Az Uninstall-AzureRm figyelmeztető üzenete hozzáadva a PS Core-ban</span><span class="sxs-lookup"><span data-stu-id="3ef75-2491">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="3ef75-2492">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="3ef75-2492">Az.Aks</span></span>
* <span data-ttu-id="3ef75-2493">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2493">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3ef75-2494">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3ef75-2494">Az.Automation</span></span>
* <span data-ttu-id="3ef75-2495">Mostantól támogatottak a Python 2-runbookok.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2495">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="3ef75-2496">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2496">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="3ef75-2497">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3ef75-2497">Az.Cdn</span></span>
* <span data-ttu-id="3ef75-2498">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2498">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3ef75-2499">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-2499">Az.Compute</span></span>
* <span data-ttu-id="3ef75-2500">Az Invoke-AzVMReimage parancsmag hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2500">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="3ef75-2501">A TempDisk paraméter hozzá lett adva a Set-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2501">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="3ef75-2502">A New-AzVM figyelmeztető üzenete ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2502">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="3ef75-2503">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3ef75-2503">Az.ContainerRegistry</span></span>
* <span data-ttu-id="3ef75-2504">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2504">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3ef75-2505">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3ef75-2505">Az.DataFactory</span></span>
* <span data-ttu-id="3ef75-2506">Az ADF .Net SDK verziója 3.0.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2506">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3ef75-2507">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3ef75-2507">Az.DataLakeStore</span></span>
* <span data-ttu-id="3ef75-2508">Ki lett javítva az ADLS-végponttal kapcsolatos probléma az MSI használatakor.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2508">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="3ef75-2509">További információ: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="3ef75-2509">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="3ef75-2510">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2510">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3ef75-2511">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3ef75-2511">Az.IotHub</span></span>
* <span data-ttu-id="3ef75-2512">Az Encoding formátum hozzá lett adva az Add-IotHubRoutingEndpoint parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2512">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3ef75-2513">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3ef75-2513">Az.KeyVault</span></span>
* <span data-ttu-id="3ef75-2514">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2514">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3ef75-2515">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-2515">Az.Network</span></span>
* <span data-ttu-id="3ef75-2516">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2516">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="3ef75-2517">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-2517">Az.Resources</span></span>
* <span data-ttu-id="3ef75-2518">A helytelen példák ki lettek javítva a New-AzADAppCredential és a New-AzADSpCredential referenciadokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2518">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="3ef75-2519">Ki lett javítva az a hiba, amikor a -TemplateFile paraméter nem lett feloldva az erőforráscsoportokat üzembe helyező parancsmagok végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2519">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="3ef75-2520">Az.Resources: A New-AzureRmPolicyDefinition -Mode alapértelmezett értékének dokumentációja ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2520">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="3ef75-2521">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="3ef75-2521">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="3ef75-2522">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="3ef75-2522">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="3ef75-2523">Ki lett javítva a „PSResourceGroupDeployment” objektum formázásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2523">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="3ef75-2524">További információ: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="3ef75-2524">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3ef75-2525">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3ef75-2525">Az.ServiceFabric</span></span>
* <span data-ttu-id="3ef75-2526">Visszaállítás a VMSS-modell tanúsítványának hozzáadásakor bekövetkező kivétel-visszaadás esetén; javított hiba: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2526">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="3ef75-2527">Bizonyos hibaüzenetek ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2527">Fix some error messages.</span></span>
* <span data-ttu-id="3ef75-2528">Ki lett javítva az alapértelmezett ARM-sablonnal való fürtlétrehozás a New-AzServiceFabriCluster esetében, amely nem működött az Az-ba történő migrálással.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2528">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="3ef75-2529">Ki lett javítva a fürt-/alkalmazástanúsítvány létrehozása, így mostantól csak a fürtnek megfelelő virtuálisgép-méretezési csoportokhoz (Virtual Machine Scale Sets) lesznek hozzáadva, a fürtazonosító bővítményben való ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2529">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="3ef75-2530">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="3ef75-2530">Az.SignalR</span></span>
* <span data-ttu-id="3ef75-2531">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2531">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="3ef75-2532">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-2532">Az.Sql</span></span>
* <span data-ttu-id="3ef75-2533">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2533">Update incorrect online help URLs</span></span>
* <span data-ttu-id="3ef75-2534">A LicenseType paraméter paraméterleírása frissítve lett a lehetséges értékekkel.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2534">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="3ef75-2535">Ki lett javítva az a hiba, amikor egy felügyelt példány identitásának frissítése nem működött, ha az volt az egyetlen frissített tulajdonság.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2535">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="3ef75-2536">Egyéni rendezések támogatása a felügyelt példányokon</span><span class="sxs-lookup"><span data-stu-id="3ef75-2536">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3ef75-2537">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3ef75-2537">Az.Storage</span></span>
* <span data-ttu-id="3ef75-2538">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2538">Update incorrect online help URLs</span></span>
* <span data-ttu-id="3ef75-2539">Részletes hibaüzenet megjelenítése klasszikus naplózás/metrika get/set műveletei esetében a prémium szintű Storage-fiókon, mivel a prémium szintű Storage-fiók nem támogatja a klasszikus naplózást/metrikát.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2539">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="3ef75-2540">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="3ef75-2540">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="3ef75-2541">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="3ef75-2541">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="3ef75-2542">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="3ef75-2542">Az.TrafficManager</span></span>
* <span data-ttu-id="3ef75-2543">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2543">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3ef75-2544">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3ef75-2544">Az.Websites</span></span>
* <span data-ttu-id="3ef75-2545">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2545">Update incorrect online help URLs</span></span>
* <span data-ttu-id="3ef75-2546">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól a megfelelő erőforráscsoportba és helyre tölti fel a tanúsítványt, ha az alkalmazás ASE-n üzemel.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2546">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="3ef75-2547">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól nem írja felül a címkéket SSL-tanúsítvány alkalmazáshoz való kötésekor.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2547">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="3ef75-2548">1.1.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="3ef75-2548">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3ef75-2549">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3ef75-2549">Az.Accounts</span></span>
* <span data-ttu-id="3ef75-2550">A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-2550">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3ef75-2551">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-2551">Az.Compute</span></span>
* <span data-ttu-id="3ef75-2552">A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni</span><span class="sxs-lookup"><span data-stu-id="3ef75-2552">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="3ef75-2553">Frissült az azonosító leírása a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="3ef75-2553">Updated the description of ID in help files</span></span>
* <span data-ttu-id="3ef75-2554">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="3ef75-2554">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3ef75-2555">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3ef75-2555">Az.DataLakeStore</span></span>
* <span data-ttu-id="3ef75-2556">A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2556">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="3ef75-2557">A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva</span><span class="sxs-lookup"><span data-stu-id="3ef75-2557">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="3ef75-2558">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3ef75-2558">Az.EventGrid</span></span>
* <span data-ttu-id="3ef75-2559">Frissítve a 2019-01-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2559">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="3ef75-2560">A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához</span><span class="sxs-lookup"><span data-stu-id="3ef75-2560">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="3ef75-2561">New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="3ef75-2561">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="3ef75-2562">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="3ef75-2562">Event Time-To-Live,</span></span>
        - <span data-ttu-id="3ef75-2563">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="3ef75-2563">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="3ef75-2564">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2564">Dead letter endpoint.</span></span>
    - <span data-ttu-id="3ef75-2565">Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="3ef75-2565">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="3ef75-2566">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="3ef75-2566">Event Time-To-Live,</span></span>
        - <span data-ttu-id="3ef75-2567">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="3ef75-2567">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="3ef75-2568">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2568">Dead letter endpoint.</span></span>
* <span data-ttu-id="3ef75-2569">Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2569">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="3ef75-2570">Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2570">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3ef75-2571">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3ef75-2571">Az.IotHub</span></span>
* <span data-ttu-id="3ef75-2572">Frissítve az IoT Hub SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="3ef75-2572">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="3ef75-2573">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3ef75-2573">Az.LogicApp</span></span>
* <span data-ttu-id="3ef75-2574">A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel</span><span class="sxs-lookup"><span data-stu-id="3ef75-2574">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="3ef75-2575">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-2575">Az.Resources</span></span>
* <span data-ttu-id="3ef75-2576">Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="3ef75-2576">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="3ef75-2577">További információ: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="3ef75-2577">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="3ef75-2578">Ki lett javítva a -Custom paraméter kezelése a New/Set-AzPolicyDefinition parancsban</span><span class="sxs-lookup"><span data-stu-id="3ef75-2578">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="3ef75-2579">Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="3ef75-2579">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="3ef75-2580">A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-2580">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="3ef75-2581">További információ: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="3ef75-2581">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="3ef75-2582">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="3ef75-2582">Az.SignalR</span></span>
* <span data-ttu-id="3ef75-2583">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="3ef75-2583">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="3ef75-2584">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-2584">Az.Sql</span></span>
* <span data-ttu-id="3ef75-2585">A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2585">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3ef75-2586">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3ef75-2586">Az.Storage</span></span>
* <span data-ttu-id="3ef75-2587">A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva</span><span class="sxs-lookup"><span data-stu-id="3ef75-2587">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="3ef75-2588">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3ef75-2588">New-AzStorageContext</span></span>
* <span data-ttu-id="3ef75-2589">A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz</span><span class="sxs-lookup"><span data-stu-id="3ef75-2589">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="3ef75-2590">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="3ef75-2590">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3ef75-2591">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3ef75-2591">Az.Websites</span></span>
* <span data-ttu-id="3ef75-2592">Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban</span><span class="sxs-lookup"><span data-stu-id="3ef75-2592">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="3ef75-2593">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="3ef75-2593">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="3ef75-2594">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="3ef75-2594">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="3ef75-2595">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="3ef75-2595">General</span></span>

- <span data-ttu-id="3ef75-2596">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="3ef75-2596">General Availability of Az Module</span></span>
- <span data-ttu-id="3ef75-2597">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-2597">Online help for each module</span></span>
- <span data-ttu-id="3ef75-2598">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="3ef75-2598">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="3ef75-2599">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3ef75-2599">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="3ef75-2600">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3ef75-2600">Az.Accounts</span></span>
- <span data-ttu-id="3ef75-2601">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="3ef75-2601">Changed from Az.Profile</span></span>
- <span data-ttu-id="3ef75-2602">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-2602">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="3ef75-2603">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3ef75-2603">Az.ApiManagement</span></span>
- <span data-ttu-id="3ef75-2604">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="3ef75-2604">Fixes for #7002</span></span>
- <span data-ttu-id="3ef75-2605">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3ef75-2605">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="3ef75-2606">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3ef75-2606">Az.Batch</span></span>
- <span data-ttu-id="3ef75-2607">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2607">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="3ef75-2608">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2608">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="3ef75-2609">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3ef75-2609">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="3ef75-2610">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="3ef75-2610">Az.Billing</span></span>
- <span data-ttu-id="3ef75-2611">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2611">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="3ef75-2612">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-2612">Az.CognitivServices</span></span>
- <span data-ttu-id="3ef75-2613">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2613">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="3ef75-2614">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2614">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="3ef75-2615">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3ef75-2615">Az.ContainerInstance</span></span>
- <span data-ttu-id="3ef75-2616">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="3ef75-2616">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="3ef75-2617">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="3ef75-2617">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="3ef75-2618">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3ef75-2618">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="3ef75-2619">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3ef75-2619">Az.DataLakeStore</span></span>
- <span data-ttu-id="3ef75-2620">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3ef75-2620">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="3ef75-2621">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3ef75-2621">Az.Monitor</span></span>
- <span data-ttu-id="3ef75-2622">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3ef75-2622">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="3ef75-2623">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3ef75-2623">Az.KeyVault</span></span>
- <span data-ttu-id="3ef75-2624">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2624">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="3ef75-2625">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="3ef75-2625">Az.MachineLearning</span></span>
- <span data-ttu-id="3ef75-2626">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="3ef75-2626">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="3ef75-2627">Az.Media</span><span class="sxs-lookup"><span data-stu-id="3ef75-2627">Az.Media</span></span>
- <span data-ttu-id="3ef75-2628">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="3ef75-2628">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="3ef75-2629">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-2629">Az.Network</span></span>
<span data-ttu-id="3ef75-2630">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2630">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="3ef75-2631">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="3ef75-2631">New cmdlets added:</span></span>
        - <span data-ttu-id="3ef75-2632">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3ef75-2632">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3ef75-2633">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3ef75-2633">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3ef75-2634">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3ef75-2634">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3ef75-2635">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3ef75-2635">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3ef75-2636">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3ef75-2636">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3ef75-2637">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="3ef75-2637">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="3ef75-2638">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="3ef75-2638">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="3ef75-2639">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ef75-2639">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="3ef75-2640">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3ef75-2640">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="3ef75-2641">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3ef75-2641">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="3ef75-2642">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3ef75-2642">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="3ef75-2643">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3ef75-2643">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="3ef75-2644">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3ef75-2644">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="3ef75-2645">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3ef75-2645">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="3ef75-2646">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2646">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="3ef75-2647">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3ef75-2647">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="3ef75-2648">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3ef75-2648">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="3ef75-2649">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3ef75-2649">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="3ef75-2650">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3ef75-2650">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="3ef75-2651">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="3ef75-2651">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="3ef75-2652">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3ef75-2652">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="3ef75-2653">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3ef75-2653">Az.OperationalInsights</span></span>
- <span data-ttu-id="3ef75-2654">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3ef75-2654">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="3ef75-2655">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="3ef75-2655">Az.Profile</span></span>
- <span data-ttu-id="3ef75-2656">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3ef75-2656">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="3ef75-2657">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-2657">Az.RecoveryServices</span></span>
- <span data-ttu-id="3ef75-2658">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3ef75-2658">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="3ef75-2659">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-2659">Az.Resources</span></span>
- <span data-ttu-id="3ef75-2660">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3ef75-2660">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="3ef75-2661">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3ef75-2661">Az.ServiceFabric</span></span>
- <span data-ttu-id="3ef75-2662">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="3ef75-2662">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="3ef75-2663">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3ef75-2663">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="3ef75-2664">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="3ef75-2664">Az.SIgnalR</span></span>
- <span data-ttu-id="3ef75-2665">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="3ef75-2665">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="3ef75-2666">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-2666">Az.Sql</span></span>
- <span data-ttu-id="3ef75-2667">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-2667">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="3ef75-2668">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="3ef75-2668">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="3ef75-2669">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3ef75-2669">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="3ef75-2670">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3ef75-2670">Az.Storage</span></span>
- <span data-ttu-id="3ef75-2671">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3ef75-2671">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="3ef75-2672">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3ef75-2672">Az.Websites</span></span>
- <span data-ttu-id="3ef75-2673">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3ef75-2673">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="3ef75-2674">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="3ef75-2674">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="3ef75-2675">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="3ef75-2675">General</span></span>

* <span data-ttu-id="3ef75-2676">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-2676">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="3ef75-2677">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-2677">Az.Compute</span></span>

* <span data-ttu-id="3ef75-2678">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2678">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="3ef75-2679">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3ef75-2679">Az.DataLakeStore</span></span>

* <span data-ttu-id="3ef75-2680">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="3ef75-2680">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="3ef75-2681">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3ef75-2681">Az.FrontDoor</span></span>

* <span data-ttu-id="3ef75-2682">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-2682">Fixed some broken links</span></span>
    - <span data-ttu-id="3ef75-2683">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2683">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="3ef75-2684">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2684">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="3ef75-2685">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-2685">Az.RecoveryServices</span></span>

* <span data-ttu-id="3ef75-2686">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2686">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="3ef75-2687">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2687">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="3ef75-2688">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-2688">Az.Resources</span></span>

* <span data-ttu-id="3ef75-2689">[https://github.com/Azure/azure-powershell/issues/7679](https://github.com/Azure/azure-powershell/issues/7679 ) javítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-2689">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="3ef75-2690">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2690">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="3ef75-2691">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-2691">Az.Sql</span></span>

* <span data-ttu-id="3ef75-2692">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-2692">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="3ef75-2693">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="3ef75-2693">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="3ef75-2694">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2694">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="3ef75-2695">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3ef75-2695">Az.Storage</span></span>

* <span data-ttu-id="3ef75-2696">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-2696">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="3ef75-2697">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2697">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="3ef75-2698">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="3ef75-2698">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="3ef75-2699">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="3ef75-2699">Support Static Website configuration</span></span>
    - <span data-ttu-id="3ef75-2700">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="3ef75-2700">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="3ef75-2701">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="3ef75-2701">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="3ef75-2702">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3ef75-2702">Az.Websites</span></span>

* <span data-ttu-id="3ef75-2703">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3ef75-2703">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="3ef75-2704">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2704">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="3ef75-2705">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2705">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="3ef75-2706">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="3ef75-2706">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="3ef75-2707">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3ef75-2707">Az.ApiManagement</span></span>
* <span data-ttu-id="3ef75-2708">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2708">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="3ef75-2709">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3ef75-2709">Az.Automation</span></span>
* <span data-ttu-id="3ef75-2710">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2710">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="3ef75-2711">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2711">Added Update Management cmdlets</span></span>
* <span data-ttu-id="3ef75-2712">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2712">Added Source Control cmdlets</span></span>
* <span data-ttu-id="3ef75-2713">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2713">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="3ef75-2714">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2714">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="3ef75-2715">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-2715">Az.Compute</span></span>
* <span data-ttu-id="3ef75-2716">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2716">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="3ef75-2717">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2717">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="3ef75-2718">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3ef75-2718">Az.ContainerInstance</span></span>
* <span data-ttu-id="3ef75-2719">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2719">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="3ef75-2720">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="3ef75-2720">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="3ef75-2721">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2721">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="3ef75-2722">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-2722">Az.Network</span></span>
* <span data-ttu-id="3ef75-2723">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2723">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="3ef75-2724">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2724">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="3ef75-2725">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2725">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="3ef75-2726">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2726">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="3ef75-2727">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="3ef75-2727">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="3ef75-2728">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2728">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="3ef75-2729">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2729">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="3ef75-2730">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="3ef75-2730">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="3ef75-2731">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2731">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="3ef75-2732">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2732">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="3ef75-2733">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="3ef75-2733">Az.Relay</span></span>
* <span data-ttu-id="3ef75-2734">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2734">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="3ef75-2735">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-2735">Az.Resources</span></span>
* <span data-ttu-id="3ef75-2736">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2736">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="3ef75-2737">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2737">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="3ef75-2738">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2738">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="3ef75-2739">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3ef75-2739">Az.ServiceFabric</span></span>
* <span data-ttu-id="3ef75-2740">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2740">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="3ef75-2741">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-2741">Az.Sql</span></span>
* <span data-ttu-id="3ef75-2742">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2742">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="3ef75-2743">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3ef75-2743">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="3ef75-2744">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3ef75-2744">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="3ef75-2745">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3ef75-2745">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="3ef75-2746">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3ef75-2746">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="3ef75-2747">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="3ef75-2747">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="3ef75-2748">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="3ef75-2748">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="3ef75-2749">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="3ef75-2749">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="3ef75-2750">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="3ef75-2750">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="3ef75-2751">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2751">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="3ef75-2752">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2752">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="3ef75-2753">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2753">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="3ef75-2754">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2754">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="3ef75-2755">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2755">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="3ef75-2756">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2756">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="3ef75-2757">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2757">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="3ef75-2758">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2758">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="3ef75-2759">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="3ef75-2759">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="3ef75-2760">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="3ef75-2760">General</span></span>
* <span data-ttu-id="3ef75-2761">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2761">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="3ef75-2762">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="3ef75-2762">Az.Profile</span></span>
* <span data-ttu-id="3ef75-2763">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2763">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="3ef75-2764">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="3ef75-2764">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="3ef75-2765">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="3ef75-2765">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="3ef75-2766">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="3ef75-2766">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="3ef75-2767">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="3ef75-2767">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="3ef75-2768">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="3ef75-2768">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="3ef75-2769">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="3ef75-2769">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="3ef75-2770">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-2770">Az.CognitiveServices</span></span>
* <span data-ttu-id="3ef75-2771">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2771">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3ef75-2772">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-2772">Az.Compute</span></span>
* <span data-ttu-id="3ef75-2773">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="3ef75-2773">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="3ef75-2774">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="3ef75-2774">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="3ef75-2775">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2775">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3ef75-2776">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3ef75-2776">Az.DataLakeStore</span></span>
* <span data-ttu-id="3ef75-2777">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2777">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="3ef75-2778">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2778">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="3ef75-2779">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="3ef75-2779">Az.Insights</span></span>
* <span data-ttu-id="3ef75-2780">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="3ef75-2780">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="3ef75-2781">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="3ef75-2781">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="3ef75-2782">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="3ef75-2782">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="3ef75-2783">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="3ef75-2783">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3ef75-2784">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-2784">Az.Network</span></span>
* <span data-ttu-id="3ef75-2785">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="3ef75-2785">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="3ef75-2786">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="3ef75-2786">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="3ef75-2787">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="3ef75-2787">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="3ef75-2788">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="3ef75-2788">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="3ef75-2789">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="3ef75-2789">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="3ef75-2790">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="3ef75-2790">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="3ef75-2791">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="3ef75-2791">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3ef75-2792">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3ef75-2792">Az.PolicyInsights</span></span>
* <span data-ttu-id="3ef75-2793">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-2793">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="3ef75-2794">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-2794">Az.Resources</span></span>
* <span data-ttu-id="3ef75-2795">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402 ) javítása</span><span class="sxs-lookup"><span data-stu-id="3ef75-2795">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="3ef75-2796">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="3ef75-2796">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3ef75-2797">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3ef75-2797">Az.ServiceBus</span></span>
* <span data-ttu-id="3ef75-2798">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2798">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3ef75-2799">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3ef75-2799">Az.ServiceFabric</span></span>
* <span data-ttu-id="3ef75-2800">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2800">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="3ef75-2801">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="3ef75-2801">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="3ef75-2802">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="3ef75-2802">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="3ef75-2803">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="3ef75-2803">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="3ef75-2804">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2804">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="3ef75-2805">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="3ef75-2805">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="3ef75-2806">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="3ef75-2806">Az.Profile</span></span>
* <span data-ttu-id="3ef75-2807">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2807">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="3ef75-2808">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2808">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3ef75-2809">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-2809">Az.Compute</span></span>
* <span data-ttu-id="3ef75-2810">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2810">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="3ef75-2811">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2811">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3ef75-2812">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3ef75-2812">Az.DataLakeStore</span></span>
* <span data-ttu-id="3ef75-2813">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="3ef75-2813">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="3ef75-2814">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2814">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="3ef75-2815">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2815">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="3ef75-2816">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2816">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="3ef75-2817">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2817">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3ef75-2818">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-2818">Az.Network</span></span>
* <span data-ttu-id="3ef75-2819">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2819">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="3ef75-2820">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2820">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3ef75-2821">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-2821">Az.Resources</span></span>
* <span data-ttu-id="3ef75-2822">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="3ef75-2822">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="3ef75-2823">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2823">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="3ef75-2824">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="3ef75-2824">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="3ef75-2825">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="3ef75-2825">Azure.Storage</span></span>
* <span data-ttu-id="3ef75-2826">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="3ef75-2826">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="3ef75-2827">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="3ef75-2827">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="3ef75-2828">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="3ef75-2828">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="3ef75-2829">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2829">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="3ef75-2830">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="3ef75-2830">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3ef75-2831">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3ef75-2831">Az.CognitiveServices</span></span>
* <span data-ttu-id="3ef75-2832">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2832">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3ef75-2833">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef75-2833">Az.Compute</span></span>
* <span data-ttu-id="3ef75-2834">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2834">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="3ef75-2835">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2835">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="3ef75-2836">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="3ef75-2836">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="3ef75-2837">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3ef75-2837">Az.DataFactoryV2</span></span>
* <span data-ttu-id="3ef75-2838">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2838">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3ef75-2839">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef75-2839">Az.Network</span></span>
* <span data-ttu-id="3ef75-2840">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2840">Added NetworkProfile functionality.</span></span> <span data-ttu-id="3ef75-2841">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3ef75-2841">new cmdlets added</span></span>
    - <span data-ttu-id="3ef75-2842">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3ef75-2842">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="3ef75-2843">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3ef75-2843">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="3ef75-2844">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3ef75-2844">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="3ef75-2845">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3ef75-2845">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="3ef75-2846">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="3ef75-2846">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="3ef75-2847">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="3ef75-2847">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="3ef75-2848">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="3ef75-2848">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="3ef75-2849">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="3ef75-2849">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="3ef75-2850">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="3ef75-2850">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="3ef75-2851">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="3ef75-2851">Az.RedisCache</span></span>
* <span data-ttu-id="3ef75-2852">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="3ef75-2852">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="3ef75-2853">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-2853">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="3ef75-2854">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef75-2854">Az.Resources</span></span>
* <span data-ttu-id="3ef75-2855">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3ef75-2855">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="3ef75-2856">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="3ef75-2856">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="3ef75-2857">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3ef75-2857">Az.Sql</span></span>
* <span data-ttu-id="3ef75-2858">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="3ef75-2858">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3ef75-2859">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3ef75-2859">Az.Websites</span></span>
* <span data-ttu-id="3ef75-2860">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="3ef75-2860">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="3ef75-2861">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="3ef75-2861">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="3ef75-2862">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="3ef75-2862">0.2.0 - September 2018</span></span>
 <span data-ttu-id="3ef75-2863">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="3ef75-2863">Initial Release</span></span>
