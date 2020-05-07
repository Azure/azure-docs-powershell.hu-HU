---
title: Az Azure PowerShell kibocsátási megjegyzései
description: Megismerheti az Azure PowerShell-modulok legújabb frissítéseit.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: 98a24c805fbf43dd899119d43301b4261c1f60dc
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/05/2020
ms.locfileid: "75035761"
---
## <a name="280---october-2019"></a><span data-ttu-id="59c1f-103">2.8.0 – 2019. október</span><span class="sxs-lookup"><span data-stu-id="59c1f-103">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="59c1f-104">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="59c1f-104">General</span></span>
* <span data-ttu-id="59c1f-105">Az.HealthcareApis 1.0.0-s kiadás</span><span class="sxs-lookup"><span data-stu-id="59c1f-105">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="59c1f-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="59c1f-106">Az.Accounts</span></span>
* <span data-ttu-id="59c1f-107">A telemetria és az URL-címek újraírásának frissítése a létrehozott modulok esetében, a Windows-egységek tesztelésének javítása.</span><span class="sxs-lookup"><span data-stu-id="59c1f-107">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="59c1f-108">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="59c1f-108">Az.ApiManagement</span></span>
* <span data-ttu-id="59c1f-109">**Set-AzApiManagementApi** – Az API a következőre való frissítésének támogatása: ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="59c1f-109">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="59c1f-110">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="59c1f-110">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="59c1f-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="59c1f-111">Az.Automation</span></span>
* <span data-ttu-id="59c1f-112">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag a Linux újraindítási beállítási paramétere kapcsán.</span><span class="sxs-lookup"><span data-stu-id="59c1f-112">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="59c1f-113">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="59c1f-113">Az.Batch</span></span>
* <span data-ttu-id="59c1f-114">A **Get-AzBatchNodeAgentSku** elavult, így a 2.0.0-ás verziótól a **Get-AzBatchSupportImage** váltja fel.</span><span class="sxs-lookup"><span data-stu-id="59c1f-114">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="59c1f-115">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c1f-115">Az.Compute</span></span>
* <span data-ttu-id="59c1f-116">A Priority, EvictionPolicy és MaxPrice paraméterek hozzáadása a New-AzVM és a New-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-116">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="59c1f-117">Az Add-AzVMAdditionalUnattendContent és az Add-AzVMSshPublicKey parancsmagok figyelmeztető üzenetének és súgójának kijavítása</span><span class="sxs-lookup"><span data-stu-id="59c1f-117">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="59c1f-118">A -skipVmBackup kivétel kijavítása felügyelt lemezekkel rendelkező Linux rendszerű virtuális gépek esetében a Set-AzVMDiskEncryptionExtension kapcsán.</span><span class="sxs-lookup"><span data-stu-id="59c1f-118">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="59c1f-119">A titkosítási beállítások frissítési hibájának kijavítása a Set-AzVMDiskEncryptionExtension kétmenetes forgatókönyvében.</span><span class="sxs-lookup"><span data-stu-id="59c1f-119">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="59c1f-120">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="59c1f-120">Az.DataFactory</span></span>
* <span data-ttu-id="59c1f-121">CRUD-parancsok lettek hozzáadva az ADF V2-adatfolyamhoz: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow és Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="59c1f-121">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="59c1f-122">Műveleti parancsok lettek hozzáadva az ADF V2-adatfolyam hibakeresési munkamenetéhez: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand és Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="59c1f-122">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="59c1f-123">Az ADF .Net SDK a 4.2.0-ás verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="59c1f-123">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="59c1f-124">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="59c1f-124">Az.DataLakeStore</span></span>
* <span data-ttu-id="59c1f-125">A fiókérvényesítés javítása, hogy a "-" jelölésű fiókok tartomány nélkül is továbbíthatók legyenek</span><span class="sxs-lookup"><span data-stu-id="59c1f-125">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="59c1f-126">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="59c1f-126">Az.HealthcareApis</span></span>
* <span data-ttu-id="59c1f-127">A PowerShell az 1.0.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="59c1f-127">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="59c1f-128">Az SDK a 1.0.2-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="59c1f-128">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="59c1f-129">Frissítés a tesztekben az új SDK-verzióra való hivatkozáshoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-129">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="59c1f-130">A kimeneti struktúra beágyazottról simítottra frissült.</span><span class="sxs-lookup"><span data-stu-id="59c1f-130">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="59c1f-131">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="59c1f-131">Az.IotHub</span></span>
* <span data-ttu-id="59c1f-132">Új útválasztási forrás hozzáadása: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="59c1f-132">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="59c1f-133">Kisebb hibajavítás: A Get-AzIothub nem adja vissza a következőt: subscriptionId</span><span class="sxs-lookup"><span data-stu-id="59c1f-133">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="59c1f-134">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="59c1f-134">Az.Monitor</span></span>
* <span data-ttu-id="59c1f-135">Új műveleticsoport-fogadók hozzáadva a New-AzActionGroupReceiver parancsmaghoz:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="59c1f-135">New action group receivers added for New-AzActionGroupReceiver:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="59c1f-136">Az általános riasztási séma használata engedélyezve a fogadók számára.</span><span class="sxs-lookup"><span data-stu-id="59c1f-136">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="59c1f-137">Ez nem vonatkozik az SMS, az Azure App leküldéses üzenetei, az ITSM és a Voice fogadóira.</span><span class="sxs-lookup"><span data-stu-id="59c1f-137">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="59c1f-138">A webhookok mostantól az Azure Active Directory-hitelesítés használatát is támogatják.</span><span class="sxs-lookup"><span data-stu-id="59c1f-138">Webhooks now supports Azure active directory authentication.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="59c1f-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="59c1f-139">Az.Network</span></span>
* <span data-ttu-id="59c1f-140">Új Get-AzAvailableServiceAlias parancsmag hozzáadva, amely a szolgáltatásvégpont-szabályzatokhoz használható aliasok beszerzéséhez hívható meg.</span><span class="sxs-lookup"><span data-stu-id="59c1f-140">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="59c1f-141">Forgalomválasztók hozzáadásának támogatása a virtuális hálózati átjáró kapcsolataihoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-141">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="59c1f-142">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="59c1f-142">New cmdlets added:</span></span>
        - <span data-ttu-id="59c1f-143">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="59c1f-143">New-AzIpsecTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="59c1f-144">A -TrafficSelectorPolicies opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="59c1f-144">Cmdlets updated with optional parameter -TrafficSelectorPolicies</span></span>
        - <span data-ttu-id="59c1f-145">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="59c1f-145">New-AzVirtualNetworkGatewayConnection</span></span>
        - <span data-ttu-id="59c1f-146">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="59c1f-146">Set-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="59c1f-147">Az ESP és AH protokollok támogatása a hálózati biztonsági szabályzati konfigurációkban</span><span class="sxs-lookup"><span data-stu-id="59c1f-147">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="59c1f-148">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="59c1f-148">Updated cmdlets:</span></span>
        - <span data-ttu-id="59c1f-149">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="59c1f-149">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="59c1f-150">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="59c1f-150">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="59c1f-151">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="59c1f-151">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="59c1f-152">Tovább javult a Cortex-parancsmagok kivételeinek kezelése</span><span class="sxs-lookup"><span data-stu-id="59c1f-152">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="59c1f-153">A VirtualNetworkGateways új generációi és termékváltozatai</span><span class="sxs-lookup"><span data-stu-id="59c1f-153">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="59c1f-154">A VirtualNetworkGateways új generációinak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="59c1f-154">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="59c1f-155">A VirtualNetworkGateways új, nagy átviteli sebességű termékváltozatainak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="59c1f-155">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="59c1f-156">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="59c1f-156">Az.RedisCache</span></span>
* <span data-ttu-id="59c1f-157">Frissült a Set-AzRedisCache referenciadokumentációja, amely most már tartalmazza a -Size paraméter hiányzó értékeit.</span><span class="sxs-lookup"><span data-stu-id="59c1f-157">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="59c1f-158">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="59c1f-158">Az.Sql</span></span>
* <span data-ttu-id="59c1f-159">Az Active Directory-rendszergazda a felügyelt példányon való beállításának támogatása</span><span class="sxs-lookup"><span data-stu-id="59c1f-159">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="59c1f-160">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="59c1f-160">Az.Storage</span></span>
* <span data-ttu-id="59c1f-161">Az Storage-ügyfélkódtár a 11.1.0-s verzióra frissült.</span><span class="sxs-lookup"><span data-stu-id="59c1f-161">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="59c1f-162">A Management plane API-val rendelkező tárolók listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="59c1f-162">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="59c1f-163">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="59c1f-163">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="59c1f-164">A tárfiókok előfizetésből történő listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="59c1f-164">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="59c1f-165">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="59c1f-165">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="59c1f-166">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="59c1f-166">Az.StorageSync</span></span>
* <span data-ttu-id="59c1f-167">A Reset-AzStorageSyncServerCertificate 9810-es hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="59c1f-167">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="59c1f-168">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="59c1f-168">Az.Websites</span></span>
* <span data-ttu-id="59c1f-169">Egy alkalmazáshoz tartozó ASP Set-AzWebApp általi frissítése sikertelen volt</span><span class="sxs-lookup"><span data-stu-id="59c1f-169">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="59c1f-170">2.7.0 – 2019. szeptember</span><span class="sxs-lookup"><span data-stu-id="59c1f-170">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="59c1f-171">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="59c1f-171">Az.ApiManagement</span></span>
* <span data-ttu-id="59c1f-172">Frissítve lett a „-Format” paraméter leírása a „Set-AzApiManagementPolicy” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="59c1f-172">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="59c1f-173">El lettek távolítva az elavult „Update-AzApiManagementDeployment” parancsmag referenciái a referenciadokumentációból.</span><span class="sxs-lookup"><span data-stu-id="59c1f-173">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="59c1f-174">A „Set-AzApiManagement” használható helyette.</span><span class="sxs-lookup"><span data-stu-id="59c1f-174">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="59c1f-175">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="59c1f-175">Az.Automation</span></span>
* <span data-ttu-id="59c1f-176">Ki lett javítva a „Register-AzAutomationDscNode” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="59c1f-176">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="59c1f-177">Hozzá lett adva az operációs rendszerrel kapcsolatos korlátozások pontosítása a Register-AzAutomationDSCNode parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-177">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="59c1f-178">Ki lett javítva a Start-AzAutomationRunbook parancsmag null értékű hivatkozás okozta kivétele a -Wait paraméter esetén.</span><span class="sxs-lookup"><span data-stu-id="59c1f-178">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="59c1f-179">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c1f-179">Az.Compute</span></span>
* <span data-ttu-id="59c1f-180">Hozzá lett adva az UploadSizeInBytes paraméter a New-AzDiskConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-180">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="59c1f-181">Hozzá lett adva az Incremental paraméter a New-AzSnapshotConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-181">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="59c1f-182">Alacsony prioritású virtuálisgép-funkció hozzáadása:</span><span class="sxs-lookup"><span data-stu-id="59c1f-182">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="59c1f-183">Hozzá lett adva a MaxPrice, az EvictionPolicy és a Priority paraméter a New-AzVMConfig parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="59c1f-183">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="59c1f-184">Hozzá lett adva a MaxPrice paraméter a New-AzVmssConfig, az Update-AzVM és az Update-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="59c1f-184">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="59c1f-185">Ki lett javítva a Get-AzAvailabilitySet parancsmag virtuálisgép-hivatkozással kapcsolatos hibája, amely miatt a parancsmag az előfizetésben található összes rendelkezésreállási csoportot listázta.</span><span class="sxs-lookup"><span data-stu-id="59c1f-185">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="59c1f-186">Ki lett javítva a Get-AzRemoteDesktopFile parancsmag esetében jelentkező null kivétel.</span><span class="sxs-lookup"><span data-stu-id="59c1f-186">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="59c1f-187">Ki lett javítva virtuális merevlemezek Seek metódusa a végrelatív pozíció esetében.</span><span class="sxs-lookup"><span data-stu-id="59c1f-187">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="59c1f-188">Ki lett javítva az UltraSSD hibája a New-AzVM és az Update-AzVM parancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="59c1f-188">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="59c1f-189">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="59c1f-189">Az.DataFactory</span></span>
* <span data-ttu-id="59c1f-190">Hozzá lett adva 3 új parancs (az Add-AzDataFactoryV2TriggerSubscription, a Remove-AzDataFactoryV2TriggerSubscription és a Get-AzDataFactoryV2TriggerSubscriptionStatus) az ADF V2-höz</span><span class="sxs-lookup"><span data-stu-id="59c1f-190">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="59c1f-191">Az ADF .Net SDK a 4.1.3-as verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="59c1f-191">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="59c1f-192">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="59c1f-192">Az.HDInsight</span></span>
* <span data-ttu-id="59c1f-193">Kompatibilitástörő változások a meghívással kapcsolatban</span><span class="sxs-lookup"><span data-stu-id="59c1f-193">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="59c1f-194">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="59c1f-194">Az.IotHub</span></span>
* <span data-ttu-id="59c1f-195">Hozzá lett adva az IoTHubok földrajzilag párosított vészhelyreállítási régiójába történő feladatátvétel meghívásának támogatása.</span><span class="sxs-lookup"><span data-stu-id="59c1f-195">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="59c1f-196">Hozzá lett adva az IoTHubok üzenetbővítés-kezelésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="59c1f-196">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="59c1f-197">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="59c1f-197">New cmdlets are:</span></span>
    - <span data-ttu-id="59c1f-198">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="59c1f-198">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="59c1f-199">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="59c1f-199">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="59c1f-200">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="59c1f-200">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="59c1f-201">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="59c1f-201">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="59c1f-202">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="59c1f-202">Az.Monitor</span></span>
* <span data-ttu-id="59c1f-203">A legújabb Monitor SDK-ra mutat, azaz a 0.24.1-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="59c1f-203">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="59c1f-204">Nem kompatibilitástörő változásokkal bővíti a Metrics parancsmagokat, így az egységek számbavétele számos új értéket támogat.</span><span class="sxs-lookup"><span data-stu-id="59c1f-204">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="59c1f-205">Ezek írásvédett parancsmagok, ezért a parancsmagok bemenetében nem történik változás.</span><span class="sxs-lookup"><span data-stu-id="59c1f-205">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="59c1f-206">Az **ActionGroups**-kérések api-version értéke mostantól **2019-06-01**, korábban **2018-03-01** volt.</span><span class="sxs-lookup"><span data-stu-id="59c1f-206">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="59c1f-207">A forgatókönyvtesztek frissültek, így igazodnak a változáshoz.</span><span class="sxs-lookup"><span data-stu-id="59c1f-207">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="59c1f-208">Az **EmailReceiver** és a **WebhookReceiver** osztályok konstruktoraihoz hozzá lett adva egy új kötelező argumentum, a **useCommonAlertSchema** nevű logikai érték.</span><span class="sxs-lookup"><span data-stu-id="59c1f-208">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="59c1f-209">A kompatibilitástörő változás parancsmagok elől való elrejtése érdekében a rögzített érték jelenleg a **false** (hamis).</span><span class="sxs-lookup"><span data-stu-id="59c1f-209">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="59c1f-210">**MEGJEGYZÉS**: Ez egy átmeneti módosítás, amelyet a Riasztások csapatnak érvényesítenie kell.</span><span class="sxs-lookup"><span data-stu-id="59c1f-210">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="59c1f-211">A **Source** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="59c1f-211">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="59c1f-212">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="59c1f-212">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="59c1f-213">Az **AlertingAction** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="59c1f-213">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="59c1f-214">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="59c1f-214">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="59c1f-215">A dinamikus küszöbérték kritériumainak támogatása a 2-es verziójú metrikariasztás esetében</span><span class="sxs-lookup"><span data-stu-id="59c1f-215">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="59c1f-216">New-AzMetricAlertRuleV2Criteria: mostantól a dinamikus küszöbértékek kritériumait is létrehozza</span><span class="sxs-lookup"><span data-stu-id="59c1f-216">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="59c1f-217">Add-AzMetricAlertRuleV2: mostantól a dinamikus küszöbértékek kritériumait is elfogadja</span><span class="sxs-lookup"><span data-stu-id="59c1f-217">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="59c1f-218">Az ütemezett lekérdezési szabályok parancsmagjainak (SQR) fejlesztései</span><span class="sxs-lookup"><span data-stu-id="59c1f-218">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="59c1f-219">A parancsmagok a „Location” paraméter mindkét formátumát elfogadják: a helyet (például eastus) és a hely megjelenített nevét is (például USA keleti régiója)</span><span class="sxs-lookup"><span data-stu-id="59c1f-219">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="59c1f-220">Megfelelően ábrázolva lett az „Enabled” paraméter a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="59c1f-220">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="59c1f-221">Példák lettek hozzáadva az „ActionGroup” opcionális paraméterhez</span><span class="sxs-lookup"><span data-stu-id="59c1f-221">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="59c1f-222">Általánosan továbbfejlesztett súgófájlok</span><span class="sxs-lookup"><span data-stu-id="59c1f-222">Overall improved help files</span></span>
* <span data-ttu-id="59c1f-223">Ki lett javítva a „Set-AzActionRule” hatókörtípusának meghatározásával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="59c1f-223">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="59c1f-224">Az.Network</span><span class="sxs-lookup"><span data-stu-id="59c1f-224">Az.Network</span></span>
* <span data-ttu-id="59c1f-225">Ki lett javítva a „New-AzApplicationGateway” referenciadokumentációjában található helytelen példa</span><span class="sxs-lookup"><span data-stu-id="59c1f-225">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="59c1f-226">Hozzá lett adva egy csomagrögzítés összes tulajdonságának lekérésével kapcsolatos megjegyzés a „Get-AzNetworkWatcherPacketCapture” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="59c1f-226">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="59c1f-227">Ki lett javítva a „Test-AzNetworkWatcherIPFlow” referenciadokumentációjában található példa a hálózati adapterek megfelelő számbavétele érdekében</span><span class="sxs-lookup"><span data-stu-id="59c1f-227">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="59c1f-228">Tovább lett fejlesztve a felhőkivétel-elemzés az esetleges további részletek megjelenítése érdekében</span><span class="sxs-lookup"><span data-stu-id="59c1f-228">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="59c1f-229">Tovább lett fejlesztve a felhőkivétel-elemzés az SDK-kivételek további típusainak kezelése érdekében</span><span class="sxs-lookup"><span data-stu-id="59c1f-229">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="59c1f-230">Ki lett javítva a biztonságiszabály-modellek helytelen leképezése</span><span class="sxs-lookup"><span data-stu-id="59c1f-230">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="59c1f-231">Hozzá lettek adva a privát IP-cím funkcióval kapcsolatos tulajdonságok a hálózati adapterhez</span><span class="sxs-lookup"><span data-stu-id="59c1f-231">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="59c1f-232">Hozzá lett adva a „PrivateEndpoint” tulajdonság PSResourceId típusúként a PSNetworkInterface osztályhoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-232">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="59c1f-233">Hozzá lett adva a „PrivateLinkConnectionProperties” tulajdonság PSIpConfigurationConnectivityInformation típusúként a PSNetworkInterfaceIPConfiguration osztályhoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-233">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="59c1f-234">Hozzá lett adva a PSIpConfigurationConnectivityInformation nevű új modellosztály</span><span class="sxs-lookup"><span data-stu-id="59c1f-234">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="59c1f-235">Hozzá lett adva az új ApplicationRuleProtocolType „mssql” az Azure Firewall-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-235">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="59c1f-236">MultiLink-támogatás a Virtuális WAN-ben</span><span class="sxs-lookup"><span data-stu-id="59c1f-236">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="59c1f-237">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="59c1f-237">New cmdlets</span></span>
        - <span data-ttu-id="59c1f-238">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="59c1f-238">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="59c1f-239">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="59c1f-239">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="59c1f-240">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="59c1f-240">Updated cmdlet:</span></span>
        - <span data-ttu-id="59c1f-241">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="59c1f-241">New-VpnSite</span></span>
        - <span data-ttu-id="59c1f-242">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="59c1f-242">Update-VpnSite</span></span>
        - <span data-ttu-id="59c1f-243">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="59c1f-243">New-VpnConnection</span></span>
        - <span data-ttu-id="59c1f-244">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="59c1f-244">Update-VpnConnection</span></span>
* <span data-ttu-id="59c1f-245">Ki lettek javítva bizonyos PowerShell-példák dokumentumai, hogy az AzureRM-parancsmagok helyett az Az-parancsmagokat használják</span><span class="sxs-lookup"><span data-stu-id="59c1f-245">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="59c1f-246">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="59c1f-246">Az.RecoveryServices</span></span>
* <span data-ttu-id="59c1f-247">Frissítve lett az AzureVMpolicy objektum a ProtectedItemsCount attribútummal</span><span class="sxs-lookup"><span data-stu-id="59c1f-247">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="59c1f-248">Tesztek lettek hozzáadva a virtuális gép szabályzatához és az eredeti Storage-fiók visszaállításához</span><span class="sxs-lookup"><span data-stu-id="59c1f-248">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="59c1f-249">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c1f-249">Az.Resources</span></span>
* <span data-ttu-id="59c1f-250">Ki lett javítva a hiba, amely miatt a New-AzRoleAssignment parancsot nem lehetett meghívni a Scope paraméter nélkül.</span><span class="sxs-lookup"><span data-stu-id="59c1f-250">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="59c1f-251">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="59c1f-251">Az.ServiceFabric</span></span>
* <span data-ttu-id="59c1f-252">Ki lett javítva az „Update-AzServiceFabricReliability” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="59c1f-252">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="59c1f-253">Új parancsmagok lettek hozzáadva az alkalmazás és a szolgáltatások felügyeletéhez:</span><span class="sxs-lookup"><span data-stu-id="59c1f-253">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="59c1f-254">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="59c1f-254">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="59c1f-255">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="59c1f-255">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="59c1f-256">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="59c1f-256">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="59c1f-257">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="59c1f-257">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="59c1f-258">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="59c1f-258">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="59c1f-259">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="59c1f-259">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="59c1f-260">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="59c1f-260">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="59c1f-261">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="59c1f-261">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="59c1f-262">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="59c1f-262">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="59c1f-263">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="59c1f-263">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="59c1f-264">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="59c1f-264">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="59c1f-265">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="59c1f-265">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="59c1f-266">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="59c1f-266">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="59c1f-267">A Service Fabric SDK az 1.2.0-s verzióra frissült, amely a Service Fabric erőforrás-szolgáltató 2019-03-01 api-versionjét használja.</span><span class="sxs-lookup"><span data-stu-id="59c1f-267">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="59c1f-268">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="59c1f-268">Az.SignalR</span></span>
* <span data-ttu-id="59c1f-269">Hozzá lettek adva az Update, Restart, CheckNameAvailability és GetUsage parancsmagok</span><span class="sxs-lookup"><span data-stu-id="59c1f-269">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="59c1f-270">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="59c1f-270">Az.Sql</span></span>
* <span data-ttu-id="59c1f-271">Frissítve lett a „Get-AzSqlElasticPool” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="59c1f-271">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="59c1f-272">Hozzá lett adva egy rugalmas készlet létrehozását bemutató virtuálismag-példa (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="59c1f-272">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="59c1f-273">El lett távolítva az EmailAddresses érvényesítése és annak ellenőrzése, hogy az EmailAdmins értéke hamis-e abban az esetben, ha az EmailAddresses üres a Set-AzSqlServerAdvancedThreatProtectionPolicy és a Set-AzSqlDatabaseAdvancedThreatProtectionPolicy parancsmagban</span><span class="sxs-lookup"><span data-stu-id="59c1f-273">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="59c1f-274">Engedélyezve lettek a kiszolgáló-/adatbázis-naplózási beállítások abban az esetben, ha több olyan diagnosztikai beállítás létezik, amelyek engedélyezik a naplózási kategóriát.</span><span class="sxs-lookup"><span data-stu-id="59c1f-274">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="59c1f-275">Ki lett javítva az e-mail-címek ellenőrzése több, SQL-sebezhetőségi felméréshez használt parancsmagban (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting és Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="59c1f-275">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="59c1f-276">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="59c1f-276">Az.Storage</span></span>
* <span data-ttu-id="59c1f-277">Frissítve lett a „Get-AzStorageAccountKey” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="59c1f-277">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="59c1f-278">A forrásfájl SMB-tulajdonságai (fájlattribútumok, fájl létrehozásának ideje, fájl utolsó írásának ideje) célfájlban történő megtartásának támogatása az Azure File-beli feltöltés/letöltés esetében</span><span class="sxs-lookup"><span data-stu-id="59c1f-278">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="59c1f-279">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="59c1f-279">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="59c1f-280">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="59c1f-280">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="59c1f-281">Ki lett javítva a tulajdonság-/metaadathibával meghiúsuló blokkblobfeltöltés a tárolóképes ImmutabilityPolicy esetében.</span><span class="sxs-lookup"><span data-stu-id="59c1f-281">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="59c1f-282">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="59c1f-282">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="59c1f-283">Az Azure File-megosztások Management plane API-val történő kezelésének támogatása</span><span class="sxs-lookup"><span data-stu-id="59c1f-283">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="59c1f-284">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="59c1f-284">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="59c1f-285">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="59c1f-285">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="59c1f-286">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="59c1f-286">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="59c1f-287">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="59c1f-287">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="59c1f-288">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="59c1f-288">Az.Websites</span></span>
* <span data-ttu-id="59c1f-289">Ki lett javítva az a probléma, amely miatt a webalkalmazás Címkéi törölve lettek az alkalmazás új ASP-be történő migrálásakor</span><span class="sxs-lookup"><span data-stu-id="59c1f-289">Fixing issue where webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="59c1f-290">Ki lett javítva a Publish-AzureWebapp parancs a Linux és Windows rendszeren történő működés érdekében</span><span class="sxs-lookup"><span data-stu-id="59c1f-290">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="59c1f-291">Frissítve lett a „Get-AzWebAppPublishingProfile” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="59c1f-291">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="59c1f-292">2.6.0 – 2019. augusztus</span><span class="sxs-lookup"><span data-stu-id="59c1f-292">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="59c1f-293">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="59c1f-293">General</span></span>
* <span data-ttu-id="59c1f-294">Különféle elgépelések kijavítva több modulban</span><span class="sxs-lookup"><span data-stu-id="59c1f-294">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="59c1f-295">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="59c1f-295">Az.Accounts</span></span>
* <span data-ttu-id="59c1f-296">Felhasználó által hozzárendelt MSI támogatása az Azure Functions-hitelesítésben (#9479)</span><span class="sxs-lookup"><span data-stu-id="59c1f-296">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="59c1f-297">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="59c1f-297">Az.Aks</span></span>
* <span data-ttu-id="59c1f-298">A Get-AzAks kimenetével kapcsolatos probléma ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="59c1f-298">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="59c1f-299">További információ: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="59c1f-299">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="59c1f-300">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="59c1f-300">Az.ApiManagement</span></span>
* <span data-ttu-id="59c1f-301">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="59c1f-301">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="59c1f-302">Frissült a .net nuget verziója, amely nem kényszeríti ki a productId, az apiId, a groupId és a userId korlátozásait</span><span class="sxs-lookup"><span data-stu-id="59c1f-302">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="59c1f-303">**Get-AzApiManagementProduct** – A termékek API-val történő lekérdezése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="59c1f-303">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="59c1f-304">**New-AzApiManagementApiRevision** – Ki lett javítva az a probléma, amely miatt az ApiRevisionDescription nem lett beállítva az új API-változat létrehozásakor https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="59c1f-304">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="59c1f-305">Ki lett javítva a PsApiManagementOAuth2AuthrozationServer modell elírása PsApiManagementOAuth2AuthorizationServer értékre</span><span class="sxs-lookup"><span data-stu-id="59c1f-305">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="59c1f-306">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="59c1f-306">Az.Batch</span></span>
* <span data-ttu-id="59c1f-307">Ki lett javítva a súgóüzenetben és a dokumentációban található elgépelés, nagy kezdőbetűs Windows értékre</span><span class="sxs-lookup"><span data-stu-id="59c1f-307">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="59c1f-308">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="59c1f-308">Az.Cdn</span></span>
* <span data-ttu-id="59c1f-309">Ki lett javítva egy elgépelés CDN modulátalakító segédben</span><span class="sxs-lookup"><span data-stu-id="59c1f-309">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="59c1f-310">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c1f-310">Az.Compute</span></span>
* <span data-ttu-id="59c1f-311">Új VmssId a New-AzVMConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-311">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="59c1f-312">Új TerminateScheduledEvents és a TerminateScheduledEventNotBeforeTimeoutInMinutes paraméterek a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-312">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="59c1f-313">Új HyperVGeneration tulajdonság a VM-rendszerképobjektumhoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-313">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="59c1f-314">Új Host és HostGroup jellemzők</span><span class="sxs-lookup"><span data-stu-id="59c1f-314">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="59c1f-315">Új parancsmagok:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="59c1f-315">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="59c1f-316">Új HostId paraméter a New-AzVMConfig és a New-AzVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-316">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="59c1f-317">Az Invoke-AzVMRunCommand dokumentációjában található példa frissítve lett a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="59c1f-317">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="59c1f-318">A -VolumeType leírása frissítve lett a set-AzVMDiskEncryptionExtension és a set-AzVmssDiskEncryptionExtension referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="59c1f-318">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="59c1f-319">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="59c1f-319">Az.DataFactory</span></span>
* <span data-ttu-id="59c1f-320">A New-AzDataFactoryEncryptValue dokumentációjában a Windows szó nagy kezdőbetűsre lett javítva</span><span class="sxs-lookup"><span data-stu-id="59c1f-320">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="59c1f-321">Az ADF .Net SDK a 4.1.2-es verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="59c1f-321">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="59c1f-322">Új DataProxyIntegrationRuntimeName, DataProxyIntegrationRuntimeName és DataProxyStagingPath paraméterek lettek hozzáadva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz, lehetővé téve a helyi integrációs modul SSIS integrációs modul proxyjaként való beállítását</span><span class="sxs-lookup"><span data-stu-id="59c1f-322">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="59c1f-323">Frissítve lett a PSTriggerRun, hogy megjelenítse az aktivált folyamatokat, üzeneteket és tulajdonságokat, illetve a PSActivityRun, hogy megjelenítse a tevékenységtípust</span><span class="sxs-lookup"><span data-stu-id="59c1f-323">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="59c1f-324">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="59c1f-324">Az.DataLakeStore</span></span>
* <span data-ttu-id="59c1f-325">Ki lett javítva a Get-DataLakeStoreDeletedItem lefagyása hibák vagy távoli kivételek esetén.</span><span class="sxs-lookup"><span data-stu-id="59c1f-325">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="59c1f-326">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="59c1f-326">Az.EventHub</span></span>
* <span data-ttu-id="59c1f-327">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNteworkRule paraméter a Set-AzEventHubNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="59c1f-327">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="59c1f-328">Ki lett javítva a 9558-as számú hiba: Set-AzEventHubNamespace a PUT helyett a PATCH kérést használta</span><span class="sxs-lookup"><span data-stu-id="59c1f-328">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="59c1f-329">új EnableKafka paraméter a Set-AzEventHubNamespace parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-329">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="59c1f-330">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="59c1f-330">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="59c1f-331">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="59c1f-331">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="59c1f-332">Ki lett javítva egy elgépelés a dokumentációban, ahol az Azure csupa kisbetűvel szerepelt</span><span class="sxs-lookup"><span data-stu-id="59c1f-332">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="59c1f-333">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="59c1f-333">Az.Monitor</span></span>
* <span data-ttu-id="59c1f-334">Hibás paraméternév lett kijavítva a súgódokumentációban</span><span class="sxs-lookup"><span data-stu-id="59c1f-334">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="59c1f-335">Az.Network</span><span class="sxs-lookup"><span data-stu-id="59c1f-335">Az.Network</span></span>
* <span data-ttu-id="59c1f-336">Frissítve lett a New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="59c1f-336">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="59c1f-337">A PublicIpAddress elavult, mert a kiszolgálóoldalon nem használatos.</span><span class="sxs-lookup"><span data-stu-id="59c1f-337">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="59c1f-338">Hozzá lett adva egy opcionális Primary paraméter, amely azt jelzi, hogy a jelenlegi IP-konfiguráció elsődleges-e.</span><span class="sxs-lookup"><span data-stu-id="59c1f-338">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="59c1f-339">Javítva lett az SDK kérelemhiba-kivételének kezelése – kijavítja azt a problémát, amely miatt az SDK-kivételek kezelése korábban nem volt megfelelő, és a fontos hibarészletek nem jelentek meg</span><span class="sxs-lookup"><span data-stu-id="59c1f-339">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="59c1f-340">Be lett állítva, hogy az IPv6 IP-előtag ellenőrzési logikája ellenőrizze az IPv6-előtag hosszának megfelelőségét.</span><span class="sxs-lookup"><span data-stu-id="59c1f-340">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="59c1f-341">Frissült a Get-AzVirtualNetworkSubnetConfig: Új paraméterkészlet lett hozzáadva az alhálózat erőforrás-azonosítója szerinti lekéréshez.</span><span class="sxs-lookup"><span data-stu-id="59c1f-341">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="59c1f-342">Frissült az AzNetworkServiceTag Location paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="59c1f-342">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="59c1f-343">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="59c1f-343">Az.OperationalInsights</span></span>
* <span data-ttu-id="59c1f-344">Frissült a New-AzOperationalInsightsLinuxSyslogDataSource dokumentációja</span><span class="sxs-lookup"><span data-stu-id="59c1f-344">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="59c1f-345">Példa hozzáadva</span><span class="sxs-lookup"><span data-stu-id="59c1f-345">Added example</span></span>
    - <span data-ttu-id="59c1f-346">A -Name paraméter leírása frissítve lett</span><span class="sxs-lookup"><span data-stu-id="59c1f-346">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="59c1f-347">Új példa lett hozzáadva a New-AzOperationalInsightsWindowsEventDataSource parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-347">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="59c1f-348">Módosult a New-AzOperationalInsightsWindowsEventDataSource -Name paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="59c1f-348">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="59c1f-349">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="59c1f-349">Az.RecoveryServices</span></span>
* <span data-ttu-id="59c1f-350">Frissült a Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="59c1f-350">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="59c1f-351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c1f-351">Az.Resources</span></span>
* <span data-ttu-id="59c1f-352">A Microsoft.Resource mostantól támogatja a 2019-05-10-es új api-verziót</span><span class="sxs-lookup"><span data-stu-id="59c1f-352">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="59c1f-353">Mostantól támogatott a copy.count = 0 a változók, erőforrások és tulajdonságok esetében</span><span class="sxs-lookup"><span data-stu-id="59c1f-353">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="59c1f-354">A condition = false vagy copy.count = 0 tulajdonságú erőforrások teljes módban törölve lesznek</span><span class="sxs-lookup"><span data-stu-id="59c1f-354">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="59c1f-355">A súgódokumentációhoz hozzá lett adva egy példa a szabályzatok előfizetési szinten történő hozzárendeléséhez</span><span class="sxs-lookup"><span data-stu-id="59c1f-355">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="59c1f-356">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="59c1f-356">Az.ServiceBus</span></span>
* <span data-ttu-id="59c1f-357">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNetworkRule paraméter a Set-AzServiceBusNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="59c1f-357">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="59c1f-358">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="59c1f-358">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="59c1f-359">Új Test-AzServiceBusNameAvailability parancs lett hozzáadva annak ellenőrzésére, hogy az üzenetsor és a témakör neve elérhető-e</span><span class="sxs-lookup"><span data-stu-id="59c1f-359">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="59c1f-360">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="59c1f-360">Az.ServiceFabric</span></span>
* <span data-ttu-id="59c1f-361">Ki lettek javítva a csomóponttípus-hozzáadási parancsmag hibái:</span><span class="sxs-lookup"><span data-stu-id="59c1f-361">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="59c1f-362">NullReferenceException hiba történt, ha az erőforráscsoport más, a Service Fabric-fürthöz nem kapcsolódó VMSS-sel rendelkezett.</span><span class="sxs-lookup"><span data-stu-id="59c1f-362">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="59c1f-363">Kijavított hiba: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="59c1f-363">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="59c1f-364">Ki lett javítva egy hiba, amely miatt a parancsmag futása meghiúsult, ha a virtualNetwork a fürttől eltérő erőforráscsoportban volt.</span><span class="sxs-lookup"><span data-stu-id="59c1f-364">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="59c1f-365">kijavított hiba: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="59c1f-365">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="59c1f-366">Az Add-AzServiceFabricApplicationCertificate parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="59c1f-366">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="59c1f-367">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="59c1f-367">Az.Sql</span></span>
* <span data-ttu-id="59c1f-368">Frissült a régi naplózási parancsmagok dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="59c1f-368">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="59c1f-369">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="59c1f-369">Az.Storage</span></span>
* <span data-ttu-id="59c1f-370">A Get/Close-AzStorageFileHandle súgója további parancsmagpélda-forgatókönyvek hozzáadásával és a paraméterek leírásának frissítésével változott</span><span class="sxs-lookup"><span data-stu-id="59c1f-370">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="59c1f-371">A StandardBlobTier mostantól támogatott a blobfeltöltési és -másolási műveletekhez</span><span class="sxs-lookup"><span data-stu-id="59c1f-371">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="59c1f-372">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="59c1f-372">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="59c1f-373">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="59c1f-373">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="59c1f-374">A rehidratálás prioritása mostantól támogatott a blobmásoláskor</span><span class="sxs-lookup"><span data-stu-id="59c1f-374">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="59c1f-375">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="59c1f-375">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="59c1f-376">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="59c1f-376">Az.Websites</span></span>
* <span data-ttu-id="59c1f-377">Magyarázat hozzáadva a Set-AzWebApp és a Set-AzWebAppSlot parancsmagok -AppSettings paraméteréhez</span><span class="sxs-lookup"><span data-stu-id="59c1f-377">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="59c1f-378">2.5.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="59c1f-378">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="59c1f-379">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="59c1f-379">Az.Accounts</span></span>
* <span data-ttu-id="59c1f-380">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="59c1f-380">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="59c1f-381">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="59c1f-381">Az.ApplicationInsights</span></span>
* <span data-ttu-id="59c1f-382">A Remove-AzApplicationInsightsApiKey dokumentáció példájában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="59c1f-382">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="59c1f-383">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="59c1f-383">Az.Automation</span></span>
* <span data-ttu-id="59c1f-384">Az erőforrássztringben található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="59c1f-384">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="59c1f-385">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="59c1f-385">Az.CognitiveServices</span></span>
* <span data-ttu-id="59c1f-386">NetworkRuleSet támogatás hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="59c1f-386">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="59c1f-387">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c1f-387">Az.Compute</span></span>
* <span data-ttu-id="59c1f-388">A virtuálisgép-példány nézetobjektumaiból hiányzó tulajdonságok (ComputerName, OsName, OsVersion és HyperVGeneration) hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="59c1f-388">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="59c1f-389">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="59c1f-389">Az.ContainerRegistry</span></span>
* <span data-ttu-id="59c1f-390">A Remove-AzContainerRegistryReplication Replikáció paraméterében lévő elírás javítása</span><span class="sxs-lookup"><span data-stu-id="59c1f-390">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="59c1f-391">További információ: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="59c1f-391">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="59c1f-392">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="59c1f-392">Az.DataFactory</span></span>
* <span data-ttu-id="59c1f-393">Az ADF .Net SDK a 4.1.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="59c1f-393">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="59c1f-394">A Get-AzDataFactoryV2PipelineRun dokumentációjában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="59c1f-394">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="59c1f-395">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="59c1f-395">Az.EventHub</span></span>
* <span data-ttu-id="59c1f-396">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="59c1f-396">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="59c1f-397">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="59c1f-397">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="59c1f-398">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="59c1f-398">Az.KeyVault</span></span>
* <span data-ttu-id="59c1f-399">A KeySize tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="59c1f-399">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="59c1f-400">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="59c1f-400">Az.LogicApp</span></span>
* <span data-ttu-id="59c1f-401">A Get-AzIntegrationAccountMap javítása, hogy minden leképezéstípust listázzon</span><span class="sxs-lookup"><span data-stu-id="59c1f-401">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="59c1f-402">Új MapType paraméter hozzáadva a szűréshez</span><span class="sxs-lookup"><span data-stu-id="59c1f-402">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="59c1f-403">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="59c1f-403">Az.ManagedServices</span></span>
* <span data-ttu-id="59c1f-404">Az API 2019. 06. 01-én kiadott (GA) verziójának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="59c1f-404">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="59c1f-405">Az.Network</span><span class="sxs-lookup"><span data-stu-id="59c1f-405">Az.Network</span></span>
* <span data-ttu-id="59c1f-406">A privát végpont és privát kapcsolatszolgáltatás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="59c1f-406">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="59c1f-407">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="59c1f-407">New cmdlets</span></span>
        - <span data-ttu-id="59c1f-408">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="59c1f-408">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="59c1f-409">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="59c1f-409">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="59c1f-410">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="59c1f-410">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="59c1f-411">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="59c1f-411">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="59c1f-412">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="59c1f-412">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="59c1f-413">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="59c1f-413">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="59c1f-414">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="59c1f-414">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="59c1f-415">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="59c1f-415">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="59c1f-416">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies jelző a VirtualNetwork alhálózatban</span><span class="sxs-lookup"><span data-stu-id="59c1f-416">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="59c1f-417">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig frissítve</span><span class="sxs-lookup"><span data-stu-id="59c1f-417">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="59c1f-418">Hozzá lett adva a -PrivateEndpointNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát végpont esetében.</span><span class="sxs-lookup"><span data-stu-id="59c1f-418">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="59c1f-419">Hozzá lett adva a -PrivateLinkServiceNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát kapcsolati szolgáltatás esetében.</span><span class="sxs-lookup"><span data-stu-id="59c1f-419">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="59c1f-420">Az AzPrivateLinkService parancsmag ServiceName paramétere átnevezve a Name névre a ServiceName aliasszal a visszamenőleges kompatibilitás érdekében</span><span class="sxs-lookup"><span data-stu-id="59c1f-420">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="59c1f-421">ICMP-protokoll engedélyezése a hálózati biztonsági szabályzati konfigurációkhoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-421">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="59c1f-422">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="59c1f-422">Updated cmdlets</span></span>
        - <span data-ttu-id="59c1f-423">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="59c1f-423">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="59c1f-424">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="59c1f-424">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="59c1f-425">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="59c1f-425">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="59c1f-426">A ConnectionProtocolType (Ikev1/Ikev2) hozzáadva a New-AzVirtualNetworkGatewayConnection konfigurálható paramétereként</span><span class="sxs-lookup"><span data-stu-id="59c1f-426">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="59c1f-427">PrivateIpAddressVersion hozzáadva a LoadBalancerFrontendIpConfigurationhöz</span><span class="sxs-lookup"><span data-stu-id="59c1f-427">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="59c1f-428">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="59c1f-428">Updated cmdlet:</span></span>
        - <span data-ttu-id="59c1f-429">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="59c1f-429">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="59c1f-430">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="59c1f-430">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="59c1f-431">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="59c1f-431">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="59c1f-432">Application Gateway New-AzApplicationGatewayProbeConfig parancs frissítése a mintavétel egyéni portjának támogatásához</span><span class="sxs-lookup"><span data-stu-id="59c1f-432">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="59c1f-433">Frissített New-AzApplicationGatewayProbeConfig: A Port opcionális paraméter hozzáadva, amelyet a rendszer a háttérrendszer-kiszolgáló mintavételére használ.</span><span class="sxs-lookup"><span data-stu-id="59c1f-433">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="59c1f-434">Ez a paraméter a Standard_V2 és WAF_V2 termékváltozatokban használható.</span><span class="sxs-lookup"><span data-stu-id="59c1f-434">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="59c1f-435">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="59c1f-435">Az.OperationalInsights</span></span>
* <span data-ttu-id="59c1f-436">A mentett keresések alapértelmezett verziója 1 értékre frissítve.</span><span class="sxs-lookup"><span data-stu-id="59c1f-436">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="59c1f-437">Null reguláris kifejezések kezelése javítva az egyéni naplókban</span><span class="sxs-lookup"><span data-stu-id="59c1f-437">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="59c1f-438">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="59c1f-438">Az.RecoveryServices</span></span>
* <span data-ttu-id="59c1f-439">A Get-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="59c1f-439">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="59c1f-440">A Get-AzRecoveryServicesBackupContainer.md frissítése</span><span class="sxs-lookup"><span data-stu-id="59c1f-440">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="59c1f-441">A Get-AzRecoveryServicesVault.md frissítése</span><span class="sxs-lookup"><span data-stu-id="59c1f-441">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="59c1f-442">A Wait-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="59c1f-442">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="59c1f-443">A Set-AzRecoveryServicesVaultContext.md frissítése</span><span class="sxs-lookup"><span data-stu-id="59c1f-443">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="59c1f-444">A Get-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="59c1f-444">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="59c1f-445">A Get-AzRecoveryServicesBackupRecoveryPoint.md frissítése</span><span class="sxs-lookup"><span data-stu-id="59c1f-445">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="59c1f-446">A Restore-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="59c1f-446">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="59c1f-447">A tároló Azure-fájlmegosztásban való regisztrációjának törlésére szolgáló szolgáltatáshívás frissítése</span><span class="sxs-lookup"><span data-stu-id="59c1f-447">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="59c1f-448">A Set-AzRecoveryServicesAsrAlertSetting.md frissítése</span><span class="sxs-lookup"><span data-stu-id="59c1f-448">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="59c1f-449">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c1f-449">Az.Resources</span></span>
- <span data-ttu-id="59c1f-450">A New-AzResourceGroupDeployment dokumentációban hivatkozott hiányzó parancsmag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="59c1f-450">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="59c1f-451">A szabályzat parancsmagjai frissítve a 2019. 01. 01. dátumú új API-verzió használatára</span><span class="sxs-lookup"><span data-stu-id="59c1f-451">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="59c1f-452">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="59c1f-452">Az.ServiceBus</span></span>
* <span data-ttu-id="59c1f-453">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="59c1f-453">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="59c1f-454">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="59c1f-454">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="59c1f-455">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="59c1f-455">Az.Sql</span></span>
* <span data-ttu-id="59c1f-456">A Set-AzSqlDatabaseSecondary parancsmag hiányzó példáinak javítása</span><span class="sxs-lookup"><span data-stu-id="59c1f-456">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="59c1f-457">A biztonságirés-felmérés e-mail-cím megadása nélkül beállított ismétlődő vizsgálatának javítása</span><span class="sxs-lookup"><span data-stu-id="59c1f-457">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="59c1f-458">Egy kis elírás javítása egy figyelmeztető üzenetben.</span><span class="sxs-lookup"><span data-stu-id="59c1f-458">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="59c1f-459">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="59c1f-459">Az.Storage</span></span>
* <span data-ttu-id="59c1f-460">A Get-AzStorageAccount hivatkozási dokumentációjában található példa frissítése a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="59c1f-460">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="59c1f-461">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="59c1f-461">Az.StorageSync</span></span>
* <span data-ttu-id="59c1f-462">Az Invoke-AzStorageSyncChangeDetection parancsmag hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="59c1f-462">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="59c1f-463">A 9551-es hiba javítása a TierFilesOlderThanDays betartásához</span><span class="sxs-lookup"><span data-stu-id="59c1f-463">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="59c1f-464">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="59c1f-464">Az.Websites</span></span>
* <span data-ttu-id="59c1f-465">A hiba elhárítása, amely miatt a Get-AzWebApp és a Set-AzWebApp nem adott vissza egyes SiteConfig tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="59c1f-465">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="59c1f-466">Egy új Location paraméter hozzáadása a Get-AzDeletedWebApp és a Restore-AzDeletedWebApp parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-466">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="59c1f-467">A webalkalmazás-tárhelyek New-AzWebApp -IncludeSourceWebAppSlots használatával történő klónozásakor jelentkező hiba javítása</span><span class="sxs-lookup"><span data-stu-id="59c1f-467">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="59c1f-468">2.4.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="59c1f-468">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="59c1f-469">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="59c1f-469">Az.Accounts</span></span>
* <span data-ttu-id="59c1f-470">Profilparancsmagok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="59c1f-470">Add support for profile cmdlets</span></span>
* <span data-ttu-id="59c1f-471">A létrehozott parancsmagokban lévő környezetek és adatsíkok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="59c1f-471">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="59c1f-472">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen végpontot használt az adatsík parancsmagjaihoz Windows PowerShellben</span><span class="sxs-lookup"><span data-stu-id="59c1f-472">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="59c1f-473">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="59c1f-473">Az.Advisor</span></span>
* <span data-ttu-id="59c1f-474">Az Az.Advisor GA-kiadása</span><span class="sxs-lookup"><span data-stu-id="59c1f-474">GA release of Az.Advisor</span></span>
* <span data-ttu-id="59c1f-475">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="59c1f-475">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="59c1f-476">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="59c1f-476">Az.ApiManagement</span></span>
* <span data-ttu-id="59c1f-477">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="59c1f-477">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="59c1f-478">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="59c1f-478">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="59c1f-479">Előfizetések felhasználó és termék szerinti lekérdezésének támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="59c1f-479">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="59c1f-480">„/”, „/apis”, „/apis/echo-api” hatókör használatával történő lekérdezés támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="59c1f-480">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="59c1f-481">A következő hibák ki lettek javítva: https://github.com/Azure/azure-powershell/issues/9307 és https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="59c1f-481">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="59c1f-482">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="59c1f-482">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="59c1f-483">Az „ApiVersion” és az „ApiVersionSetId” megadhatóvá vált az API-k importálásakor</span><span class="sxs-lookup"><span data-stu-id="59c1f-483">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="59c1f-484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="59c1f-484">Az.Automation</span></span>
* <span data-ttu-id="59c1f-485">A Set-AzAutomationConnectionFieldValue parancsmag sztringértékek kezelése esetén fellépő hibája javítva lett.</span><span class="sxs-lookup"><span data-stu-id="59c1f-485">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="59c1f-486">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c1f-486">Az.Compute</span></span>
* <span data-ttu-id="59c1f-487">A HyperVGeneration paraméter hozzáadása a New-AzImageConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-487">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="59c1f-488">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="59c1f-488">Az.DataFactory</span></span>
* <span data-ttu-id="59c1f-489">A tevékenység-, folyamat- és eseményindító-futtatási kimenetek lekérdezési ADF-parancsmagjainak frissítése a Select-Object folyamat támogatásához.</span><span class="sxs-lookup"><span data-stu-id="59c1f-489">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="59c1f-490">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="59c1f-490">Az.EventGrid</span></span>
* <span data-ttu-id="59c1f-491">Az elgépelés ki lett javítva a New-AzEventGridSubscription dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="59c1f-491">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="59c1f-492">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="59c1f-492">Az.IotHub</span></span>
* <span data-ttu-id="59c1f-493">Az engedélyezési szabályzati kulcsok újragenerálásának támogatása hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="59c1f-493">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="59c1f-494">Az.Network</span><span class="sxs-lookup"><span data-stu-id="59c1f-494">Az.Network</span></span>
* <span data-ttu-id="59c1f-495">A „RoutingPreference” hozzáadva a nyilvános IP-címkékhez</span><span class="sxs-lookup"><span data-stu-id="59c1f-495">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="59c1f-496">Javítottuk a példákat a „Get-AzNetworkServiceTag” referenciadokumentációban</span><span class="sxs-lookup"><span data-stu-id="59c1f-496">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="59c1f-497">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="59c1f-497">Az.PolicyInsights</span></span>
* <span data-ttu-id="59c1f-498">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyState parancsmagban</span><span class="sxs-lookup"><span data-stu-id="59c1f-498">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="59c1f-499">További információ: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="59c1f-499">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="59c1f-500">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="59c1f-500">Az.OperationalInsights</span></span>
* <span data-ttu-id="59c1f-501">Javítottuk a Get-AzOperationalInsightsDataSource parancsmagban visszaadott CustomLog adatforrásmodellt</span><span class="sxs-lookup"><span data-stu-id="59c1f-501">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="59c1f-502">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="59c1f-502">Az.RecoveryServices</span></span>
* <span data-ttu-id="59c1f-503">Az IaaSVMs get-policy parancsának javítása</span><span class="sxs-lookup"><span data-stu-id="59c1f-503">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="59c1f-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c1f-504">Az.Resources</span></span>
    - <span data-ttu-id="59c1f-505">A Get-AzPolicyState -Top paraméter súgószövegének javítása</span><span class="sxs-lookup"><span data-stu-id="59c1f-505">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="59c1f-506">Ügyféloldali lapozás támogatásának hozzáadása a Get-AzPolicyAlias parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-506">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="59c1f-507">Új (-PolicyParameters és -PolicyParametersObject) paraméterek hozzáadása a Set-AzPolicyAssignment parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-507">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="59c1f-508">A Policy-parancsmagok néhány dokumentumának és példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="59c1f-508">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="59c1f-509">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="59c1f-509">Az.ServiceBus</span></span>
* <span data-ttu-id="59c1f-510">A 4938-as hiba javítása – A New-AzureRmServiceBusQueue parancsmag BadRequest értéket ad vissza a MaxSizeInMegabytes megadásakor</span><span class="sxs-lookup"><span data-stu-id="59c1f-510">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="59c1f-511">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="59c1f-511">Az.Sql</span></span>
* <span data-ttu-id="59c1f-512">A példány-feladatátvételi csoportok parancsmagjainak hozzáadása az előzetes kiadásból a nyilvános kiadáshoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-512">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="59c1f-513">Az Azure SQL Server\Database Auditing támogatása új parancsmagokkal.</span><span class="sxs-lookup"><span data-stu-id="59c1f-513">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="59c1f-514">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="59c1f-514">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="59c1f-515">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="59c1f-515">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="59c1f-516">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="59c1f-516">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="59c1f-517">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="59c1f-517">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="59c1f-518">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="59c1f-518">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="59c1f-519">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="59c1f-519">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="59c1f-520">E-mailes korlátozások eltávolítása a sebezhetőségi felmérés beállításaiból</span><span class="sxs-lookup"><span data-stu-id="59c1f-520">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="59c1f-521">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="59c1f-521">Az.Storage</span></span>
* <span data-ttu-id="59c1f-522">Az „-IndexDocument” és „-ErrorDocument404Path” paraméter módosítása kötelezőről opcionálisra a következő parancsmagban:</span><span class="sxs-lookup"><span data-stu-id="59c1f-522">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="59c1f-523">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="59c1f-523">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="59c1f-524">A Get-AzStorageBlobContent súgójának frissítése egy példa hozzáadásával</span><span class="sxs-lookup"><span data-stu-id="59c1f-524">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="59c1f-525">További hibaadatok megjelenítése, ha a parancsmag futtatása StorageException miatt meghiúsul</span><span class="sxs-lookup"><span data-stu-id="59c1f-525">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="59c1f-526">Storage-fiók létrehozásának és frissítésének támogatása Azure Files AAD DS-hitelesítéssel</span><span class="sxs-lookup"><span data-stu-id="59c1f-526">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="59c1f-527">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="59c1f-527">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="59c1f-528">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="59c1f-528">Set-AzStorageAccount</span></span>
* <span data-ttu-id="59c1f-529">Támogatás a fájlmegosztások, fájlkönyvtárak vagy fájlok fájlleíróinak listázásához vagy bezárásához</span><span class="sxs-lookup"><span data-stu-id="59c1f-529">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="59c1f-530">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="59c1f-530">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="59c1f-531">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="59c1f-531">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="59c1f-532">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="59c1f-532">Az.StorageSync</span></span>
* <span data-ttu-id="59c1f-533">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="59c1f-533">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="59c1f-534">2.3.2 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="59c1f-534">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="59c1f-535">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="59c1f-535">Az.Accounts</span></span>
* <span data-ttu-id="59c1f-536">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen URL-címeket használt a Functions-hívásokhoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-536">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="59c1f-537">További információ: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="59c1f-537">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="59c1f-538">Javítva lett az aliasok hibája az AzureRM–Az parancsmagok közötti átvitel esetében</span><span class="sxs-lookup"><span data-stu-id="59c1f-538">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="59c1f-539">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="59c1f-539">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="59c1f-540">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="59c1f-540">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="59c1f-541">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c1f-541">Az.Compute</span></span>
* <span data-ttu-id="59c1f-542">A „New-AzVm” és „New-AzVmss” egyszerű paraméterkészletek mostantól elfogadják a „ProximityPlacementGroup” paramétert.</span><span class="sxs-lookup"><span data-stu-id="59c1f-542">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="59c1f-543">Az elgépelés ki lett javítva a „New-AzVM” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="59c1f-543">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="59c1f-544">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="59c1f-544">Az.Dns</span></span>
* <span data-ttu-id="59c1f-545">Az elgépelés ki lett javítva a „Set-AzDnsZone” súgópéldáinál.</span><span class="sxs-lookup"><span data-stu-id="59c1f-545">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="59c1f-546">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="59c1f-546">Az.EventGrid</span></span>
* <span data-ttu-id="59c1f-547">Frissítve a 2019-06-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="59c1f-547">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="59c1f-548">Új parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="59c1f-548">New cmdlets:</span></span>
    - <span data-ttu-id="59c1f-549">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="59c1f-549">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="59c1f-550">Létrehoz egy új Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="59c1f-550">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="59c1f-551">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="59c1f-551">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="59c1f-552">Lekéri egy Event Grid-tartomány részleteit, vagy az aktuális Azure-előfizetéshez tartozó összes Event Grid-tartomány listáját.</span><span class="sxs-lookup"><span data-stu-id="59c1f-552">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="59c1f-553">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="59c1f-553">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="59c1f-554">Eltávolít egy Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="59c1f-554">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="59c1f-555">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="59c1f-555">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="59c1f-556">Újra létrehozza a megosztott hozzáférési kulcsot az Azure Event Grid-tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="59c1f-556">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="59c1f-557">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="59c1f-557">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="59c1f-558">Lekéri az Event Grid-tartományban való esemény-közzétételhez használt megosztott hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="59c1f-558">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="59c1f-559">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="59c1f-559">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="59c1f-560">Új Azure Event Grid-tartományi témakört hoz létre.</span><span class="sxs-lookup"><span data-stu-id="59c1f-560">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="59c1f-561">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="59c1f-561">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="59c1f-562">Lekéri egy Event Grid-tartományi témakör részleteit, vagy az aktuális Azure-előfizetés adott Event Grid-tartományához tartozó Event Grid-tartományi témakörök listáját</span><span class="sxs-lookup"><span data-stu-id="59c1f-562">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="59c1f-563">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="59c1f-563">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="59c1f-564">Eltávolít egy meglévő Azure Event Grid-tartományi témakört.</span><span class="sxs-lookup"><span data-stu-id="59c1f-564">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="59c1f-565">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="59c1f-565">Updated cmdlets:</span></span>
    - <span data-ttu-id="59c1f-566">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="59c1f-566">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="59c1f-567">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="59c1f-567">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="59c1f-568">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="59c1f-568">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="59c1f-569">Új paraméterkészletek lettek hozzáadva tartományok és tartományi témakörök esetében, lehetővé téve a meglévő paraméterek (például EndPointType, SubjectBeginsWith stb.) újbóli felhasználását.</span><span class="sxs-lookup"><span data-stu-id="59c1f-569">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="59c1f-570">Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="59c1f-570">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="59c1f-571">Esemény-előfizetés lejárati dátuma,</span><span class="sxs-lookup"><span data-stu-id="59c1f-571">Event subscription expiration date,</span></span>
            - <span data-ttu-id="59c1f-572">Speciális szűrési paraméterek.</span><span class="sxs-lookup"><span data-stu-id="59c1f-572">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="59c1f-573">Új felsorolási érték lett hozzáadva a servicebusqueue elem célértékeként.</span><span class="sxs-lookup"><span data-stu-id="59c1f-573">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="59c1f-574">Nem engedélyezett az -IncludedEventType beállításnál az „All” érték használata és a következővel való helyettesítése:</span><span class="sxs-lookup"><span data-stu-id="59c1f-574">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="59c1f-575">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="59c1f-575">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="59c1f-576">Új opcionális paraméterek (Top, ODataQuery és NextLink) az eredmények tördelésének és szűrésének támogatásához.</span><span class="sxs-lookup"><span data-stu-id="59c1f-576">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="59c1f-577">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="59c1f-577">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="59c1f-578">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="59c1f-578">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="59c1f-579">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="59c1f-579">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="59c1f-580">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="59c1f-580">Az.FrontDoor</span></span>
* <span data-ttu-id="59c1f-581">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="59c1f-581">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="59c1f-582">Hozzá lett adva az átalakítások támogatása és az új operátorértékek automatikus kitöltése (RegEx)</span><span class="sxs-lookup"><span data-stu-id="59c1f-582">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="59c1f-583">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="59c1f-583">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="59c1f-584">Hozzá lett adva az új értékek automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="59c1f-584">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="59c1f-585">Az.Network</span><span class="sxs-lookup"><span data-stu-id="59c1f-585">Az.Network</span></span>
* <span data-ttu-id="59c1f-586">Virtuális hálózati átjárók erőforrás-támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="59c1f-586">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="59c1f-587">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="59c1f-587">New cmdlets</span></span>
        - <span data-ttu-id="59c1f-588">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="59c1f-588">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="59c1f-589">AvailablePrivateEndpointType hozzáadva</span><span class="sxs-lookup"><span data-stu-id="59c1f-589">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="59c1f-590">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="59c1f-590">New cmdlets</span></span> 
        - <span data-ttu-id="59c1f-591">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="59c1f-591">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="59c1f-592">PrivatePrivateLinkService hozzáadva</span><span class="sxs-lookup"><span data-stu-id="59c1f-592">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="59c1f-593">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="59c1f-593">New cmdlets</span></span> 
        - <span data-ttu-id="59c1f-594">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="59c1f-594">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="59c1f-595">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="59c1f-595">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="59c1f-596">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="59c1f-596">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="59c1f-597">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="59c1f-597">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="59c1f-598">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="59c1f-598">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="59c1f-599">PrivateEndpoint hozzáadva</span><span class="sxs-lookup"><span data-stu-id="59c1f-599">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="59c1f-600">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="59c1f-600">New cmdlets</span></span>
        - <span data-ttu-id="59c1f-601">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="59c1f-601">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="59c1f-602">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="59c1f-602">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="59c1f-603">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="59c1f-603">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="59c1f-604">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="59c1f-604">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="59c1f-605">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: UseLocalAzureIpAddress jelző a VpnConnection elemen</span><span class="sxs-lookup"><span data-stu-id="59c1f-605">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="59c1f-606">Frissítve lett a New-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="59c1f-606">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="59c1f-607">Frissítve lett a Set-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="59c1f-607">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="59c1f-608">Hozzá lett adva az írásvédett PeeredConnections mező az ExpressRoute-társhálózatlétesítések esetében.</span><span class="sxs-lookup"><span data-stu-id="59c1f-608">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="59c1f-609">Hozzá lett adva az írásvédett GlobalReachEnabled mező az ExpressRoute esetében.</span><span class="sxs-lookup"><span data-stu-id="59c1f-609">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="59c1f-610">Kompatibilitástörő változást okozó attribútum lett hozzáadva, amely jelzi az AllowGlobalReach mező elavulását az ExpressRouteCircuit-modellben</span><span class="sxs-lookup"><span data-stu-id="59c1f-610">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="59c1f-611">Javítva lett a 8756-os hiba a TargetListenerID AzApplicationGatewayRedirectConfiguration-parancsmagokkal való használata során</span><span class="sxs-lookup"><span data-stu-id="59c1f-611">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="59c1f-612">Javítva lett a hiba a New-AzApplicationGatewayPathRuleConfig parancsmagban, amely megakadályozta az átírási szabálykészlet beállítását.</span><span class="sxs-lookup"><span data-stu-id="59c1f-612">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="59c1f-613">Javítva lett a VirtualNetworkTaps megjelenítése a NetworkInterfaceIpConfiguration esetében</span><span class="sxs-lookup"><span data-stu-id="59c1f-613">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="59c1f-614">Javítva lettek a Cortex Get-parancsmagok az összes rész felsorolásához</span><span class="sxs-lookup"><span data-stu-id="59c1f-614">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="59c1f-615">Javítva lett a VirtualHub-hivatkozás létrehozása az ExpressRouteGateways, VpnGateway esetében</span><span class="sxs-lookup"><span data-stu-id="59c1f-615">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="59c1f-616">Hozzá lett adva a rendelkezésreállási zónák támogatása az AzureFirewall és a NatGateway esetében</span><span class="sxs-lookup"><span data-stu-id="59c1f-616">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="59c1f-617">Hozzá lett adva a Get-AzNetworkServiceTag parancsmag</span><span class="sxs-lookup"><span data-stu-id="59c1f-617">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="59c1f-618">Hozzá lett adva a több nyilvános IP-cím támogatása az Azure Firewall esetében</span><span class="sxs-lookup"><span data-stu-id="59c1f-618">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="59c1f-619">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="59c1f-619">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="59c1f-620">Hozzá lett adva a -PublicIpAddress paraméter, amely egy vagy több nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="59c1f-620">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="59c1f-621">Hozzá lett adva a -VirtualNetwork paraméter, amely virtuális hálózati objektumokat fogad el</span><span class="sxs-lookup"><span data-stu-id="59c1f-621">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="59c1f-622">Hozzá lett adva az AddPublicIpAddress és RemovePublicIpAddress metódus a tűzfalobjektumok esetében, és nyilvános IP-cím-objektumokat fogadnak el bemeneti adatként</span><span class="sxs-lookup"><span data-stu-id="59c1f-622">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="59c1f-623">Elavult a -PublicIpName és a -VirtualNetworkName paraméter</span><span class="sxs-lookup"><span data-stu-id="59c1f-623">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="59c1f-624">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: VpnClient AAD-alapú hitelesítési beállítások megadása a virtuális hálózati átjárók erőforrásaihoz.</span><span class="sxs-lookup"><span data-stu-id="59c1f-624">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="59c1f-625">Frissült a New-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="59c1f-625">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="59c1f-626">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="59c1f-626">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="59c1f-627">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva a RemoveAadAuthentication opcionális kapcsolóparaméter a VpnClient AAD-alapú hitelesítési beállítások eltávolításához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="59c1f-627">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="59c1f-628">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="59c1f-628">Az.OperationalInsights</span></span>
* <span data-ttu-id="59c1f-629">Engedélyezve lett a **pergb2018** tarifacsomag a „New-AzureRmOperationalInsightsWorkspace” parancs esetében</span><span class="sxs-lookup"><span data-stu-id="59c1f-629">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="59c1f-630">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c1f-630">Az.Resources</span></span>
* <span data-ttu-id="59c1f-631">További sablonexportálási beállítások támogatása</span><span class="sxs-lookup"><span data-stu-id="59c1f-631">Support for additional Template Export options</span></span>
    - <span data-ttu-id="59c1f-632">Hozzá lett adva a „-SkipResourceNameParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="59c1f-632">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="59c1f-633">Hozzá lett adva a „-SkipAllParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="59c1f-633">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="59c1f-634">Hozzá lett adva a „-Resource” paraméter az Export-AzResourceGroup esetében az exportált erőforrások szűréséhez</span><span class="sxs-lookup"><span data-stu-id="59c1f-634">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="59c1f-635">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="59c1f-635">Az.ServiceFabric</span></span>
* <span data-ttu-id="59c1f-636">Ki lett javítva az a hiba, hogy a ByExistingKeyVault tanúsítvány hozzáadása bizonyos esetekben helytelen ujjlenyomatot kért le</span><span class="sxs-lookup"><span data-stu-id="59c1f-636">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="59c1f-637">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="59c1f-637">Az.Sql</span></span>
* <span data-ttu-id="59c1f-638">Javítva lett az Advanced Threat Protection Storage-végpontjának utótagja</span><span class="sxs-lookup"><span data-stu-id="59c1f-638">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="59c1f-639">Javítva lett, hogy az Advanced Data Security engedélyezése felülbírálja az Advanced Threat Protection-szabályzatot</span><span class="sxs-lookup"><span data-stu-id="59c1f-639">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="59c1f-640">Új parancsmagok lettek hozzáadva a Management.Sql esetében, amelyek lehetővé teszik az ügyfelek számára TDE-kulcsok hozzáadását és TDE-védő beállítását a felügyelt példányokhoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-640">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="59c1f-641">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="59c1f-641">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="59c1f-642">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="59c1f-642">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="59c1f-643">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="59c1f-643">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="59c1f-644">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="59c1f-644">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="59c1f-645">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="59c1f-645">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="59c1f-646">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="59c1f-646">Az.Storage</span></span>
* <span data-ttu-id="59c1f-647">A FileStorage és az SkuName Premium_ZRS altípus támogatása Storage-fiókok létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="59c1f-647">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="59c1f-648">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="59c1f-648">New-AzStorageAccount</span></span>
* <span data-ttu-id="59c1f-649">Egyértelműsítve lett a blobmódosíthatatlansági parancsmag leírása</span><span class="sxs-lookup"><span data-stu-id="59c1f-649">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="59c1f-650">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="59c1f-650">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="59c1f-651">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="59c1f-651">Az.Websites</span></span>
* <span data-ttu-id="59c1f-652">Optimalizálva lett a Get-AzWebAppCertificate parancsmag, hogy erőforráscsoport szerint szűrjön a kiszolgálón, ne ügyfél szerint</span><span class="sxs-lookup"><span data-stu-id="59c1f-652">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="59c1f-653">Hozzá lett adva a -UseDisasterRecovery kapcsolóparaméter a Get-AzWebAppSnapshot parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-653">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="59c1f-654">2.2.0 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="59c1f-654">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="59c1f-655">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="59c1f-655">Az.Cdn</span></span>
* <span data-ttu-id="59c1f-656">Frissített parancsmagok a rulesEngine szolgáltatás támogatásához a 2019. 04. 15. API-verzión</span><span class="sxs-lookup"><span data-stu-id="59c1f-656">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="59c1f-657">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c1f-657">Az.Compute</span></span>
* <span data-ttu-id="59c1f-658">A `NoWait` paraméter hozzáadása, amely elindítja a műveletet, és azonnal visszatér, még a művelet befejezése előtt.</span><span class="sxs-lookup"><span data-stu-id="59c1f-658">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="59c1f-659">Frissített parancsmagok:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="59c1f-659">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="59c1f-660">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="59c1f-660">Az.EventHub</span></span>
* <span data-ttu-id="59c1f-661">A 9231-es hiba javítása – a Get-AzEventHubNamespace nem ad vissza címkéket</span><span class="sxs-lookup"><span data-stu-id="59c1f-661">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="59c1f-662">A 9230-as hiba javítása – a Get-AzEventHubNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="59c1f-662">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="59c1f-663">Az.Network</span><span class="sxs-lookup"><span data-stu-id="59c1f-663">Az.Network</span></span>
* <span data-ttu-id="59c1f-664">ResourceID és InputObject frissítése a Nat-átjárón</span><span class="sxs-lookup"><span data-stu-id="59c1f-664">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="59c1f-665">ResourceID és InputObject aliasának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="59c1f-665">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="59c1f-666">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="59c1f-666">Az.PolicyInsights</span></span>
* <span data-ttu-id="59c1f-667">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyEvent parancsmagban</span><span class="sxs-lookup"><span data-stu-id="59c1f-667">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="59c1f-668">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="59c1f-668">Az.RecoveryServices</span></span>
* <span data-ttu-id="59c1f-669">Az IaaSVM szabályzat minimális megőrzési ideje 7 napról 1-re módosult</span><span class="sxs-lookup"><span data-stu-id="59c1f-669">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="59c1f-670">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="59c1f-670">Az.ServiceBus</span></span>
* <span data-ttu-id="59c1f-671">A 9182-es hiba javítása – a Get-AzServiceBusNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="59c1f-671">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="59c1f-672">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="59c1f-672">Az.ServiceFabric</span></span>
* <span data-ttu-id="59c1f-673">Az Update-AzServiceFabricReliability hibaüzenetében lévő gépelési hiba kijavítása</span><span class="sxs-lookup"><span data-stu-id="59c1f-673">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="59c1f-674">A Service Fabric parancssorok hiányzó karakterének pótlása</span><span class="sxs-lookup"><span data-stu-id="59c1f-674">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="59c1f-675">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="59c1f-675">Az.Sql</span></span>
* <span data-ttu-id="59c1f-676">A DnsZonePartner paraméter hozzáadása a New-AzureSqlInstance parancsmaghoz az AutoDr képesség a felügyelt példányon való támogatásához.</span><span class="sxs-lookup"><span data-stu-id="59c1f-676">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="59c1f-677">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag kivezetése</span><span class="sxs-lookup"><span data-stu-id="59c1f-677">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="59c1f-678">Threat Detection parancsmagok átnevezése Advanced Threat Protection névre</span><span class="sxs-lookup"><span data-stu-id="59c1f-678">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="59c1f-679">A New-AzSqlInstance, - StorageSizeInGB és - LicenseType paraméterek mostantól nem kötelezőek.</span><span class="sxs-lookup"><span data-stu-id="59c1f-679">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="59c1f-680">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="59c1f-680">Az.Websites</span></span>
* <span data-ttu-id="59c1f-681">javítja azt a hibát, amely miatt a Set-AzWebApp és a Set-AzWebAppSlot a -WebApp tulajdonsággal való használata eltávolította a címkéket</span><span class="sxs-lookup"><span data-stu-id="59c1f-681">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="59c1f-682">2.1.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="59c1f-682">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="59c1f-683">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="59c1f-683">Az.ApiManagement</span></span>
* <span data-ttu-id="59c1f-684">Új parancsmagok a globális és API-szintű diagnosztika kezeléshez</span><span class="sxs-lookup"><span data-stu-id="59c1f-684">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="59c1f-685">**Get-AzApiManagementDiagnostic** – A globális vagy API hatókörre konfigurált diagnosztika beolvasása</span><span class="sxs-lookup"><span data-stu-id="59c1f-685">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="59c1f-686">**New-AzApiManagementDiagnostic** – Új diagnosztika létrehozása a globális vagy API szintű hatókörhöz</span><span class="sxs-lookup"><span data-stu-id="59c1f-686">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="59c1f-687">**New-AzApiManagementHttpMessageDiagnostic** – Diagnosztikai beállítás létrehozása arra vonatkozóan, hogy mely fejléceknél naplózzon a rendszer, és mekkora legyen a törzs mérete bájtban</span><span class="sxs-lookup"><span data-stu-id="59c1f-687">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="59c1f-688">**New-AzApiManagementPipelineDiagnosticSetting** – Diagnosztikai beállítások létrehozása az átjáróra érkező és onnan induló HTTP-üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="59c1f-688">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="59c1f-689">**New-AzApiManagementSamplingSetting** – Mintavételezési beállítások létrehozása diagnosztikai kérésekhez/válaszokhoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-689">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="59c1f-690">**Remove-AzApiManagementDiagnostic** – Diagnosztikai entitás eltávolítása globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="59c1f-690">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="59c1f-691">**Set-AzApiManagementDiagnostic** – Diagnosztikai entitás frissítése globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="59c1f-691">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="59c1f-692">Új parancsmagok az ApiManagement szolgáltatás gyorsítótárának kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="59c1f-692">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="59c1f-693">**Get-AzApiManagementCache** – Az azonosító által megadott vagy az összes gyorsítótár részleteinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="59c1f-693">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="59c1f-694">**New-AzApiManagementCache** – Új alapértelmezett gyorsítótár létrehozása vagy gyorsítótár létrehozása adott Azure-régióban</span><span class="sxs-lookup"><span data-stu-id="59c1f-694">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="59c1f-695">**Remove-AzApiManagementCache** – Gyorsítótár eltávolítása</span><span class="sxs-lookup"><span data-stu-id="59c1f-695">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="59c1f-696">**Update-AzApiManagementCache** – Gyorsítótár frissítése</span><span class="sxs-lookup"><span data-stu-id="59c1f-696">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="59c1f-697">Új parancsmagok az API-séma kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="59c1f-697">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="59c1f-698">**New-AzApiManagementSchema** – Új séma létrehozása egy API-hoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-698">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="59c1f-699">**Get-AzApiManagementSchema** – Az API-ban konfigurált sémák beolvasása</span><span class="sxs-lookup"><span data-stu-id="59c1f-699">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="59c1f-700">**Remove-AzApiManagementSchema** – Az API-ban konfigurált sémák eltávolítása</span><span class="sxs-lookup"><span data-stu-id="59c1f-700">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="59c1f-701">**Set-AzApiManagementSchema** – Az API-ban konfigurált séma frissítése</span><span class="sxs-lookup"><span data-stu-id="59c1f-701">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="59c1f-702">Új parancsmag a felhasználói jogkivonat létrehozásához</span><span class="sxs-lookup"><span data-stu-id="59c1f-702">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="59c1f-703">**New-AzApiManagementUserToken** – Új, alapértelmezés szerint 8 órán át érvényes felhasználói jogkivonat létrehozása. Ezen parancsmag használatával lehet a „GIT” felhasználó számára jogkivonatot létrehozni.</span><span class="sxs-lookup"><span data-stu-id="59c1f-703">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="59c1f-704">Új parancsmag a hálózat állapotának lekérdezéséhez</span><span class="sxs-lookup"><span data-stu-id="59c1f-704">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="59c1f-705">**Get-AzApiManagementNetworkStatus** – Azon erőforrások hálózati állapotának beolvasása, amelyektől az API Management szolgáltatás függ.</span><span class="sxs-lookup"><span data-stu-id="59c1f-705">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="59c1f-706">Ez hasznos lehet, ha az ApiManagement szolgáltatást virtuális hálózatra telepíti, és ellenőrizni kell, hogy rendben működnek-e a függőségek.</span><span class="sxs-lookup"><span data-stu-id="59c1f-706">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="59c1f-707">A **New-AzApiManagement** parancsmag frissítése az ApiManagement szolgáltatás kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="59c1f-707">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="59c1f-708">Mostantól az új „Consumption” SKU is támogatott</span><span class="sxs-lookup"><span data-stu-id="59c1f-708">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="59c1f-709">Mostantól az „EnableClientCertificate” jelző a „Consumption” SKU-hoz is bekapcsolható</span><span class="sxs-lookup"><span data-stu-id="59c1f-709">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="59c1f-710">Az új **New-AzApiManagementSslSetting** parancsmag lehetővé teszi a „TLS/SSL” beállítás konfigurálását a „Háttér” és „Előtér” esetén is.</span><span class="sxs-lookup"><span data-stu-id="59c1f-710">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="59c1f-711">Ez egy ApiManagement szolgáltatás előterén a titkosítások, mint például a 3DES, valamint a szerverprotokollok, mint például a Http2 konfigurálására is alkalmas.</span><span class="sxs-lookup"><span data-stu-id="59c1f-711">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="59c1f-712">Mostantól támogatott a „DeveloperPortal” gazdanév ApiManagement szolgáltatáson történő konfigurálása.</span><span class="sxs-lookup"><span data-stu-id="59c1f-712">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="59c1f-713">A **Get-AzApiManagementSsoToken** parancsmagok frissítése a „PsApiManagement” objektum bemenetként való használatához</span><span class="sxs-lookup"><span data-stu-id="59c1f-713">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="59c1f-714">A parancsmag frissítése a hibaüzenetek beágyazott megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="59c1f-714">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="59c1f-715">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hibakód: ValidationError Hibaüzenet: Egy vagy több mező hibás értéket tartalmaz: Hiba részletei:    [Kód=ValidationError, Üzenet=Hiba a log-to-eventhub elemben, 3. sor, 10. oszlop: A naplózó nem található, Cél=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="59c1f-715">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="59c1f-716">Az **Export-AzApiManagementApi** parancsmag frissítse az API-k OpenApi 3.0 formátumban való exportálásához</span><span class="sxs-lookup"><span data-stu-id="59c1f-716">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="59c1f-717">Az **Import-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="59c1f-717">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="59c1f-718">API importálása az OpenApi 3.0 dokumentumspecifikációból</span><span class="sxs-lookup"><span data-stu-id="59c1f-718">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="59c1f-719">A bármely (Swagger, Wadl, Wsdl, OpenAPI) dokumentumban megadott PsApiManagementSchema tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="59c1f-719">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="59c1f-720">A bármely dokumentumban megadott ServiceUrl tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="59c1f-720">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="59c1f-721">A **Get-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) való visszaadásához</span><span class="sxs-lookup"><span data-stu-id="59c1f-721">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="59c1f-722">A **Set-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) és XML-nek megfelelő feloldójeles formátumban (xml használatával) való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="59c1f-722">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="59c1f-723">A **New-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="59c1f-723">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="59c1f-724">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="59c1f-724">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="59c1f-725">API létrehozása ApiVersionSet tulajdonságban</span><span class="sxs-lookup"><span data-stu-id="59c1f-725">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="59c1f-726">API klónozása SourceApiId és SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="59c1f-726">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="59c1f-727">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="59c1f-727">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="59c1f-728">A **Set-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="59c1f-728">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="59c1f-729">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="59c1f-729">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="59c1f-730">API frissítése ApiVersionSet tulajdonságba</span><span class="sxs-lookup"><span data-stu-id="59c1f-730">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="59c1f-731">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="59c1f-731">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="59c1f-732">A **New-AzApiManagementRevision** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="59c1f-732">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="59c1f-733">Létező változat klónozása (címkék, termékek, műveletek és szabályzatok másolása) a SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="59c1f-733">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="59c1f-734">Az új változat a szülő ApiId értékét veszi át</span><span class="sxs-lookup"><span data-stu-id="59c1f-734">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="59c1f-735">ApiRevisionDescription biztosítása</span><span class="sxs-lookup"><span data-stu-id="59c1f-735">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="59c1f-736">A „ServiceUrl” felülírása API klónozáskor</span><span class="sxs-lookup"><span data-stu-id="59c1f-736">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="59c1f-737">A **New-AzApiManagementIdentityProvider** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="59c1f-737">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="59c1f-738">AAD vagy AADB2C konfigurálása hitelesítésszolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="59c1f-738">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="59c1f-739">SignupPolicy, SigninPolicy, ProfileEditingPolicy és PasswordResetPolicy beállítása</span><span class="sxs-lookup"><span data-stu-id="59c1f-739">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="59c1f-740">A **New-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="59c1f-740">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="59c1f-741">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-741">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="59c1f-742">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-742">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="59c1f-743">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="59c1f-743">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="59c1f-744">A **Set-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="59c1f-744">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="59c1f-745">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-745">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="59c1f-746">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-746">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="59c1f-747">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="59c1f-747">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="59c1f-748">Az alábbi parancsmagok frissültek a ResourceID bemenetként való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="59c1f-748">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="59c1f-749">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="59c1f-749">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="59c1f-750">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="59c1f-750">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="59c1f-751">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="59c1f-751">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="59c1f-752">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="59c1f-752">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="59c1f-753">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="59c1f-753">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="59c1f-754">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="59c1f-754">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="59c1f-755">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="59c1f-755">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="59c1f-756">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="59c1f-756">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="59c1f-757">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="59c1f-757">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="59c1f-758">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="59c1f-758">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="59c1f-759">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="59c1f-759">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="59c1f-760">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="59c1f-760">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="59c1f-761">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="59c1f-761">Az.Automation</span></span>
* <span data-ttu-id="59c1f-762">A Get-AzAutomationJobOutputRecord frissítése a JSON- és a szövegrekordértékek kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="59c1f-762">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="59c1f-763">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="59c1f-763">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="59c1f-764">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="59c1f-764">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="59c1f-765">A Start-AzAutomationDscCompilationJob viselkedésének módosítása a munka elindítására a befejezésre való várakozás helyett</span><span class="sxs-lookup"><span data-stu-id="59c1f-765">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="59c1f-766">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="59c1f-766">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="59c1f-767">A Get-AzAutomationDscNode azon hibájának javítása, amely miatt a -Name használatakor az összes csomópontot visszaadta.</span><span class="sxs-lookup"><span data-stu-id="59c1f-767">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="59c1f-768">Most már csak az egyező csomópontot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="59c1f-768">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="59c1f-769">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c1f-769">Az.Compute</span></span>
* <span data-ttu-id="59c1f-770">A ProtectFromScaleIn és a ProtectFromScaleSetAction paraméterek hozzáadása az Update-AzVmssVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-770">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="59c1f-771">A New-azvm fedőparaméter-készlet mostantól alapértelmezetten egy elérhető helyet használ, ha az USA keleti régiója nem támogatott</span><span class="sxs-lookup"><span data-stu-id="59c1f-771">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="59c1f-772">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="59c1f-772">Az.DataLakeStore</span></span>
* <span data-ttu-id="59c1f-773">Az ADLS SDK frissítése a httpclient használatához, integrált adatsíkteszteléssel az Azure-keretrendszerben</span><span class="sxs-lookup"><span data-stu-id="59c1f-773">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="59c1f-774">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="59c1f-774">Az.Monitor</span></span>
* <span data-ttu-id="59c1f-775">A hibás paraméternevek kijavítása a súgópéldákban</span><span class="sxs-lookup"><span data-stu-id="59c1f-775">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="59c1f-776">Az.Network</span><span class="sxs-lookup"><span data-stu-id="59c1f-776">Az.Network</span></span>
* <span data-ttu-id="59c1f-777">DisableBgpRoutePropagation jelölő hozzáadása az érvényes útválasztási táblázathoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-777">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="59c1f-778">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="59c1f-778">Updated cmdlet:</span></span>
        - <span data-ttu-id="59c1f-779">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="59c1f-779">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="59c1f-780">A dupla kötőjel kijavítása a New-AzApplicationGatewayTrustedRootCertificate dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="59c1f-780">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="59c1f-781">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c1f-781">Az.Resources</span></span>
* <span data-ttu-id="59c1f-782">Új Get-AzureRmDenyAssignment parancsmag hozzáadása a megtagadási hozzárendelések lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="59c1f-782">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="59c1f-783">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="59c1f-783">Az.Sql</span></span>
* <span data-ttu-id="59c1f-784">Advanced Threat Protection parancsmagok átnevezése Advanced Data Security névre és a sebezhetőségi felmérés alapértelmezett engedélyezése</span><span class="sxs-lookup"><span data-stu-id="59c1f-784">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="59c1f-785">2.0.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="59c1f-785">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="59c1f-786">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="59c1f-786">Az.Accounts</span></span>
* <span data-ttu-id="59c1f-787">Az Authentication Library frissítése a felhasználóneves/jelszavas hitelesítéssel kapcsolatos ADFS-problémák kijavításához</span><span class="sxs-lookup"><span data-stu-id="59c1f-787">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="59c1f-788">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="59c1f-788">Az.CognitiveServices</span></span>
* <span data-ttu-id="59c1f-789">Csak a Bing jogi nyilatkozat jelenik meg a Bing Search-szolgáltatásoknál.</span><span class="sxs-lookup"><span data-stu-id="59c1f-789">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="59c1f-790">A sikertelen fióklétrehozás hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="59c1f-790">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="59c1f-791">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c1f-791">Az.Compute</span></span>
* <span data-ttu-id="59c1f-792">Közelségi elhelyezési csoport szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="59c1f-792">Proximity placement group feature.</span></span>
    - <span data-ttu-id="59c1f-793">A következő új parancsmagok lettek hozzáadva:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="59c1f-793">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="59c1f-794">Az új ProximityPlacementGroupId paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="59c1f-794">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="59c1f-795">A StorageAccountType paraméter hozzá lett adva a New-AzGalleryImageVersion parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="59c1f-795">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="59c1f-796">A New-AzGalleryImageVersion TargetRegion paramétere tartalmazhatja a következőt: StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="59c1f-796">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="59c1f-797">A SkipShutdown kapcsolóparaméter hozzá lett adva a Stop-AzVM és Stop-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-797">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="59c1f-798">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="59c1f-798">Breaking changes</span></span>
    - <span data-ttu-id="59c1f-799">A Set-AzVMBootDiagnostics parancsmag új neve: Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="59c1f-799">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="59c1f-800">Az Export-AzLogAnalyticThrottledRequests parancsmag új neve: Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="59c1f-800">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="59c1f-801">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="59c1f-801">Az.DeploymentManager</span></span>
* <span data-ttu-id="59c1f-802">Az Azure Deployment Manager-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="59c1f-802">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="59c1f-803">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="59c1f-803">Az.Dns</span></span>
* <span data-ttu-id="59c1f-804">Automatikus DNS NameServer-delegálás</span><span class="sxs-lookup"><span data-stu-id="59c1f-804">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="59c1f-805">A DNS-zóna létrehozási parancsmag további opcionális paraméterként elfogadja a szülőzóna nevét.</span><span class="sxs-lookup"><span data-stu-id="59c1f-805">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="59c1f-806">Névkiszolgálói rekordokat ad hozzá a szülőzónában az újonnan létrehozott gyermekzóna számára.</span><span class="sxs-lookup"><span data-stu-id="59c1f-806">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="59c1f-807">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="59c1f-807">Az.FrontDoor</span></span>
* <span data-ttu-id="59c1f-808">Az Azure FrontDoor-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="59c1f-808">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="59c1f-809">A WAF-parancsmagok új neve tartalmazza a „Waf” sztringet</span><span class="sxs-lookup"><span data-stu-id="59c1f-809">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="59c1f-810">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="59c1f-810">Az.HDInsight</span></span>
* <span data-ttu-id="59c1f-811">A következő két parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="59c1f-811">Removed two cmdlets:</span></span>
    - <span data-ttu-id="59c1f-812">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="59c1f-812">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="59c1f-813">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="59c1f-813">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="59c1f-814">Egy új, Set-AzHDInsightGatewayCredential nevű parancsmag lett hozzáadva a Grant-AzHDInsightHttpServicesAccess helyett</span><span class="sxs-lookup"><span data-stu-id="59c1f-814">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="59c1f-815">A Get-AzHDInsightJobOutput parancsmag frissítve lett, hogy különbséget tegyen az olvasói és a HDInsight-operátori szerepkör között:</span><span class="sxs-lookup"><span data-stu-id="59c1f-815">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="59c1f-816">Az olvasói szerepkörrel rendelkező felhasználóknak explicit módon meg kell adniuk a DefaultStorageAccountKey paramétert, ellenkező esetben hiba történik.</span><span class="sxs-lookup"><span data-stu-id="59c1f-816">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="59c1f-817">A HDInsight-operátori szerepkörrel rendelkező felhasználókat ez nem érinti.</span><span class="sxs-lookup"><span data-stu-id="59c1f-817">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="59c1f-818">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="59c1f-818">Az.Monitor</span></span>
* <span data-ttu-id="59c1f-819">Az SQR API (ütemezett lekérdezési szabály) új parancsmagjai</span><span class="sxs-lookup"><span data-stu-id="59c1f-819">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="59c1f-820">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="59c1f-820">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="59c1f-821">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="59c1f-821">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="59c1f-822">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="59c1f-822">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="59c1f-823">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="59c1f-823">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="59c1f-824">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="59c1f-824">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="59c1f-825">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="59c1f-825">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="59c1f-826">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="59c1f-826">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="59c1f-827">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="59c1f-827">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="59c1f-828">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="59c1f-828">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="59c1f-829">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="59c1f-829">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="59c1f-830">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="59c1f-830">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="59c1f-831">[További](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) információk az SQR API-ról</span><span class="sxs-lookup"><span data-stu-id="59c1f-831">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="59c1f-832">A frissített Az.Monitor.md tartalmazza a GenV2 (nem klasszikus) metrikaalapú riasztási szabály parancsmagjait</span><span class="sxs-lookup"><span data-stu-id="59c1f-832">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="59c1f-833">Az.Network</span><span class="sxs-lookup"><span data-stu-id="59c1f-833">Az.Network</span></span>
* <span data-ttu-id="59c1f-834">A NAT-átjáró erőforrás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="59c1f-834">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="59c1f-835">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="59c1f-835">New cmdlets</span></span>
        - <span data-ttu-id="59c1f-836">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="59c1f-836">New-AzNatGateway</span></span>
        - <span data-ttu-id="59c1f-837">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="59c1f-837">Get-AzNatGateway</span></span>
        - <span data-ttu-id="59c1f-838">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="59c1f-838">Set-AzNatGateway</span></span>
        - <span data-ttu-id="59c1f-839">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="59c1f-839">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="59c1f-840">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="59c1f-840">Updated cmdlets</span></span>
        - <span data-ttu-id="59c1f-841">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="59c1f-841">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="59c1f-842">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="59c1f-842">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="59c1f-843">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: Egyéni útvonalak beállítása/eltávolítása a Brooklyn Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="59c1f-843">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="59c1f-844">Frissült a New-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="59c1f-844">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="59c1f-845">Frissült a Set-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="59c1f-845">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="59c1f-846">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="59c1f-846">Az.PolicyInsights</span></span>
* <span data-ttu-id="59c1f-847">A szabályzat-kiértékelési adatok lekérdezésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="59c1f-847">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="59c1f-848">Az -Expand paraméter hozzá lett adva a Get-AzPolicyState parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="59c1f-848">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="59c1f-849">Az -Expand PolicyEvaluationDetails támogatása.</span><span class="sxs-lookup"><span data-stu-id="59c1f-849">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="59c1f-850">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="59c1f-850">Az.RecoveryServices</span></span>
* <span data-ttu-id="59c1f-851">Az előfizetések közötti Azure–Azure Site Recovery átvitel támogatása.</span><span class="sxs-lookup"><span data-stu-id="59c1f-851">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="59c1f-852">Az Azure Site Recovery jövőbeni kompatibilitástörő változásainak jelölése.</span><span class="sxs-lookup"><span data-stu-id="59c1f-852">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="59c1f-853">Ki lett javítva az Azure Site Recovery helyreállítási és műveletterve.</span><span class="sxs-lookup"><span data-stu-id="59c1f-853">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="59c1f-854">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure hálózatleképezés.</span><span class="sxs-lookup"><span data-stu-id="59c1f-854">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="59c1f-855">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure védelemirány felügyelt lemezek esetében.</span><span class="sxs-lookup"><span data-stu-id="59c1f-855">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="59c1f-856">További kisebb javítások.</span><span class="sxs-lookup"><span data-stu-id="59c1f-856">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="59c1f-857">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="59c1f-857">Az.Relay</span></span>
* <span data-ttu-id="59c1f-858">Az elgépelések ki lettek javítva az ügyféloldali üzenetekben</span><span class="sxs-lookup"><span data-stu-id="59c1f-858">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="59c1f-859">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="59c1f-859">Az.ServiceBus</span></span>
* <span data-ttu-id="59c1f-860">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="59c1f-860">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="59c1f-861">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="59c1f-861">Az.Storage</span></span>
* <span data-ttu-id="59c1f-862">A Storage ügyféloldali kódtárának frissítése a 10.0.1-es verziójára (az SDK összes objektuma esetében módosul a névtér a Microsoft.WindowsAzure.Storage. *névtérről a Microsoft.Azure.Storage.* névtérre)</span><span class="sxs-lookup"><span data-stu-id="59c1f-862">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="59c1f-863">Frissítés a Microsoft.Azure.Management.Storage 11.0.0-s verziójára az új API-verzió (2019. 04. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="59c1f-863">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="59c1f-864">A Tárfiók létrehozása parancs esetében az alapértelmezett Storage-fiókaltípus a Storage helyett mostantól a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="59c1f-864">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="59c1f-865">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="59c1f-865">New-AzStorageAccount</span></span>
* <span data-ttu-id="59c1f-866">A Storage-fiók Sku.Name parancsmagkimenete módosul, hogy igazodjon a bemeneti SkuName paraméterhez, egy aláhúzásjel („_”) hozzáadásával – például a StandardLRS a Standard_LRS névre módosul</span><span class="sxs-lookup"><span data-stu-id="59c1f-866">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="59c1f-867">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="59c1f-867">New-AzStorageAccount</span></span>
    - <span data-ttu-id="59c1f-868">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="59c1f-868">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="59c1f-869">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="59c1f-869">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="59c1f-870">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="59c1f-870">Az.Websites</span></span>
* <span data-ttu-id="59c1f-871">Az Altípus tulajdonság mostantól meg lesz adva a Get-AzWebApp által visszaadott PSSite objektumokhoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-871">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="59c1f-872">A Get-AzWebApp\*Metrics és a Get-AzAppServicePlanMetrics megjelölve elavultként</span><span class="sxs-lookup"><span data-stu-id="59c1f-872">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="59c1f-873">1.8.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="59c1f-873">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="59c1f-874">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="59c1f-874">Highlights since the last major release</span></span>
* <span data-ttu-id="59c1f-875">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="59c1f-875">General availability of `Az` module</span></span>
* <span data-ttu-id="59c1f-876">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="59c1f-876">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="59c1f-877">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="59c1f-877">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="59c1f-878">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="59c1f-878">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="59c1f-879">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="59c1f-879">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="59c1f-880">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="59c1f-880">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="59c1f-881">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-881">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="59c1f-882">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="59c1f-882">Az.Accounts</span></span>
* <span data-ttu-id="59c1f-883">Eltávolítás-AzureRm megfelelően törölni a Mac modulok frissítése</span><span class="sxs-lookup"><span data-stu-id="59c1f-883">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="59c1f-884">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="59c1f-884">Az.Batch</span></span>
* <span data-ttu-id="59c1f-885">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="59c1f-885">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="59c1f-886">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="59c1f-886">Az.Cdn</span></span>
* <span data-ttu-id="59c1f-887">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="59c1f-887">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="59c1f-888">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="59c1f-888">Az.CognitiveServices</span></span>
* <span data-ttu-id="59c1f-889">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="59c1f-889">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="59c1f-890">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c1f-890">Az.Compute</span></span>
* <span data-ttu-id="59c1f-891">Az AEM telepítési kapcsolatos problémák megoldásához, ha a lemezek erőforrás-azonosítók kisbetűs resourcegroups volt az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="59c1f-891">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="59c1f-892">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="59c1f-892">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="59c1f-893">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="59c1f-893">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="59c1f-894">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="59c1f-894">Az.DataFactory</span></span>
* <span data-ttu-id="59c1f-895">Adjon hozzá SsisProperties, ha a NodeCount felügyelt integrációs modul nem null értékű.</span><span class="sxs-lookup"><span data-stu-id="59c1f-895">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="59c1f-896">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="59c1f-896">Az.DataLakeStore</span></span>
* <span data-ttu-id="59c1f-897">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="59c1f-897">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="59c1f-898">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="59c1f-898">Az.EventGrid</span></span>
* <span data-ttu-id="59c1f-899">A Súgó szöveg jelzi, hogy erőforrásokat kell létrehozni a create/update eseményt előfizetés parancsmagok használata előtt végpont frissítése.</span><span class="sxs-lookup"><span data-stu-id="59c1f-899">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="59c1f-900">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="59c1f-900">Az.EventHub</span></span>
* <span data-ttu-id="59c1f-901">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="59c1f-901">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="59c1f-902">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="59c1f-902">Az.HDInsight</span></span>
* <span data-ttu-id="59c1f-903">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="59c1f-903">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="59c1f-904">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="59c1f-904">Az.IotHub</span></span>
* <span data-ttu-id="59c1f-905">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="59c1f-905">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="59c1f-906">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="59c1f-906">Az.KeyVault</span></span>
* <span data-ttu-id="59c1f-907">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="59c1f-907">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="59c1f-908">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="59c1f-908">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="59c1f-909">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="59c1f-909">Az.MachineLearning</span></span>
* <span data-ttu-id="59c1f-910">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="59c1f-910">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="59c1f-911">Az.Media</span><span class="sxs-lookup"><span data-stu-id="59c1f-911">Az.Media</span></span>
* <span data-ttu-id="59c1f-912">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="59c1f-912">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="59c1f-913">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="59c1f-913">Az.Monitor</span></span>
  * <span data-ttu-id="59c1f-914">Riasztási szabály (nem klasszikus) GenV2 mérőszám-alapú új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="59c1f-914">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="59c1f-915">Új AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="59c1f-915">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="59c1f-916">Új AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="59c1f-916">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="59c1f-917">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="59c1f-917">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="59c1f-918">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="59c1f-918">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="59c1f-919">Adjon hozzá AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="59c1f-919">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="59c1f-920">Frissített verzió 0.22.0-preview figyelő SDK</span><span class="sxs-lookup"><span data-stu-id="59c1f-920">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="59c1f-921">Az.Network</span><span class="sxs-lookup"><span data-stu-id="59c1f-921">Az.Network</span></span>
* <span data-ttu-id="59c1f-922">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="59c1f-922">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="59c1f-923">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="59c1f-923">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="59c1f-924">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="59c1f-924">Az.NotificationHubs</span></span>
* <span data-ttu-id="59c1f-925">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="59c1f-925">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="59c1f-926">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="59c1f-926">Az.OperationalInsights</span></span>
* <span data-ttu-id="59c1f-927">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="59c1f-927">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="59c1f-928">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="59c1f-928">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="59c1f-929">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="59c1f-929">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="59c1f-930">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="59c1f-930">Az.RecoveryServices</span></span>
* <span data-ttu-id="59c1f-931">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="59c1f-931">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="59c1f-932">Frissített táblázatos formában az SQL azure-beli virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="59c1f-932">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="59c1f-933">A hozzáadott alternatív módszert AzureFileShare hely beolvasása</span><span class="sxs-lookup"><span data-stu-id="59c1f-933">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="59c1f-934">Frissített ScheduleRunDays SchedulePolicy objektumban időzóna szerint</span><span class="sxs-lookup"><span data-stu-id="59c1f-934">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="59c1f-935">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="59c1f-935">Az.RedisCache</span></span>
* <span data-ttu-id="59c1f-936">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="59c1f-936">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="59c1f-937">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c1f-937">Az.Resources</span></span>
* <span data-ttu-id="59c1f-938">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="59c1f-938">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="59c1f-939">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="59c1f-939">Az.Sql</span></span>
* <span data-ttu-id="59c1f-940">Cserélje le a függőségi figyelő SDK közös kód</span><span class="sxs-lookup"><span data-stu-id="59c1f-940">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="59c1f-941">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="59c1f-941">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="59c1f-942">Továbbfejlesztett folyamat, amely több oszlop osztályozási.</span><span class="sxs-lookup"><span data-stu-id="59c1f-942">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="59c1f-943">Termékváltozat tulajdonságok (termékváltozat neve, családi, kapacitás) válasz a Get-AzSqlServerServiceObjective és formátum táblaként alapértelmezés szerint tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="59c1f-943">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="59c1f-944">Lehetővé teszi a Get-AzSqlServerServiceObjective anélkül, hogy a régióban egy már létező kiszolgáló hely alapján.</span><span class="sxs-lookup"><span data-stu-id="59c1f-944">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="59c1f-945">Hozzon létre felügyelt példányt az időzóna-paraméter támogatása.</span><span class="sxs-lookup"><span data-stu-id="59c1f-945">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="59c1f-946">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="59c1f-946">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="59c1f-947">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="59c1f-947">Az.Websites</span></span>
* <span data-ttu-id="59c1f-948">a Set-AzWebApp és a Set-AzWebAppSlot távolítja el a címkék a végrehajtási javítások</span><span class="sxs-lookup"><span data-stu-id="59c1f-948">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="59c1f-949">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="59c1f-949">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="59c1f-950">A webhelyek SDK frissítése.</span><span class="sxs-lookup"><span data-stu-id="59c1f-950">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="59c1f-951">A AdminSiteName tulajdonság PSAppServicePlan eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="59c1f-951">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="59c1f-952">1.7.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="59c1f-952">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="59c1f-953">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="59c1f-953">Highlights since the last major release</span></span>
* <span data-ttu-id="59c1f-954">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="59c1f-954">General availability of `Az` module</span></span>
* <span data-ttu-id="59c1f-955">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="59c1f-955">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="59c1f-956">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="59c1f-956">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="59c1f-957">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="59c1f-957">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="59c1f-958">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="59c1f-958">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="59c1f-959">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="59c1f-959">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="59c1f-960">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-960">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="59c1f-961">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="59c1f-961">Az.Accounts</span></span>
* <span data-ttu-id="59c1f-962">Frissített Add-AzEnvironment és Set-AzEnvironment parancsmag az AzureAnalysisServicesEndpointResourceId paraméter elfogadásához</span><span class="sxs-lookup"><span data-stu-id="59c1f-962">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="59c1f-963">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="59c1f-963">Az.AnalysisServices</span></span>
* <span data-ttu-id="59c1f-964">ServiceClient használata DataPlane-parancsmagokban és az eredeti hitelesítési logika eltávolítása</span><span class="sxs-lookup"><span data-stu-id="59c1f-964">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="59c1f-965">Az Add-AzureASAccount burkolóként való megadása a Connect-AzAccount számára a kompatibilitástörő változás elkerüléséhez</span><span class="sxs-lookup"><span data-stu-id="59c1f-965">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="59c1f-966">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="59c1f-966">Az.Automation</span></span>
* <span data-ttu-id="59c1f-967">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag belefoglalásokat érintő hibája.</span><span class="sxs-lookup"><span data-stu-id="59c1f-967">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="59c1f-968">Az IncludedKbNumber és az IncludedPackageNameMask paraméter mostantól működőképes.</span><span class="sxs-lookup"><span data-stu-id="59c1f-968">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="59c1f-969">Hibajavítás az Azure Automation frissítéskezelési dinamikus csoportja esetében</span><span class="sxs-lookup"><span data-stu-id="59c1f-969">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="59c1f-970">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c1f-970">Az.Compute</span></span>
* <span data-ttu-id="59c1f-971">HyperVGeneration paraméter hozzáadása a New-AzDiskConfig és a New-AzSnapshotConfig parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-971">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="59c1f-972">Virtuális gépek más bérlők katalógus-rendszerképével való létrehozásának engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="59c1f-972">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="59c1f-973">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="59c1f-973">Az.ContainerInstance</span></span>
* <span data-ttu-id="59c1f-974">Ki lett javítva a New-AzContainerGroup üres záró argumentumot hozzáadó -Command paraméterével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="59c1f-974">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="59c1f-975">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="59c1f-975">Az.DataFactory</span></span>
* <span data-ttu-id="59c1f-976">Az ADF .Net SDK verziója 3.0.2-re frissült.</span><span class="sxs-lookup"><span data-stu-id="59c1f-976">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="59c1f-977">A Set-AzDataFactoryV2 parancsmag a RepoConfiguration beállításaihoz tartozó kiegészítő paraméterekkel lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="59c1f-977">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="59c1f-978">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c1f-978">Az.Resources</span></span>
* <span data-ttu-id="59c1f-979">Továbbfejlesztett szolgáltatókezelés a Get-AzResource esetében, -ResourceId vagy -ResourceGroupName, -Name és -ResourceType paraméterek megadásakor</span><span class="sxs-lookup"><span data-stu-id="59c1f-979">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="59c1f-980">Továbbfejlesztett hibakezelés a Test-AzDeployment és a Test-AzResourceGroupDeployment esetében</span><span class="sxs-lookup"><span data-stu-id="59c1f-980">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="59c1f-981">A hibákat nem a telepítés ellenőrzése során kezeli, hanem a parancs kimenetébe foglalja bele</span><span class="sxs-lookup"><span data-stu-id="59c1f-981">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="59c1f-982">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="59c1f-982">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="59c1f-983">-IgnoreDynamicParameters kapcsolóparaméter hozzáadása telepítési parancsmagokhoz a rendszer által feltett kérdések szkriptekben és feladatokban való mellőzéséhez</span><span class="sxs-lookup"><span data-stu-id="59c1f-983">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="59c1f-984">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="59c1f-984">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="59c1f-985">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="59c1f-985">Az.Sql</span></span>
* <span data-ttu-id="59c1f-986">Adatbázisadat-besorolás támogatása.</span><span class="sxs-lookup"><span data-stu-id="59c1f-986">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="59c1f-987">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="59c1f-987">Az.Storage</span></span>
* <span data-ttu-id="59c1f-988">Részletes hibaüzenet megjelenítése Storage-környezet -UseConnectedAccount paraméterrel történő létrehozásakor az Azure-fiókba való bejelentkezés nélkül</span><span class="sxs-lookup"><span data-stu-id="59c1f-988">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="59c1f-989">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="59c1f-989">New-AzStorageContext</span></span>
* <span data-ttu-id="59c1f-990">Adott Storage-fiók Blob service-tulajdonságai kezelésének támogatása Management plane API-val</span><span class="sxs-lookup"><span data-stu-id="59c1f-990">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="59c1f-991">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="59c1f-991">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="59c1f-992">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="59c1f-992">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="59c1f-993">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="59c1f-993">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="59c1f-994">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="59c1f-994">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="59c1f-995">Az -AsJob támogatása blobok és fájlok feltöltéséhez, valamint parancsmagok letöltéséhez</span><span class="sxs-lookup"><span data-stu-id="59c1f-995">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="59c1f-996">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="59c1f-996">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="59c1f-997">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="59c1f-997">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="59c1f-998">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="59c1f-998">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="59c1f-999">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="59c1f-999">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="59c1f-1000">1.6.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="59c1f-1000">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="59c1f-1001">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="59c1f-1001">Highlights since the last major release</span></span>
* <span data-ttu-id="59c1f-1002">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="59c1f-1002">General availability of `Az` module</span></span>
* <span data-ttu-id="59c1f-1003">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="59c1f-1003">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="59c1f-1004">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="59c1f-1004">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="59c1f-1005">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="59c1f-1005">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="59c1f-1006">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="59c1f-1006">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="59c1f-1007">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="59c1f-1007">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="59c1f-1008">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-1008">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="59c1f-1009">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="59c1f-1009">Az.Automation</span></span>
* <span data-ttu-id="59c1f-1010">Az Azure Automation frissítéskezelése módosult, hogy támogassa az alábbi új funkciókat:</span><span class="sxs-lookup"><span data-stu-id="59c1f-1010">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="59c1f-1011">Dinamikus csoportosítás</span><span class="sxs-lookup"><span data-stu-id="59c1f-1011">Dynamic grouping</span></span>
    * <span data-ttu-id="59c1f-1012">Előzetesen és utólagosan futtatandó szkriptek</span><span class="sxs-lookup"><span data-stu-id="59c1f-1012">Pre-Post script</span></span>
    * <span data-ttu-id="59c1f-1013">Újraindítási beállítás</span><span class="sxs-lookup"><span data-stu-id="59c1f-1013">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="59c1f-1014">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c1f-1014">Az.Compute</span></span>
* <span data-ttu-id="59c1f-1015">Ki lett javítva az elérési útvonal feloldásával kapcsolatos hiba a Get-AzVmBootDiagnosticsData esetében</span><span class="sxs-lookup"><span data-stu-id="59c1f-1015">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="59c1f-1016">A Compute ügyfélkódtár frissült a 25.0.0 verzióra</span><span class="sxs-lookup"><span data-stu-id="59c1f-1016">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="59c1f-1017">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="59c1f-1017">Az.KeyVault</span></span>
* <span data-ttu-id="59c1f-1018">Helyettesítő karakterek támogatásának hozzáadása a KeyVault-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-1018">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="59c1f-1019">Az.Network</span><span class="sxs-lookup"><span data-stu-id="59c1f-1019">Az.Network</span></span>
* <span data-ttu-id="59c1f-1020">Az Intelligens veszélyforrás-felderítés támogatásának hozzáadása az Azure Firewallhoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-1020">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="59c1f-1021">Az Application Gateway-tűzfalszabályzat legfelső szintű erőforrása és egyéni szabályok hozzáadva</span><span class="sxs-lookup"><span data-stu-id="59c1f-1021">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="59c1f-1022">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="59c1f-1022">Az.RecoveryServices</span></span>
* <span data-ttu-id="59c1f-1023">A SnapshotRetentionInDays hozzáadása az Azure-beli virtuális gépek szabályzatához az azonnali RP támogatása érdekében</span><span class="sxs-lookup"><span data-stu-id="59c1f-1023">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="59c1f-1024">Folyamat támogatásának hozzáadása a regisztrációtörlési tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-1024">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="59c1f-1025">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c1f-1025">Az.Resources</span></span>
* <span data-ttu-id="59c1f-1026">Helyettesítő karakterek támogatásának hozzáadása a Get-AzResource és Get-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="59c1f-1026">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="59c1f-1027">Az ARM általános hívása esetén használt hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="59c1f-1027">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="59c1f-1028">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="59c1f-1028">Az.Sql</span></span>
* <span data-ttu-id="59c1f-1029">A Fenyegetésészlelés parancsmagjainak paramétere (ExcludeDetectionType) a DetectionType helyett string[] lett, hogy a jövőben is használható legyen az új DetectionType-ok hozzáadásakor, valamint az automatikus kitöltés támogatása érdekében.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1029">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="59c1f-1030">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="59c1f-1030">Az.Storage</span></span>
* <span data-ttu-id="59c1f-1031">Tárfiók felügyeleti szabályzata lekérésének/beállításának/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="59c1f-1031">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="59c1f-1032">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="59c1f-1032">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="59c1f-1033">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="59c1f-1033">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="59c1f-1034">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="59c1f-1034">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="59c1f-1035">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="59c1f-1035">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="59c1f-1036">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="59c1f-1036">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="59c1f-1037">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="59c1f-1037">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="59c1f-1038">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="59c1f-1038">Az.Websites</span></span>
* <span data-ttu-id="59c1f-1039">Ki lett javítva az ARM-sablon azon hibája, amely miatt meghiúsul az összes tárolóhely a New-AzWebApp - IncludeSourceWebAppSlots használatával történő klónozása</span><span class="sxs-lookup"><span data-stu-id="59c1f-1039">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="59c1f-1040">1.5.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="59c1f-1040">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="59c1f-1041">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="59c1f-1041">Az.Accounts</span></span>
* <span data-ttu-id="59c1f-1042">A Register-AzModule parancs hozzáadása az AutoRest által létrehozott parancsmagok támogatásához</span><span class="sxs-lookup"><span data-stu-id="59c1f-1042">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="59c1f-1043">A Connect-AzAccount példáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="59c1f-1043">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="59c1f-1044">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="59c1f-1044">Az.Automation</span></span>
* <span data-ttu-id="59c1f-1045">A bizonyos havi ütemezések lekérésekor jelentkező hiba kijavítva számos Azure Automation-parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="59c1f-1045">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="59c1f-1046">Ki lett javítva a hiba, amely miatt a Get-AzAutomationDscNode csak az első 20 csomópontot adta vissza.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1046">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="59c1f-1047">Most már az összes csomópontot visszaadja</span><span class="sxs-lookup"><span data-stu-id="59c1f-1047">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="59c1f-1048">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="59c1f-1048">Az.Cdn</span></span>
* <span data-ttu-id="59c1f-1049">Új Powershell-parancsmagok hozzáadva az Egyéni tartományi Https engedélyezése/letiltása szolgáltatáshoz, a régiek elavultak</span><span class="sxs-lookup"><span data-stu-id="59c1f-1049">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="59c1f-1050">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c1f-1050">Az.Compute</span></span>
* <span data-ttu-id="59c1f-1051">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-1051">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="59c1f-1052">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="59c1f-1052">Az.DataFactory</span></span>
* <span data-ttu-id="59c1f-1053">Az ADF .Net SDK verziója 3.0.1-re frissült</span><span class="sxs-lookup"><span data-stu-id="59c1f-1053">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="59c1f-1054">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="59c1f-1054">Az.LogicApp</span></span>
* <span data-ttu-id="59c1f-1055">Ki lett javítva a hiba, amely miatt a ListWorkflows csak az eredmények első oldalát kérte le</span><span class="sxs-lookup"><span data-stu-id="59c1f-1055">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="59c1f-1056">Az.Network</span><span class="sxs-lookup"><span data-stu-id="59c1f-1056">Az.Network</span></span>
* <span data-ttu-id="59c1f-1057">Helyettesítő karakterek támogatásának hozzáadása a Network-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-1057">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="59c1f-1058">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="59c1f-1058">Az.RecoveryServices</span></span>
* <span data-ttu-id="59c1f-1059">Azure-beli virtuális gépen futtatott SQL Server támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="59c1f-1059">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="59c1f-1060">SDK-frissítés</span><span class="sxs-lookup"><span data-stu-id="59c1f-1060">SDK Update</span></span>
* <span data-ttu-id="59c1f-1061">VMappContainer ellenőrzés eltávolítva a Get-ProtectableItem parancsmagból</span><span class="sxs-lookup"><span data-stu-id="59c1f-1061">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="59c1f-1062">Name és ServerName paraméterek hozzáadva a Get-ProtectableItem parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-1062">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="59c1f-1063">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c1f-1063">Az.Resources</span></span>
* <span data-ttu-id="59c1f-1064">`-TemplateObject` paraméter hozzáadva az üzembe helyező parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-1064">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="59c1f-1065">További információ: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="59c1f-1065">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="59c1f-1066">Ki lett javítva a hiba, amely akkor jelentkezett, amikor a(z) `Get-AzResource` eredménye át lett irányítva a következőbe: `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="59c1f-1066">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="59c1f-1067">További információ: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="59c1f-1067">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="59c1f-1068">Ki lett javítva a JSON-adattípus módosításával kapcsolatos probléma, amely a(z) `Set-AzResource` futtatásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="59c1f-1068">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="59c1f-1069">További információ: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="59c1f-1069">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="59c1f-1070">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="59c1f-1070">Az.Sql</span></span>
* <span data-ttu-id="59c1f-1071">Az AuditingEndpointsCommunicator frissítése.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1071">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="59c1f-1072">Ki lett javítva az új diagnosztikai beállítások létrehozásakor jelentkező ritka eset viselkedése.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1072">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="59c1f-1073">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="59c1f-1073">Az.Storage</span></span>
* <span data-ttu-id="59c1f-1074">A BlockBlobStorage altípus támogatása a Storage-fiók létrehozásakor      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="59c1f-1074">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="59c1f-1075">1.4.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="59c1f-1075">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="59c1f-1076">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="59c1f-1076">Az.AnalysisServices</span></span>
* <span data-ttu-id="59c1f-1077">Az AddAzureASAccount parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="59c1f-1077">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="59c1f-1078">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="59c1f-1078">Az.Automation</span></span>
* <span data-ttu-id="59c1f-1079">Az Import-AzAutomationDscNodeConfiguration súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="59c1f-1079">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="59c1f-1080">A konfigurációnév-ellenőrzés hozzáadva az Import-AzAutomationDscConfiguration parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-1080">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="59c1f-1081">Továbbfejlesztett hibakezelés az Import-AzAutomationDscConfiguration parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="59c1f-1081">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="59c1f-1082">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="59c1f-1082">Az.CognitiveServices</span></span>
* <span data-ttu-id="59c1f-1083">A CustomSubdomainName új választható paraméterként hozzáadva a New-AzCognitiveServicesAccount parancsmaghoz, amellyel altartomány adható meg az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1083">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="59c1f-1084">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c1f-1084">Az.Compute</span></span>
* <span data-ttu-id="59c1f-1085">Kijavítva az azonosító paraméterkészleteivel kapcsolatos probléma</span><span class="sxs-lookup"><span data-stu-id="59c1f-1085">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="59c1f-1086">Frissült a Get-AzVMExtension parancsmag, hogy az összes telepített bővítményt listázza, ha a Name paraméter nincs megadva</span><span class="sxs-lookup"><span data-stu-id="59c1f-1086">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="59c1f-1087">A Tag és a ResourceId paraméterek hozzáadva az Update-AzImage parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-1087">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="59c1f-1088">A Get-AzVmssVM példányazonosító nélkül, az InstanceView használatával példánynézetben listázni tudja a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1088">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="59c1f-1089">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="59c1f-1089">Az.DataLakeStore</span></span>
* <span data-ttu-id="59c1f-1090">Parancsmagok hozzáadása a törölt ADL-elemek enumerálásához és visszaállításához</span><span class="sxs-lookup"><span data-stu-id="59c1f-1090">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="59c1f-1091">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="59c1f-1091">Az.EventHub</span></span>
* <span data-ttu-id="59c1f-1092">Új SkipEmptyArchives logikai tulajdonság hozzáadva az üres archívumok kihagyásához az Eventhub CaptureDescription osztályában</span><span class="sxs-lookup"><span data-stu-id="59c1f-1092">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="59c1f-1093">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="59c1f-1093">Az.KeyVault</span></span>
* <span data-ttu-id="59c1f-1094">A Set-AzKeyVaultSecret címkézésének kijavítása</span><span class="sxs-lookup"><span data-stu-id="59c1f-1094">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="59c1f-1095">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="59c1f-1095">Az.LogicApp</span></span>
* <span data-ttu-id="59c1f-1096">Hozzáadva az integrációs fiókok alapszintű termékváltozatában</span><span class="sxs-lookup"><span data-stu-id="59c1f-1096">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="59c1f-1097">Hozzáadva az XSLT 2.0-ban, az XSLT 3.0-ban és a Liquid leképezéstípusok esetén</span><span class="sxs-lookup"><span data-stu-id="59c1f-1097">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="59c1f-1098">Új parancsmagok az integrációs fiók szerelvényeihez</span><span class="sxs-lookup"><span data-stu-id="59c1f-1098">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="59c1f-1099">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="59c1f-1099">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="59c1f-1100">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="59c1f-1100">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="59c1f-1101">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="59c1f-1101">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="59c1f-1102">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="59c1f-1102">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="59c1f-1103">Új parancsmagok az integrációs fiók kötegkonfigurációjához</span><span class="sxs-lookup"><span data-stu-id="59c1f-1103">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="59c1f-1104">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="59c1f-1104">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="59c1f-1105">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="59c1f-1105">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="59c1f-1106">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="59c1f-1106">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="59c1f-1107">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="59c1f-1107">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="59c1f-1108">A Logic Apps SDK frissítése a 4.1.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="59c1f-1108">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="59c1f-1109">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="59c1f-1109">Az.Monitor</span></span>
* <span data-ttu-id="59c1f-1110">A Get-AzMetric súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="59c1f-1110">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="59c1f-1111">Az.Network</span><span class="sxs-lookup"><span data-stu-id="59c1f-1111">Az.Network</span></span>
* <span data-ttu-id="59c1f-1112">Az Add-AzApplicationGatewayCustomError súgójában lévő példa frissítése</span><span class="sxs-lookup"><span data-stu-id="59c1f-1112">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="59c1f-1113">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="59c1f-1113">Az.OperationalInsights</span></span>
* <span data-ttu-id="59c1f-1114">Kibővített támogatás a New és a Get ApplicationInsights adatforráshoz.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1114">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="59c1f-1115">Új „ApplicationInsights” altípus hozzáadva az adott munkaterület Get specific és Get all Application Insights-adatforrásainak támogatásához.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1115">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="59c1f-1116">A New-AzOperationalInsightsApplicationInsightsDataSource parancsmag hozzáadva adatforrás létrehozásához a következő Application Insights-erőforrásparaméterekkel: subscriptionId, resourceGroupName és name.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1116">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="59c1f-1117">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c1f-1117">Az.Resources</span></span>
* <span data-ttu-id="59c1f-1118">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="59c1f-1118">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="59c1f-1119">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="59c1f-1119">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="59c1f-1120">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="59c1f-1120">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="59c1f-1121">Ki lett javítva a KeyCredentials ismételt létrehozását megakadályozó hiba</span><span class="sxs-lookup"><span data-stu-id="59c1f-1121">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="59c1f-1122">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="59c1f-1122">Az.Sql</span></span>
* <span data-ttu-id="59c1f-1123">Rugalmas SQL DB-skálázási szint támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="59c1f-1123">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="59c1f-1124">Ki lett javítva az a hiba, hogy a visszaállítási kérésben szereplő szükségtelen tulajdonságok megadása miatt a visszaállítás esetenként meghiúsult</span><span class="sxs-lookup"><span data-stu-id="59c1f-1124">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="59c1f-1125">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="59c1f-1125">Az.Websites</span></span>
* <span data-ttu-id="59c1f-1126">A Get-AzWebAppSlotMetrics példájának javítása</span><span class="sxs-lookup"><span data-stu-id="59c1f-1126">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="59c1f-1127">1.3.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="59c1f-1127">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="59c1f-1128">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="59c1f-1128">Az.Accounts</span></span>
* <span data-ttu-id="59c1f-1129">Frissítés a ClientRuntime legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="59c1f-1129">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="59c1f-1130">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="59c1f-1130">Az.AnalysisServices</span></span>
<span data-ttu-id="59c1f-1131">Az Az.AnalysisServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1131">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="59c1f-1132">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c1f-1132">Az.Compute</span></span>
* <span data-ttu-id="59c1f-1133">AEM-bővítmény: Mostantól az UltraSSD, valamint a P60, P70 és P80 lemezek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1133">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="59c1f-1134">A Set-AzVMBootDiagnostics súgóleírása frissült.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1134">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="59c1f-1135">Az Update-AzImage súgóleírása és példája frissült.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1135">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="59c1f-1136">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="59c1f-1136">Az.RecoveryServices</span></span>
<span data-ttu-id="59c1f-1137">Az Az.RecoveryServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1137">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="59c1f-1138">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c1f-1138">Az.Resources</span></span>
* <span data-ttu-id="59c1f-1139">Az erőforráscsoportok címkézése ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1139">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="59c1f-1140">További információ: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="59c1f-1140">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="59c1f-1141">Ki lett javítva az a hiba, amikor a `Get-AzureRmRoleAssignment` nem vette figyelembe az -ErrorAction paramétert.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1141">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="59c1f-1142">További információ: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="59c1f-1142">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="59c1f-1143">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="59c1f-1143">Az.Sql</span></span>
* <span data-ttu-id="59c1f-1144">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hozzáadva</span><span class="sxs-lookup"><span data-stu-id="59c1f-1144">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="59c1f-1145">Ki lett javítva az a hiba, amikor az Azure-fiókba való bejelentkezés hiánya nullref kivételt eredményezett az SQL-parancsmagok végrehajtásakor.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1145">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="59c1f-1146">A nullref kivétel ki lett javítva a Get-AzSqlCapabilityben.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1146">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="59c1f-1147">1.2.1 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="59c1f-1147">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="59c1f-1148">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="59c1f-1148">Az.Accounts</span></span>
* <span data-ttu-id="59c1f-1149">A hitelesítés megfelelő verziójával rendelkező kiadás</span><span class="sxs-lookup"><span data-stu-id="59c1f-1149">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="59c1f-1150">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="59c1f-1150">Az.AnalysisServices</span></span>
* <span data-ttu-id="59c1f-1151">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="59c1f-1151">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="59c1f-1152">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="59c1f-1152">Az.RecoveryServices</span></span>
* <span data-ttu-id="59c1f-1153">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="59c1f-1153">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="59c1f-1154">1.2.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="59c1f-1154">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="59c1f-1155">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="59c1f-1155">Az.Accounts</span></span>
* <span data-ttu-id="59c1f-1156">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="59c1f-1156">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="59c1f-1157">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1157">Update incorrect online help URLs</span></span>
* <span data-ttu-id="59c1f-1158">Az Uninstall-AzureRm figyelmeztető üzenete hozzáadva a PS Core-ban</span><span class="sxs-lookup"><span data-stu-id="59c1f-1158">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="59c1f-1159">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="59c1f-1159">Az.Aks</span></span>
* <span data-ttu-id="59c1f-1160">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1160">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="59c1f-1161">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="59c1f-1161">Az.Automation</span></span>
* <span data-ttu-id="59c1f-1162">Mostantól támogatottak a Python 2-runbookok.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1162">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="59c1f-1163">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1163">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="59c1f-1164">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="59c1f-1164">Az.Cdn</span></span>
* <span data-ttu-id="59c1f-1165">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1165">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="59c1f-1166">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c1f-1166">Az.Compute</span></span>
* <span data-ttu-id="59c1f-1167">Az Invoke-AzVMReimage parancsmag hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1167">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="59c1f-1168">A TempDisk paraméter hozzá lett adva a Set-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1168">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="59c1f-1169">A New-AzVM figyelmeztető üzenete ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1169">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="59c1f-1170">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="59c1f-1170">Az.ContainerRegistry</span></span>
* <span data-ttu-id="59c1f-1171">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1171">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="59c1f-1172">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="59c1f-1172">Az.DataFactory</span></span>
* <span data-ttu-id="59c1f-1173">Az ADF .Net SDK verziója 3.0.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1173">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="59c1f-1174">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="59c1f-1174">Az.DataLakeStore</span></span>
* <span data-ttu-id="59c1f-1175">Ki lett javítva az ADLS-végponttal kapcsolatos probléma az MSI használatakor.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1175">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="59c1f-1176">További információ: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="59c1f-1176">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="59c1f-1177">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1177">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="59c1f-1178">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="59c1f-1178">Az.IotHub</span></span>
* <span data-ttu-id="59c1f-1179">Az Encoding formátum hozzá lett adva az Add-IotHubRoutingEndpoint parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1179">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="59c1f-1180">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="59c1f-1180">Az.KeyVault</span></span>
* <span data-ttu-id="59c1f-1181">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1181">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="59c1f-1182">Az.Network</span><span class="sxs-lookup"><span data-stu-id="59c1f-1182">Az.Network</span></span>
* <span data-ttu-id="59c1f-1183">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1183">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="59c1f-1184">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c1f-1184">Az.Resources</span></span>
* <span data-ttu-id="59c1f-1185">A helytelen példák ki lettek javítva a New-AzADAppCredential és a New-AzADSpCredential referenciadokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1185">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="59c1f-1186">Ki lett javítva az a hiba, amikor a -TemplateFile paraméter nem lett feloldva az erőforráscsoportokat üzembe helyező parancsmagok végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1186">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="59c1f-1187">Az.Resources: A New-AzureRmPolicyDefinition -Mode alapértelmezett értékének dokumentációja ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1187">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="59c1f-1188">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="59c1f-1188">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="59c1f-1189">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="59c1f-1189">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="59c1f-1190">Ki lett javítva a „PSResourceGroupDeployment” objektum formázásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1190">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="59c1f-1191">További információ: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="59c1f-1191">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="59c1f-1192">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="59c1f-1192">Az.ServiceFabric</span></span>
* <span data-ttu-id="59c1f-1193">Visszaállítás a VMSS-modell tanúsítványának hozzáadásakor bekövetkező kivétel-visszaadás esetén; javított hiba: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1193">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="59c1f-1194">Bizonyos hibaüzenetek ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1194">Fix some error messages.</span></span>
* <span data-ttu-id="59c1f-1195">Ki lett javítva az alapértelmezett ARM-sablonnal való fürtlétrehozás a New-AzServiceFabriCluster esetében, amely nem működött az Az-ba történő migrálással.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1195">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="59c1f-1196">Ki lett javítva a fürt-/alkalmazástanúsítvány létrehozása, így mostantól csak a fürtnek megfelelő virtuálisgép-méretezési csoportokhoz (Virtual Machine Scale Sets) lesznek hozzáadva, a fürtazonosító bővítményben való ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1196">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="59c1f-1197">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="59c1f-1197">Az.SignalR</span></span>
* <span data-ttu-id="59c1f-1198">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1198">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="59c1f-1199">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="59c1f-1199">Az.Sql</span></span>
* <span data-ttu-id="59c1f-1200">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1200">Update incorrect online help URLs</span></span>
* <span data-ttu-id="59c1f-1201">A LicenseType paraméter paraméterleírása frissítve lett a lehetséges értékekkel.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1201">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="59c1f-1202">Ki lett javítva az a hiba, amikor egy felügyelt példány identitásának frissítése nem működött, ha az volt az egyetlen frissített tulajdonság.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1202">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="59c1f-1203">Egyéni rendezések támogatása a felügyelt példányokon</span><span class="sxs-lookup"><span data-stu-id="59c1f-1203">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="59c1f-1204">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="59c1f-1204">Az.Storage</span></span>
* <span data-ttu-id="59c1f-1205">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1205">Update incorrect online help URLs</span></span>
* <span data-ttu-id="59c1f-1206">Részletes hibaüzenet megjelenítése klasszikus naplózás/metrika get/set műveletei esetében a prémium szintű Storage-fiókon, mivel a prémium szintű Storage-fiók nem támogatja a klasszikus naplózást/metrikát.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1206">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="59c1f-1207">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="59c1f-1207">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="59c1f-1208">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="59c1f-1208">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="59c1f-1209">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="59c1f-1209">Az.TrafficManager</span></span>
* <span data-ttu-id="59c1f-1210">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1210">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="59c1f-1211">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="59c1f-1211">Az.Websites</span></span>
* <span data-ttu-id="59c1f-1212">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1212">Update incorrect online help URLs</span></span>
* <span data-ttu-id="59c1f-1213">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól a megfelelő erőforráscsoportba és helyre tölti fel a tanúsítványt, ha az alkalmazás ASE-n üzemel.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1213">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="59c1f-1214">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól nem írja felül a címkéket SSL-tanúsítvány alkalmazáshoz való kötésekor.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1214">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="59c1f-1215">1.1.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="59c1f-1215">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="59c1f-1216">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="59c1f-1216">Az.Accounts</span></span>
* <span data-ttu-id="59c1f-1217">A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-1217">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="59c1f-1218">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c1f-1218">Az.Compute</span></span>
* <span data-ttu-id="59c1f-1219">A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni</span><span class="sxs-lookup"><span data-stu-id="59c1f-1219">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="59c1f-1220">Frissült az azonosító leírása a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="59c1f-1220">Updated the description of ID in help files</span></span>
* <span data-ttu-id="59c1f-1221">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="59c1f-1221">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="59c1f-1222">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="59c1f-1222">Az.DataLakeStore</span></span>
* <span data-ttu-id="59c1f-1223">A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1223">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="59c1f-1224">A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva</span><span class="sxs-lookup"><span data-stu-id="59c1f-1224">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="59c1f-1225">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="59c1f-1225">Az.EventGrid</span></span>
* <span data-ttu-id="59c1f-1226">Frissítve a 2019-01-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1226">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="59c1f-1227">A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához</span><span class="sxs-lookup"><span data-stu-id="59c1f-1227">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="59c1f-1228">New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="59c1f-1228">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="59c1f-1229">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="59c1f-1229">Event Time-To-Live,</span></span>
        - <span data-ttu-id="59c1f-1230">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="59c1f-1230">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="59c1f-1231">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1231">Dead letter endpoint.</span></span>
    - <span data-ttu-id="59c1f-1232">Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="59c1f-1232">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="59c1f-1233">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="59c1f-1233">Event Time-To-Live,</span></span>
        - <span data-ttu-id="59c1f-1234">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="59c1f-1234">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="59c1f-1235">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1235">Dead letter endpoint.</span></span>
* <span data-ttu-id="59c1f-1236">Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1236">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="59c1f-1237">Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1237">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="59c1f-1238">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="59c1f-1238">Az.IotHub</span></span>
* <span data-ttu-id="59c1f-1239">Frissítve az IoT Hub SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="59c1f-1239">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="59c1f-1240">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="59c1f-1240">Az.LogicApp</span></span>
* <span data-ttu-id="59c1f-1241">A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel</span><span class="sxs-lookup"><span data-stu-id="59c1f-1241">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="59c1f-1242">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c1f-1242">Az.Resources</span></span>
* <span data-ttu-id="59c1f-1243">Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="59c1f-1243">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="59c1f-1244">További információ: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="59c1f-1244">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="59c1f-1245">Ki lett javítva a -Custom paraméter kezelése a New/Set-AzPolicyDefinition parancsban</span><span class="sxs-lookup"><span data-stu-id="59c1f-1245">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="59c1f-1246">Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="59c1f-1246">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="59c1f-1247">A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében</span><span class="sxs-lookup"><span data-stu-id="59c1f-1247">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="59c1f-1248">További információ: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="59c1f-1248">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="59c1f-1249">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="59c1f-1249">Az.SignalR</span></span>
* <span data-ttu-id="59c1f-1250">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="59c1f-1250">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="59c1f-1251">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="59c1f-1251">Az.Sql</span></span>
* <span data-ttu-id="59c1f-1252">A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1252">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="59c1f-1253">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="59c1f-1253">Az.Storage</span></span>
* <span data-ttu-id="59c1f-1254">A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva</span><span class="sxs-lookup"><span data-stu-id="59c1f-1254">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="59c1f-1255">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="59c1f-1255">New-AzStorageContext</span></span>
* <span data-ttu-id="59c1f-1256">A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz</span><span class="sxs-lookup"><span data-stu-id="59c1f-1256">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="59c1f-1257">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="59c1f-1257">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="59c1f-1258">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="59c1f-1258">Az.Websites</span></span>
* <span data-ttu-id="59c1f-1259">Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban</span><span class="sxs-lookup"><span data-stu-id="59c1f-1259">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="59c1f-1260">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="59c1f-1260">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="59c1f-1261">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="59c1f-1261">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="59c1f-1262">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="59c1f-1262">General</span></span>

- <span data-ttu-id="59c1f-1263">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="59c1f-1263">General Availability of Az Module</span></span>
- <span data-ttu-id="59c1f-1264">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-1264">Online help for each module</span></span>
- <span data-ttu-id="59c1f-1265">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="59c1f-1265">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="59c1f-1266">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="59c1f-1266">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="59c1f-1267">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="59c1f-1267">Az.Accounts</span></span>
- <span data-ttu-id="59c1f-1268">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="59c1f-1268">Changed from Az.Profile</span></span>
- <span data-ttu-id="59c1f-1269">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-1269">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="59c1f-1270">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="59c1f-1270">Az.ApiManagement</span></span>
- <span data-ttu-id="59c1f-1271">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="59c1f-1271">Fixes for #7002</span></span>
- <span data-ttu-id="59c1f-1272">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="59c1f-1272">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="59c1f-1273">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="59c1f-1273">Az.Batch</span></span>
- <span data-ttu-id="59c1f-1274">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1274">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="59c1f-1275">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1275">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="59c1f-1276">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="59c1f-1276">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="59c1f-1277">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="59c1f-1277">Az.Billing</span></span>
- <span data-ttu-id="59c1f-1278">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1278">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="59c1f-1279">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="59c1f-1279">Az.CognitivServices</span></span>
- <span data-ttu-id="59c1f-1280">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1280">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="59c1f-1281">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1281">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="59c1f-1282">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="59c1f-1282">Az.ContainerInstance</span></span>
- <span data-ttu-id="59c1f-1283">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="59c1f-1283">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="59c1f-1284">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="59c1f-1284">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="59c1f-1285">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="59c1f-1285">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="59c1f-1286">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="59c1f-1286">Az.DataLakeStore</span></span>
- <span data-ttu-id="59c1f-1287">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="59c1f-1287">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="59c1f-1288">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="59c1f-1288">Az.Monitor</span></span>
- <span data-ttu-id="59c1f-1289">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="59c1f-1289">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="59c1f-1290">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="59c1f-1290">Az.KeyVault</span></span>
- <span data-ttu-id="59c1f-1291">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1291">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="59c1f-1292">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="59c1f-1292">Az.MachineLearning</span></span>
- <span data-ttu-id="59c1f-1293">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="59c1f-1293">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="59c1f-1294">Az.Media</span><span class="sxs-lookup"><span data-stu-id="59c1f-1294">Az.Media</span></span>
- <span data-ttu-id="59c1f-1295">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="59c1f-1295">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="59c1f-1296">Az.Network</span><span class="sxs-lookup"><span data-stu-id="59c1f-1296">Az.Network</span></span>
<span data-ttu-id="59c1f-1297">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1297">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="59c1f-1298">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="59c1f-1298">New cmdlets added:</span></span>
        - <span data-ttu-id="59c1f-1299">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="59c1f-1299">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="59c1f-1300">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="59c1f-1300">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="59c1f-1301">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="59c1f-1301">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="59c1f-1302">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="59c1f-1302">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="59c1f-1303">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="59c1f-1303">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="59c1f-1304">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="59c1f-1304">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="59c1f-1305">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="59c1f-1305">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="59c1f-1306">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="59c1f-1306">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="59c1f-1307">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="59c1f-1307">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="59c1f-1308">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="59c1f-1308">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="59c1f-1309">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="59c1f-1309">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="59c1f-1310">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="59c1f-1310">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="59c1f-1311">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="59c1f-1311">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="59c1f-1312">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="59c1f-1312">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="59c1f-1313">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1313">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="59c1f-1314">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="59c1f-1314">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="59c1f-1315">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="59c1f-1315">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="59c1f-1316">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="59c1f-1316">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="59c1f-1317">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="59c1f-1317">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="59c1f-1318">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="59c1f-1318">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="59c1f-1319">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="59c1f-1319">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="59c1f-1320">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="59c1f-1320">Az.OperationalInsights</span></span>
- <span data-ttu-id="59c1f-1321">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="59c1f-1321">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="59c1f-1322">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="59c1f-1322">Az.Profile</span></span>
- <span data-ttu-id="59c1f-1323">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="59c1f-1323">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="59c1f-1324">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="59c1f-1324">Az.RecoveryServices</span></span>
- <span data-ttu-id="59c1f-1325">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="59c1f-1325">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="59c1f-1326">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c1f-1326">Az.Resources</span></span>
- <span data-ttu-id="59c1f-1327">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="59c1f-1327">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="59c1f-1328">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="59c1f-1328">Az.ServiceFabric</span></span>
- <span data-ttu-id="59c1f-1329">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="59c1f-1329">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="59c1f-1330">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="59c1f-1330">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="59c1f-1331">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="59c1f-1331">Az.SIgnalR</span></span>
- <span data-ttu-id="59c1f-1332">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="59c1f-1332">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="59c1f-1333">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="59c1f-1333">Az.Sql</span></span>
- <span data-ttu-id="59c1f-1334">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-1334">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="59c1f-1335">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="59c1f-1335">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="59c1f-1336">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="59c1f-1336">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="59c1f-1337">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="59c1f-1337">Az.Storage</span></span>
- <span data-ttu-id="59c1f-1338">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="59c1f-1338">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="59c1f-1339">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="59c1f-1339">Az.Websites</span></span>
- <span data-ttu-id="59c1f-1340">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="59c1f-1340">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="59c1f-1341">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="59c1f-1341">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="59c1f-1342">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="59c1f-1342">General</span></span>

* <span data-ttu-id="59c1f-1343">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="59c1f-1343">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="59c1f-1344">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c1f-1344">Az.Compute</span></span>

* <span data-ttu-id="59c1f-1345">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1345">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="59c1f-1346">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="59c1f-1346">Az.DataLakeStore</span></span>

* <span data-ttu-id="59c1f-1347">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="59c1f-1347">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="59c1f-1348">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="59c1f-1348">Az.FrontDoor</span></span>

* <span data-ttu-id="59c1f-1349">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="59c1f-1349">Fixed some broken links</span></span>
    - <span data-ttu-id="59c1f-1350">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1350">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="59c1f-1351">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1351">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="59c1f-1352">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="59c1f-1352">Az.RecoveryServices</span></span>

* <span data-ttu-id="59c1f-1353">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1353">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="59c1f-1354">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1354">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="59c1f-1355">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c1f-1355">Az.Resources</span></span>

* <span data-ttu-id="59c1f-1356">[https://github.com/Azure/azure-powershell/issues/7679](https://github.com/Azure/azure-powershell/issues/7679 ) javítása</span><span class="sxs-lookup"><span data-stu-id="59c1f-1356">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="59c1f-1357">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1357">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="59c1f-1358">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="59c1f-1358">Az.Sql</span></span>

* <span data-ttu-id="59c1f-1359">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="59c1f-1359">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="59c1f-1360">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="59c1f-1360">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="59c1f-1361">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1361">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="59c1f-1362">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="59c1f-1362">Az.Storage</span></span>

* <span data-ttu-id="59c1f-1363">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-1363">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="59c1f-1364">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1364">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="59c1f-1365">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="59c1f-1365">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="59c1f-1366">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="59c1f-1366">Support Static Website configuration</span></span>
    - <span data-ttu-id="59c1f-1367">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="59c1f-1367">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="59c1f-1368">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="59c1f-1368">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="59c1f-1369">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="59c1f-1369">Az.Websites</span></span>

* <span data-ttu-id="59c1f-1370">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="59c1f-1370">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="59c1f-1371">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1371">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="59c1f-1372">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1372">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="59c1f-1373">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="59c1f-1373">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="59c1f-1374">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="59c1f-1374">Az.ApiManagement</span></span>
* <span data-ttu-id="59c1f-1375">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1375">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="59c1f-1376">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="59c1f-1376">Az.Automation</span></span>
* <span data-ttu-id="59c1f-1377">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1377">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="59c1f-1378">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1378">Added Update Management cmdlets</span></span>
* <span data-ttu-id="59c1f-1379">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1379">Added Source Control cmdlets</span></span>
* <span data-ttu-id="59c1f-1380">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1380">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="59c1f-1381">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1381">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="59c1f-1382">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c1f-1382">Az.Compute</span></span>
* <span data-ttu-id="59c1f-1383">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1383">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="59c1f-1384">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1384">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="59c1f-1385">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="59c1f-1385">Az.ContainerInstance</span></span>
* <span data-ttu-id="59c1f-1386">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1386">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="59c1f-1387">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="59c1f-1387">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="59c1f-1388">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1388">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="59c1f-1389">Az.Network</span><span class="sxs-lookup"><span data-stu-id="59c1f-1389">Az.Network</span></span>
* <span data-ttu-id="59c1f-1390">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1390">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="59c1f-1391">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1391">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="59c1f-1392">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1392">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="59c1f-1393">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1393">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="59c1f-1394">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="59c1f-1394">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="59c1f-1395">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1395">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="59c1f-1396">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1396">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="59c1f-1397">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="59c1f-1397">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="59c1f-1398">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1398">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="59c1f-1399">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1399">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="59c1f-1400">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="59c1f-1400">Az.Relay</span></span>
* <span data-ttu-id="59c1f-1401">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1401">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="59c1f-1402">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c1f-1402">Az.Resources</span></span>
* <span data-ttu-id="59c1f-1403">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1403">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="59c1f-1404">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1404">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="59c1f-1405">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1405">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="59c1f-1406">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="59c1f-1406">Az.ServiceFabric</span></span>
* <span data-ttu-id="59c1f-1407">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1407">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="59c1f-1408">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="59c1f-1408">Az.Sql</span></span>
* <span data-ttu-id="59c1f-1409">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1409">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="59c1f-1410">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="59c1f-1410">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="59c1f-1411">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="59c1f-1411">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="59c1f-1412">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="59c1f-1412">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="59c1f-1413">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="59c1f-1413">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="59c1f-1414">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="59c1f-1414">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="59c1f-1415">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="59c1f-1415">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="59c1f-1416">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="59c1f-1416">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="59c1f-1417">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="59c1f-1417">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="59c1f-1418">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1418">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="59c1f-1419">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1419">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="59c1f-1420">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1420">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="59c1f-1421">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1421">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="59c1f-1422">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1422">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="59c1f-1423">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1423">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="59c1f-1424">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1424">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="59c1f-1425">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1425">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="59c1f-1426">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="59c1f-1426">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="59c1f-1427">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="59c1f-1427">General</span></span>
* <span data-ttu-id="59c1f-1428">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1428">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="59c1f-1429">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="59c1f-1429">Az.Profile</span></span>
* <span data-ttu-id="59c1f-1430">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1430">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="59c1f-1431">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="59c1f-1431">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="59c1f-1432">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="59c1f-1432">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="59c1f-1433">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="59c1f-1433">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="59c1f-1434">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="59c1f-1434">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="59c1f-1435">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="59c1f-1435">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="59c1f-1436">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="59c1f-1436">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="59c1f-1437">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="59c1f-1437">Az.CognitiveServices</span></span>
* <span data-ttu-id="59c1f-1438">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1438">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="59c1f-1439">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c1f-1439">Az.Compute</span></span>
* <span data-ttu-id="59c1f-1440">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="59c1f-1440">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="59c1f-1441">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="59c1f-1441">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="59c1f-1442">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1442">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="59c1f-1443">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="59c1f-1443">Az.DataLakeStore</span></span>
* <span data-ttu-id="59c1f-1444">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1444">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="59c1f-1445">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1445">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="59c1f-1446">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="59c1f-1446">Az.Insights</span></span>
* <span data-ttu-id="59c1f-1447">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="59c1f-1447">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="59c1f-1448">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="59c1f-1448">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="59c1f-1449">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="59c1f-1449">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="59c1f-1450">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="59c1f-1450">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="59c1f-1451">Az.Network</span><span class="sxs-lookup"><span data-stu-id="59c1f-1451">Az.Network</span></span>
* <span data-ttu-id="59c1f-1452">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="59c1f-1452">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="59c1f-1453">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="59c1f-1453">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="59c1f-1454">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="59c1f-1454">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="59c1f-1455">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="59c1f-1455">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="59c1f-1456">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="59c1f-1456">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="59c1f-1457">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="59c1f-1457">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="59c1f-1458">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="59c1f-1458">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="59c1f-1459">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="59c1f-1459">Az.PolicyInsights</span></span>
* <span data-ttu-id="59c1f-1460">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="59c1f-1460">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="59c1f-1461">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c1f-1461">Az.Resources</span></span>
* <span data-ttu-id="59c1f-1462">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402 ) javítása</span><span class="sxs-lookup"><span data-stu-id="59c1f-1462">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="59c1f-1463">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="59c1f-1463">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="59c1f-1464">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="59c1f-1464">Az.ServiceBus</span></span>
* <span data-ttu-id="59c1f-1465">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1465">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="59c1f-1466">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="59c1f-1466">Az.ServiceFabric</span></span>
* <span data-ttu-id="59c1f-1467">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1467">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="59c1f-1468">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="59c1f-1468">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="59c1f-1469">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="59c1f-1469">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="59c1f-1470">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="59c1f-1470">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="59c1f-1471">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1471">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="59c1f-1472">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="59c1f-1472">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="59c1f-1473">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="59c1f-1473">Az.Profile</span></span>
* <span data-ttu-id="59c1f-1474">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1474">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="59c1f-1475">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1475">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="59c1f-1476">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c1f-1476">Az.Compute</span></span>
* <span data-ttu-id="59c1f-1477">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1477">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="59c1f-1478">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1478">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="59c1f-1479">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="59c1f-1479">Az.DataLakeStore</span></span>
* <span data-ttu-id="59c1f-1480">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="59c1f-1480">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="59c1f-1481">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1481">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="59c1f-1482">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1482">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="59c1f-1483">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1483">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="59c1f-1484">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1484">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="59c1f-1485">Az.Network</span><span class="sxs-lookup"><span data-stu-id="59c1f-1485">Az.Network</span></span>
* <span data-ttu-id="59c1f-1486">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1486">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="59c1f-1487">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1487">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="59c1f-1488">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c1f-1488">Az.Resources</span></span>
* <span data-ttu-id="59c1f-1489">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="59c1f-1489">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="59c1f-1490">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1490">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="59c1f-1491">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="59c1f-1491">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="59c1f-1492">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="59c1f-1492">Azure.Storage</span></span>
* <span data-ttu-id="59c1f-1493">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="59c1f-1493">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="59c1f-1494">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="59c1f-1494">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="59c1f-1495">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="59c1f-1495">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="59c1f-1496">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1496">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="59c1f-1497">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="59c1f-1497">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="59c1f-1498">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="59c1f-1498">Az.CognitiveServices</span></span>
* <span data-ttu-id="59c1f-1499">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1499">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="59c1f-1500">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="59c1f-1500">Az.Compute</span></span>
* <span data-ttu-id="59c1f-1501">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1501">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="59c1f-1502">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1502">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="59c1f-1503">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="59c1f-1503">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="59c1f-1504">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="59c1f-1504">Az.DataFactoryV2</span></span>
* <span data-ttu-id="59c1f-1505">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1505">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="59c1f-1506">Az.Network</span><span class="sxs-lookup"><span data-stu-id="59c1f-1506">Az.Network</span></span>
* <span data-ttu-id="59c1f-1507">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1507">Added NetworkProfile functionality.</span></span> <span data-ttu-id="59c1f-1508">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="59c1f-1508">new cmdlets added</span></span>
    - <span data-ttu-id="59c1f-1509">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="59c1f-1509">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="59c1f-1510">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="59c1f-1510">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="59c1f-1511">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="59c1f-1511">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="59c1f-1512">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="59c1f-1512">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="59c1f-1513">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="59c1f-1513">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="59c1f-1514">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="59c1f-1514">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="59c1f-1515">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="59c1f-1515">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="59c1f-1516">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="59c1f-1516">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="59c1f-1517">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="59c1f-1517">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="59c1f-1518">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="59c1f-1518">Az.RedisCache</span></span>
* <span data-ttu-id="59c1f-1519">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="59c1f-1519">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="59c1f-1520">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-1520">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="59c1f-1521">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="59c1f-1521">Az.Resources</span></span>
* <span data-ttu-id="59c1f-1522">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="59c1f-1522">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="59c1f-1523">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="59c1f-1523">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="59c1f-1524">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="59c1f-1524">Az.Sql</span></span>
* <span data-ttu-id="59c1f-1525">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="59c1f-1525">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="59c1f-1526">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="59c1f-1526">Az.Websites</span></span>
* <span data-ttu-id="59c1f-1527">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="59c1f-1527">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="59c1f-1528">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="59c1f-1528">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="59c1f-1529">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="59c1f-1529">0.2.0 - September 2018</span></span>
 <span data-ttu-id="59c1f-1530">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="59c1f-1530">Initial Release</span></span>
