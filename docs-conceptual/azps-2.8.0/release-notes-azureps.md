---
title: Az Azure PowerShell kibocsátási megjegyzései
description: Megismerheti az Azure PowerShell-modulok legújabb frissítéseit.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 656e61e7f208367fc7fae28f73d1b6f289831d77
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427734"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="b422e-103">Az Azure PowerShell kibocsátási megjegyzései</span><span class="sxs-lookup"><span data-stu-id="b422e-103">Azure PowerShell release notes</span></span>
## <a name="280---october-2019"></a><span data-ttu-id="b422e-104">2.8.0 – 2019. október</span><span class="sxs-lookup"><span data-stu-id="b422e-104">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="b422e-105">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="b422e-105">General</span></span>
* <span data-ttu-id="b422e-106">Az.HealthcareApis 1.0.0-s kiadás</span><span class="sxs-lookup"><span data-stu-id="b422e-106">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b422e-107">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b422e-107">Az.Accounts</span></span>
* <span data-ttu-id="b422e-108">A telemetria és az URL-címek újraírásának frissítése a létrehozott modulok esetében, a Windows-egységek tesztelésének javítása.</span><span class="sxs-lookup"><span data-stu-id="b422e-108">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="b422e-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b422e-109">Az.ApiManagement</span></span>
* <span data-ttu-id="b422e-110">**Set-AzApiManagementApi** – Az API a következőre való frissítésének támogatása: ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b422e-110">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="b422e-111">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="b422e-111">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b422e-112">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b422e-112">Az.Automation</span></span>
* <span data-ttu-id="b422e-113">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag a Linux újraindítási beállítási paramétere kapcsán.</span><span class="sxs-lookup"><span data-stu-id="b422e-113">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="b422e-114">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b422e-114">Az.Batch</span></span>
* <span data-ttu-id="b422e-115">A **Get-AzBatchNodeAgentSku** elavult, így a 2.0.0-ás verziótól a **Get-AzBatchSupportImage** váltja fel.</span><span class="sxs-lookup"><span data-stu-id="b422e-115">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b422e-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b422e-116">Az.Compute</span></span>
* <span data-ttu-id="b422e-117">A Priority, EvictionPolicy és MaxPrice paraméterek hozzáadása a New-AzVM és a New-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="b422e-117">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="b422e-118">Az Add-AzVMAdditionalUnattendContent és az Add-AzVMSshPublicKey parancsmagok figyelmeztető üzenetének és súgójának kijavítása</span><span class="sxs-lookup"><span data-stu-id="b422e-118">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="b422e-119">A -skipVmBackup kivétel kijavítása felügyelt lemezekkel rendelkező Linux rendszerű virtuális gépek esetében a Set-AzVMDiskEncryptionExtension kapcsán.</span><span class="sxs-lookup"><span data-stu-id="b422e-119">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="b422e-120">A titkosítási beállítások frissítési hibájának kijavítása a Set-AzVMDiskEncryptionExtension kétmenetes forgatókönyvében.</span><span class="sxs-lookup"><span data-stu-id="b422e-120">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b422e-121">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b422e-121">Az.DataFactory</span></span>
* <span data-ttu-id="b422e-122">CRUD-parancsok lettek hozzáadva az ADF V2-adatfolyamhoz: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow és Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="b422e-122">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="b422e-123">Műveleti parancsok lettek hozzáadva az ADF V2-adatfolyam hibakeresési munkamenetéhez: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand és Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="b422e-123">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="b422e-124">Az ADF .Net SDK a 4.2.0-ás verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="b422e-124">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b422e-125">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b422e-125">Az.DataLakeStore</span></span>
* <span data-ttu-id="b422e-126">A fiókérvényesítés javítása, hogy a "-" jelölésű fiókok tartomány nélkül is továbbíthatók legyenek</span><span class="sxs-lookup"><span data-stu-id="b422e-126">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="b422e-127">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="b422e-127">Az.HealthcareApis</span></span>
* <span data-ttu-id="b422e-128">A PowerShell az 1.0.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="b422e-128">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="b422e-129">Az SDK a 1.0.2-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="b422e-129">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="b422e-130">Frissítés a tesztekben az új SDK-verzióra való hivatkozáshoz</span><span class="sxs-lookup"><span data-stu-id="b422e-130">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="b422e-131">A kimeneti struktúra beágyazottról simítottra frissült.</span><span class="sxs-lookup"><span data-stu-id="b422e-131">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b422e-132">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b422e-132">Az.IotHub</span></span>
* <span data-ttu-id="b422e-133">Új útválasztási forrás hozzáadása: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="b422e-133">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="b422e-134">Kisebb hibajavítás: A Get-AzIothub nem adja vissza a következőt: subscriptionId</span><span class="sxs-lookup"><span data-stu-id="b422e-134">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b422e-135">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b422e-135">Az.Monitor</span></span>
* <span data-ttu-id="b422e-136">Új műveleticsoport-fogadók hozzáadva a New-AzActionGroupReceiver parancsmaghoz:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="b422e-136">New action group receivers added for New-AzActionGroupReceiver:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="b422e-137">Az általános riasztási séma használata engedélyezve a fogadók számára.</span><span class="sxs-lookup"><span data-stu-id="b422e-137">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="b422e-138">Ez nem vonatkozik az SMS, az Azure App leküldéses üzenetei, az ITSM és a Voice fogadóira.</span><span class="sxs-lookup"><span data-stu-id="b422e-138">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="b422e-139">A webhookok mostantól az Azure Active Directory-hitelesítés használatát is támogatják.</span><span class="sxs-lookup"><span data-stu-id="b422e-139">Webhooks now supports Azure active directory authentication.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b422e-140">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b422e-140">Az.Network</span></span>
* <span data-ttu-id="b422e-141">Új Get-AzAvailableServiceAlias parancsmag hozzáadva, amely a szolgáltatásvégpont-szabályzatokhoz használható aliasok beszerzéséhez hívható meg.</span><span class="sxs-lookup"><span data-stu-id="b422e-141">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="b422e-142">Forgalomválasztók hozzáadásának támogatása a virtuális hálózati átjáró kapcsolataihoz</span><span class="sxs-lookup"><span data-stu-id="b422e-142">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="b422e-143">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="b422e-143">New cmdlets added:</span></span>
        - <span data-ttu-id="b422e-144">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="b422e-144">New-AzIpsecTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="b422e-145">A -TrafficSelectorPolicies opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b422e-145">Cmdlets updated with optional parameter -TrafficSelectorPolicies</span></span>
        - <span data-ttu-id="b422e-146">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b422e-146">New-AzVirtualNetworkGatewayConnection</span></span>
        - <span data-ttu-id="b422e-147">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b422e-147">Set-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="b422e-148">Az ESP és AH protokollok támogatása a hálózati biztonsági szabályzati konfigurációkban</span><span class="sxs-lookup"><span data-stu-id="b422e-148">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="b422e-149">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="b422e-149">Updated cmdlets:</span></span>
        - <span data-ttu-id="b422e-150">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b422e-150">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="b422e-151">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b422e-151">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="b422e-152">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b422e-152">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="b422e-153">Tovább javult a Cortex-parancsmagok kivételeinek kezelése</span><span class="sxs-lookup"><span data-stu-id="b422e-153">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="b422e-154">A VirtualNetworkGateways új generációi és termékváltozatai</span><span class="sxs-lookup"><span data-stu-id="b422e-154">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="b422e-155">A VirtualNetworkGateways új generációinak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="b422e-155">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="b422e-156">A VirtualNetworkGateways új, nagy átviteli sebességű termékváltozatainak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="b422e-156">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="b422e-157">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b422e-157">Az.RedisCache</span></span>
* <span data-ttu-id="b422e-158">Frissült a Set-AzRedisCache referenciadokumentációja, amely most már tartalmazza a -Size paraméter hiányzó értékeit.</span><span class="sxs-lookup"><span data-stu-id="b422e-158">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="b422e-159">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b422e-159">Az.Sql</span></span>
* <span data-ttu-id="b422e-160">Az Active Directory-rendszergazda a felügyelt példányon való beállításának támogatása</span><span class="sxs-lookup"><span data-stu-id="b422e-160">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b422e-161">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b422e-161">Az.Storage</span></span>
* <span data-ttu-id="b422e-162">Az Storage-ügyfélkódtár a 11.1.0-s verzióra frissült.</span><span class="sxs-lookup"><span data-stu-id="b422e-162">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="b422e-163">A Management plane API-val rendelkező tárolók listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="b422e-163">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="b422e-164">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b422e-164">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="b422e-165">A tárfiókok előfizetésből történő listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="b422e-165">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="b422e-166">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b422e-166">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="b422e-167">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="b422e-167">Az.StorageSync</span></span>
* <span data-ttu-id="b422e-168">A Reset-AzStorageSyncServerCertificate 9810-es hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="b422e-168">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b422e-169">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b422e-169">Az.Websites</span></span>
* <span data-ttu-id="b422e-170">Egy alkalmazáshoz tartozó ASP Set-AzWebApp általi frissítése sikertelen volt</span><span class="sxs-lookup"><span data-stu-id="b422e-170">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="b422e-171">2.7.0 – 2019. szeptember</span><span class="sxs-lookup"><span data-stu-id="b422e-171">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="b422e-172">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b422e-172">Az.ApiManagement</span></span>
* <span data-ttu-id="b422e-173">Frissítve lett a „-Format” paraméter leírása a „Set-AzApiManagementPolicy” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="b422e-173">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="b422e-174">El lettek távolítva az elavult „Update-AzApiManagementDeployment” parancsmag referenciái a referenciadokumentációból.</span><span class="sxs-lookup"><span data-stu-id="b422e-174">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="b422e-175">A „Set-AzApiManagement” használható helyette.</span><span class="sxs-lookup"><span data-stu-id="b422e-175">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b422e-176">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b422e-176">Az.Automation</span></span>
* <span data-ttu-id="b422e-177">Ki lett javítva a „Register-AzAutomationDscNode” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="b422e-177">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="b422e-178">Hozzá lett adva az operációs rendszerrel kapcsolatos korlátozások pontosítása a Register-AzAutomationDSCNode parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b422e-178">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="b422e-179">Ki lett javítva a Start-AzAutomationRunbook parancsmag null értékű hivatkozás okozta kivétele a -Wait paraméter esetén.</span><span class="sxs-lookup"><span data-stu-id="b422e-179">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b422e-180">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b422e-180">Az.Compute</span></span>
* <span data-ttu-id="b422e-181">Hozzá lett adva az UploadSizeInBytes paraméter a New-AzDiskConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b422e-181">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="b422e-182">Hozzá lett adva az Incremental paraméter a New-AzSnapshotConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b422e-182">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="b422e-183">Alacsony prioritású virtuálisgép-funkció hozzáadása:</span><span class="sxs-lookup"><span data-stu-id="b422e-183">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="b422e-184">Hozzá lett adva a MaxPrice, az EvictionPolicy és a Priority paraméter a New-AzVMConfig parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="b422e-184">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="b422e-185">Hozzá lett adva a MaxPrice paraméter a New-AzVmssConfig, az Update-AzVM és az Update-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="b422e-185">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="b422e-186">Ki lett javítva a Get-AzAvailabilitySet parancsmag virtuálisgép-hivatkozással kapcsolatos hibája, amely miatt a parancsmag az előfizetésben található összes rendelkezésreállási csoportot listázta.</span><span class="sxs-lookup"><span data-stu-id="b422e-186">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="b422e-187">Ki lett javítva a Get-AzRemoteDesktopFile parancsmag esetében jelentkező null kivétel.</span><span class="sxs-lookup"><span data-stu-id="b422e-187">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="b422e-188">Ki lett javítva virtuális merevlemezek Seek metódusa a végrelatív pozíció esetében.</span><span class="sxs-lookup"><span data-stu-id="b422e-188">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="b422e-189">Ki lett javítva az UltraSSD hibája a New-AzVM és az Update-AzVM parancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="b422e-189">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b422e-190">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b422e-190">Az.DataFactory</span></span>
* <span data-ttu-id="b422e-191">Hozzá lett adva 3 új parancs (az Add-AzDataFactoryV2TriggerSubscription, a Remove-AzDataFactoryV2TriggerSubscription és a Get-AzDataFactoryV2TriggerSubscriptionStatus) az ADF V2-höz</span><span class="sxs-lookup"><span data-stu-id="b422e-191">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="b422e-192">Az ADF .Net SDK a 4.1.3-as verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="b422e-192">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="b422e-193">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b422e-193">Az.HDInsight</span></span>
* <span data-ttu-id="b422e-194">Kompatibilitástörő változások a meghívással kapcsolatban</span><span class="sxs-lookup"><span data-stu-id="b422e-194">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b422e-195">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b422e-195">Az.IotHub</span></span>
* <span data-ttu-id="b422e-196">Hozzá lett adva az IoTHubok földrajzilag párosított vészhelyreállítási régiójába történő feladatátvétel meghívásának támogatása.</span><span class="sxs-lookup"><span data-stu-id="b422e-196">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="b422e-197">Hozzá lett adva az IoTHubok üzenetbővítés-kezelésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="b422e-197">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="b422e-198">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="b422e-198">New cmdlets are:</span></span>
    - <span data-ttu-id="b422e-199">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="b422e-199">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="b422e-200">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="b422e-200">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="b422e-201">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="b422e-201">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="b422e-202">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="b422e-202">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b422e-203">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b422e-203">Az.Monitor</span></span>
* <span data-ttu-id="b422e-204">A legújabb Monitor SDK-ra mutat, azaz a 0.24.1-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="b422e-204">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="b422e-205">Nem kompatibilitástörő változásokkal bővíti a Metrics parancsmagokat, így az egységek számbavétele számos új értéket támogat.</span><span class="sxs-lookup"><span data-stu-id="b422e-205">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="b422e-206">Ezek írásvédett parancsmagok, ezért a parancsmagok bemenetében nem történik változás.</span><span class="sxs-lookup"><span data-stu-id="b422e-206">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="b422e-207">Az **ActionGroups**-kérések api-version értéke mostantól **2019-06-01**, korábban **2018-03-01** volt.</span><span class="sxs-lookup"><span data-stu-id="b422e-207">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="b422e-208">A forgatókönyvtesztek frissültek, így igazodnak a változáshoz.</span><span class="sxs-lookup"><span data-stu-id="b422e-208">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="b422e-209">Az **EmailReceiver** és a **WebhookReceiver** osztályok konstruktoraihoz hozzá lett adva egy új kötelező argumentum, a **useCommonAlertSchema** nevű logikai érték.</span><span class="sxs-lookup"><span data-stu-id="b422e-209">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="b422e-210">A kompatibilitástörő változás parancsmagok elől való elrejtése érdekében a rögzített érték jelenleg a **false** (hamis).</span><span class="sxs-lookup"><span data-stu-id="b422e-210">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="b422e-211">**MEGJEGYZÉS**: Ez egy átmeneti módosítás, amelyet a Riasztások csapatnak érvényesítenie kell.</span><span class="sxs-lookup"><span data-stu-id="b422e-211">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="b422e-212">A **Source** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="b422e-212">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="b422e-213">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="b422e-213">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="b422e-214">Az **AlertingAction** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="b422e-214">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="b422e-215">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="b422e-215">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="b422e-216">A dinamikus küszöbérték kritériumainak támogatása a 2-es verziójú metrikariasztás esetében</span><span class="sxs-lookup"><span data-stu-id="b422e-216">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="b422e-217">New-AzMetricAlertRuleV2Criteria: mostantól a dinamikus küszöbértékek kritériumait is létrehozza</span><span class="sxs-lookup"><span data-stu-id="b422e-217">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="b422e-218">Add-AzMetricAlertRuleV2: mostantól a dinamikus küszöbértékek kritériumait is elfogadja</span><span class="sxs-lookup"><span data-stu-id="b422e-218">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="b422e-219">Az ütemezett lekérdezési szabályok parancsmagjainak (SQR) fejlesztései</span><span class="sxs-lookup"><span data-stu-id="b422e-219">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="b422e-220">A parancsmagok a „Location” paraméter mindkét formátumát elfogadják: a helyet (például eastus) és a hely megjelenített nevét is (például USA keleti régiója)</span><span class="sxs-lookup"><span data-stu-id="b422e-220">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="b422e-221">Megfelelően ábrázolva lett az „Enabled” paraméter a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="b422e-221">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="b422e-222">Példák lettek hozzáadva az „ActionGroup” opcionális paraméterhez</span><span class="sxs-lookup"><span data-stu-id="b422e-222">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="b422e-223">Általánosan továbbfejlesztett súgófájlok</span><span class="sxs-lookup"><span data-stu-id="b422e-223">Overall improved help files</span></span>
* <span data-ttu-id="b422e-224">Ki lett javítva a „Set-AzActionRule” hatókörtípusának meghatározásával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="b422e-224">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b422e-225">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b422e-225">Az.Network</span></span>
* <span data-ttu-id="b422e-226">Ki lett javítva a „New-AzApplicationGateway” referenciadokumentációjában található helytelen példa</span><span class="sxs-lookup"><span data-stu-id="b422e-226">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="b422e-227">Hozzá lett adva egy csomagrögzítés összes tulajdonságának lekérésével kapcsolatos megjegyzés a „Get-AzNetworkWatcherPacketCapture” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="b422e-227">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="b422e-228">Ki lett javítva a „Test-AzNetworkWatcherIPFlow” referenciadokumentációjában található példa a hálózati adapterek megfelelő számbavétele érdekében</span><span class="sxs-lookup"><span data-stu-id="b422e-228">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="b422e-229">Tovább lett fejlesztve a felhőkivétel-elemzés az esetleges további részletek megjelenítése érdekében</span><span class="sxs-lookup"><span data-stu-id="b422e-229">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="b422e-230">Tovább lett fejlesztve a felhőkivétel-elemzés az SDK-kivételek további típusainak kezelése érdekében</span><span class="sxs-lookup"><span data-stu-id="b422e-230">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="b422e-231">Ki lett javítva a biztonságiszabály-modellek helytelen leképezése</span><span class="sxs-lookup"><span data-stu-id="b422e-231">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="b422e-232">Hozzá lettek adva a privát IP-cím funkcióval kapcsolatos tulajdonságok a hálózati adapterhez</span><span class="sxs-lookup"><span data-stu-id="b422e-232">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="b422e-233">Hozzá lett adva a „PrivateEndpoint” tulajdonság PSResourceId típusúként a PSNetworkInterface osztályhoz</span><span class="sxs-lookup"><span data-stu-id="b422e-233">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="b422e-234">Hozzá lett adva a „PrivateLinkConnectionProperties” tulajdonság PSIpConfigurationConnectivityInformation típusúként a PSNetworkInterfaceIPConfiguration osztályhoz</span><span class="sxs-lookup"><span data-stu-id="b422e-234">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="b422e-235">Hozzá lett adva a PSIpConfigurationConnectivityInformation nevű új modellosztály</span><span class="sxs-lookup"><span data-stu-id="b422e-235">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="b422e-236">Hozzá lett adva az új ApplicationRuleProtocolType „mssql” az Azure Firewall-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="b422e-236">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="b422e-237">MultiLink-támogatás a Virtuális WAN-ben</span><span class="sxs-lookup"><span data-stu-id="b422e-237">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="b422e-238">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b422e-238">New cmdlets</span></span>
        - <span data-ttu-id="b422e-239">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="b422e-239">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="b422e-240">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="b422e-240">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="b422e-241">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="b422e-241">Updated cmdlet:</span></span>
        - <span data-ttu-id="b422e-242">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="b422e-242">New-VpnSite</span></span>
        - <span data-ttu-id="b422e-243">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="b422e-243">Update-VpnSite</span></span>
        - <span data-ttu-id="b422e-244">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="b422e-244">New-VpnConnection</span></span>
        - <span data-ttu-id="b422e-245">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="b422e-245">Update-VpnConnection</span></span>
* <span data-ttu-id="b422e-246">Ki lettek javítva bizonyos PowerShell-példák dokumentumai, hogy az AzureRM-parancsmagok helyett az Az-parancsmagokat használják</span><span class="sxs-lookup"><span data-stu-id="b422e-246">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b422e-247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b422e-247">Az.RecoveryServices</span></span>
* <span data-ttu-id="b422e-248">Frissítve lett az AzureVMpolicy objektum a ProtectedItemsCount attribútummal</span><span class="sxs-lookup"><span data-stu-id="b422e-248">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="b422e-249">Tesztek lettek hozzáadva a virtuális gép szabályzatához és az eredeti Storage-fiók visszaállításához</span><span class="sxs-lookup"><span data-stu-id="b422e-249">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="b422e-250">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b422e-250">Az.Resources</span></span>
* <span data-ttu-id="b422e-251">Ki lett javítva a hiba, amely miatt a New-AzRoleAssignment parancsot nem lehetett meghívni a Scope paraméter nélkül.</span><span class="sxs-lookup"><span data-stu-id="b422e-251">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b422e-252">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b422e-252">Az.ServiceFabric</span></span>
* <span data-ttu-id="b422e-253">Ki lett javítva az „Update-AzServiceFabricReliability” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="b422e-253">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="b422e-254">Új parancsmagok lettek hozzáadva az alkalmazás és a szolgáltatások felügyeletéhez:</span><span class="sxs-lookup"><span data-stu-id="b422e-254">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="b422e-255">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="b422e-255">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="b422e-256">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="b422e-256">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="b422e-257">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="b422e-257">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="b422e-258">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="b422e-258">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="b422e-259">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="b422e-259">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="b422e-260">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="b422e-260">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="b422e-261">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="b422e-261">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="b422e-262">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="b422e-262">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="b422e-263">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="b422e-263">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="b422e-264">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="b422e-264">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="b422e-265">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="b422e-265">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="b422e-266">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="b422e-266">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="b422e-267">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="b422e-267">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="b422e-268">A Service Fabric SDK az 1.2.0-s verzióra frissült, amely a Service Fabric erőforrás-szolgáltató 2019-03-01 api-versionjét használja.</span><span class="sxs-lookup"><span data-stu-id="b422e-268">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="b422e-269">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="b422e-269">Az.SignalR</span></span>
* <span data-ttu-id="b422e-270">Hozzá lettek adva az Update, Restart, CheckNameAvailability és GetUsage parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b422e-270">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="b422e-271">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b422e-271">Az.Sql</span></span>
* <span data-ttu-id="b422e-272">Frissítve lett a „Get-AzSqlElasticPool” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="b422e-272">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="b422e-273">Hozzá lett adva egy rugalmas készlet létrehozását bemutató virtuálismag-példa (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="b422e-273">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="b422e-274">El lett távolítva az EmailAddresses érvényesítése és annak ellenőrzése, hogy az EmailAdmins értéke hamis-e abban az esetben, ha az EmailAddresses üres a Set-AzSqlServerAdvancedThreatProtectionPolicy és a Set-AzSqlDatabaseAdvancedThreatProtectionPolicy parancsmagban</span><span class="sxs-lookup"><span data-stu-id="b422e-274">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="b422e-275">Engedélyezve lettek a kiszolgáló-/adatbázis-naplózási beállítások abban az esetben, ha több olyan diagnosztikai beállítás létezik, amelyek engedélyezik a naplózási kategóriát.</span><span class="sxs-lookup"><span data-stu-id="b422e-275">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="b422e-276">Ki lett javítva az e-mail-címek ellenőrzése több, SQL-sebezhetőségi felméréshez használt parancsmagban (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting és Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="b422e-276">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b422e-277">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b422e-277">Az.Storage</span></span>
* <span data-ttu-id="b422e-278">Frissítve lett a „Get-AzStorageAccountKey” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="b422e-278">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="b422e-279">A forrásfájl SMB-tulajdonságai (fájlattribútumok, fájl létrehozásának ideje, fájl utolsó írásának ideje) célfájlban történő megtartásának támogatása az Azure File-beli feltöltés/letöltés esetében</span><span class="sxs-lookup"><span data-stu-id="b422e-279">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="b422e-280">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b422e-280">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="b422e-281">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b422e-281">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="b422e-282">Ki lett javítva a tulajdonság-/metaadathibával meghiúsuló blokkblobfeltöltés a tárolóképes ImmutabilityPolicy esetében.</span><span class="sxs-lookup"><span data-stu-id="b422e-282">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="b422e-283">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b422e-283">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="b422e-284">Az Azure File-megosztások Management plane API-val történő kezelésének támogatása</span><span class="sxs-lookup"><span data-stu-id="b422e-284">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="b422e-285">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="b422e-285">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="b422e-286">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="b422e-286">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="b422e-287">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="b422e-287">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="b422e-288">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="b422e-288">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b422e-289">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b422e-289">Az.Websites</span></span>
* <span data-ttu-id="b422e-290">Ki lett javítva az a probléma, amely miatt a webalkalmazás Címkéi törölve lettek az alkalmazás új ASP-be történő migrálásakor</span><span class="sxs-lookup"><span data-stu-id="b422e-290">Fixing issue where webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="b422e-291">Ki lett javítva a Publish-AzureWebapp parancs a Linux és Windows rendszeren történő működés érdekében</span><span class="sxs-lookup"><span data-stu-id="b422e-291">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="b422e-292">Frissítve lett a „Get-AzWebAppPublishingProfile” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="b422e-292">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="b422e-293">2.6.0 – 2019. augusztus</span><span class="sxs-lookup"><span data-stu-id="b422e-293">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="b422e-294">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="b422e-294">General</span></span>
* <span data-ttu-id="b422e-295">Különféle elgépelések kijavítva több modulban</span><span class="sxs-lookup"><span data-stu-id="b422e-295">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b422e-296">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b422e-296">Az.Accounts</span></span>
* <span data-ttu-id="b422e-297">Felhasználó által hozzárendelt MSI támogatása az Azure Functions-hitelesítésben (#9479)</span><span class="sxs-lookup"><span data-stu-id="b422e-297">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="b422e-298">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="b422e-298">Az.Aks</span></span>
* <span data-ttu-id="b422e-299">A Get-AzAks kimenetével kapcsolatos probléma ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="b422e-299">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="b422e-300">További információ: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="b422e-300">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="b422e-301">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b422e-301">Az.ApiManagement</span></span>
* <span data-ttu-id="b422e-302">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="b422e-302">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="b422e-303">Frissült a .net nuget verziója, amely nem kényszeríti ki a productId, az apiId, a groupId és a userId korlátozásait</span><span class="sxs-lookup"><span data-stu-id="b422e-303">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="b422e-304">**Get-AzApiManagementProduct** – A termékek API-val történő lekérdezése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="b422e-304">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="b422e-305">**New-AzApiManagementApiRevision** – Ki lett javítva az a probléma, amely miatt az ApiRevisionDescription nem lett beállítva az új API-változat létrehozásakor https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="b422e-305">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="b422e-306">Ki lett javítva a PsApiManagementOAuth2AuthrozationServer modell elírása PsApiManagementOAuth2AuthorizationServer értékre</span><span class="sxs-lookup"><span data-stu-id="b422e-306">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="b422e-307">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b422e-307">Az.Batch</span></span>
* <span data-ttu-id="b422e-308">Ki lett javítva a súgóüzenetben és a dokumentációban található elgépelés, nagy kezdőbetűs Windows értékre</span><span class="sxs-lookup"><span data-stu-id="b422e-308">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b422e-309">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b422e-309">Az.Cdn</span></span>
* <span data-ttu-id="b422e-310">Ki lett javítva egy elgépelés CDN modulátalakító segédben</span><span class="sxs-lookup"><span data-stu-id="b422e-310">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b422e-311">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b422e-311">Az.Compute</span></span>
* <span data-ttu-id="b422e-312">Új VmssId a New-AzVMConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b422e-312">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="b422e-313">Új TerminateScheduledEvents és a TerminateScheduledEventNotBeforeTimeoutInMinutes paraméterek a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b422e-313">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="b422e-314">Új HyperVGeneration tulajdonság a VM-rendszerképobjektumhoz</span><span class="sxs-lookup"><span data-stu-id="b422e-314">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="b422e-315">Új Host és HostGroup jellemzők</span><span class="sxs-lookup"><span data-stu-id="b422e-315">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="b422e-316">Új parancsmagok:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="b422e-316">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="b422e-317">Új HostId paraméter a New-AzVMConfig és a New-AzVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b422e-317">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="b422e-318">Az Invoke-AzVMRunCommand dokumentációjában található példa frissítve lett a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="b422e-318">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="b422e-319">A -VolumeType leírása frissítve lett a set-AzVMDiskEncryptionExtension és a set-AzVmssDiskEncryptionExtension referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="b422e-319">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b422e-320">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b422e-320">Az.DataFactory</span></span>
* <span data-ttu-id="b422e-321">A New-AzDataFactoryEncryptValue dokumentációjában a Windows szó nagy kezdőbetűsre lett javítva</span><span class="sxs-lookup"><span data-stu-id="b422e-321">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="b422e-322">Az ADF .Net SDK a 4.1.2-es verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="b422e-322">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="b422e-323">Új DataProxyIntegrationRuntimeName, DataProxyIntegrationRuntimeName és DataProxyStagingPath paraméterek lettek hozzáadva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz, lehetővé téve a helyi integrációs modul SSIS integrációs modul proxyjaként való beállítását</span><span class="sxs-lookup"><span data-stu-id="b422e-323">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="b422e-324">Frissítve lett a PSTriggerRun, hogy megjelenítse az aktivált folyamatokat, üzeneteket és tulajdonságokat, illetve a PSActivityRun, hogy megjelenítse a tevékenységtípust</span><span class="sxs-lookup"><span data-stu-id="b422e-324">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b422e-325">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b422e-325">Az.DataLakeStore</span></span>
* <span data-ttu-id="b422e-326">Ki lett javítva a Get-DataLakeStoreDeletedItem lefagyása hibák vagy távoli kivételek esetén.</span><span class="sxs-lookup"><span data-stu-id="b422e-326">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b422e-327">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b422e-327">Az.EventHub</span></span>
* <span data-ttu-id="b422e-328">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNteworkRule paraméter a Set-AzEventHubNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="b422e-328">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="b422e-329">Ki lett javítva a 9558-as számú hiba: Set-AzEventHubNamespace a PUT helyett a PATCH kérést használta</span><span class="sxs-lookup"><span data-stu-id="b422e-329">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="b422e-330">új EnableKafka paraméter a Set-AzEventHubNamespace parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b422e-330">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="b422e-331">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="b422e-331">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="b422e-332">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="b422e-332">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="b422e-333">Ki lett javítva egy elgépelés a dokumentációban, ahol az Azure csupa kisbetűvel szerepelt</span><span class="sxs-lookup"><span data-stu-id="b422e-333">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b422e-334">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b422e-334">Az.Monitor</span></span>
* <span data-ttu-id="b422e-335">Hibás paraméternév lett kijavítva a súgódokumentációban</span><span class="sxs-lookup"><span data-stu-id="b422e-335">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b422e-336">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b422e-336">Az.Network</span></span>
* <span data-ttu-id="b422e-337">Frissítve lett a New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b422e-337">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="b422e-338">A PublicIpAddress elavult, mert a kiszolgálóoldalon nem használatos.</span><span class="sxs-lookup"><span data-stu-id="b422e-338">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="b422e-339">Hozzá lett adva egy opcionális Primary paraméter, amely azt jelzi, hogy a jelenlegi IP-konfiguráció elsődleges-e.</span><span class="sxs-lookup"><span data-stu-id="b422e-339">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="b422e-340">Javítva lett az SDK kérelemhiba-kivételének kezelése – kijavítja azt a problémát, amely miatt az SDK-kivételek kezelése korábban nem volt megfelelő, és a fontos hibarészletek nem jelentek meg</span><span class="sxs-lookup"><span data-stu-id="b422e-340">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="b422e-341">Be lett állítva, hogy az IPv6 IP-előtag ellenőrzési logikája ellenőrizze az IPv6-előtag hosszának megfelelőségét.</span><span class="sxs-lookup"><span data-stu-id="b422e-341">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="b422e-342">Frissült a Get-AzVirtualNetworkSubnetConfig: Új paraméterkészlet lett hozzáadva az alhálózat erőforrás-azonosítója szerinti lekéréshez.</span><span class="sxs-lookup"><span data-stu-id="b422e-342">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="b422e-343">Frissült az AzNetworkServiceTag Location paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="b422e-343">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b422e-344">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b422e-344">Az.OperationalInsights</span></span>
* <span data-ttu-id="b422e-345">Frissült a New-AzOperationalInsightsLinuxSyslogDataSource dokumentációja</span><span class="sxs-lookup"><span data-stu-id="b422e-345">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="b422e-346">Példa hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b422e-346">Added example</span></span>
    - <span data-ttu-id="b422e-347">A -Name paraméter leírása frissítve lett</span><span class="sxs-lookup"><span data-stu-id="b422e-347">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="b422e-348">Új példa lett hozzáadva a New-AzOperationalInsightsWindowsEventDataSource parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b422e-348">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="b422e-349">Módosult a New-AzOperationalInsightsWindowsEventDataSource -Name paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="b422e-349">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b422e-350">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b422e-350">Az.RecoveryServices</span></span>
* <span data-ttu-id="b422e-351">Frissült a Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="b422e-351">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="b422e-352">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b422e-352">Az.Resources</span></span>
* <span data-ttu-id="b422e-353">A Microsoft.Resource mostantól támogatja a 2019-05-10-es új api-verziót</span><span class="sxs-lookup"><span data-stu-id="b422e-353">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="b422e-354">Mostantól támogatott a copy.count = 0 a változók, erőforrások és tulajdonságok esetében</span><span class="sxs-lookup"><span data-stu-id="b422e-354">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="b422e-355">A condition = false vagy copy.count = 0 tulajdonságú erőforrások teljes módban törölve lesznek</span><span class="sxs-lookup"><span data-stu-id="b422e-355">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="b422e-356">A súgódokumentációhoz hozzá lett adva egy példa a szabályzatok előfizetési szinten történő hozzárendeléséhez</span><span class="sxs-lookup"><span data-stu-id="b422e-356">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b422e-357">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b422e-357">Az.ServiceBus</span></span>
* <span data-ttu-id="b422e-358">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNetworkRule paraméter a Set-AzServiceBusNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="b422e-358">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="b422e-359">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="b422e-359">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="b422e-360">Új Test-AzServiceBusNameAvailability parancs lett hozzáadva annak ellenőrzésére, hogy az üzenetsor és a témakör neve elérhető-e</span><span class="sxs-lookup"><span data-stu-id="b422e-360">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b422e-361">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b422e-361">Az.ServiceFabric</span></span>
* <span data-ttu-id="b422e-362">Ki lettek javítva a csomóponttípus-hozzáadási parancsmag hibái:</span><span class="sxs-lookup"><span data-stu-id="b422e-362">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="b422e-363">NullReferenceException hiba történt, ha az erőforráscsoport más, a Service Fabric-fürthöz nem kapcsolódó VMSS-sel rendelkezett.</span><span class="sxs-lookup"><span data-stu-id="b422e-363">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="b422e-364">Kijavított hiba: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="b422e-364">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="b422e-365">Ki lett javítva egy hiba, amely miatt a parancsmag futása meghiúsult, ha a virtualNetwork a fürttől eltérő erőforráscsoportban volt.</span><span class="sxs-lookup"><span data-stu-id="b422e-365">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="b422e-366">kijavított hiba: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="b422e-366">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="b422e-367">Az Add-AzServiceFabricApplicationCertificate parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="b422e-367">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="b422e-368">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b422e-368">Az.Sql</span></span>
* <span data-ttu-id="b422e-369">Frissült a régi naplózási parancsmagok dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="b422e-369">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b422e-370">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b422e-370">Az.Storage</span></span>
* <span data-ttu-id="b422e-371">A Get/Close-AzStorageFileHandle súgója további parancsmagpélda-forgatókönyvek hozzáadásával és a paraméterek leírásának frissítésével változott</span><span class="sxs-lookup"><span data-stu-id="b422e-371">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="b422e-372">A StandardBlobTier mostantól támogatott a blobfeltöltési és -másolási műveletekhez</span><span class="sxs-lookup"><span data-stu-id="b422e-372">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="b422e-373">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b422e-373">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="b422e-374">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b422e-374">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="b422e-375">A rehidratálás prioritása mostantól támogatott a blobmásoláskor</span><span class="sxs-lookup"><span data-stu-id="b422e-375">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="b422e-376">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b422e-376">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b422e-377">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b422e-377">Az.Websites</span></span>
* <span data-ttu-id="b422e-378">Magyarázat hozzáadva a Set-AzWebApp és a Set-AzWebAppSlot parancsmagok -AppSettings paraméteréhez</span><span class="sxs-lookup"><span data-stu-id="b422e-378">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="b422e-379">2.5.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="b422e-379">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b422e-380">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b422e-380">Az.Accounts</span></span>
* <span data-ttu-id="b422e-381">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="b422e-381">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="b422e-382">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="b422e-382">Az.ApplicationInsights</span></span>
* <span data-ttu-id="b422e-383">A Remove-AzApplicationInsightsApiKey dokumentáció példájában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="b422e-383">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b422e-384">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b422e-384">Az.Automation</span></span>
* <span data-ttu-id="b422e-385">Az erőforrássztringben található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="b422e-385">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b422e-386">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b422e-386">Az.CognitiveServices</span></span>
* <span data-ttu-id="b422e-387">NetworkRuleSet támogatás hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="b422e-387">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b422e-388">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b422e-388">Az.Compute</span></span>
* <span data-ttu-id="b422e-389">A virtuálisgép-példány nézetobjektumaiból hiányzó tulajdonságok (ComputerName, OsName, OsVersion és HyperVGeneration) hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="b422e-389">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="b422e-390">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b422e-390">Az.ContainerRegistry</span></span>
* <span data-ttu-id="b422e-391">A Remove-AzContainerRegistryReplication Replikáció paraméterében lévő elírás javítása</span><span class="sxs-lookup"><span data-stu-id="b422e-391">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="b422e-392">További információ: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="b422e-392">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b422e-393">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b422e-393">Az.DataFactory</span></span>
* <span data-ttu-id="b422e-394">Az ADF .Net SDK a 4.1.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="b422e-394">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="b422e-395">A Get-AzDataFactoryV2PipelineRun dokumentációjában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="b422e-395">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b422e-396">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b422e-396">Az.EventHub</span></span>
* <span data-ttu-id="b422e-397">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="b422e-397">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="b422e-398">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="b422e-398">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b422e-399">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b422e-399">Az.KeyVault</span></span>
* <span data-ttu-id="b422e-400">A KeySize tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="b422e-400">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b422e-401">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b422e-401">Az.LogicApp</span></span>
* <span data-ttu-id="b422e-402">A Get-AzIntegrationAccountMap javítása, hogy minden leképezéstípust listázzon</span><span class="sxs-lookup"><span data-stu-id="b422e-402">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="b422e-403">Új MapType paraméter hozzáadva a szűréshez</span><span class="sxs-lookup"><span data-stu-id="b422e-403">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="b422e-404">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="b422e-404">Az.ManagedServices</span></span>
* <span data-ttu-id="b422e-405">Az API 2019. 06. 01-én kiadott (GA) verziójának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b422e-405">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b422e-406">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b422e-406">Az.Network</span></span>
* <span data-ttu-id="b422e-407">A privát végpont és privát kapcsolatszolgáltatás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b422e-407">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="b422e-408">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b422e-408">New cmdlets</span></span>
        - <span data-ttu-id="b422e-409">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b422e-409">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="b422e-410">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b422e-410">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="b422e-411">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b422e-411">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b422e-412">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b422e-412">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b422e-413">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b422e-413">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b422e-414">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b422e-414">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="b422e-415">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="b422e-415">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="b422e-416">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b422e-416">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="b422e-417">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies jelző a VirtualNetwork alhálózatban</span><span class="sxs-lookup"><span data-stu-id="b422e-417">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="b422e-418">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig frissítve</span><span class="sxs-lookup"><span data-stu-id="b422e-418">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="b422e-419">Hozzá lett adva a -PrivateEndpointNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát végpont esetében.</span><span class="sxs-lookup"><span data-stu-id="b422e-419">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="b422e-420">Hozzá lett adva a -PrivateLinkServiceNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát kapcsolati szolgáltatás esetében.</span><span class="sxs-lookup"><span data-stu-id="b422e-420">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="b422e-421">Az AzPrivateLinkService parancsmag ServiceName paramétere átnevezve a Name névre a ServiceName aliasszal a visszamenőleges kompatibilitás érdekében</span><span class="sxs-lookup"><span data-stu-id="b422e-421">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="b422e-422">ICMP-protokoll engedélyezése a hálózati biztonsági szabályzati konfigurációkhoz</span><span class="sxs-lookup"><span data-stu-id="b422e-422">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="b422e-423">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b422e-423">Updated cmdlets</span></span>
        - <span data-ttu-id="b422e-424">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b422e-424">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="b422e-425">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b422e-425">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="b422e-426">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b422e-426">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="b422e-427">A ConnectionProtocolType (Ikev1/Ikev2) hozzáadva a New-AzVirtualNetworkGatewayConnection konfigurálható paramétereként</span><span class="sxs-lookup"><span data-stu-id="b422e-427">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="b422e-428">PrivateIpAddressVersion hozzáadva a LoadBalancerFrontendIpConfigurationhöz</span><span class="sxs-lookup"><span data-stu-id="b422e-428">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="b422e-429">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="b422e-429">Updated cmdlet:</span></span>
        - <span data-ttu-id="b422e-430">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b422e-430">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="b422e-431">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b422e-431">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="b422e-432">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b422e-432">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="b422e-433">Application Gateway New-AzApplicationGatewayProbeConfig parancs frissítése a mintavétel egyéni portjának támogatásához</span><span class="sxs-lookup"><span data-stu-id="b422e-433">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="b422e-434">Frissített New-AzApplicationGatewayProbeConfig: A Port opcionális paraméter hozzáadva, amelyet a rendszer a háttérrendszer-kiszolgáló mintavételére használ.</span><span class="sxs-lookup"><span data-stu-id="b422e-434">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="b422e-435">Ez a paraméter a Standard_V2 és WAF_V2 termékváltozatokban használható.</span><span class="sxs-lookup"><span data-stu-id="b422e-435">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b422e-436">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b422e-436">Az.OperationalInsights</span></span>
* <span data-ttu-id="b422e-437">A mentett keresések alapértelmezett verziója 1 értékre frissítve.</span><span class="sxs-lookup"><span data-stu-id="b422e-437">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="b422e-438">Null reguláris kifejezések kezelése javítva az egyéni naplókban</span><span class="sxs-lookup"><span data-stu-id="b422e-438">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b422e-439">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b422e-439">Az.RecoveryServices</span></span>
* <span data-ttu-id="b422e-440">A Get-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="b422e-440">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="b422e-441">A Get-AzRecoveryServicesBackupContainer.md frissítése</span><span class="sxs-lookup"><span data-stu-id="b422e-441">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="b422e-442">A Get-AzRecoveryServicesVault.md frissítése</span><span class="sxs-lookup"><span data-stu-id="b422e-442">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="b422e-443">A Wait-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="b422e-443">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="b422e-444">A Set-AzRecoveryServicesVaultContext.md frissítése</span><span class="sxs-lookup"><span data-stu-id="b422e-444">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="b422e-445">A Get-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="b422e-445">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="b422e-446">A Get-AzRecoveryServicesBackupRecoveryPoint.md frissítése</span><span class="sxs-lookup"><span data-stu-id="b422e-446">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="b422e-447">A Restore-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="b422e-447">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="b422e-448">A tároló Azure-fájlmegosztásban való regisztrációjának törlésére szolgáló szolgáltatáshívás frissítése</span><span class="sxs-lookup"><span data-stu-id="b422e-448">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="b422e-449">A Set-AzRecoveryServicesAsrAlertSetting.md frissítése</span><span class="sxs-lookup"><span data-stu-id="b422e-449">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="b422e-450">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b422e-450">Az.Resources</span></span>
- <span data-ttu-id="b422e-451">A New-AzResourceGroupDeployment dokumentációban hivatkozott hiányzó parancsmag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b422e-451">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="b422e-452">A szabályzat parancsmagjai frissítve a 2019. 01. 01. dátumú új API-verzió használatára</span><span class="sxs-lookup"><span data-stu-id="b422e-452">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b422e-453">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b422e-453">Az.ServiceBus</span></span>
* <span data-ttu-id="b422e-454">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="b422e-454">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="b422e-455">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="b422e-455">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="b422e-456">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b422e-456">Az.Sql</span></span>
* <span data-ttu-id="b422e-457">A Set-AzSqlDatabaseSecondary parancsmag hiányzó példáinak javítása</span><span class="sxs-lookup"><span data-stu-id="b422e-457">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="b422e-458">A biztonságirés-felmérés e-mail-cím megadása nélkül beállított ismétlődő vizsgálatának javítása</span><span class="sxs-lookup"><span data-stu-id="b422e-458">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="b422e-459">Egy kis elírás javítása egy figyelmeztető üzenetben.</span><span class="sxs-lookup"><span data-stu-id="b422e-459">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b422e-460">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b422e-460">Az.Storage</span></span>
* <span data-ttu-id="b422e-461">A Get-AzStorageAccount hivatkozási dokumentációjában található példa frissítése a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="b422e-461">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="b422e-462">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="b422e-462">Az.StorageSync</span></span>
* <span data-ttu-id="b422e-463">Az Invoke-AzStorageSyncChangeDetection parancsmag hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="b422e-463">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="b422e-464">A 9551-es hiba javítása a TierFilesOlderThanDays betartásához</span><span class="sxs-lookup"><span data-stu-id="b422e-464">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b422e-465">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b422e-465">Az.Websites</span></span>
* <span data-ttu-id="b422e-466">A hiba elhárítása, amely miatt a Get-AzWebApp és a Set-AzWebApp nem adott vissza egyes SiteConfig tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="b422e-466">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="b422e-467">Egy új Location paraméter hozzáadása a Get-AzDeletedWebApp és a Restore-AzDeletedWebApp parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b422e-467">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="b422e-468">A webalkalmazás-tárhelyek New-AzWebApp -IncludeSourceWebAppSlots használatával történő klónozásakor jelentkező hiba javítása</span><span class="sxs-lookup"><span data-stu-id="b422e-468">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="b422e-469">2.4.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="b422e-469">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b422e-470">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b422e-470">Az.Accounts</span></span>
* <span data-ttu-id="b422e-471">Profilparancsmagok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="b422e-471">Add support for profile cmdlets</span></span>
* <span data-ttu-id="b422e-472">A létrehozott parancsmagokban lévő környezetek és adatsíkok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="b422e-472">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="b422e-473">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen végpontot használt az adatsík parancsmagjaihoz Windows PowerShellben</span><span class="sxs-lookup"><span data-stu-id="b422e-473">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="b422e-474">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="b422e-474">Az.Advisor</span></span>
* <span data-ttu-id="b422e-475">Az Az.Advisor GA-kiadása</span><span class="sxs-lookup"><span data-stu-id="b422e-475">GA release of Az.Advisor</span></span>
* <span data-ttu-id="b422e-476">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="b422e-476">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="b422e-477">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b422e-477">Az.ApiManagement</span></span>
* <span data-ttu-id="b422e-478">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="b422e-478">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="b422e-479">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="b422e-479">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="b422e-480">Előfizetések felhasználó és termék szerinti lekérdezésének támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b422e-480">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="b422e-481">„/”, „/apis”, „/apis/echo-api” hatókör használatával történő lekérdezés támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b422e-481">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="b422e-482">A következő hibák ki lettek javítva: https://github.com/Azure/azure-powershell/issues/9307 és https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="b422e-482">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="b422e-483">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="b422e-483">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="b422e-484">Az „ApiVersion” és az „ApiVersionSetId” megadhatóvá vált az API-k importálásakor</span><span class="sxs-lookup"><span data-stu-id="b422e-484">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b422e-485">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b422e-485">Az.Automation</span></span>
* <span data-ttu-id="b422e-486">A Set-AzAutomationConnectionFieldValue parancsmag sztringértékek kezelése esetén fellépő hibája javítva lett.</span><span class="sxs-lookup"><span data-stu-id="b422e-486">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b422e-487">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b422e-487">Az.Compute</span></span>
* <span data-ttu-id="b422e-488">A HyperVGeneration paraméter hozzáadása a New-AzImageConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b422e-488">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b422e-489">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b422e-489">Az.DataFactory</span></span>
* <span data-ttu-id="b422e-490">A tevékenység-, folyamat- és eseményindító-futtatási kimenetek lekérdezési ADF-parancsmagjainak frissítése a Select-Object folyamat támogatásához.</span><span class="sxs-lookup"><span data-stu-id="b422e-490">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b422e-491">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b422e-491">Az.EventGrid</span></span>
* <span data-ttu-id="b422e-492">Az elgépelés ki lett javítva a New-AzEventGridSubscription dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="b422e-492">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b422e-493">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b422e-493">Az.IotHub</span></span>
* <span data-ttu-id="b422e-494">Az engedélyezési szabályzati kulcsok újragenerálásának támogatása hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="b422e-494">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b422e-495">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b422e-495">Az.Network</span></span>
* <span data-ttu-id="b422e-496">A „RoutingPreference” hozzáadva a nyilvános IP-címkékhez</span><span class="sxs-lookup"><span data-stu-id="b422e-496">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="b422e-497">Javítottuk a példákat a „Get-AzNetworkServiceTag” referenciadokumentációban</span><span class="sxs-lookup"><span data-stu-id="b422e-497">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b422e-498">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b422e-498">Az.PolicyInsights</span></span>
* <span data-ttu-id="b422e-499">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyState parancsmagban</span><span class="sxs-lookup"><span data-stu-id="b422e-499">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="b422e-500">További információ: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="b422e-500">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b422e-501">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b422e-501">Az.OperationalInsights</span></span>
* <span data-ttu-id="b422e-502">Javítottuk a Get-AzOperationalInsightsDataSource parancsmagban visszaadott CustomLog adatforrásmodellt</span><span class="sxs-lookup"><span data-stu-id="b422e-502">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b422e-503">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b422e-503">Az.RecoveryServices</span></span>
* <span data-ttu-id="b422e-504">Az IaaSVMs get-policy parancsának javítása</span><span class="sxs-lookup"><span data-stu-id="b422e-504">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="b422e-505">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b422e-505">Az.Resources</span></span>
    - <span data-ttu-id="b422e-506">A Get-AzPolicyState -Top paraméter súgószövegének javítása</span><span class="sxs-lookup"><span data-stu-id="b422e-506">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="b422e-507">Ügyféloldali lapozás támogatásának hozzáadása a Get-AzPolicyAlias parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b422e-507">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="b422e-508">Új (-PolicyParameters és -PolicyParametersObject) paraméterek hozzáadása a Set-AzPolicyAssignment parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b422e-508">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="b422e-509">A Policy-parancsmagok néhány dokumentumának és példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="b422e-509">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b422e-510">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b422e-510">Az.ServiceBus</span></span>
* <span data-ttu-id="b422e-511">A 4938-as hiba javítása – A New-AzureRmServiceBusQueue parancsmag BadRequest értéket ad vissza a MaxSizeInMegabytes megadásakor</span><span class="sxs-lookup"><span data-stu-id="b422e-511">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="b422e-512">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b422e-512">Az.Sql</span></span>
* <span data-ttu-id="b422e-513">A példány-feladatátvételi csoportok parancsmagjainak hozzáadása az előzetes kiadásból a nyilvános kiadáshoz</span><span class="sxs-lookup"><span data-stu-id="b422e-513">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="b422e-514">Az Azure SQL Server\Database Auditing támogatása új parancsmagokkal.</span><span class="sxs-lookup"><span data-stu-id="b422e-514">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="b422e-515">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="b422e-515">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="b422e-516">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="b422e-516">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="b422e-517">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="b422e-517">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="b422e-518">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="b422e-518">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="b422e-519">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="b422e-519">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="b422e-520">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="b422e-520">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="b422e-521">E-mailes korlátozások eltávolítása a sebezhetőségi felmérés beállításaiból</span><span class="sxs-lookup"><span data-stu-id="b422e-521">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b422e-522">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b422e-522">Az.Storage</span></span>
* <span data-ttu-id="b422e-523">Az „-IndexDocument” és „-ErrorDocument404Path” paraméter módosítása kötelezőről opcionálisra a következő parancsmagban:</span><span class="sxs-lookup"><span data-stu-id="b422e-523">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="b422e-524">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="b422e-524">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="b422e-525">A Get-AzStorageBlobContent súgójának frissítése egy példa hozzáadásával</span><span class="sxs-lookup"><span data-stu-id="b422e-525">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="b422e-526">További hibaadatok megjelenítése, ha a parancsmag futtatása StorageException miatt meghiúsul</span><span class="sxs-lookup"><span data-stu-id="b422e-526">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="b422e-527">Storage-fiók létrehozásának és frissítésének támogatása Azure Files AAD DS-hitelesítéssel</span><span class="sxs-lookup"><span data-stu-id="b422e-527">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="b422e-528">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b422e-528">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="b422e-529">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b422e-529">Set-AzStorageAccount</span></span>
* <span data-ttu-id="b422e-530">Támogatás a fájlmegosztások, fájlkönyvtárak vagy fájlok fájlleíróinak listázásához vagy bezárásához</span><span class="sxs-lookup"><span data-stu-id="b422e-530">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="b422e-531">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="b422e-531">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="b422e-532">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="b422e-532">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="b422e-533">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="b422e-533">Az.StorageSync</span></span>
* <span data-ttu-id="b422e-534">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="b422e-534">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="b422e-535">2.3.2 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="b422e-535">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b422e-536">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b422e-536">Az.Accounts</span></span>
* <span data-ttu-id="b422e-537">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen URL-címeket használt a Functions-hívásokhoz</span><span class="sxs-lookup"><span data-stu-id="b422e-537">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="b422e-538">További információ: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="b422e-538">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="b422e-539">Javítva lett az aliasok hibája az AzureRM–Az parancsmagok közötti átvitel esetében</span><span class="sxs-lookup"><span data-stu-id="b422e-539">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="b422e-540">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="b422e-540">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="b422e-541">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="b422e-541">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b422e-542">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b422e-542">Az.Compute</span></span>
* <span data-ttu-id="b422e-543">A „New-AzVm” és „New-AzVmss” egyszerű paraméterkészletek mostantól elfogadják a „ProximityPlacementGroup” paramétert.</span><span class="sxs-lookup"><span data-stu-id="b422e-543">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="b422e-544">Az elgépelés ki lett javítva a „New-AzVM” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="b422e-544">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="b422e-545">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="b422e-545">Az.Dns</span></span>
* <span data-ttu-id="b422e-546">Az elgépelés ki lett javítva a „Set-AzDnsZone” súgópéldáinál.</span><span class="sxs-lookup"><span data-stu-id="b422e-546">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b422e-547">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b422e-547">Az.EventGrid</span></span>
* <span data-ttu-id="b422e-548">Frissítve a 2019-06-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="b422e-548">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="b422e-549">Új parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="b422e-549">New cmdlets:</span></span>
    - <span data-ttu-id="b422e-550">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="b422e-550">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="b422e-551">Létrehoz egy új Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="b422e-551">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="b422e-552">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="b422e-552">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="b422e-553">Lekéri egy Event Grid-tartomány részleteit, vagy az aktuális Azure-előfizetéshez tartozó összes Event Grid-tartomány listáját.</span><span class="sxs-lookup"><span data-stu-id="b422e-553">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="b422e-554">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="b422e-554">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="b422e-555">Eltávolít egy Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="b422e-555">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="b422e-556">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="b422e-556">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="b422e-557">Újra létrehozza a megosztott hozzáférési kulcsot az Azure Event Grid-tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="b422e-557">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="b422e-558">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="b422e-558">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="b422e-559">Lekéri az Event Grid-tartományban való esemény-közzétételhez használt megosztott hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="b422e-559">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="b422e-560">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="b422e-560">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="b422e-561">Új Azure Event Grid-tartományi témakört hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b422e-561">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="b422e-562">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="b422e-562">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="b422e-563">Lekéri egy Event Grid-tartományi témakör részleteit, vagy az aktuális Azure-előfizetés adott Event Grid-tartományához tartozó Event Grid-tartományi témakörök listáját</span><span class="sxs-lookup"><span data-stu-id="b422e-563">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="b422e-564">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="b422e-564">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="b422e-565">Eltávolít egy meglévő Azure Event Grid-tartományi témakört.</span><span class="sxs-lookup"><span data-stu-id="b422e-565">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="b422e-566">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="b422e-566">Updated cmdlets:</span></span>
    - <span data-ttu-id="b422e-567">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="b422e-567">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="b422e-568">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="b422e-568">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="b422e-569">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="b422e-569">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="b422e-570">Új paraméterkészletek lettek hozzáadva tartományok és tartományi témakörök esetében, lehetővé téve a meglévő paraméterek (például EndPointType, SubjectBeginsWith stb.) újbóli felhasználását.</span><span class="sxs-lookup"><span data-stu-id="b422e-570">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="b422e-571">Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="b422e-571">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="b422e-572">Esemény-előfizetés lejárati dátuma,</span><span class="sxs-lookup"><span data-stu-id="b422e-572">Event subscription expiration date,</span></span>
            - <span data-ttu-id="b422e-573">Speciális szűrési paraméterek.</span><span class="sxs-lookup"><span data-stu-id="b422e-573">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="b422e-574">Új felsorolási érték lett hozzáadva a servicebusqueue elem célértékeként.</span><span class="sxs-lookup"><span data-stu-id="b422e-574">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="b422e-575">Nem engedélyezett az -IncludedEventType beállításnál az „All” érték használata és a következővel való helyettesítése:</span><span class="sxs-lookup"><span data-stu-id="b422e-575">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="b422e-576">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="b422e-576">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="b422e-577">Új opcionális paraméterek (Top, ODataQuery és NextLink) az eredmények tördelésének és szűrésének támogatásához.</span><span class="sxs-lookup"><span data-stu-id="b422e-577">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="b422e-578">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="b422e-578">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="b422e-579">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="b422e-579">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="b422e-580">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="b422e-580">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="b422e-581">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b422e-581">Az.FrontDoor</span></span>
* <span data-ttu-id="b422e-582">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="b422e-582">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="b422e-583">Hozzá lett adva az átalakítások támogatása és az új operátorértékek automatikus kitöltése (RegEx)</span><span class="sxs-lookup"><span data-stu-id="b422e-583">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="b422e-584">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="b422e-584">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="b422e-585">Hozzá lett adva az új értékek automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="b422e-585">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b422e-586">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b422e-586">Az.Network</span></span>
* <span data-ttu-id="b422e-587">Virtuális hálózati átjárók erőforrás-támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b422e-587">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="b422e-588">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b422e-588">New cmdlets</span></span>
        - <span data-ttu-id="b422e-589">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="b422e-589">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="b422e-590">AvailablePrivateEndpointType hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b422e-590">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="b422e-591">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b422e-591">New cmdlets</span></span>
        - <span data-ttu-id="b422e-592">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="b422e-592">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="b422e-593">PrivatePrivateLinkService hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b422e-593">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="b422e-594">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b422e-594">New cmdlets</span></span>
        - <span data-ttu-id="b422e-595">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b422e-595">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="b422e-596">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b422e-596">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="b422e-597">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b422e-597">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="b422e-598">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b422e-598">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="b422e-599">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b422e-599">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="b422e-600">PrivateEndpoint hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b422e-600">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="b422e-601">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b422e-601">New cmdlets</span></span>
        - <span data-ttu-id="b422e-602">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b422e-602">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="b422e-603">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b422e-603">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="b422e-604">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b422e-604">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="b422e-605">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="b422e-605">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="b422e-606">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: UseLocalAzureIpAddress jelző a VpnConnection elemen</span><span class="sxs-lookup"><span data-stu-id="b422e-606">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="b422e-607">Frissítve lett a New-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="b422e-607">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="b422e-608">Frissítve lett a Set-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="b422e-608">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="b422e-609">Hozzá lett adva az írásvédett PeeredConnections mező az ExpressRoute-társhálózatlétesítések esetében.</span><span class="sxs-lookup"><span data-stu-id="b422e-609">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="b422e-610">Hozzá lett adva az írásvédett GlobalReachEnabled mező az ExpressRoute esetében.</span><span class="sxs-lookup"><span data-stu-id="b422e-610">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="b422e-611">Kompatibilitástörő változást okozó attribútum lett hozzáadva, amely jelzi az AllowGlobalReach mező elavulását az ExpressRouteCircuit-modellben</span><span class="sxs-lookup"><span data-stu-id="b422e-611">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="b422e-612">Javítva lett a 8756-os hiba a TargetListenerID AzApplicationGatewayRedirectConfiguration-parancsmagokkal való használata során</span><span class="sxs-lookup"><span data-stu-id="b422e-612">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="b422e-613">Javítva lett a hiba a New-AzApplicationGatewayPathRuleConfig parancsmagban, amely megakadályozta az átírási szabálykészlet beállítását.</span><span class="sxs-lookup"><span data-stu-id="b422e-613">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="b422e-614">Javítva lett a VirtualNetworkTaps megjelenítése a NetworkInterfaceIpConfiguration esetében</span><span class="sxs-lookup"><span data-stu-id="b422e-614">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="b422e-615">Javítva lettek a Cortex Get-parancsmagok az összes rész felsorolásához</span><span class="sxs-lookup"><span data-stu-id="b422e-615">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="b422e-616">Javítva lett a VirtualHub-hivatkozás létrehozása az ExpressRouteGateways, VpnGateway esetében</span><span class="sxs-lookup"><span data-stu-id="b422e-616">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="b422e-617">Hozzá lett adva a rendelkezésreállási zónák támogatása az AzureFirewall és a NatGateway esetében</span><span class="sxs-lookup"><span data-stu-id="b422e-617">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="b422e-618">Hozzá lett adva a Get-AzNetworkServiceTag parancsmag</span><span class="sxs-lookup"><span data-stu-id="b422e-618">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="b422e-619">Hozzá lett adva a több nyilvános IP-cím támogatása az Azure Firewall esetében</span><span class="sxs-lookup"><span data-stu-id="b422e-619">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="b422e-620">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="b422e-620">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="b422e-621">Hozzá lett adva a -PublicIpAddress paraméter, amely egy vagy több nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="b422e-621">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="b422e-622">Hozzá lett adva a -VirtualNetwork paraméter, amely virtuális hálózati objektumokat fogad el</span><span class="sxs-lookup"><span data-stu-id="b422e-622">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="b422e-623">Hozzá lett adva az AddPublicIpAddress és RemovePublicIpAddress metódus a tűzfalobjektumok esetében, és nyilvános IP-cím-objektumokat fogadnak el bemeneti adatként</span><span class="sxs-lookup"><span data-stu-id="b422e-623">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="b422e-624">Elavult a -PublicIpName és a -VirtualNetworkName paraméter</span><span class="sxs-lookup"><span data-stu-id="b422e-624">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="b422e-625">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: VpnClient AAD-alapú hitelesítési beállítások megadása a virtuális hálózati átjárók erőforrásaihoz.</span><span class="sxs-lookup"><span data-stu-id="b422e-625">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="b422e-626">Frissült a New-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="b422e-626">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="b422e-627">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="b422e-627">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="b422e-628">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva a RemoveAadAuthentication opcionális kapcsolóparaméter a VpnClient AAD-alapú hitelesítési beállítások eltávolításához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="b422e-628">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b422e-629">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b422e-629">Az.OperationalInsights</span></span>
* <span data-ttu-id="b422e-630">Engedélyezve lett a **pergb2018** tarifacsomag a „New-AzureRmOperationalInsightsWorkspace” parancs esetében</span><span class="sxs-lookup"><span data-stu-id="b422e-630">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="b422e-631">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b422e-631">Az.Resources</span></span>
* <span data-ttu-id="b422e-632">További sablonexportálási beállítások támogatása</span><span class="sxs-lookup"><span data-stu-id="b422e-632">Support for additional Template Export options</span></span>
    - <span data-ttu-id="b422e-633">Hozzá lett adva a „-SkipResourceNameParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="b422e-633">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="b422e-634">Hozzá lett adva a „-SkipAllParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="b422e-634">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="b422e-635">Hozzá lett adva a „-Resource” paraméter az Export-AzResourceGroup esetében az exportált erőforrások szűréséhez</span><span class="sxs-lookup"><span data-stu-id="b422e-635">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b422e-636">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b422e-636">Az.ServiceFabric</span></span>
* <span data-ttu-id="b422e-637">Ki lett javítva az a hiba, hogy a ByExistingKeyVault tanúsítvány hozzáadása bizonyos esetekben helytelen ujjlenyomatot kért le</span><span class="sxs-lookup"><span data-stu-id="b422e-637">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="b422e-638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b422e-638">Az.Sql</span></span>
* <span data-ttu-id="b422e-639">Javítva lett az Advanced Threat Protection Storage-végpontjának utótagja</span><span class="sxs-lookup"><span data-stu-id="b422e-639">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="b422e-640">Javítva lett, hogy az Advanced Data Security engedélyezése felülbírálja az Advanced Threat Protection-szabályzatot</span><span class="sxs-lookup"><span data-stu-id="b422e-640">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="b422e-641">Új parancsmagok lettek hozzáadva a Management.Sql esetében, amelyek lehetővé teszik az ügyfelek számára TDE-kulcsok hozzáadását és TDE-védő beállítását a felügyelt példányokhoz</span><span class="sxs-lookup"><span data-stu-id="b422e-641">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="b422e-642">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b422e-642">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="b422e-643">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b422e-643">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="b422e-644">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b422e-644">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="b422e-645">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="b422e-645">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="b422e-646">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="b422e-646">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b422e-647">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b422e-647">Az.Storage</span></span>
* <span data-ttu-id="b422e-648">A FileStorage és az SkuName Premium_ZRS altípus támogatása Storage-fiókok létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="b422e-648">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="b422e-649">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b422e-649">New-AzStorageAccount</span></span>
* <span data-ttu-id="b422e-650">Egyértelműsítve lett a blobmódosíthatatlansági parancsmag leírása</span><span class="sxs-lookup"><span data-stu-id="b422e-650">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="b422e-651">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b422e-651">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b422e-652">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b422e-652">Az.Websites</span></span>
* <span data-ttu-id="b422e-653">Optimalizálva lett a Get-AzWebAppCertificate parancsmag, hogy erőforráscsoport szerint szűrjön a kiszolgálón, ne ügyfél szerint</span><span class="sxs-lookup"><span data-stu-id="b422e-653">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="b422e-654">Hozzá lett adva a -UseDisasterRecovery kapcsolóparaméter a Get-AzWebAppSnapshot parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b422e-654">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="b422e-655">2.2.0 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="b422e-655">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="b422e-656">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b422e-656">Az.Cdn</span></span>
* <span data-ttu-id="b422e-657">Frissített parancsmagok a rulesEngine szolgáltatás támogatásához a 2019. 04. 15. API-verzión</span><span class="sxs-lookup"><span data-stu-id="b422e-657">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b422e-658">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b422e-658">Az.Compute</span></span>
* <span data-ttu-id="b422e-659">A `NoWait` paraméter hozzáadása, amely elindítja a műveletet, és azonnal visszatér, még a művelet befejezése előtt.</span><span class="sxs-lookup"><span data-stu-id="b422e-659">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="b422e-660">Frissített parancsmagok:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="b422e-660">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b422e-661">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b422e-661">Az.EventHub</span></span>
* <span data-ttu-id="b422e-662">A 9231-es hiba javítása – a Get-AzEventHubNamespace nem ad vissza címkéket</span><span class="sxs-lookup"><span data-stu-id="b422e-662">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="b422e-663">A 9230-as hiba javítása – a Get-AzEventHubNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="b422e-663">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b422e-664">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b422e-664">Az.Network</span></span>
* <span data-ttu-id="b422e-665">ResourceID és InputObject frissítése a Nat-átjárón</span><span class="sxs-lookup"><span data-stu-id="b422e-665">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="b422e-666">ResourceID és InputObject aliasának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="b422e-666">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b422e-667">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b422e-667">Az.PolicyInsights</span></span>
* <span data-ttu-id="b422e-668">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyEvent parancsmagban</span><span class="sxs-lookup"><span data-stu-id="b422e-668">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b422e-669">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b422e-669">Az.RecoveryServices</span></span>
* <span data-ttu-id="b422e-670">Az IaaSVM szabályzat minimális megőrzési ideje 7 napról 1-re módosult</span><span class="sxs-lookup"><span data-stu-id="b422e-670">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b422e-671">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b422e-671">Az.ServiceBus</span></span>
* <span data-ttu-id="b422e-672">A 9182-es hiba javítása – a Get-AzServiceBusNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="b422e-672">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b422e-673">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b422e-673">Az.ServiceFabric</span></span>
* <span data-ttu-id="b422e-674">Az Update-AzServiceFabricReliability hibaüzenetében lévő gépelési hiba kijavítása</span><span class="sxs-lookup"><span data-stu-id="b422e-674">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="b422e-675">A Service Fabric parancssorok hiányzó karakterének pótlása</span><span class="sxs-lookup"><span data-stu-id="b422e-675">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="b422e-676">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b422e-676">Az.Sql</span></span>
* <span data-ttu-id="b422e-677">A DnsZonePartner paraméter hozzáadása a New-AzureSqlInstance parancsmaghoz az AutoDr képesség a felügyelt példányon való támogatásához.</span><span class="sxs-lookup"><span data-stu-id="b422e-677">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="b422e-678">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag kivezetése</span><span class="sxs-lookup"><span data-stu-id="b422e-678">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="b422e-679">Threat Detection parancsmagok átnevezése Advanced Threat Protection névre</span><span class="sxs-lookup"><span data-stu-id="b422e-679">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="b422e-680">A New-AzSqlInstance, - StorageSizeInGB és - LicenseType paraméterek mostantól nem kötelezőek.</span><span class="sxs-lookup"><span data-stu-id="b422e-680">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b422e-681">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b422e-681">Az.Websites</span></span>
* <span data-ttu-id="b422e-682">javítja azt a hibát, amely miatt a Set-AzWebApp és a Set-AzWebAppSlot a -WebApp tulajdonsággal való használata eltávolította a címkéket</span><span class="sxs-lookup"><span data-stu-id="b422e-682">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="b422e-683">2.1.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="b422e-683">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="b422e-684">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b422e-684">Az.ApiManagement</span></span>
* <span data-ttu-id="b422e-685">Új parancsmagok a globális és API-szintű diagnosztika kezeléshez</span><span class="sxs-lookup"><span data-stu-id="b422e-685">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="b422e-686">**Get-AzApiManagementDiagnostic** – A globális vagy API hatókörre konfigurált diagnosztika beolvasása</span><span class="sxs-lookup"><span data-stu-id="b422e-686">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="b422e-687">**New-AzApiManagementDiagnostic** – Új diagnosztika létrehozása a globális vagy API szintű hatókörhöz</span><span class="sxs-lookup"><span data-stu-id="b422e-687">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="b422e-688">**New-AzApiManagementHttpMessageDiagnostic** – Diagnosztikai beállítás létrehozása arra vonatkozóan, hogy mely fejléceknél naplózzon a rendszer, és mekkora legyen a törzs mérete bájtban</span><span class="sxs-lookup"><span data-stu-id="b422e-688">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="b422e-689">**New-AzApiManagementPipelineDiagnosticSetting** – Diagnosztikai beállítások létrehozása az átjáróra érkező és onnan induló HTTP-üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="b422e-689">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="b422e-690">**New-AzApiManagementSamplingSetting** – Mintavételezési beállítások létrehozása diagnosztikai kérésekhez/válaszokhoz</span><span class="sxs-lookup"><span data-stu-id="b422e-690">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="b422e-691">**Remove-AzApiManagementDiagnostic** – Diagnosztikai entitás eltávolítása globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="b422e-691">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="b422e-692">**Set-AzApiManagementDiagnostic** – Diagnosztikai entitás frissítése globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="b422e-692">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="b422e-693">Új parancsmagok az ApiManagement szolgáltatás gyorsítótárának kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="b422e-693">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="b422e-694">**Get-AzApiManagementCache** – Az azonosító által megadott vagy az összes gyorsítótár részleteinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="b422e-694">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="b422e-695">**New-AzApiManagementCache** – Új alapértelmezett gyorsítótár létrehozása vagy gyorsítótár létrehozása adott Azure-régióban</span><span class="sxs-lookup"><span data-stu-id="b422e-695">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="b422e-696">**Remove-AzApiManagementCache** – Gyorsítótár eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b422e-696">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="b422e-697">**Update-AzApiManagementCache** – Gyorsítótár frissítése</span><span class="sxs-lookup"><span data-stu-id="b422e-697">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="b422e-698">Új parancsmagok az API-séma kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="b422e-698">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="b422e-699">**New-AzApiManagementSchema** – Új séma létrehozása egy API-hoz</span><span class="sxs-lookup"><span data-stu-id="b422e-699">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="b422e-700">**Get-AzApiManagementSchema** – Az API-ban konfigurált sémák beolvasása</span><span class="sxs-lookup"><span data-stu-id="b422e-700">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="b422e-701">**Remove-AzApiManagementSchema** – Az API-ban konfigurált sémák eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b422e-701">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="b422e-702">**Set-AzApiManagementSchema** – Az API-ban konfigurált séma frissítése</span><span class="sxs-lookup"><span data-stu-id="b422e-702">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="b422e-703">Új parancsmag a felhasználói jogkivonat létrehozásához</span><span class="sxs-lookup"><span data-stu-id="b422e-703">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="b422e-704">**New-AzApiManagementUserToken** – Új, alapértelmezés szerint 8 órán át érvényes felhasználói jogkivonat létrehozása. Ezen parancsmag használatával lehet a „GIT” felhasználó számára jogkivonatot létrehozni.</span><span class="sxs-lookup"><span data-stu-id="b422e-704">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="b422e-705">Új parancsmag a hálózat állapotának lekérdezéséhez</span><span class="sxs-lookup"><span data-stu-id="b422e-705">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="b422e-706">**Get-AzApiManagementNetworkStatus** – Azon erőforrások hálózati állapotának beolvasása, amelyektől az API Management szolgáltatás függ.</span><span class="sxs-lookup"><span data-stu-id="b422e-706">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="b422e-707">Ez hasznos lehet, ha az ApiManagement szolgáltatást virtuális hálózatra telepíti, és ellenőrizni kell, hogy rendben működnek-e a függőségek.</span><span class="sxs-lookup"><span data-stu-id="b422e-707">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="b422e-708">A **New-AzApiManagement** parancsmag frissítése az ApiManagement szolgáltatás kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="b422e-708">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="b422e-709">Mostantól az új „Consumption” SKU is támogatott</span><span class="sxs-lookup"><span data-stu-id="b422e-709">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="b422e-710">Mostantól az „EnableClientCertificate” jelző a „Consumption” SKU-hoz is bekapcsolható</span><span class="sxs-lookup"><span data-stu-id="b422e-710">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="b422e-711">Az új **New-AzApiManagementSslSetting** parancsmag lehetővé teszi a „TLS/SSL” beállítás konfigurálását a „Háttér” és „Előtér” esetén is.</span><span class="sxs-lookup"><span data-stu-id="b422e-711">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="b422e-712">Ez egy ApiManagement szolgáltatás előterén a titkosítások, mint például a 3DES, valamint a szerverprotokollok, mint például a Http2 konfigurálására is alkalmas.</span><span class="sxs-lookup"><span data-stu-id="b422e-712">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="b422e-713">Mostantól támogatott a „DeveloperPortal” gazdanév ApiManagement szolgáltatáson történő konfigurálása.</span><span class="sxs-lookup"><span data-stu-id="b422e-713">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="b422e-714">A **Get-AzApiManagementSsoToken** parancsmagok frissítése a „PsApiManagement” objektum bemenetként való használatához</span><span class="sxs-lookup"><span data-stu-id="b422e-714">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="b422e-715">A parancsmag frissítése a hibaüzenetek beágyazott megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="b422e-715">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="b422e-716">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hibakód: ValidationError Hibaüzenet: Egy vagy több mező hibás értéket tartalmaz: Hiba részletei:    [Kód=ValidationError, Üzenet=Hiba a log-to-eventhub elemben, 3. sor, 10. oszlop: A naplózó nem található, Cél=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="b422e-716">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="b422e-717">Az **Export-AzApiManagementApi** parancsmag frissítse az API-k OpenApi 3.0 formátumban való exportálásához</span><span class="sxs-lookup"><span data-stu-id="b422e-717">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="b422e-718">Az **Import-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="b422e-718">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="b422e-719">API importálása az OpenApi 3.0 dokumentumspecifikációból</span><span class="sxs-lookup"><span data-stu-id="b422e-719">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="b422e-720">A bármely (Swagger, Wadl, Wsdl, OpenAPI) dokumentumban megadott PsApiManagementSchema tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="b422e-720">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="b422e-721">A bármely dokumentumban megadott ServiceUrl tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="b422e-721">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="b422e-722">A **Get-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) való visszaadásához</span><span class="sxs-lookup"><span data-stu-id="b422e-722">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="b422e-723">A **Set-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) és XML-nek megfelelő feloldójeles formátumban (xml használatával) való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="b422e-723">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="b422e-724">A **New-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="b422e-724">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="b422e-725">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="b422e-725">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="b422e-726">API létrehozása ApiVersionSet tulajdonságban</span><span class="sxs-lookup"><span data-stu-id="b422e-726">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="b422e-727">API klónozása SourceApiId és SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="b422e-727">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="b422e-728">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="b422e-728">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="b422e-729">A **Set-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="b422e-729">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="b422e-730">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="b422e-730">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="b422e-731">API frissítése ApiVersionSet tulajdonságba</span><span class="sxs-lookup"><span data-stu-id="b422e-731">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="b422e-732">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="b422e-732">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="b422e-733">A **New-AzApiManagementRevision** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="b422e-733">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="b422e-734">Létező változat klónozása (címkék, termékek, műveletek és szabályzatok másolása) a SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="b422e-734">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="b422e-735">Az új változat a szülő ApiId értékét veszi át</span><span class="sxs-lookup"><span data-stu-id="b422e-735">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="b422e-736">ApiRevisionDescription biztosítása</span><span class="sxs-lookup"><span data-stu-id="b422e-736">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="b422e-737">A „ServiceUrl” felülírása API klónozáskor</span><span class="sxs-lookup"><span data-stu-id="b422e-737">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="b422e-738">A **New-AzApiManagementIdentityProvider** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="b422e-738">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="b422e-739">AAD vagy AADB2C konfigurálása hitelesítésszolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="b422e-739">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="b422e-740">SignupPolicy, SigninPolicy, ProfileEditingPolicy és PasswordResetPolicy beállítása</span><span class="sxs-lookup"><span data-stu-id="b422e-740">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="b422e-741">A **New-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="b422e-741">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="b422e-742">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="b422e-742">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="b422e-743">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="b422e-743">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="b422e-744">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="b422e-744">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="b422e-745">A **Set-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="b422e-745">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="b422e-746">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="b422e-746">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="b422e-747">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="b422e-747">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="b422e-748">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="b422e-748">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="b422e-749">Az alábbi parancsmagok frissültek a ResourceID bemenetként való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="b422e-749">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="b422e-750">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b422e-750">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="b422e-751">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="b422e-751">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="b422e-752">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b422e-752">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="b422e-753">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="b422e-753">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="b422e-754">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b422e-754">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="b422e-755">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="b422e-755">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="b422e-756">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="b422e-756">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="b422e-757">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b422e-757">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="b422e-758">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="b422e-758">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="b422e-759">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b422e-759">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="b422e-760">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b422e-760">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="b422e-761">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b422e-761">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b422e-762">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b422e-762">Az.Automation</span></span>
* <span data-ttu-id="b422e-763">A Get-AzAutomationJobOutputRecord frissítése a JSON- és a szövegrekordértékek kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="b422e-763">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="b422e-764">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="b422e-764">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="b422e-765">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="b422e-765">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="b422e-766">A Start-AzAutomationDscCompilationJob viselkedésének módosítása a munka elindítására a befejezésre való várakozás helyett</span><span class="sxs-lookup"><span data-stu-id="b422e-766">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="b422e-767">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="b422e-767">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="b422e-768">A Get-AzAutomationDscNode azon hibájának javítása, amely miatt a -Name használatakor az összes csomópontot visszaadta.</span><span class="sxs-lookup"><span data-stu-id="b422e-768">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="b422e-769">Most már csak az egyező csomópontot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="b422e-769">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b422e-770">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b422e-770">Az.Compute</span></span>
* <span data-ttu-id="b422e-771">A ProtectFromScaleIn és a ProtectFromScaleSetAction paraméterek hozzáadása az Update-AzVmssVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b422e-771">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="b422e-772">A New-azvm fedőparaméter-készlet mostantól alapértelmezetten egy elérhető helyet használ, ha az USA keleti régiója nem támogatott</span><span class="sxs-lookup"><span data-stu-id="b422e-772">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b422e-773">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b422e-773">Az.DataLakeStore</span></span>
* <span data-ttu-id="b422e-774">Az ADLS SDK frissítése a httpclient használatához, integrált adatsíkteszteléssel az Azure-keretrendszerben</span><span class="sxs-lookup"><span data-stu-id="b422e-774">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b422e-775">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b422e-775">Az.Monitor</span></span>
* <span data-ttu-id="b422e-776">A hibás paraméternevek kijavítása a súgópéldákban</span><span class="sxs-lookup"><span data-stu-id="b422e-776">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b422e-777">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b422e-777">Az.Network</span></span>
* <span data-ttu-id="b422e-778">DisableBgpRoutePropagation jelölő hozzáadása az érvényes útválasztási táblázathoz</span><span class="sxs-lookup"><span data-stu-id="b422e-778">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="b422e-779">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="b422e-779">Updated cmdlet:</span></span>
        - <span data-ttu-id="b422e-780">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="b422e-780">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="b422e-781">A dupla kötőjel kijavítása a New-AzApplicationGatewayTrustedRootCertificate dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="b422e-781">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="b422e-782">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b422e-782">Az.Resources</span></span>
* <span data-ttu-id="b422e-783">Új Get-AzureRmDenyAssignment parancsmag hozzáadása a megtagadási hozzárendelések lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="b422e-783">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="b422e-784">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b422e-784">Az.Sql</span></span>
* <span data-ttu-id="b422e-785">Advanced Threat Protection parancsmagok átnevezése Advanced Data Security névre és a sebezhetőségi felmérés alapértelmezett engedélyezése</span><span class="sxs-lookup"><span data-stu-id="b422e-785">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="b422e-786">2.0.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="b422e-786">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b422e-787">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b422e-787">Az.Accounts</span></span>
* <span data-ttu-id="b422e-788">Az Authentication Library frissítése a felhasználóneves/jelszavas hitelesítéssel kapcsolatos ADFS-problémák kijavításához</span><span class="sxs-lookup"><span data-stu-id="b422e-788">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b422e-789">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b422e-789">Az.CognitiveServices</span></span>
* <span data-ttu-id="b422e-790">Csak a Bing jogi nyilatkozat jelenik meg a Bing Search-szolgáltatásoknál.</span><span class="sxs-lookup"><span data-stu-id="b422e-790">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="b422e-791">A sikertelen fióklétrehozás hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="b422e-791">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b422e-792">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b422e-792">Az.Compute</span></span>
* <span data-ttu-id="b422e-793">Közelségi elhelyezési csoport szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="b422e-793">Proximity placement group feature.</span></span>
    - <span data-ttu-id="b422e-794">A következő új parancsmagok lettek hozzáadva:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="b422e-794">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="b422e-795">Az új ProximityPlacementGroupId paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="b422e-795">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="b422e-796">A StorageAccountType paraméter hozzá lett adva a New-AzGalleryImageVersion parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="b422e-796">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="b422e-797">A New-AzGalleryImageVersion TargetRegion paramétere tartalmazhatja a következőt: StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="b422e-797">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="b422e-798">A SkipShutdown kapcsolóparaméter hozzá lett adva a Stop-AzVM és Stop-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="b422e-798">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="b422e-799">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="b422e-799">Breaking changes</span></span>
    - <span data-ttu-id="b422e-800">A Set-AzVMBootDiagnostics parancsmag új neve: Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="b422e-800">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="b422e-801">Az Export-AzLogAnalyticThrottledRequests parancsmag új neve: Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="b422e-801">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="b422e-802">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="b422e-802">Az.DeploymentManager</span></span>
* <span data-ttu-id="b422e-803">Az Azure Deployment Manager-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="b422e-803">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="b422e-804">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="b422e-804">Az.Dns</span></span>
* <span data-ttu-id="b422e-805">Automatikus DNS NameServer-delegálás</span><span class="sxs-lookup"><span data-stu-id="b422e-805">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="b422e-806">A DNS-zóna létrehozási parancsmag további opcionális paraméterként elfogadja a szülőzóna nevét.</span><span class="sxs-lookup"><span data-stu-id="b422e-806">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="b422e-807">Névkiszolgálói rekordokat ad hozzá a szülőzónában az újonnan létrehozott gyermekzóna számára.</span><span class="sxs-lookup"><span data-stu-id="b422e-807">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="b422e-808">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b422e-808">Az.FrontDoor</span></span>
* <span data-ttu-id="b422e-809">Az Azure FrontDoor-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="b422e-809">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="b422e-810">A WAF-parancsmagok új neve tartalmazza a „Waf” sztringet</span><span class="sxs-lookup"><span data-stu-id="b422e-810">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="b422e-811">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b422e-811">Az.HDInsight</span></span>
* <span data-ttu-id="b422e-812">A következő két parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="b422e-812">Removed two cmdlets:</span></span>
    - <span data-ttu-id="b422e-813">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="b422e-813">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="b422e-814">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="b422e-814">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="b422e-815">Egy új, Set-AzHDInsightGatewayCredential nevű parancsmag lett hozzáadva a Grant-AzHDInsightHttpServicesAccess helyett</span><span class="sxs-lookup"><span data-stu-id="b422e-815">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="b422e-816">A Get-AzHDInsightJobOutput parancsmag frissítve lett, hogy különbséget tegyen az olvasói és a HDInsight-operátori szerepkör között:</span><span class="sxs-lookup"><span data-stu-id="b422e-816">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="b422e-817">Az olvasói szerepkörrel rendelkező felhasználóknak explicit módon meg kell adniuk a DefaultStorageAccountKey paramétert, ellenkező esetben hiba történik.</span><span class="sxs-lookup"><span data-stu-id="b422e-817">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="b422e-818">A HDInsight-operátori szerepkörrel rendelkező felhasználókat ez nem érinti.</span><span class="sxs-lookup"><span data-stu-id="b422e-818">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b422e-819">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b422e-819">Az.Monitor</span></span>
* <span data-ttu-id="b422e-820">Az SQR API (ütemezett lekérdezési szabály) új parancsmagjai</span><span class="sxs-lookup"><span data-stu-id="b422e-820">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="b422e-821">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="b422e-821">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="b422e-822">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="b422e-822">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="b422e-823">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="b422e-823">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="b422e-824">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="b422e-824">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="b422e-825">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="b422e-825">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="b422e-826">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="b422e-826">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="b422e-827">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b422e-827">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="b422e-828">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b422e-828">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="b422e-829">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b422e-829">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="b422e-830">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b422e-830">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="b422e-831">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b422e-831">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="b422e-832">[További](/rest/api/monitor/scheduledqueryrules) információk az SQR API-ról</span><span class="sxs-lookup"><span data-stu-id="b422e-832">[More](/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="b422e-833">A frissített Az.Monitor.md tartalmazza a GenV2 (nem klasszikus) metrikaalapú riasztási szabály parancsmagjait</span><span class="sxs-lookup"><span data-stu-id="b422e-833">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b422e-834">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b422e-834">Az.Network</span></span>
* <span data-ttu-id="b422e-835">A NAT-átjáró erőforrás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b422e-835">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="b422e-836">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b422e-836">New cmdlets</span></span>
        - <span data-ttu-id="b422e-837">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="b422e-837">New-AzNatGateway</span></span>
        - <span data-ttu-id="b422e-838">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="b422e-838">Get-AzNatGateway</span></span>
        - <span data-ttu-id="b422e-839">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="b422e-839">Set-AzNatGateway</span></span>
        - <span data-ttu-id="b422e-840">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="b422e-840">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="b422e-841">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b422e-841">Updated cmdlets</span></span>
        - <span data-ttu-id="b422e-842">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="b422e-842">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="b422e-843">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="b422e-843">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="b422e-844">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: Egyéni útvonalak beállítása/eltávolítása a Brooklyn Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="b422e-844">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="b422e-845">Frissült a New-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="b422e-845">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="b422e-846">Frissült a Set-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="b422e-846">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b422e-847">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b422e-847">Az.PolicyInsights</span></span>
* <span data-ttu-id="b422e-848">A szabályzat-kiértékelési adatok lekérdezésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="b422e-848">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="b422e-849">Az -Expand paraméter hozzá lett adva a Get-AzPolicyState parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="b422e-849">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="b422e-850">Az -Expand PolicyEvaluationDetails támogatása.</span><span class="sxs-lookup"><span data-stu-id="b422e-850">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b422e-851">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b422e-851">Az.RecoveryServices</span></span>
* <span data-ttu-id="b422e-852">Az előfizetések közötti Azure–Azure Site Recovery átvitel támogatása.</span><span class="sxs-lookup"><span data-stu-id="b422e-852">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="b422e-853">Az Azure Site Recovery jövőbeni kompatibilitástörő változásainak jelölése.</span><span class="sxs-lookup"><span data-stu-id="b422e-853">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="b422e-854">Ki lett javítva az Azure Site Recovery helyreállítási és műveletterve.</span><span class="sxs-lookup"><span data-stu-id="b422e-854">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="b422e-855">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure hálózatleképezés.</span><span class="sxs-lookup"><span data-stu-id="b422e-855">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="b422e-856">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure védelemirány felügyelt lemezek esetében.</span><span class="sxs-lookup"><span data-stu-id="b422e-856">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="b422e-857">További kisebb javítások.</span><span class="sxs-lookup"><span data-stu-id="b422e-857">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="b422e-858">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="b422e-858">Az.Relay</span></span>
* <span data-ttu-id="b422e-859">Az elgépelések ki lettek javítva az ügyféloldali üzenetekben</span><span class="sxs-lookup"><span data-stu-id="b422e-859">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b422e-860">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b422e-860">Az.ServiceBus</span></span>
* <span data-ttu-id="b422e-861">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="b422e-861">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b422e-862">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b422e-862">Az.Storage</span></span>
* <span data-ttu-id="b422e-863">A Storage ügyféloldali kódtárának frissítése a 10.0.1-es verziójára (az SDK összes objektuma esetében módosul a névtér a Microsoft.WindowsAzure.Storage. *névtérről a Microsoft.Azure.Storage.* névtérre)</span><span class="sxs-lookup"><span data-stu-id="b422e-863">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="b422e-864">Frissítés a Microsoft.Azure.Management.Storage 11.0.0-s verziójára az új API-verzió (2019. 04. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="b422e-864">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="b422e-865">A Tárfiók létrehozása parancs esetében az alapértelmezett Storage-fiókaltípus a Storage helyett mostantól a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="b422e-865">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="b422e-866">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b422e-866">New-AzStorageAccount</span></span>
* <span data-ttu-id="b422e-867">A Storage-fiók Sku.Name parancsmagkimenete módosul, hogy igazodjon a bemeneti SkuName paraméterhez, egy aláhúzásjel („_”) hozzáadásával – például a StandardLRS a Standard_LRS névre módosul</span><span class="sxs-lookup"><span data-stu-id="b422e-867">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="b422e-868">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b422e-868">New-AzStorageAccount</span></span>
    - <span data-ttu-id="b422e-869">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b422e-869">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="b422e-870">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b422e-870">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b422e-871">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b422e-871">Az.Websites</span></span>
* <span data-ttu-id="b422e-872">Az Altípus tulajdonság mostantól meg lesz adva a Get-AzWebApp által visszaadott PSSite objektumokhoz</span><span class="sxs-lookup"><span data-stu-id="b422e-872">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="b422e-873">A Get-AzWebApp\*Metrics és a Get-AzAppServicePlanMetrics megjelölve elavultként</span><span class="sxs-lookup"><span data-stu-id="b422e-873">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="b422e-874">1.8.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="b422e-874">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b422e-875">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="b422e-875">Highlights since the last major release</span></span>
* <span data-ttu-id="b422e-876">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="b422e-876">General availability of `Az` module</span></span>
* <span data-ttu-id="b422e-877">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="b422e-877">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="b422e-878">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="b422e-878">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="b422e-879">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="b422e-879">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="b422e-880">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="b422e-880">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b422e-881">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="b422e-881">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="b422e-882">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="b422e-882">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b422e-883">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b422e-883">Az.Accounts</span></span>
* <span data-ttu-id="b422e-884">Eltávolítás-AzureRm megfelelően törölni a Mac modulok frissítése</span><span class="sxs-lookup"><span data-stu-id="b422e-884">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="b422e-885">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b422e-885">Az.Batch</span></span>
* <span data-ttu-id="b422e-886">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="b422e-886">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b422e-887">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b422e-887">Az.Cdn</span></span>
* <span data-ttu-id="b422e-888">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="b422e-888">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b422e-889">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b422e-889">Az.CognitiveServices</span></span>
* <span data-ttu-id="b422e-890">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="b422e-890">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b422e-891">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b422e-891">Az.Compute</span></span>
* <span data-ttu-id="b422e-892">Az AEM telepítési kapcsolatos problémák megoldásához, ha a lemezek erőforrás-azonosítók kisbetűs resourcegroups volt az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="b422e-892">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="b422e-893">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="b422e-893">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b422e-894">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="b422e-894">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b422e-895">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b422e-895">Az.DataFactory</span></span>
* <span data-ttu-id="b422e-896">Adjon hozzá SsisProperties, ha a NodeCount felügyelt integrációs modul nem null értékű.</span><span class="sxs-lookup"><span data-stu-id="b422e-896">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b422e-897">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b422e-897">Az.DataLakeStore</span></span>
* <span data-ttu-id="b422e-898">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="b422e-898">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b422e-899">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b422e-899">Az.EventGrid</span></span>
* <span data-ttu-id="b422e-900">A Súgó szöveg jelzi, hogy erőforrásokat kell létrehozni a create/update eseményt előfizetés parancsmagok használata előtt végpont frissítése.</span><span class="sxs-lookup"><span data-stu-id="b422e-900">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b422e-901">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b422e-901">Az.EventHub</span></span>
* <span data-ttu-id="b422e-902">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="b422e-902">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="b422e-903">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b422e-903">Az.HDInsight</span></span>
* <span data-ttu-id="b422e-904">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="b422e-904">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b422e-905">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b422e-905">Az.IotHub</span></span>
* <span data-ttu-id="b422e-906">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="b422e-906">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b422e-907">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b422e-907">Az.KeyVault</span></span>
* <span data-ttu-id="b422e-908">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="b422e-908">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b422e-909">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="b422e-909">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="b422e-910">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="b422e-910">Az.MachineLearning</span></span>
* <span data-ttu-id="b422e-911">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="b422e-911">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="b422e-912">Az.Media</span><span class="sxs-lookup"><span data-stu-id="b422e-912">Az.Media</span></span>
* <span data-ttu-id="b422e-913">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="b422e-913">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b422e-914">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b422e-914">Az.Monitor</span></span>
  * <span data-ttu-id="b422e-915">Riasztási szabály (nem klasszikus) GenV2 mérőszám-alapú új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b422e-915">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="b422e-916">Új AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="b422e-916">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="b422e-917">Új AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="b422e-917">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="b422e-918">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="b422e-918">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="b422e-919">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="b422e-919">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="b422e-920">Adjon hozzá AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="b422e-920">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="b422e-921">Frissített verzió 0.22.0-preview figyelő SDK</span><span class="sxs-lookup"><span data-stu-id="b422e-921">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b422e-922">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b422e-922">Az.Network</span></span>
* <span data-ttu-id="b422e-923">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="b422e-923">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b422e-924">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="b422e-924">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="b422e-925">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="b422e-925">Az.NotificationHubs</span></span>
* <span data-ttu-id="b422e-926">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="b422e-926">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b422e-927">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b422e-927">Az.OperationalInsights</span></span>
* <span data-ttu-id="b422e-928">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="b422e-928">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="b422e-929">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="b422e-929">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="b422e-930">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="b422e-930">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b422e-931">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b422e-931">Az.RecoveryServices</span></span>
* <span data-ttu-id="b422e-932">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="b422e-932">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b422e-933">Frissített táblázatos formában az SQL azure-beli virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="b422e-933">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="b422e-934">A hozzáadott alternatív módszert AzureFileShare hely beolvasása</span><span class="sxs-lookup"><span data-stu-id="b422e-934">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="b422e-935">Frissített ScheduleRunDays SchedulePolicy objektumban időzóna szerint</span><span class="sxs-lookup"><span data-stu-id="b422e-935">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="b422e-936">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b422e-936">Az.RedisCache</span></span>
* <span data-ttu-id="b422e-937">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="b422e-937">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b422e-938">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b422e-938">Az.Resources</span></span>
* <span data-ttu-id="b422e-939">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="b422e-939">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="b422e-940">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b422e-940">Az.Sql</span></span>
* <span data-ttu-id="b422e-941">Cserélje le a függőségi figyelő SDK közös kód</span><span class="sxs-lookup"><span data-stu-id="b422e-941">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="b422e-942">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="b422e-942">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b422e-943">Továbbfejlesztett folyamat, amely több oszlop osztályozási.</span><span class="sxs-lookup"><span data-stu-id="b422e-943">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="b422e-944">Termékváltozat tulajdonságok (termékváltozat neve, családi, kapacitás) válasz a Get-AzSqlServerServiceObjective és formátum táblaként alapértelmezés szerint tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b422e-944">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="b422e-945">Lehetővé teszi a Get-AzSqlServerServiceObjective anélkül, hogy a régióban egy már létező kiszolgáló hely alapján.</span><span class="sxs-lookup"><span data-stu-id="b422e-945">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="b422e-946">Hozzon létre felügyelt példányt az időzóna-paraméter támogatása.</span><span class="sxs-lookup"><span data-stu-id="b422e-946">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="b422e-947">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="b422e-947">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b422e-948">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b422e-948">Az.Websites</span></span>
* <span data-ttu-id="b422e-949">a Set-AzWebApp és a Set-AzWebAppSlot távolítja el a címkék a végrehajtási javítások</span><span class="sxs-lookup"><span data-stu-id="b422e-949">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="b422e-950">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="b422e-950">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b422e-951">A webhelyek SDK frissítése.</span><span class="sxs-lookup"><span data-stu-id="b422e-951">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="b422e-952">A AdminSiteName tulajdonság PSAppServicePlan eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="b422e-952">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="b422e-953">1.7.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="b422e-953">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b422e-954">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="b422e-954">Highlights since the last major release</span></span>
* <span data-ttu-id="b422e-955">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="b422e-955">General availability of `Az` module</span></span>
* <span data-ttu-id="b422e-956">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="b422e-956">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="b422e-957">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="b422e-957">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="b422e-958">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="b422e-958">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="b422e-959">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="b422e-959">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b422e-960">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="b422e-960">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="b422e-961">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="b422e-961">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b422e-962">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b422e-962">Az.Accounts</span></span>
* <span data-ttu-id="b422e-963">Frissített Add-AzEnvironment és Set-AzEnvironment parancsmag az AzureAnalysisServicesEndpointResourceId paraméter elfogadásához</span><span class="sxs-lookup"><span data-stu-id="b422e-963">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b422e-964">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b422e-964">Az.AnalysisServices</span></span>
* <span data-ttu-id="b422e-965">ServiceClient használata DataPlane-parancsmagokban és az eredeti hitelesítési logika eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b422e-965">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="b422e-966">Az Add-AzureASAccount burkolóként való megadása a Connect-AzAccount számára a kompatibilitástörő változás elkerüléséhez</span><span class="sxs-lookup"><span data-stu-id="b422e-966">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b422e-967">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b422e-967">Az.Automation</span></span>
* <span data-ttu-id="b422e-968">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag belefoglalásokat érintő hibája.</span><span class="sxs-lookup"><span data-stu-id="b422e-968">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="b422e-969">Az IncludedKbNumber és az IncludedPackageNameMask paraméter mostantól működőképes.</span><span class="sxs-lookup"><span data-stu-id="b422e-969">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="b422e-970">Hibajavítás az Azure Automation frissítéskezelési dinamikus csoportja esetében</span><span class="sxs-lookup"><span data-stu-id="b422e-970">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b422e-971">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b422e-971">Az.Compute</span></span>
* <span data-ttu-id="b422e-972">HyperVGeneration paraméter hozzáadása a New-AzDiskConfig és a New-AzSnapshotConfig parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="b422e-972">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="b422e-973">Virtuális gépek más bérlők katalógus-rendszerképével való létrehozásának engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="b422e-973">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="b422e-974">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b422e-974">Az.ContainerInstance</span></span>
* <span data-ttu-id="b422e-975">Ki lett javítva a New-AzContainerGroup üres záró argumentumot hozzáadó -Command paraméterével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="b422e-975">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b422e-976">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b422e-976">Az.DataFactory</span></span>
* <span data-ttu-id="b422e-977">Az ADF .Net SDK verziója 3.0.2-re frissült.</span><span class="sxs-lookup"><span data-stu-id="b422e-977">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="b422e-978">A Set-AzDataFactoryV2 parancsmag a RepoConfiguration beállításaihoz tartozó kiegészítő paraméterekkel lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="b422e-978">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b422e-979">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b422e-979">Az.Resources</span></span>
* <span data-ttu-id="b422e-980">Továbbfejlesztett szolgáltatókezelés a Get-AzResource esetében, -ResourceId vagy -ResourceGroupName, -Name és -ResourceType paraméterek megadásakor</span><span class="sxs-lookup"><span data-stu-id="b422e-980">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="b422e-981">Továbbfejlesztett hibakezelés a Test-AzDeployment és a Test-AzResourceGroupDeployment esetében</span><span class="sxs-lookup"><span data-stu-id="b422e-981">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="b422e-982">A hibákat nem a telepítés ellenőrzése során kezeli, hanem a parancs kimenetébe foglalja bele</span><span class="sxs-lookup"><span data-stu-id="b422e-982">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="b422e-983">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="b422e-983">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="b422e-984">-IgnoreDynamicParameters kapcsolóparaméter hozzáadása telepítési parancsmagokhoz a rendszer által feltett kérdések szkriptekben és feladatokban való mellőzéséhez</span><span class="sxs-lookup"><span data-stu-id="b422e-984">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="b422e-985">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="b422e-985">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="b422e-986">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b422e-986">Az.Sql</span></span>
* <span data-ttu-id="b422e-987">Adatbázisadat-besorolás támogatása.</span><span class="sxs-lookup"><span data-stu-id="b422e-987">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b422e-988">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b422e-988">Az.Storage</span></span>
* <span data-ttu-id="b422e-989">Részletes hibaüzenet megjelenítése Storage-környezet -UseConnectedAccount paraméterrel történő létrehozásakor az Azure-fiókba való bejelentkezés nélkül</span><span class="sxs-lookup"><span data-stu-id="b422e-989">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="b422e-990">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b422e-990">New-AzStorageContext</span></span>
* <span data-ttu-id="b422e-991">Adott Storage-fiók Blob service-tulajdonságai kezelésének támogatása Management plane API-val</span><span class="sxs-lookup"><span data-stu-id="b422e-991">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="b422e-992">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="b422e-992">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="b422e-993">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="b422e-993">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="b422e-994">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b422e-994">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="b422e-995">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b422e-995">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="b422e-996">Az -AsJob támogatása blobok és fájlok feltöltéséhez, valamint parancsmagok letöltéséhez</span><span class="sxs-lookup"><span data-stu-id="b422e-996">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="b422e-997">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b422e-997">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="b422e-998">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b422e-998">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="b422e-999">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b422e-999">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="b422e-1000">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b422e-1000">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="b422e-1001">1.6.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="b422e-1001">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b422e-1002">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="b422e-1002">Highlights since the last major release</span></span>
* <span data-ttu-id="b422e-1003">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="b422e-1003">General availability of `Az` module</span></span>
* <span data-ttu-id="b422e-1004">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="b422e-1004">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="b422e-1005">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="b422e-1005">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="b422e-1006">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="b422e-1006">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="b422e-1007">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="b422e-1007">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b422e-1008">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="b422e-1008">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="b422e-1009">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="b422e-1009">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b422e-1010">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b422e-1010">Az.Automation</span></span>
* <span data-ttu-id="b422e-1011">Az Azure Automation frissítéskezelése módosult, hogy támogassa az alábbi új funkciókat:</span><span class="sxs-lookup"><span data-stu-id="b422e-1011">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="b422e-1012">Dinamikus csoportosítás</span><span class="sxs-lookup"><span data-stu-id="b422e-1012">Dynamic grouping</span></span>
    * <span data-ttu-id="b422e-1013">Előzetesen és utólagosan futtatandó szkriptek</span><span class="sxs-lookup"><span data-stu-id="b422e-1013">Pre-Post script</span></span>
    * <span data-ttu-id="b422e-1014">Újraindítási beállítás</span><span class="sxs-lookup"><span data-stu-id="b422e-1014">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b422e-1015">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b422e-1015">Az.Compute</span></span>
* <span data-ttu-id="b422e-1016">Ki lett javítva az elérési útvonal feloldásával kapcsolatos hiba a Get-AzVmBootDiagnosticsData esetében</span><span class="sxs-lookup"><span data-stu-id="b422e-1016">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="b422e-1017">A Compute ügyfélkódtár frissült a 25.0.0 verzióra</span><span class="sxs-lookup"><span data-stu-id="b422e-1017">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b422e-1018">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b422e-1018">Az.KeyVault</span></span>
* <span data-ttu-id="b422e-1019">Helyettesítő karakterek támogatásának hozzáadása a KeyVault-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="b422e-1019">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b422e-1020">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b422e-1020">Az.Network</span></span>
* <span data-ttu-id="b422e-1021">Az Intelligens veszélyforrás-felderítés támogatásának hozzáadása az Azure Firewallhoz</span><span class="sxs-lookup"><span data-stu-id="b422e-1021">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="b422e-1022">Az Application Gateway-tűzfalszabályzat legfelső szintű erőforrása és egyéni szabályok hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b422e-1022">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b422e-1023">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b422e-1023">Az.RecoveryServices</span></span>
* <span data-ttu-id="b422e-1024">A SnapshotRetentionInDays hozzáadása az Azure-beli virtuális gépek szabályzatához az azonnali RP támogatása érdekében</span><span class="sxs-lookup"><span data-stu-id="b422e-1024">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="b422e-1025">Folyamat támogatásának hozzáadása a regisztrációtörlési tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="b422e-1025">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="b422e-1026">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b422e-1026">Az.Resources</span></span>
* <span data-ttu-id="b422e-1027">Helyettesítő karakterek támogatásának hozzáadása a Get-AzResource és Get-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="b422e-1027">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="b422e-1028">Az ARM általános hívása esetén használt hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="b422e-1028">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="b422e-1029">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b422e-1029">Az.Sql</span></span>
* <span data-ttu-id="b422e-1030">A Fenyegetésészlelés parancsmagjainak paramétere (ExcludeDetectionType) a DetectionType helyett string[] lett, hogy a jövőben is használható legyen az új DetectionType-ok hozzáadásakor, valamint az automatikus kitöltés támogatása érdekében.</span><span class="sxs-lookup"><span data-stu-id="b422e-1030">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b422e-1031">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b422e-1031">Az.Storage</span></span>
* <span data-ttu-id="b422e-1032">Tárfiók felügyeleti szabályzata lekérésének/beállításának/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="b422e-1032">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="b422e-1033">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b422e-1033">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="b422e-1034">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b422e-1034">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="b422e-1035">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b422e-1035">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="b422e-1036">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="b422e-1036">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="b422e-1037">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="b422e-1037">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="b422e-1038">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="b422e-1038">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b422e-1039">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b422e-1039">Az.Websites</span></span>
* <span data-ttu-id="b422e-1040">Ki lett javítva az ARM-sablon azon hibája, amely miatt meghiúsul az összes tárolóhely a New-AzWebApp - IncludeSourceWebAppSlots használatával történő klónozása</span><span class="sxs-lookup"><span data-stu-id="b422e-1040">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="b422e-1041">1.5.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="b422e-1041">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b422e-1042">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b422e-1042">Az.Accounts</span></span>
* <span data-ttu-id="b422e-1043">A Register-AzModule parancs hozzáadása az AutoRest által létrehozott parancsmagok támogatásához</span><span class="sxs-lookup"><span data-stu-id="b422e-1043">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="b422e-1044">A Connect-AzAccount példáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="b422e-1044">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b422e-1045">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b422e-1045">Az.Automation</span></span>
* <span data-ttu-id="b422e-1046">A bizonyos havi ütemezések lekérésekor jelentkező hiba kijavítva számos Azure Automation-parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="b422e-1046">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="b422e-1047">Ki lett javítva a hiba, amely miatt a Get-AzAutomationDscNode csak az első 20 csomópontot adta vissza.</span><span class="sxs-lookup"><span data-stu-id="b422e-1047">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="b422e-1048">Most már az összes csomópontot visszaadja</span><span class="sxs-lookup"><span data-stu-id="b422e-1048">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b422e-1049">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b422e-1049">Az.Cdn</span></span>
* <span data-ttu-id="b422e-1050">Új Powershell-parancsmagok hozzáadva az Egyéni tartományi Https engedélyezése/letiltása szolgáltatáshoz, a régiek elavultak</span><span class="sxs-lookup"><span data-stu-id="b422e-1050">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b422e-1051">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b422e-1051">Az.Compute</span></span>
* <span data-ttu-id="b422e-1052">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="b422e-1052">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b422e-1053">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b422e-1053">Az.DataFactory</span></span>
* <span data-ttu-id="b422e-1054">Az ADF .Net SDK verziója 3.0.1-re frissült</span><span class="sxs-lookup"><span data-stu-id="b422e-1054">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b422e-1055">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b422e-1055">Az.LogicApp</span></span>
* <span data-ttu-id="b422e-1056">Ki lett javítva a hiba, amely miatt a ListWorkflows csak az eredmények első oldalát kérte le</span><span class="sxs-lookup"><span data-stu-id="b422e-1056">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b422e-1057">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b422e-1057">Az.Network</span></span>
* <span data-ttu-id="b422e-1058">Helyettesítő karakterek támogatásának hozzáadása a Network-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="b422e-1058">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b422e-1059">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b422e-1059">Az.RecoveryServices</span></span>
* <span data-ttu-id="b422e-1060">Azure-beli virtuális gépen futtatott SQL Server támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="b422e-1060">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="b422e-1061">SDK-frissítés</span><span class="sxs-lookup"><span data-stu-id="b422e-1061">SDK Update</span></span>
* <span data-ttu-id="b422e-1062">VMappContainer ellenőrzés eltávolítva a Get-ProtectableItem parancsmagból</span><span class="sxs-lookup"><span data-stu-id="b422e-1062">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="b422e-1063">Name és ServerName paraméterek hozzáadva a Get-ProtectableItem parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b422e-1063">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="b422e-1064">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b422e-1064">Az.Resources</span></span>
* <span data-ttu-id="b422e-1065">`-TemplateObject` paraméter hozzáadva az üzembe helyező parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="b422e-1065">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="b422e-1066">További információ: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="b422e-1066">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="b422e-1067">Ki lett javítva a hiba, amely akkor jelentkezett, amikor a(z) `Get-AzResource` eredménye át lett irányítva a következőbe: `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="b422e-1067">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="b422e-1068">További információ: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="b422e-1068">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="b422e-1069">Ki lett javítva a JSON-adattípus módosításával kapcsolatos probléma, amely a(z) `Set-AzResource` futtatásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="b422e-1069">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="b422e-1070">További információ: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="b422e-1070">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="b422e-1071">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b422e-1071">Az.Sql</span></span>
* <span data-ttu-id="b422e-1072">Az AuditingEndpointsCommunicator frissítése.</span><span class="sxs-lookup"><span data-stu-id="b422e-1072">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="b422e-1073">Ki lett javítva az új diagnosztikai beállítások létrehozásakor jelentkező ritka eset viselkedése.</span><span class="sxs-lookup"><span data-stu-id="b422e-1073">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b422e-1074">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b422e-1074">Az.Storage</span></span>
* <span data-ttu-id="b422e-1075">A BlockBlobStorage altípus támogatása a Storage-fiók létrehozásakor      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b422e-1075">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="b422e-1076">1.4.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="b422e-1076">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="b422e-1077">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b422e-1077">Az.AnalysisServices</span></span>
* <span data-ttu-id="b422e-1078">Az AddAzureASAccount parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="b422e-1078">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b422e-1079">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b422e-1079">Az.Automation</span></span>
* <span data-ttu-id="b422e-1080">Az Import-AzAutomationDscNodeConfiguration súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="b422e-1080">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="b422e-1081">A konfigurációnév-ellenőrzés hozzáadva az Import-AzAutomationDscConfiguration parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b422e-1081">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="b422e-1082">Továbbfejlesztett hibakezelés az Import-AzAutomationDscConfiguration parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="b422e-1082">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b422e-1083">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b422e-1083">Az.CognitiveServices</span></span>
* <span data-ttu-id="b422e-1084">A CustomSubdomainName új választható paraméterként hozzáadva a New-AzCognitiveServicesAccount parancsmaghoz, amellyel altartomány adható meg az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="b422e-1084">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b422e-1085">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b422e-1085">Az.Compute</span></span>
* <span data-ttu-id="b422e-1086">Kijavítva az azonosító paraméterkészleteivel kapcsolatos probléma</span><span class="sxs-lookup"><span data-stu-id="b422e-1086">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="b422e-1087">Frissült a Get-AzVMExtension parancsmag, hogy az összes telepített bővítményt listázza, ha a Name paraméter nincs megadva</span><span class="sxs-lookup"><span data-stu-id="b422e-1087">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="b422e-1088">A Tag és a ResourceId paraméterek hozzáadva az Update-AzImage parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b422e-1088">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="b422e-1089">A Get-AzVmssVM példányazonosító nélkül, az InstanceView használatával példánynézetben listázni tudja a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="b422e-1089">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b422e-1090">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b422e-1090">Az.DataLakeStore</span></span>
* <span data-ttu-id="b422e-1091">Parancsmagok hozzáadása a törölt ADL-elemek enumerálásához és visszaállításához</span><span class="sxs-lookup"><span data-stu-id="b422e-1091">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b422e-1092">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b422e-1092">Az.EventHub</span></span>
* <span data-ttu-id="b422e-1093">Új SkipEmptyArchives logikai tulajdonság hozzáadva az üres archívumok kihagyásához az Eventhub CaptureDescription osztályában</span><span class="sxs-lookup"><span data-stu-id="b422e-1093">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b422e-1094">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b422e-1094">Az.KeyVault</span></span>
* <span data-ttu-id="b422e-1095">A Set-AzKeyVaultSecret címkézésének kijavítása</span><span class="sxs-lookup"><span data-stu-id="b422e-1095">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b422e-1096">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b422e-1096">Az.LogicApp</span></span>
* <span data-ttu-id="b422e-1097">Hozzáadva az integrációs fiókok alapszintű termékváltozatában</span><span class="sxs-lookup"><span data-stu-id="b422e-1097">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="b422e-1098">Hozzáadva az XSLT 2.0-ban, az XSLT 3.0-ban és a Liquid leképezéstípusok esetén</span><span class="sxs-lookup"><span data-stu-id="b422e-1098">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="b422e-1099">Új parancsmagok az integrációs fiók szerelvényeihez</span><span class="sxs-lookup"><span data-stu-id="b422e-1099">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="b422e-1100">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b422e-1100">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b422e-1101">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b422e-1101">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b422e-1102">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b422e-1102">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b422e-1103">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b422e-1103">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="b422e-1104">Új parancsmagok az integrációs fiók kötegkonfigurációjához</span><span class="sxs-lookup"><span data-stu-id="b422e-1104">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="b422e-1105">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b422e-1105">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b422e-1106">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b422e-1106">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b422e-1107">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b422e-1107">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b422e-1108">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b422e-1108">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="b422e-1109">A Logic Apps SDK frissítése a 4.1.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="b422e-1109">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b422e-1110">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b422e-1110">Az.Monitor</span></span>
* <span data-ttu-id="b422e-1111">A Get-AzMetric súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="b422e-1111">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b422e-1112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b422e-1112">Az.Network</span></span>
* <span data-ttu-id="b422e-1113">Az Add-AzApplicationGatewayCustomError súgójában lévő példa frissítése</span><span class="sxs-lookup"><span data-stu-id="b422e-1113">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b422e-1114">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b422e-1114">Az.OperationalInsights</span></span>
* <span data-ttu-id="b422e-1115">Kibővített támogatás a New és a Get ApplicationInsights adatforráshoz.</span><span class="sxs-lookup"><span data-stu-id="b422e-1115">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="b422e-1116">Új „ApplicationInsights” altípus hozzáadva az adott munkaterület Get specific és Get all Application Insights-adatforrásainak támogatásához.</span><span class="sxs-lookup"><span data-stu-id="b422e-1116">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="b422e-1117">A New-AzOperationalInsightsApplicationInsightsDataSource parancsmag hozzáadva adatforrás létrehozásához a következő Application Insights-erőforrásparaméterekkel: subscriptionId, resourceGroupName és name.</span><span class="sxs-lookup"><span data-stu-id="b422e-1117">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b422e-1118">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b422e-1118">Az.Resources</span></span>
* <span data-ttu-id="b422e-1119">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="b422e-1119">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="b422e-1120">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="b422e-1120">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="b422e-1121">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="b422e-1121">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="b422e-1122">Ki lett javítva a KeyCredentials ismételt létrehozását megakadályozó hiba</span><span class="sxs-lookup"><span data-stu-id="b422e-1122">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="b422e-1123">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b422e-1123">Az.Sql</span></span>
* <span data-ttu-id="b422e-1124">Rugalmas SQL DB-skálázási szint támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b422e-1124">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="b422e-1125">Ki lett javítva az a hiba, hogy a visszaállítási kérésben szereplő szükségtelen tulajdonságok megadása miatt a visszaállítás esetenként meghiúsult</span><span class="sxs-lookup"><span data-stu-id="b422e-1125">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b422e-1126">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b422e-1126">Az.Websites</span></span>
* <span data-ttu-id="b422e-1127">A Get-AzWebAppSlotMetrics példájának javítása</span><span class="sxs-lookup"><span data-stu-id="b422e-1127">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="b422e-1128">1.3.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="b422e-1128">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b422e-1129">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b422e-1129">Az.Accounts</span></span>
* <span data-ttu-id="b422e-1130">Frissítés a ClientRuntime legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="b422e-1130">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b422e-1131">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b422e-1131">Az.AnalysisServices</span></span>
<span data-ttu-id="b422e-1132">Az Az.AnalysisServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="b422e-1132">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b422e-1133">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b422e-1133">Az.Compute</span></span>
* <span data-ttu-id="b422e-1134">AEM-bővítmény: Mostantól az UltraSSD, valamint a P60, P70 és P80 lemezek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="b422e-1134">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="b422e-1135">A Set-AzVMBootDiagnostics súgóleírása frissült.</span><span class="sxs-lookup"><span data-stu-id="b422e-1135">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="b422e-1136">Az Update-AzImage súgóleírása és példája frissült.</span><span class="sxs-lookup"><span data-stu-id="b422e-1136">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b422e-1137">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b422e-1137">Az.RecoveryServices</span></span>
<span data-ttu-id="b422e-1138">Az Az.RecoveryServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="b422e-1138">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b422e-1139">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b422e-1139">Az.Resources</span></span>
* <span data-ttu-id="b422e-1140">Az erőforráscsoportok címkézése ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="b422e-1140">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="b422e-1141">További információ: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="b422e-1141">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="b422e-1142">Ki lett javítva az a hiba, amikor a `Get-AzureRmRoleAssignment` nem vette figyelembe az -ErrorAction paramétert.</span><span class="sxs-lookup"><span data-stu-id="b422e-1142">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="b422e-1143">További információ: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="b422e-1143">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="b422e-1144">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b422e-1144">Az.Sql</span></span>
* <span data-ttu-id="b422e-1145">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b422e-1145">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="b422e-1146">Ki lett javítva az a hiba, amikor az Azure-fiókba való bejelentkezés hiánya nullref kivételt eredményezett az SQL-parancsmagok végrehajtásakor.</span><span class="sxs-lookup"><span data-stu-id="b422e-1146">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="b422e-1147">A nullref kivétel ki lett javítva a Get-AzSqlCapabilityben.</span><span class="sxs-lookup"><span data-stu-id="b422e-1147">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="b422e-1148">1.2.1 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="b422e-1148">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b422e-1149">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b422e-1149">Az.Accounts</span></span>
* <span data-ttu-id="b422e-1150">A hitelesítés megfelelő verziójával rendelkező kiadás</span><span class="sxs-lookup"><span data-stu-id="b422e-1150">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b422e-1151">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b422e-1151">Az.AnalysisServices</span></span>
* <span data-ttu-id="b422e-1152">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="b422e-1152">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b422e-1153">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b422e-1153">Az.RecoveryServices</span></span>
* <span data-ttu-id="b422e-1154">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="b422e-1154">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="b422e-1155">1.2.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="b422e-1155">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b422e-1156">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b422e-1156">Az.Accounts</span></span>
* <span data-ttu-id="b422e-1157">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="b422e-1157">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b422e-1158">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="b422e-1158">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b422e-1159">Az Uninstall-AzureRm figyelmeztető üzenete hozzáadva a PS Core-ban</span><span class="sxs-lookup"><span data-stu-id="b422e-1159">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="b422e-1160">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="b422e-1160">Az.Aks</span></span>
* <span data-ttu-id="b422e-1161">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="b422e-1161">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b422e-1162">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b422e-1162">Az.Automation</span></span>
* <span data-ttu-id="b422e-1163">Mostantól támogatottak a Python 2-runbookok.</span><span class="sxs-lookup"><span data-stu-id="b422e-1163">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="b422e-1164">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="b422e-1164">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b422e-1165">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b422e-1165">Az.Cdn</span></span>
* <span data-ttu-id="b422e-1166">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="b422e-1166">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b422e-1167">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b422e-1167">Az.Compute</span></span>
* <span data-ttu-id="b422e-1168">Az Invoke-AzVMReimage parancsmag hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="b422e-1168">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="b422e-1169">A TempDisk paraméter hozzá lett adva a Set-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="b422e-1169">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="b422e-1170">A New-AzVM figyelmeztető üzenete ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="b422e-1170">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="b422e-1171">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b422e-1171">Az.ContainerRegistry</span></span>
* <span data-ttu-id="b422e-1172">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="b422e-1172">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b422e-1173">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b422e-1173">Az.DataFactory</span></span>
* <span data-ttu-id="b422e-1174">Az ADF .Net SDK verziója 3.0.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="b422e-1174">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b422e-1175">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b422e-1175">Az.DataLakeStore</span></span>
* <span data-ttu-id="b422e-1176">Ki lett javítva az ADLS-végponttal kapcsolatos probléma az MSI használatakor.</span><span class="sxs-lookup"><span data-stu-id="b422e-1176">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="b422e-1177">További információ: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="b422e-1177">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="b422e-1178">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="b422e-1178">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b422e-1179">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b422e-1179">Az.IotHub</span></span>
* <span data-ttu-id="b422e-1180">Az Encoding formátum hozzá lett adva az Add-IotHubRoutingEndpoint parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="b422e-1180">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b422e-1181">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b422e-1181">Az.KeyVault</span></span>
* <span data-ttu-id="b422e-1182">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="b422e-1182">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b422e-1183">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b422e-1183">Az.Network</span></span>
* <span data-ttu-id="b422e-1184">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="b422e-1184">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="b422e-1185">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b422e-1185">Az.Resources</span></span>
* <span data-ttu-id="b422e-1186">A helytelen példák ki lettek javítva a New-AzADAppCredential és a New-AzADSpCredential referenciadokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="b422e-1186">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="b422e-1187">Ki lett javítva az a hiba, amikor a -TemplateFile paraméter nem lett feloldva az erőforráscsoportokat üzembe helyező parancsmagok végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="b422e-1187">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="b422e-1188">Az.Resources: A New-AzureRmPolicyDefinition -Mode alapértelmezett értékének dokumentációja ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="b422e-1188">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="b422e-1189">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="b422e-1189">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="b422e-1190">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="b422e-1190">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="b422e-1191">Ki lett javítva a „PSResourceGroupDeployment” objektum formázásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="b422e-1191">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="b422e-1192">További információ: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="b422e-1192">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b422e-1193">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b422e-1193">Az.ServiceFabric</span></span>
* <span data-ttu-id="b422e-1194">Visszaállítás a VMSS-modell tanúsítványának hozzáadásakor bekövetkező kivétel-visszaadás esetén; javított hiba: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="b422e-1194">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="b422e-1195">Bizonyos hibaüzenetek ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="b422e-1195">Fix some error messages.</span></span>
* <span data-ttu-id="b422e-1196">Ki lett javítva az alapértelmezett ARM-sablonnal való fürtlétrehozás a New-AzServiceFabriCluster esetében, amely nem működött az Az-ba történő migrálással.</span><span class="sxs-lookup"><span data-stu-id="b422e-1196">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="b422e-1197">Ki lett javítva a fürt-/alkalmazástanúsítvány létrehozása, így mostantól csak a fürtnek megfelelő virtuálisgép-méretezési csoportokhoz (Virtual Machine Scale Sets) lesznek hozzáadva, a fürtazonosító bővítményben való ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="b422e-1197">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="b422e-1198">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="b422e-1198">Az.SignalR</span></span>
* <span data-ttu-id="b422e-1199">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="b422e-1199">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="b422e-1200">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b422e-1200">Az.Sql</span></span>
* <span data-ttu-id="b422e-1201">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="b422e-1201">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b422e-1202">A LicenseType paraméter paraméterleírása frissítve lett a lehetséges értékekkel.</span><span class="sxs-lookup"><span data-stu-id="b422e-1202">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="b422e-1203">Ki lett javítva az a hiba, amikor egy felügyelt példány identitásának frissítése nem működött, ha az volt az egyetlen frissített tulajdonság.</span><span class="sxs-lookup"><span data-stu-id="b422e-1203">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="b422e-1204">Egyéni rendezések támogatása a felügyelt példányokon</span><span class="sxs-lookup"><span data-stu-id="b422e-1204">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b422e-1205">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b422e-1205">Az.Storage</span></span>
* <span data-ttu-id="b422e-1206">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="b422e-1206">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b422e-1207">Részletes hibaüzenet megjelenítése klasszikus naplózás/metrika get/set műveletei esetében a prémium szintű Storage-fiókon, mivel a prémium szintű Storage-fiók nem támogatja a klasszikus naplózást/metrikát.</span><span class="sxs-lookup"><span data-stu-id="b422e-1207">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="b422e-1208">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="b422e-1208">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="b422e-1209">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="b422e-1209">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="b422e-1210">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b422e-1210">Az.TrafficManager</span></span>
* <span data-ttu-id="b422e-1211">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="b422e-1211">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b422e-1212">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b422e-1212">Az.Websites</span></span>
* <span data-ttu-id="b422e-1213">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="b422e-1213">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b422e-1214">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól a megfelelő erőforráscsoportba és helyre tölti fel a tanúsítványt, ha az alkalmazás ASE-n üzemel.</span><span class="sxs-lookup"><span data-stu-id="b422e-1214">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="b422e-1215">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól nem írja felül a címkéket SSL-tanúsítvány alkalmazáshoz való kötésekor.</span><span class="sxs-lookup"><span data-stu-id="b422e-1215">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="b422e-1216">1.1.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="b422e-1216">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b422e-1217">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b422e-1217">Az.Accounts</span></span>
* <span data-ttu-id="b422e-1218">A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz</span><span class="sxs-lookup"><span data-stu-id="b422e-1218">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b422e-1219">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b422e-1219">Az.Compute</span></span>
* <span data-ttu-id="b422e-1220">A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni</span><span class="sxs-lookup"><span data-stu-id="b422e-1220">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="b422e-1221">Frissült az azonosító leírása a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="b422e-1221">Updated the description of ID in help files</span></span>
* <span data-ttu-id="b422e-1222">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="b422e-1222">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b422e-1223">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b422e-1223">Az.DataLakeStore</span></span>
* <span data-ttu-id="b422e-1224">A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.</span><span class="sxs-lookup"><span data-stu-id="b422e-1224">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="b422e-1225">A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva</span><span class="sxs-lookup"><span data-stu-id="b422e-1225">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b422e-1226">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b422e-1226">Az.EventGrid</span></span>
* <span data-ttu-id="b422e-1227">Frissítve a 2019-01-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="b422e-1227">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="b422e-1228">A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához</span><span class="sxs-lookup"><span data-stu-id="b422e-1228">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="b422e-1229">New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="b422e-1229">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="b422e-1230">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="b422e-1230">Event Time-To-Live,</span></span>
        - <span data-ttu-id="b422e-1231">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="b422e-1231">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="b422e-1232">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="b422e-1232">Dead letter endpoint.</span></span>
    - <span data-ttu-id="b422e-1233">Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="b422e-1233">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="b422e-1234">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="b422e-1234">Event Time-To-Live,</span></span>
        - <span data-ttu-id="b422e-1235">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="b422e-1235">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="b422e-1236">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="b422e-1236">Dead letter endpoint.</span></span>
* <span data-ttu-id="b422e-1237">Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.</span><span class="sxs-lookup"><span data-stu-id="b422e-1237">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="b422e-1238">Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.</span><span class="sxs-lookup"><span data-stu-id="b422e-1238">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b422e-1239">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b422e-1239">Az.IotHub</span></span>
* <span data-ttu-id="b422e-1240">Frissítve az IoT Hub SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="b422e-1240">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b422e-1241">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b422e-1241">Az.LogicApp</span></span>
* <span data-ttu-id="b422e-1242">A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel</span><span class="sxs-lookup"><span data-stu-id="b422e-1242">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="b422e-1243">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b422e-1243">Az.Resources</span></span>
* <span data-ttu-id="b422e-1244">Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="b422e-1244">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="b422e-1245">További információ: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="b422e-1245">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="b422e-1246">Ki lett javítva a -Custom paraméter kezelése a New/Set-AzPolicyDefinition parancsban</span><span class="sxs-lookup"><span data-stu-id="b422e-1246">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="b422e-1247">Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="b422e-1247">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="b422e-1248">A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében</span><span class="sxs-lookup"><span data-stu-id="b422e-1248">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="b422e-1249">További információ: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="b422e-1249">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="b422e-1250">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="b422e-1250">Az.SignalR</span></span>
* <span data-ttu-id="b422e-1251">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="b422e-1251">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="b422e-1252">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b422e-1252">Az.Sql</span></span>
* <span data-ttu-id="b422e-1253">A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.</span><span class="sxs-lookup"><span data-stu-id="b422e-1253">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b422e-1254">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b422e-1254">Az.Storage</span></span>
* <span data-ttu-id="b422e-1255">A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva</span><span class="sxs-lookup"><span data-stu-id="b422e-1255">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="b422e-1256">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b422e-1256">New-AzStorageContext</span></span>
* <span data-ttu-id="b422e-1257">A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz</span><span class="sxs-lookup"><span data-stu-id="b422e-1257">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="b422e-1258">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="b422e-1258">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b422e-1259">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b422e-1259">Az.Websites</span></span>
* <span data-ttu-id="b422e-1260">Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban</span><span class="sxs-lookup"><span data-stu-id="b422e-1260">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="b422e-1261">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="b422e-1261">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="b422e-1262">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="b422e-1262">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="b422e-1263">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="b422e-1263">General</span></span>

- <span data-ttu-id="b422e-1264">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="b422e-1264">General Availability of Az Module</span></span>
- <span data-ttu-id="b422e-1265">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="b422e-1265">Online help for each module</span></span>
- <span data-ttu-id="b422e-1266">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="b422e-1266">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="b422e-1267">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="b422e-1267">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="b422e-1268">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b422e-1268">Az.Accounts</span></span>
- <span data-ttu-id="b422e-1269">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="b422e-1269">Changed from Az.Profile</span></span>
- <span data-ttu-id="b422e-1270">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="b422e-1270">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="b422e-1271">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b422e-1271">Az.ApiManagement</span></span>
- <span data-ttu-id="b422e-1272">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="b422e-1272">Fixes for #7002</span></span>
- <span data-ttu-id="b422e-1273">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="b422e-1273">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="b422e-1274">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b422e-1274">Az.Batch</span></span>
- <span data-ttu-id="b422e-1275">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="b422e-1275">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="b422e-1276">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="b422e-1276">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="b422e-1277">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="b422e-1277">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="b422e-1278">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="b422e-1278">Az.Billing</span></span>
- <span data-ttu-id="b422e-1279">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="b422e-1279">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="b422e-1280">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="b422e-1280">Az.CognitivServices</span></span>
- <span data-ttu-id="b422e-1281">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="b422e-1281">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="b422e-1282">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="b422e-1282">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="b422e-1283">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b422e-1283">Az.ContainerInstance</span></span>
- <span data-ttu-id="b422e-1284">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="b422e-1284">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="b422e-1285">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="b422e-1285">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="b422e-1286">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="b422e-1286">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="b422e-1287">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b422e-1287">Az.DataLakeStore</span></span>
- <span data-ttu-id="b422e-1288">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="b422e-1288">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="b422e-1289">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b422e-1289">Az.Monitor</span></span>
- <span data-ttu-id="b422e-1290">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="b422e-1290">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="b422e-1291">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b422e-1291">Az.KeyVault</span></span>
- <span data-ttu-id="b422e-1292">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="b422e-1292">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="b422e-1293">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="b422e-1293">Az.MachineLearning</span></span>
- <span data-ttu-id="b422e-1294">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="b422e-1294">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="b422e-1295">Az.Media</span><span class="sxs-lookup"><span data-stu-id="b422e-1295">Az.Media</span></span>
- <span data-ttu-id="b422e-1296">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="b422e-1296">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="b422e-1297">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b422e-1297">Az.Network</span></span>
<span data-ttu-id="b422e-1298">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="b422e-1298">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="b422e-1299">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="b422e-1299">New cmdlets added:</span></span>
        - <span data-ttu-id="b422e-1300">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b422e-1300">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b422e-1301">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b422e-1301">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b422e-1302">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b422e-1302">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b422e-1303">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b422e-1303">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b422e-1304">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b422e-1304">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b422e-1305">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="b422e-1305">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="b422e-1306">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="b422e-1306">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="b422e-1307">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="b422e-1307">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="b422e-1308">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b422e-1308">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="b422e-1309">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b422e-1309">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="b422e-1310">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b422e-1310">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="b422e-1311">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b422e-1311">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="b422e-1312">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b422e-1312">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="b422e-1313">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b422e-1313">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="b422e-1314">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="b422e-1314">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="b422e-1315">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b422e-1315">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="b422e-1316">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b422e-1316">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="b422e-1317">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b422e-1317">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="b422e-1318">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b422e-1318">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="b422e-1319">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="b422e-1319">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="b422e-1320">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="b422e-1320">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="b422e-1321">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b422e-1321">Az.OperationalInsights</span></span>
- <span data-ttu-id="b422e-1322">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="b422e-1322">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="b422e-1323">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b422e-1323">Az.Profile</span></span>
- <span data-ttu-id="b422e-1324">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b422e-1324">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="b422e-1325">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b422e-1325">Az.RecoveryServices</span></span>
- <span data-ttu-id="b422e-1326">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="b422e-1326">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="b422e-1327">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b422e-1327">Az.Resources</span></span>
- <span data-ttu-id="b422e-1328">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="b422e-1328">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="b422e-1329">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b422e-1329">Az.ServiceFabric</span></span>
- <span data-ttu-id="b422e-1330">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="b422e-1330">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="b422e-1331">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="b422e-1331">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="b422e-1332">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="b422e-1332">Az.SIgnalR</span></span>
- <span data-ttu-id="b422e-1333">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="b422e-1333">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="b422e-1334">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b422e-1334">Az.Sql</span></span>
- <span data-ttu-id="b422e-1335">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="b422e-1335">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="b422e-1336">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="b422e-1336">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="b422e-1337">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="b422e-1337">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="b422e-1338">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b422e-1338">Az.Storage</span></span>
- <span data-ttu-id="b422e-1339">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="b422e-1339">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="b422e-1340">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b422e-1340">Az.Websites</span></span>
- <span data-ttu-id="b422e-1341">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="b422e-1341">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="b422e-1342">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="b422e-1342">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="b422e-1343">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="b422e-1343">General</span></span>

* <span data-ttu-id="b422e-1344">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="b422e-1344">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="b422e-1345">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b422e-1345">Az.Compute</span></span>

* <span data-ttu-id="b422e-1346">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="b422e-1346">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="b422e-1347">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b422e-1347">Az.DataLakeStore</span></span>

* <span data-ttu-id="b422e-1348">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="b422e-1348">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="b422e-1349">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b422e-1349">Az.FrontDoor</span></span>

* <span data-ttu-id="b422e-1350">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="b422e-1350">Fixed some broken links</span></span>
    - <span data-ttu-id="b422e-1351">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="b422e-1351">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="b422e-1352">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="b422e-1352">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="b422e-1353">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b422e-1353">Az.RecoveryServices</span></span>

* <span data-ttu-id="b422e-1354">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="b422e-1354">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="b422e-1355">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="b422e-1355">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="b422e-1356">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b422e-1356">Az.Resources</span></span>

* <span data-ttu-id="b422e-1357">[https://github.com/Azure/azure-powershell/issues/7679](https://github.com/Azure/azure-powershell/issues/7679 ) javítása</span><span class="sxs-lookup"><span data-stu-id="b422e-1357">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="b422e-1358">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="b422e-1358">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="b422e-1359">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b422e-1359">Az.Sql</span></span>

* <span data-ttu-id="b422e-1360">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="b422e-1360">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="b422e-1361">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="b422e-1361">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="b422e-1362">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="b422e-1362">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="b422e-1363">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b422e-1363">Az.Storage</span></span>

* <span data-ttu-id="b422e-1364">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b422e-1364">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="b422e-1365">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="b422e-1365">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="b422e-1366">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="b422e-1366">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="b422e-1367">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="b422e-1367">Support Static Website configuration</span></span>
    - <span data-ttu-id="b422e-1368">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="b422e-1368">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="b422e-1369">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="b422e-1369">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="b422e-1370">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b422e-1370">Az.Websites</span></span>

* <span data-ttu-id="b422e-1371">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b422e-1371">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="b422e-1372">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="b422e-1372">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="b422e-1373">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="b422e-1373">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="b422e-1374">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="b422e-1374">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="b422e-1375">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b422e-1375">Az.ApiManagement</span></span>
* <span data-ttu-id="b422e-1376">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="b422e-1376">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="b422e-1377">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b422e-1377">Az.Automation</span></span>
* <span data-ttu-id="b422e-1378">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="b422e-1378">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="b422e-1379">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="b422e-1379">Added Update Management cmdlets</span></span>
* <span data-ttu-id="b422e-1380">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="b422e-1380">Added Source Control cmdlets</span></span>
* <span data-ttu-id="b422e-1381">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="b422e-1381">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="b422e-1382">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="b422e-1382">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="b422e-1383">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b422e-1383">Az.Compute</span></span>
* <span data-ttu-id="b422e-1384">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="b422e-1384">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="b422e-1385">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="b422e-1385">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="b422e-1386">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b422e-1386">Az.ContainerInstance</span></span>
* <span data-ttu-id="b422e-1387">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="b422e-1387">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="b422e-1388">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="b422e-1388">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="b422e-1389">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="b422e-1389">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="b422e-1390">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b422e-1390">Az.Network</span></span>
* <span data-ttu-id="b422e-1391">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="b422e-1391">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="b422e-1392">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="b422e-1392">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="b422e-1393">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="b422e-1393">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="b422e-1394">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="b422e-1394">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="b422e-1395">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="b422e-1395">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="b422e-1396">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="b422e-1396">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="b422e-1397">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="b422e-1397">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="b422e-1398">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="b422e-1398">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="b422e-1399">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="b422e-1399">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="b422e-1400">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="b422e-1400">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="b422e-1401">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="b422e-1401">Az.Relay</span></span>
* <span data-ttu-id="b422e-1402">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="b422e-1402">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="b422e-1403">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b422e-1403">Az.Resources</span></span>
* <span data-ttu-id="b422e-1404">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="b422e-1404">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="b422e-1405">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="b422e-1405">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="b422e-1406">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="b422e-1406">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="b422e-1407">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b422e-1407">Az.ServiceFabric</span></span>
* <span data-ttu-id="b422e-1408">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="b422e-1408">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="b422e-1409">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b422e-1409">Az.Sql</span></span>
* <span data-ttu-id="b422e-1410">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="b422e-1410">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="b422e-1411">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b422e-1411">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b422e-1412">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b422e-1412">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b422e-1413">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b422e-1413">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b422e-1414">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b422e-1414">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b422e-1415">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b422e-1415">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b422e-1416">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b422e-1416">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b422e-1417">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b422e-1417">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b422e-1418">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b422e-1418">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="b422e-1419">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="b422e-1419">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="b422e-1420">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="b422e-1420">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="b422e-1421">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="b422e-1421">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="b422e-1422">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="b422e-1422">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="b422e-1423">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="b422e-1423">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="b422e-1424">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="b422e-1424">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="b422e-1425">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="b422e-1425">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="b422e-1426">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="b422e-1426">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="b422e-1427">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="b422e-1427">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="b422e-1428">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="b422e-1428">General</span></span>
* <span data-ttu-id="b422e-1429">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="b422e-1429">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="b422e-1430">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b422e-1430">Az.Profile</span></span>
* <span data-ttu-id="b422e-1431">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="b422e-1431">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="b422e-1432">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="b422e-1432">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="b422e-1433">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="b422e-1433">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="b422e-1434">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="b422e-1434">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="b422e-1435">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="b422e-1435">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="b422e-1436">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="b422e-1436">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="b422e-1437">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="b422e-1437">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="b422e-1438">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b422e-1438">Az.CognitiveServices</span></span>
* <span data-ttu-id="b422e-1439">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="b422e-1439">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b422e-1440">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b422e-1440">Az.Compute</span></span>
* <span data-ttu-id="b422e-1441">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="b422e-1441">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="b422e-1442">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="b422e-1442">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="b422e-1443">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="b422e-1443">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b422e-1444">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b422e-1444">Az.DataLakeStore</span></span>
* <span data-ttu-id="b422e-1445">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="b422e-1445">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="b422e-1446">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="b422e-1446">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="b422e-1447">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="b422e-1447">Az.Insights</span></span>
* <span data-ttu-id="b422e-1448">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="b422e-1448">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="b422e-1449">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="b422e-1449">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="b422e-1450">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="b422e-1450">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="b422e-1451">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="b422e-1451">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b422e-1452">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b422e-1452">Az.Network</span></span>
* <span data-ttu-id="b422e-1453">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="b422e-1453">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="b422e-1454">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="b422e-1454">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="b422e-1455">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="b422e-1455">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="b422e-1456">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b422e-1456">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="b422e-1457">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="b422e-1457">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="b422e-1458">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="b422e-1458">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="b422e-1459">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b422e-1459">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b422e-1460">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b422e-1460">Az.PolicyInsights</span></span>
* <span data-ttu-id="b422e-1461">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b422e-1461">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="b422e-1462">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b422e-1462">Az.Resources</span></span>
* <span data-ttu-id="b422e-1463">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402 ) javítása</span><span class="sxs-lookup"><span data-stu-id="b422e-1463">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="b422e-1464">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="b422e-1464">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b422e-1465">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b422e-1465">Az.ServiceBus</span></span>
* <span data-ttu-id="b422e-1466">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="b422e-1466">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b422e-1467">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b422e-1467">Az.ServiceFabric</span></span>
* <span data-ttu-id="b422e-1468">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="b422e-1468">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="b422e-1469">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="b422e-1469">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="b422e-1470">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="b422e-1470">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="b422e-1471">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="b422e-1471">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="b422e-1472">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="b422e-1472">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="b422e-1473">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="b422e-1473">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="b422e-1474">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b422e-1474">Az.Profile</span></span>
* <span data-ttu-id="b422e-1475">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="b422e-1475">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="b422e-1476">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="b422e-1476">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b422e-1477">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b422e-1477">Az.Compute</span></span>
* <span data-ttu-id="b422e-1478">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="b422e-1478">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="b422e-1479">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="b422e-1479">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b422e-1480">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b422e-1480">Az.DataLakeStore</span></span>
* <span data-ttu-id="b422e-1481">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="b422e-1481">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="b422e-1482">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="b422e-1482">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="b422e-1483">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="b422e-1483">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="b422e-1484">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="b422e-1484">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="b422e-1485">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="b422e-1485">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b422e-1486">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b422e-1486">Az.Network</span></span>
* <span data-ttu-id="b422e-1487">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="b422e-1487">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="b422e-1488">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="b422e-1488">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b422e-1489">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b422e-1489">Az.Resources</span></span>
* <span data-ttu-id="b422e-1490">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="b422e-1490">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="b422e-1491">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="b422e-1491">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="b422e-1492">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="b422e-1492">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="b422e-1493">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="b422e-1493">Azure.Storage</span></span>
* <span data-ttu-id="b422e-1494">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="b422e-1494">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="b422e-1495">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b422e-1495">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="b422e-1496">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="b422e-1496">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="b422e-1497">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="b422e-1497">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="b422e-1498">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="b422e-1498">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b422e-1499">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b422e-1499">Az.CognitiveServices</span></span>
* <span data-ttu-id="b422e-1500">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="b422e-1500">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b422e-1501">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b422e-1501">Az.Compute</span></span>
* <span data-ttu-id="b422e-1502">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="b422e-1502">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="b422e-1503">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="b422e-1503">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="b422e-1504">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="b422e-1504">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="b422e-1505">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b422e-1505">Az.DataFactoryV2</span></span>
* <span data-ttu-id="b422e-1506">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="b422e-1506">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b422e-1507">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b422e-1507">Az.Network</span></span>
* <span data-ttu-id="b422e-1508">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="b422e-1508">Added NetworkProfile functionality.</span></span> <span data-ttu-id="b422e-1509">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b422e-1509">new cmdlets added</span></span>
    - <span data-ttu-id="b422e-1510">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b422e-1510">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="b422e-1511">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b422e-1511">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="b422e-1512">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b422e-1512">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="b422e-1513">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b422e-1513">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="b422e-1514">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="b422e-1514">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="b422e-1515">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="b422e-1515">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="b422e-1516">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="b422e-1516">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="b422e-1517">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="b422e-1517">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="b422e-1518">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="b422e-1518">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="b422e-1519">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b422e-1519">Az.RedisCache</span></span>
* <span data-ttu-id="b422e-1520">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="b422e-1520">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="b422e-1521">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="b422e-1521">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="b422e-1522">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b422e-1522">Az.Resources</span></span>
* <span data-ttu-id="b422e-1523">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b422e-1523">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="b422e-1524">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="b422e-1524">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="b422e-1525">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b422e-1525">Az.Sql</span></span>
* <span data-ttu-id="b422e-1526">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="b422e-1526">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b422e-1527">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b422e-1527">Az.Websites</span></span>
* <span data-ttu-id="b422e-1528">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="b422e-1528">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="b422e-1529">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="b422e-1529">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="b422e-1530">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="b422e-1530">0.2.0 - September 2018</span></span>
 <span data-ttu-id="b422e-1531">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="b422e-1531">Initial Release</span></span>