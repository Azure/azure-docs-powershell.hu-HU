---
title: Az Azure PowerShell kibocsátási megjegyzései
description: Megismerheti az Azure PowerShell-modulok legújabb frissítéseit.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: 8c1369cdedf8848f3c62ca6b6bc4eb3d2d78be95
ms.sourcegitcommit: f9445d1525eac8c165637e1a80fbc92b1ab005c2
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/28/2019
ms.locfileid: "74656830"
---
## <a name="280---october-2019"></a><span data-ttu-id="a8d30-103">2.8.0 – 2019. október</span><span class="sxs-lookup"><span data-stu-id="a8d30-103">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="a8d30-104">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="a8d30-104">General</span></span>
* <span data-ttu-id="a8d30-105">Az.HealthcareApis 1.0.0-s kiadás</span><span class="sxs-lookup"><span data-stu-id="a8d30-105">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a8d30-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a8d30-106">Az.Accounts</span></span>
* <span data-ttu-id="a8d30-107">A telemetria és az URL-címek újraírásának frissítése a létrehozott modulok esetében, a Windows-egységek tesztelésének javítása.</span><span class="sxs-lookup"><span data-stu-id="a8d30-107">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a8d30-108">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a8d30-108">Az.ApiManagement</span></span>
* <span data-ttu-id="a8d30-109">**Set-AzApiManagementApi** – Az API a következőre való frissítésének támogatása: ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="a8d30-109">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="a8d30-110">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="a8d30-110">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a8d30-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a8d30-111">Az.Automation</span></span>
* <span data-ttu-id="a8d30-112">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag a Linux újraindítási beállítási paramétere kapcsán.</span><span class="sxs-lookup"><span data-stu-id="a8d30-112">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="a8d30-113">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a8d30-113">Az.Batch</span></span>
* <span data-ttu-id="a8d30-114">A **Get-AzBatchNodeAgentSku** elavult, így a 2.0.0-ás verziótól a **Get-AzBatchSupportImage** váltja fel.</span><span class="sxs-lookup"><span data-stu-id="a8d30-114">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a8d30-115">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a8d30-115">Az.Compute</span></span>
* <span data-ttu-id="a8d30-116">A Priority, EvictionPolicy és MaxPrice paraméterek hozzáadása a New-AzVM és a New-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-116">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="a8d30-117">Az Add-AzVMAdditionalUnattendContent és az Add-AzVMSshPublicKey parancsmagok figyelmeztető üzenetének és súgójának kijavítása</span><span class="sxs-lookup"><span data-stu-id="a8d30-117">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="a8d30-118">A -skipVmBackup kivétel kijavítása felügyelt lemezekkel rendelkező Linux rendszerű virtuális gépek esetében a Set-AzVMDiskEncryptionExtension kapcsán.</span><span class="sxs-lookup"><span data-stu-id="a8d30-118">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="a8d30-119">A titkosítási beállítások frissítési hibájának kijavítása a Set-AzVMDiskEncryptionExtension kétmenetes forgatókönyvében.</span><span class="sxs-lookup"><span data-stu-id="a8d30-119">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a8d30-120">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a8d30-120">Az.DataFactory</span></span>
* <span data-ttu-id="a8d30-121">CRUD-parancsok lettek hozzáadva az ADF V2-adatfolyamhoz: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow és Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="a8d30-121">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="a8d30-122">Műveleti parancsok lettek hozzáadva az ADF V2-adatfolyam hibakeresési munkamenetéhez: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand és Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="a8d30-122">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="a8d30-123">Az ADF .Net SDK a 4.2.0-ás verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="a8d30-123">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a8d30-124">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a8d30-124">Az.DataLakeStore</span></span>
* <span data-ttu-id="a8d30-125">A fiókérvényesítés javítása, hogy a "-" jelölésű fiókok tartomány nélkül is továbbíthatók legyenek</span><span class="sxs-lookup"><span data-stu-id="a8d30-125">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="a8d30-126">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="a8d30-126">Az.HealthcareApis</span></span>
* <span data-ttu-id="a8d30-127">A PowerShell az 1.0.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="a8d30-127">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="a8d30-128">Az SDK a 1.0.2-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="a8d30-128">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="a8d30-129">Frissítés a tesztekben az új SDK-verzióra való hivatkozáshoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-129">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="a8d30-130">A kimeneti struktúra beágyazottról simítottra frissült.</span><span class="sxs-lookup"><span data-stu-id="a8d30-130">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a8d30-131">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a8d30-131">Az.IotHub</span></span>
* <span data-ttu-id="a8d30-132">Új útválasztási forrás hozzáadása: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="a8d30-132">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="a8d30-133">Kisebb hibajavítás: A Get-AzIothub nem adja vissza a következőt: subscriptionId</span><span class="sxs-lookup"><span data-stu-id="a8d30-133">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="a8d30-134">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a8d30-134">Az.Monitor</span></span>
* <span data-ttu-id="a8d30-135">Új műveleticsoport-fogadók hozzáadva a New-AzActionGroupReceiver parancsmaghoz:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="a8d30-135">New action group receivers added for New-AzActionGroupReceiver:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="a8d30-136">Az általános riasztási séma használata engedélyezve a fogadók számára.</span><span class="sxs-lookup"><span data-stu-id="a8d30-136">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="a8d30-137">Ez nem vonatkozik az SMS, az Azure App leküldéses üzenetei, az ITSM és a Voice fogadóira.</span><span class="sxs-lookup"><span data-stu-id="a8d30-137">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="a8d30-138">A webhookok mostantól az Azure Active Directory-hitelesítés használatát is támogatják.</span><span class="sxs-lookup"><span data-stu-id="a8d30-138">Webhooks now supports Azure active directory authentication.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a8d30-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a8d30-139">Az.Network</span></span>
* <span data-ttu-id="a8d30-140">Új Get-AzAvailableServiceAlias parancsmag hozzáadva, amely a szolgáltatásvégpont-szabályzatokhoz használható aliasok beszerzéséhez hívható meg.</span><span class="sxs-lookup"><span data-stu-id="a8d30-140">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="a8d30-141">Forgalomválasztók hozzáadásának támogatása a virtuális hálózati átjáró kapcsolataihoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-141">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="a8d30-142">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="a8d30-142">New cmdlets added:</span></span>
        - <span data-ttu-id="a8d30-143">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="a8d30-143">New-AzIpsecTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="a8d30-144">Parancsmagok frissítve választható paraméterekkel -TrafficSelectorPolicies   -New-AzVirtualNetworkGatewayConnection   -Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a8d30-144">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzVirtualNetworkGatewayConnection   -Set-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="a8d30-145">Az ESP és AH protokollok támogatása a hálózati biztonsági szabályzati konfigurációkban</span><span class="sxs-lookup"><span data-stu-id="a8d30-145">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="a8d30-146">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="a8d30-146">Updated cmdlets:</span></span>
        - <span data-ttu-id="a8d30-147">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a8d30-147">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="a8d30-148">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a8d30-148">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="a8d30-149">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a8d30-149">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="a8d30-150">Tovább javult a Cortex-parancsmagok kivételeinek kezelése</span><span class="sxs-lookup"><span data-stu-id="a8d30-150">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="a8d30-151">A VirtualNetworkGateways új generációi és termékváltozatai</span><span class="sxs-lookup"><span data-stu-id="a8d30-151">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="a8d30-152">A VirtualNetworkGateways új generációinak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="a8d30-152">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="a8d30-153">A VirtualNetworkGateways új, nagy átviteli sebességű termékváltozatainak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="a8d30-153">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a8d30-154">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a8d30-154">Az.RedisCache</span></span>
* <span data-ttu-id="a8d30-155">Frissült a Set-AzRedisCache referenciadokumentációja, amely most már tartalmazza a -Size paraméter hiányzó értékeit.</span><span class="sxs-lookup"><span data-stu-id="a8d30-155">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="a8d30-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a8d30-156">Az.Sql</span></span>
* <span data-ttu-id="a8d30-157">Az Active Directory-rendszergazda a felügyelt példányon való beállításának támogatása</span><span class="sxs-lookup"><span data-stu-id="a8d30-157">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a8d30-158">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a8d30-158">Az.Storage</span></span>
* <span data-ttu-id="a8d30-159">Az Storage-ügyfélkódtár a 11.1.0-s verzióra frissült.</span><span class="sxs-lookup"><span data-stu-id="a8d30-159">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="a8d30-160">A Management plane API-val rendelkező tárolók listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="a8d30-160">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="a8d30-161">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a8d30-161">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="a8d30-162">A tárfiókok előfizetésből történő listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="a8d30-162">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="a8d30-163">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a8d30-163">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a8d30-164">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a8d30-164">Az.StorageSync</span></span>
* <span data-ttu-id="a8d30-165">A Reset-AzStorageSyncServerCertificate 9810-es hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="a8d30-165">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a8d30-166">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a8d30-166">Az.Websites</span></span>
* <span data-ttu-id="a8d30-167">Egy alkalmazáshoz tartozó ASP Set-AzWebApp általi frissítése sikertelen volt</span><span class="sxs-lookup"><span data-stu-id="a8d30-167">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="a8d30-168">2.7.0 – 2019. szeptember</span><span class="sxs-lookup"><span data-stu-id="a8d30-168">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="a8d30-169">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a8d30-169">Az.ApiManagement</span></span>
* <span data-ttu-id="a8d30-170">Frissítve lett a „-Format” paraméter leírása a „Set-AzApiManagementPolicy” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="a8d30-170">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="a8d30-171">El lettek távolítva az elavult „Update-AzApiManagementDeployment” parancsmag referenciái a referenciadokumentációból.</span><span class="sxs-lookup"><span data-stu-id="a8d30-171">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="a8d30-172">A „Set-AzApiManagement” használható helyette.</span><span class="sxs-lookup"><span data-stu-id="a8d30-172">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a8d30-173">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a8d30-173">Az.Automation</span></span>
* <span data-ttu-id="a8d30-174">Ki lett javítva a „Register-AzAutomationDscNode” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="a8d30-174">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="a8d30-175">Hozzá lett adva az operációs rendszerrel kapcsolatos korlátozások pontosítása a Register-AzAutomationDSCNode parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-175">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="a8d30-176">Ki lett javítva a Start-AzAutomationRunbook parancsmag null értékű hivatkozás okozta kivétele a -Wait paraméter esetén.</span><span class="sxs-lookup"><span data-stu-id="a8d30-176">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a8d30-177">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a8d30-177">Az.Compute</span></span>
* <span data-ttu-id="a8d30-178">Hozzá lett adva az UploadSizeInBytes paraméter a New-AzDiskConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-178">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="a8d30-179">Hozzá lett adva az Incremental paraméter a New-AzSnapshotConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-179">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="a8d30-180">Alacsony prioritású virtuálisgép-funkció hozzáadása:</span><span class="sxs-lookup"><span data-stu-id="a8d30-180">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="a8d30-181">Hozzá lett adva a MaxPrice, az EvictionPolicy és a Priority paraméter a New-AzVMConfig parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="a8d30-181">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="a8d30-182">Hozzá lett adva a MaxPrice paraméter a New-AzVmssConfig, az Update-AzVM és az Update-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="a8d30-182">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="a8d30-183">Ki lett javítva a Get-AzAvailabilitySet parancsmag virtuálisgép-hivatkozással kapcsolatos hibája, amely miatt a parancsmag az előfizetésben található összes rendelkezésreállási csoportot listázta.</span><span class="sxs-lookup"><span data-stu-id="a8d30-183">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="a8d30-184">Ki lett javítva a Get-AzRemoteDesktopFile parancsmag esetében jelentkező null kivétel.</span><span class="sxs-lookup"><span data-stu-id="a8d30-184">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="a8d30-185">Ki lett javítva virtuális merevlemezek Seek metódusa a végrelatív pozíció esetében.</span><span class="sxs-lookup"><span data-stu-id="a8d30-185">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="a8d30-186">Ki lett javítva az UltraSSD hibája a New-AzVM és az Update-AzVM parancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="a8d30-186">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a8d30-187">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a8d30-187">Az.DataFactory</span></span>
* <span data-ttu-id="a8d30-188">Hozzá lett adva 3 új parancs (az Add-AzDataFactoryV2TriggerSubscription, a Remove-AzDataFactoryV2TriggerSubscription és a Get-AzDataFactoryV2TriggerSubscriptionStatus) az ADF V2-höz</span><span class="sxs-lookup"><span data-stu-id="a8d30-188">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="a8d30-189">Az ADF .Net SDK a 4.1.3-as verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="a8d30-189">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="a8d30-190">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a8d30-190">Az.HDInsight</span></span>
* <span data-ttu-id="a8d30-191">Kompatibilitástörő változások a meghívással kapcsolatban</span><span class="sxs-lookup"><span data-stu-id="a8d30-191">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a8d30-192">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a8d30-192">Az.IotHub</span></span>
* <span data-ttu-id="a8d30-193">Hozzá lett adva az IoTHubok földrajzilag párosított vészhelyreállítási régiójába történő feladatátvétel meghívásának támogatása.</span><span class="sxs-lookup"><span data-stu-id="a8d30-193">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="a8d30-194">Hozzá lett adva az IoTHubok üzenetbővítés-kezelésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="a8d30-194">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="a8d30-195">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="a8d30-195">New cmdlets are:</span></span>
    - <span data-ttu-id="a8d30-196">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="a8d30-196">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="a8d30-197">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="a8d30-197">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="a8d30-198">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="a8d30-198">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="a8d30-199">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="a8d30-199">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a8d30-200">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a8d30-200">Az.Monitor</span></span>
* <span data-ttu-id="a8d30-201">A legújabb Monitor SDK-ra mutat, azaz a 0.24.1-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="a8d30-201">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="a8d30-202">Nem kompatibilitástörő változásokkal bővíti a Metrics parancsmagokat, így az egységek számbavétele számos új értéket támogat.</span><span class="sxs-lookup"><span data-stu-id="a8d30-202">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="a8d30-203">Ezek írásvédett parancsmagok, ezért a parancsmagok bemenetében nem történik változás.</span><span class="sxs-lookup"><span data-stu-id="a8d30-203">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="a8d30-204">Az **ActionGroups**-kérések api-version értéke mostantól **2019-06-01**, korábban **2018-03-01** volt.</span><span class="sxs-lookup"><span data-stu-id="a8d30-204">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="a8d30-205">A forgatókönyvtesztek frissültek, így igazodnak a változáshoz.</span><span class="sxs-lookup"><span data-stu-id="a8d30-205">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="a8d30-206">Az **EmailReceiver** és a **WebhookReceiver** osztályok konstruktoraihoz hozzá lett adva egy új kötelező argumentum, a **useCommonAlertSchema** nevű logikai érték.</span><span class="sxs-lookup"><span data-stu-id="a8d30-206">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="a8d30-207">A kompatibilitástörő változás parancsmagok elől való elrejtése érdekében a rögzített érték jelenleg a **false** (hamis).</span><span class="sxs-lookup"><span data-stu-id="a8d30-207">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="a8d30-208">**MEGJEGYZÉS**: Ez egy átmeneti módosítás, amelyet a Riasztások csapatnak érvényesítenie kell.</span><span class="sxs-lookup"><span data-stu-id="a8d30-208">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="a8d30-209">A **Source** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="a8d30-209">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="a8d30-210">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="a8d30-210">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="a8d30-211">Az **AlertingAction** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="a8d30-211">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="a8d30-212">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="a8d30-212">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="a8d30-213">A dinamikus küszöbérték kritériumainak támogatása a 2-es verziójú metrikariasztás esetében</span><span class="sxs-lookup"><span data-stu-id="a8d30-213">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="a8d30-214">New-AzMetricAlertRuleV2Criteria: mostantól a dinamikus küszöbértékek kritériumait is létrehozza</span><span class="sxs-lookup"><span data-stu-id="a8d30-214">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="a8d30-215">Add-AzMetricAlertRuleV2: mostantól a dinamikus küszöbértékek kritériumait is elfogadja</span><span class="sxs-lookup"><span data-stu-id="a8d30-215">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="a8d30-216">Az ütemezett lekérdezési szabályok parancsmagjainak (SQR) fejlesztései</span><span class="sxs-lookup"><span data-stu-id="a8d30-216">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="a8d30-217">A parancsmagok a „Location” paraméter mindkét formátumát elfogadják: a helyet (például eastus) és a hely megjelenített nevét is (például USA keleti régiója)</span><span class="sxs-lookup"><span data-stu-id="a8d30-217">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="a8d30-218">Megfelelően ábrázolva lett az „Enabled” paraméter a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="a8d30-218">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="a8d30-219">Példák lettek hozzáadva az „ActionGroup” opcionális paraméterhez</span><span class="sxs-lookup"><span data-stu-id="a8d30-219">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="a8d30-220">Általánosan továbbfejlesztett súgófájlok</span><span class="sxs-lookup"><span data-stu-id="a8d30-220">Overall improved help files</span></span>
* <span data-ttu-id="a8d30-221">Ki lett javítva a „Set-AzActionRule” hatókörtípusának meghatározásával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="a8d30-221">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a8d30-222">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a8d30-222">Az.Network</span></span>
* <span data-ttu-id="a8d30-223">Ki lett javítva a „New-AzApplicationGateway” referenciadokumentációjában található helytelen példa</span><span class="sxs-lookup"><span data-stu-id="a8d30-223">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="a8d30-224">Hozzá lett adva egy csomagrögzítés összes tulajdonságának lekérésével kapcsolatos megjegyzés a „Get-AzNetworkWatcherPacketCapture” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="a8d30-224">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="a8d30-225">Ki lett javítva a „Test-AzNetworkWatcherIPFlow” referenciadokumentációjában található példa a hálózati adapterek megfelelő számbavétele érdekében</span><span class="sxs-lookup"><span data-stu-id="a8d30-225">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="a8d30-226">Tovább lett fejlesztve a felhőkivétel-elemzés az esetleges további részletek megjelenítése érdekében</span><span class="sxs-lookup"><span data-stu-id="a8d30-226">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="a8d30-227">Tovább lett fejlesztve a felhőkivétel-elemzés az SDK-kivételek további típusainak kezelése érdekében</span><span class="sxs-lookup"><span data-stu-id="a8d30-227">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="a8d30-228">Ki lett javítva a biztonságiszabály-modellek helytelen leképezése</span><span class="sxs-lookup"><span data-stu-id="a8d30-228">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="a8d30-229">Hozzá lettek adva a privát IP-cím funkcióval kapcsolatos tulajdonságok a hálózati adapterhez</span><span class="sxs-lookup"><span data-stu-id="a8d30-229">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="a8d30-230">Hozzá lett adva a „PrivateEndpoint” tulajdonság PSResourceId típusúként a PSNetworkInterface osztályhoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-230">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="a8d30-231">Hozzá lett adva a „PrivateLinkConnectionProperties” tulajdonság PSIpConfigurationConnectivityInformation típusúként a PSNetworkInterfaceIPConfiguration osztályhoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-231">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="a8d30-232">Hozzá lett adva a PSIpConfigurationConnectivityInformation nevű új modellosztály</span><span class="sxs-lookup"><span data-stu-id="a8d30-232">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="a8d30-233">Hozzá lett adva az új ApplicationRuleProtocolType „mssql” az Azure Firewall-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-233">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="a8d30-234">MultiLink-támogatás a Virtuális WAN-ben</span><span class="sxs-lookup"><span data-stu-id="a8d30-234">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="a8d30-235">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a8d30-235">New cmdlets</span></span>
        - <span data-ttu-id="a8d30-236">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="a8d30-236">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="a8d30-237">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="a8d30-237">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="a8d30-238">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="a8d30-238">Updated cmdlet:</span></span>
        - <span data-ttu-id="a8d30-239">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="a8d30-239">New-VpnSite</span></span>
        - <span data-ttu-id="a8d30-240">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="a8d30-240">Update-VpnSite</span></span>
        - <span data-ttu-id="a8d30-241">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="a8d30-241">New-VpnConnection</span></span>
        - <span data-ttu-id="a8d30-242">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="a8d30-242">Update-VpnConnection</span></span>
* <span data-ttu-id="a8d30-243">Ki lettek javítva bizonyos PowerShell-példák dokumentumai, hogy az AzureRM-parancsmagok helyett az Az-parancsmagokat használják</span><span class="sxs-lookup"><span data-stu-id="a8d30-243">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a8d30-244">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a8d30-244">Az.RecoveryServices</span></span>
* <span data-ttu-id="a8d30-245">Frissítve lett az AzureVMpolicy objektum a ProtectedItemsCount attribútummal</span><span class="sxs-lookup"><span data-stu-id="a8d30-245">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="a8d30-246">Tesztek lettek hozzáadva a virtuális gép szabályzatához és az eredeti Storage-fiók visszaállításához</span><span class="sxs-lookup"><span data-stu-id="a8d30-246">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="a8d30-247">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a8d30-247">Az.Resources</span></span>
* <span data-ttu-id="a8d30-248">Ki lett javítva a hiba, amely miatt a New-AzRoleAssignment parancsot nem lehetett meghívni a Scope paraméter nélkül.</span><span class="sxs-lookup"><span data-stu-id="a8d30-248">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a8d30-249">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a8d30-249">Az.ServiceFabric</span></span>
* <span data-ttu-id="a8d30-250">Ki lett javítva az „Update-AzServiceFabricReliability” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="a8d30-250">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="a8d30-251">Új parancsmagok lettek hozzáadva az alkalmazás és a szolgáltatások felügyeletéhez:</span><span class="sxs-lookup"><span data-stu-id="a8d30-251">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="a8d30-252">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a8d30-252">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="a8d30-253">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="a8d30-253">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="a8d30-254">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a8d30-254">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="a8d30-255">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="a8d30-255">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="a8d30-256">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a8d30-256">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="a8d30-257">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a8d30-257">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="a8d30-258">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="a8d30-258">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="a8d30-259">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a8d30-259">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="a8d30-260">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="a8d30-260">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="a8d30-261">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a8d30-261">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="a8d30-262">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="a8d30-262">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="a8d30-263">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a8d30-263">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="a8d30-264">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="a8d30-264">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="a8d30-265">A Service Fabric SDK az 1.2.0-s verzióra frissült, amely a Service Fabric erőforrás-szolgáltató 2019-03-01 api-versionjét használja.</span><span class="sxs-lookup"><span data-stu-id="a8d30-265">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a8d30-266">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a8d30-266">Az.SignalR</span></span>
* <span data-ttu-id="a8d30-267">Hozzá lettek adva az Update, Restart, CheckNameAvailability és GetUsage parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a8d30-267">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="a8d30-268">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a8d30-268">Az.Sql</span></span>
* <span data-ttu-id="a8d30-269">Frissítve lett a „Get-AzSqlElasticPool” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="a8d30-269">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="a8d30-270">Hozzá lett adva egy rugalmas készlet létrehozását bemutató virtuálismag-példa (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="a8d30-270">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="a8d30-271">El lett távolítva az EmailAddresses érvényesítése és annak ellenőrzése, hogy az EmailAdmins értéke hamis-e abban az esetben, ha az EmailAddresses üres a Set-AzSqlServerAdvancedThreatProtectionPolicy és a Set-AzSqlDatabaseAdvancedThreatProtectionPolicy parancsmagban</span><span class="sxs-lookup"><span data-stu-id="a8d30-271">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="a8d30-272">Engedélyezve lettek a kiszolgáló-/adatbázis-naplózási beállítások abban az esetben, ha több olyan diagnosztikai beállítás létezik, amelyek engedélyezik a naplózási kategóriát.</span><span class="sxs-lookup"><span data-stu-id="a8d30-272">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="a8d30-273">Ki lett javítva az e-mail-címek ellenőrzése több, SQL-sebezhetőségi felméréshez használt parancsmagban (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting és Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="a8d30-273">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a8d30-274">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a8d30-274">Az.Storage</span></span>
* <span data-ttu-id="a8d30-275">Frissítve lett a „Get-AzStorageAccountKey” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="a8d30-275">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="a8d30-276">A forrásfájl SMB-tulajdonságai (fájlattribútumok, fájl létrehozásának ideje, fájl utolsó írásának ideje) célfájlban történő megtartásának támogatása az Azure File-beli feltöltés/letöltés esetében</span><span class="sxs-lookup"><span data-stu-id="a8d30-276">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="a8d30-277">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a8d30-277">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="a8d30-278">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a8d30-278">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="a8d30-279">Ki lett javítva a tulajdonság-/metaadathibával meghiúsuló blokkblobfeltöltés a tárolóképes ImmutabilityPolicy esetében.</span><span class="sxs-lookup"><span data-stu-id="a8d30-279">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="a8d30-280">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a8d30-280">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="a8d30-281">Az Azure File-megosztások Management plane API-val történő kezelésének támogatása</span><span class="sxs-lookup"><span data-stu-id="a8d30-281">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="a8d30-282">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a8d30-282">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="a8d30-283">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a8d30-283">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="a8d30-284">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a8d30-284">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="a8d30-285">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a8d30-285">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a8d30-286">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a8d30-286">Az.Websites</span></span>
* <span data-ttu-id="a8d30-287">Ki lett javítva az a probléma, amely miatt a webalkalmazás Címkéi törölve lettek az alkalmazás új ASP-be történő migrálásakor</span><span class="sxs-lookup"><span data-stu-id="a8d30-287">Fixing issue where webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="a8d30-288">Ki lett javítva a Publish-AzureWebapp parancs a Linux és Windows rendszeren történő működés érdekében</span><span class="sxs-lookup"><span data-stu-id="a8d30-288">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="a8d30-289">Frissítve lett a „Get-AzWebAppPublishingProfile” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="a8d30-289">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="a8d30-290">2.6.0 – 2019. augusztus</span><span class="sxs-lookup"><span data-stu-id="a8d30-290">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="a8d30-291">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="a8d30-291">General</span></span>
* <span data-ttu-id="a8d30-292">Különféle elgépelések kijavítva több modulban</span><span class="sxs-lookup"><span data-stu-id="a8d30-292">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a8d30-293">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a8d30-293">Az.Accounts</span></span>
* <span data-ttu-id="a8d30-294">Felhasználó által hozzárendelt MSI támogatása az Azure Functions-hitelesítésben (#9479)</span><span class="sxs-lookup"><span data-stu-id="a8d30-294">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="a8d30-295">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a8d30-295">Az.Aks</span></span>
* <span data-ttu-id="a8d30-296">A Get-AzAks kimenetével kapcsolatos probléma ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="a8d30-296">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="a8d30-297">További információ: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="a8d30-297">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a8d30-298">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a8d30-298">Az.ApiManagement</span></span>
* <span data-ttu-id="a8d30-299">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="a8d30-299">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="a8d30-300">Frissült a .net nuget verziója, amely nem kényszeríti ki a productId, az apiId, a groupId és a userId korlátozásait</span><span class="sxs-lookup"><span data-stu-id="a8d30-300">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="a8d30-301">**Get-AzApiManagementProduct** – A termékek API-val történő lekérdezése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="a8d30-301">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="a8d30-302">**New-AzApiManagementApiRevision** – Ki lett javítva az a probléma, amely miatt az ApiRevisionDescription nem lett beállítva az új API-változat létrehozásakor https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="a8d30-302">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="a8d30-303">Ki lett javítva a PsApiManagementOAuth2AuthrozationServer modell elírása PsApiManagementOAuth2AuthorizationServer értékre</span><span class="sxs-lookup"><span data-stu-id="a8d30-303">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a8d30-304">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a8d30-304">Az.Batch</span></span>
* <span data-ttu-id="a8d30-305">Ki lett javítva a súgóüzenetben és a dokumentációban található elgépelés, nagy kezdőbetűs Windows értékre</span><span class="sxs-lookup"><span data-stu-id="a8d30-305">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a8d30-306">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a8d30-306">Az.Cdn</span></span>
* <span data-ttu-id="a8d30-307">Ki lett javítva egy elgépelés CDN modulátalakító segédben</span><span class="sxs-lookup"><span data-stu-id="a8d30-307">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a8d30-308">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a8d30-308">Az.Compute</span></span>
* <span data-ttu-id="a8d30-309">Új VmssId a New-AzVMConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-309">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="a8d30-310">Új TerminateScheduledEvents és a TerminateScheduledEventNotBeforeTimeoutInMinutes paraméterek a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-310">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="a8d30-311">Új HyperVGeneration tulajdonság a VM-rendszerképobjektumhoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-311">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="a8d30-312">Új Host és HostGroup jellemzők</span><span class="sxs-lookup"><span data-stu-id="a8d30-312">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="a8d30-313">Új parancsmagok:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="a8d30-313">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="a8d30-314">Új HostId paraméter a New-AzVMConfig és a New-AzVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-314">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="a8d30-315">Az Invoke-AzVMRunCommand dokumentációjában található példa frissítve lett a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="a8d30-315">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="a8d30-316">A -VolumeType leírása frissítve lett a set-AzVMDiskEncryptionExtension és a set-AzVmssDiskEncryptionExtension referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="a8d30-316">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a8d30-317">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a8d30-317">Az.DataFactory</span></span>
* <span data-ttu-id="a8d30-318">A New-AzDataFactoryEncryptValue dokumentációjában a Windows szó nagy kezdőbetűsre lett javítva</span><span class="sxs-lookup"><span data-stu-id="a8d30-318">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="a8d30-319">Az ADF .Net SDK a 4.1.2-es verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="a8d30-319">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="a8d30-320">Új DataProxyIntegrationRuntimeName, DataProxyIntegrationRuntimeName és DataProxyStagingPath paraméterek lettek hozzáadva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz, lehetővé téve a helyi integrációs modul SSIS integrációs modul proxyjaként való beállítását</span><span class="sxs-lookup"><span data-stu-id="a8d30-320">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="a8d30-321">Frissítve lett a PSTriggerRun, hogy megjelenítse az aktivált folyamatokat, üzeneteket és tulajdonságokat, illetve a PSActivityRun, hogy megjelenítse a tevékenységtípust</span><span class="sxs-lookup"><span data-stu-id="a8d30-321">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a8d30-322">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a8d30-322">Az.DataLakeStore</span></span>
* <span data-ttu-id="a8d30-323">Ki lett javítva a Get-DataLakeStoreDeletedItem lefagyása hibák vagy távoli kivételek esetén.</span><span class="sxs-lookup"><span data-stu-id="a8d30-323">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a8d30-324">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a8d30-324">Az.EventHub</span></span>
* <span data-ttu-id="a8d30-325">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNteworkRule paraméter a Set-AzEventHubNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="a8d30-325">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="a8d30-326">Ki lett javítva a 9558-as számú hiba: Set-AzEventHubNamespace a PUT helyett a PATCH kérést használta</span><span class="sxs-lookup"><span data-stu-id="a8d30-326">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="a8d30-327">új EnableKafka paraméter a Set-AzEventHubNamespace parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-327">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="a8d30-328">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="a8d30-328">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="a8d30-329">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a8d30-329">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="a8d30-330">Ki lett javítva egy elgépelés a dokumentációban, ahol az Azure csupa kisbetűvel szerepelt</span><span class="sxs-lookup"><span data-stu-id="a8d30-330">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a8d30-331">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a8d30-331">Az.Monitor</span></span>
* <span data-ttu-id="a8d30-332">Hibás paraméternév lett kijavítva a súgódokumentációban</span><span class="sxs-lookup"><span data-stu-id="a8d30-332">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a8d30-333">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a8d30-333">Az.Network</span></span>
* <span data-ttu-id="a8d30-334">Frissítve lett a New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a8d30-334">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="a8d30-335">A PublicIpAddress elavult, mert a kiszolgálóoldalon nem használatos.</span><span class="sxs-lookup"><span data-stu-id="a8d30-335">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="a8d30-336">Hozzá lett adva egy opcionális Primary paraméter, amely azt jelzi, hogy a jelenlegi IP-konfiguráció elsődleges-e.</span><span class="sxs-lookup"><span data-stu-id="a8d30-336">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="a8d30-337">Javítva lett az SDK kérelemhiba-kivételének kezelése – kijavítja azt a problémát, amely miatt az SDK-kivételek kezelése korábban nem volt megfelelő, és a fontos hibarészletek nem jelentek meg</span><span class="sxs-lookup"><span data-stu-id="a8d30-337">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="a8d30-338">Be lett állítva, hogy az IPv6 IP-előtag ellenőrzési logikája ellenőrizze az IPv6-előtag hosszának megfelelőségét.</span><span class="sxs-lookup"><span data-stu-id="a8d30-338">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="a8d30-339">Frissült a Get-AzVirtualNetworkSubnetConfig: Új paraméterkészlet lett hozzáadva az alhálózat erőforrás-azonosítója szerinti lekéréshez.</span><span class="sxs-lookup"><span data-stu-id="a8d30-339">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="a8d30-340">Frissült az AzNetworkServiceTag Location paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="a8d30-340">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a8d30-341">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a8d30-341">Az.OperationalInsights</span></span>
* <span data-ttu-id="a8d30-342">Frissült a New-AzOperationalInsightsLinuxSyslogDataSource dokumentációja</span><span class="sxs-lookup"><span data-stu-id="a8d30-342">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="a8d30-343">Példa hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a8d30-343">Added example</span></span>
    - <span data-ttu-id="a8d30-344">A -Name paraméter leírása frissítve lett</span><span class="sxs-lookup"><span data-stu-id="a8d30-344">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="a8d30-345">Új példa lett hozzáadva a New-AzOperationalInsightsWindowsEventDataSource parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-345">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="a8d30-346">Módosult a New-AzOperationalInsightsWindowsEventDataSource -Name paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="a8d30-346">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a8d30-347">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a8d30-347">Az.RecoveryServices</span></span>
* <span data-ttu-id="a8d30-348">Frissült a Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="a8d30-348">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="a8d30-349">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a8d30-349">Az.Resources</span></span>
* <span data-ttu-id="a8d30-350">A Microsoft.Resource mostantól támogatja a 2019-05-10-es új api-verziót</span><span class="sxs-lookup"><span data-stu-id="a8d30-350">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="a8d30-351">Mostantól támogatott a copy.count = 0 a változók, erőforrások és tulajdonságok esetében</span><span class="sxs-lookup"><span data-stu-id="a8d30-351">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="a8d30-352">A condition = false vagy copy.count = 0 tulajdonságú erőforrások teljes módban törölve lesznek</span><span class="sxs-lookup"><span data-stu-id="a8d30-352">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="a8d30-353">A súgódokumentációhoz hozzá lett adva egy példa a szabályzatok előfizetési szinten történő hozzárendeléséhez</span><span class="sxs-lookup"><span data-stu-id="a8d30-353">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a8d30-354">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a8d30-354">Az.ServiceBus</span></span>
* <span data-ttu-id="a8d30-355">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNetworkRule paraméter a Set-AzServiceBusNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="a8d30-355">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="a8d30-356">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="a8d30-356">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="a8d30-357">Új Test-AzServiceBusNameAvailability parancs lett hozzáadva annak ellenőrzésére, hogy az üzenetsor és a témakör neve elérhető-e</span><span class="sxs-lookup"><span data-stu-id="a8d30-357">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="a8d30-358">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a8d30-358">Az.ServiceFabric</span></span>
* <span data-ttu-id="a8d30-359">Ki lettek javítva a csomóponttípus-hozzáadási parancsmag hibái:</span><span class="sxs-lookup"><span data-stu-id="a8d30-359">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="a8d30-360">NullReferenceException hiba történt, ha az erőforráscsoport más, a Service Fabric-fürthöz nem kapcsolódó VMSS-sel rendelkezett.</span><span class="sxs-lookup"><span data-stu-id="a8d30-360">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="a8d30-361">Kijavított hiba: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="a8d30-361">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="a8d30-362">Ki lett javítva egy hiba, amely miatt a parancsmag futása meghiúsult, ha a virtualNetwork a fürttől eltérő erőforráscsoportban volt.</span><span class="sxs-lookup"><span data-stu-id="a8d30-362">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="a8d30-363">kijavított hiba: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="a8d30-363">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="a8d30-364">Az Add-AzServiceFabricApplicationCertificate parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="a8d30-364">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="a8d30-365">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a8d30-365">Az.Sql</span></span>
* <span data-ttu-id="a8d30-366">Frissült a régi naplózási parancsmagok dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="a8d30-366">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a8d30-367">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a8d30-367">Az.Storage</span></span>
* <span data-ttu-id="a8d30-368">A Get/Close-AzStorageFileHandle súgója további parancsmagpélda-forgatókönyvek hozzáadásával és a paraméterek leírásának frissítésével változott</span><span class="sxs-lookup"><span data-stu-id="a8d30-368">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="a8d30-369">A StandardBlobTier mostantól támogatott a blobfeltöltési és -másolási műveletekhez</span><span class="sxs-lookup"><span data-stu-id="a8d30-369">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="a8d30-370">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a8d30-370">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="a8d30-371">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a8d30-371">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="a8d30-372">A rehidratálás prioritása mostantól támogatott a blobmásoláskor</span><span class="sxs-lookup"><span data-stu-id="a8d30-372">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="a8d30-373">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a8d30-373">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a8d30-374">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a8d30-374">Az.Websites</span></span>
* <span data-ttu-id="a8d30-375">Magyarázat hozzáadva a Set-AzWebApp és a Set-AzWebAppSlot parancsmagok -AppSettings paraméteréhez</span><span class="sxs-lookup"><span data-stu-id="a8d30-375">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="a8d30-376">2.5.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="a8d30-376">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a8d30-377">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a8d30-377">Az.Accounts</span></span>
* <span data-ttu-id="a8d30-378">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="a8d30-378">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="a8d30-379">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="a8d30-379">Az.ApplicationInsights</span></span>
* <span data-ttu-id="a8d30-380">A Remove-AzApplicationInsightsApiKey dokumentáció példájában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="a8d30-380">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="a8d30-381">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a8d30-381">Az.Automation</span></span>
* <span data-ttu-id="a8d30-382">Az erőforrássztringben található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="a8d30-382">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="a8d30-383">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a8d30-383">Az.CognitiveServices</span></span>
* <span data-ttu-id="a8d30-384">NetworkRuleSet támogatás hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="a8d30-384">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a8d30-385">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a8d30-385">Az.Compute</span></span>
* <span data-ttu-id="a8d30-386">A virtuálisgép-példány nézetobjektumaiból hiányzó tulajdonságok (ComputerName, OsName, OsVersion és HyperVGeneration) hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="a8d30-386">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="a8d30-387">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a8d30-387">Az.ContainerRegistry</span></span>
* <span data-ttu-id="a8d30-388">A Remove-AzContainerRegistryReplication Replikáció paraméterében lévő elírás javítása</span><span class="sxs-lookup"><span data-stu-id="a8d30-388">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="a8d30-389">További információ: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="a8d30-389">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a8d30-390">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a8d30-390">Az.DataFactory</span></span>
* <span data-ttu-id="a8d30-391">Az ADF .Net SDK a 4.1.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="a8d30-391">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="a8d30-392">A Get-AzDataFactoryV2PipelineRun dokumentációjában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="a8d30-392">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a8d30-393">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a8d30-393">Az.EventHub</span></span>
* <span data-ttu-id="a8d30-394">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="a8d30-394">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="a8d30-395">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="a8d30-395">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a8d30-396">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a8d30-396">Az.KeyVault</span></span>
* <span data-ttu-id="a8d30-397">A KeySize tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="a8d30-397">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a8d30-398">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a8d30-398">Az.LogicApp</span></span>
* <span data-ttu-id="a8d30-399">A Get-AzIntegrationAccountMap javítása, hogy minden leképezéstípust listázzon</span><span class="sxs-lookup"><span data-stu-id="a8d30-399">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="a8d30-400">Új MapType paraméter hozzáadva a szűréshez</span><span class="sxs-lookup"><span data-stu-id="a8d30-400">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="a8d30-401">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="a8d30-401">Az.ManagedServices</span></span>
* <span data-ttu-id="a8d30-402">Az API 2019. 06. 01-én kiadott (GA) verziójának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a8d30-402">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a8d30-403">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a8d30-403">Az.Network</span></span>
* <span data-ttu-id="a8d30-404">A privát végpont és privát kapcsolatszolgáltatás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a8d30-404">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="a8d30-405">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a8d30-405">New cmdlets</span></span>
        - <span data-ttu-id="a8d30-406">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a8d30-406">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a8d30-407">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a8d30-407">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="a8d30-408">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a8d30-408">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a8d30-409">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a8d30-409">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a8d30-410">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a8d30-410">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a8d30-411">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a8d30-411">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="a8d30-412">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="a8d30-412">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="a8d30-413">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a8d30-413">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="a8d30-414">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies jelző a VirtualNetwork alhálózatban</span><span class="sxs-lookup"><span data-stu-id="a8d30-414">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="a8d30-415">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig frissítve</span><span class="sxs-lookup"><span data-stu-id="a8d30-415">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="a8d30-416">Hozzá lett adva a -PrivateEndpointNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát végpont esetében.</span><span class="sxs-lookup"><span data-stu-id="a8d30-416">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="a8d30-417">Hozzá lett adva a -PrivateLinkServiceNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát kapcsolati szolgáltatás esetében.</span><span class="sxs-lookup"><span data-stu-id="a8d30-417">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="a8d30-418">Az AzPrivateLinkService parancsmag ServiceName paramétere átnevezve a Name névre a ServiceName aliasszal a visszamenőleges kompatibilitás érdekében</span><span class="sxs-lookup"><span data-stu-id="a8d30-418">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="a8d30-419">ICMP-protokoll engedélyezése a hálózati biztonsági szabályzati konfigurációkhoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-419">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="a8d30-420">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a8d30-420">Updated cmdlets</span></span>
        - <span data-ttu-id="a8d30-421">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a8d30-421">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="a8d30-422">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a8d30-422">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="a8d30-423">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a8d30-423">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="a8d30-424">A ConnectionProtocolType (Ikev1/Ikev2) hozzáadva a New-AzVirtualNetworkGatewayConnection konfigurálható paramétereként</span><span class="sxs-lookup"><span data-stu-id="a8d30-424">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="a8d30-425">PrivateIpAddressVersion hozzáadva a LoadBalancerFrontendIpConfigurationhöz</span><span class="sxs-lookup"><span data-stu-id="a8d30-425">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="a8d30-426">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="a8d30-426">Updated cmdlet:</span></span>
        - <span data-ttu-id="a8d30-427">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a8d30-427">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="a8d30-428">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a8d30-428">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="a8d30-429">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a8d30-429">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="a8d30-430">Application Gateway New-AzApplicationGatewayProbeConfig parancs frissítése a mintavétel egyéni portjának támogatásához</span><span class="sxs-lookup"><span data-stu-id="a8d30-430">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="a8d30-431">Frissített New-AzApplicationGatewayProbeConfig: A Port opcionális paraméter hozzáadva, amelyet a rendszer a háttérrendszer-kiszolgáló mintavételére használ.</span><span class="sxs-lookup"><span data-stu-id="a8d30-431">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="a8d30-432">Ez a paraméter a Standard_V2 és WAF_V2 termékváltozatokban használható.</span><span class="sxs-lookup"><span data-stu-id="a8d30-432">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a8d30-433">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a8d30-433">Az.OperationalInsights</span></span>
* <span data-ttu-id="a8d30-434">A mentett keresések alapértelmezett verziója 1 értékre frissítve.</span><span class="sxs-lookup"><span data-stu-id="a8d30-434">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="a8d30-435">Null reguláris kifejezések kezelése javítva az egyéni naplókban</span><span class="sxs-lookup"><span data-stu-id="a8d30-435">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a8d30-436">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a8d30-436">Az.RecoveryServices</span></span>
* <span data-ttu-id="a8d30-437">A Get-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="a8d30-437">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="a8d30-438">A Get-AzRecoveryServicesBackupContainer.md frissítése</span><span class="sxs-lookup"><span data-stu-id="a8d30-438">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="a8d30-439">A Get-AzRecoveryServicesVault.md frissítése</span><span class="sxs-lookup"><span data-stu-id="a8d30-439">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="a8d30-440">A Wait-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="a8d30-440">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="a8d30-441">A Set-AzRecoveryServicesVaultContext.md frissítése</span><span class="sxs-lookup"><span data-stu-id="a8d30-441">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="a8d30-442">A Get-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="a8d30-442">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="a8d30-443">A Get-AzRecoveryServicesBackupRecoveryPoint.md frissítése</span><span class="sxs-lookup"><span data-stu-id="a8d30-443">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="a8d30-444">A Restore-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="a8d30-444">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="a8d30-445">A tároló Azure-fájlmegosztásban való regisztrációjának törlésére szolgáló szolgáltatáshívás frissítése</span><span class="sxs-lookup"><span data-stu-id="a8d30-445">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="a8d30-446">A Set-AzRecoveryServicesAsrAlertSetting.md frissítése</span><span class="sxs-lookup"><span data-stu-id="a8d30-446">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="a8d30-447">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a8d30-447">Az.Resources</span></span>
- <span data-ttu-id="a8d30-448">A New-AzResourceGroupDeployment dokumentációban hivatkozott hiányzó parancsmag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a8d30-448">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="a8d30-449">A szabályzat parancsmagjai frissítve a 2019. 01. 01. dátumú új API-verzió használatára</span><span class="sxs-lookup"><span data-stu-id="a8d30-449">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a8d30-450">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a8d30-450">Az.ServiceBus</span></span>
* <span data-ttu-id="a8d30-451">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="a8d30-451">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="a8d30-452">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="a8d30-452">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="a8d30-453">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a8d30-453">Az.Sql</span></span>
* <span data-ttu-id="a8d30-454">A Set-AzSqlDatabaseSecondary parancsmag hiányzó példáinak javítása</span><span class="sxs-lookup"><span data-stu-id="a8d30-454">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="a8d30-455">A biztonságirés-felmérés e-mail-cím megadása nélkül beállított ismétlődő vizsgálatának javítása</span><span class="sxs-lookup"><span data-stu-id="a8d30-455">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="a8d30-456">Egy kis elírás javítása egy figyelmeztető üzenetben.</span><span class="sxs-lookup"><span data-stu-id="a8d30-456">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a8d30-457">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a8d30-457">Az.Storage</span></span>
* <span data-ttu-id="a8d30-458">A Get-AzStorageAccount hivatkozási dokumentációjában található példa frissítése a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="a8d30-458">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a8d30-459">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a8d30-459">Az.StorageSync</span></span>
* <span data-ttu-id="a8d30-460">Az Invoke-AzStorageSyncChangeDetection parancsmag hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="a8d30-460">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="a8d30-461">A 9551-es hiba javítása a TierFilesOlderThanDays betartásához</span><span class="sxs-lookup"><span data-stu-id="a8d30-461">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a8d30-462">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a8d30-462">Az.Websites</span></span>
* <span data-ttu-id="a8d30-463">A hiba elhárítása, amely miatt a Get-AzWebApp és a Set-AzWebApp nem adott vissza egyes SiteConfig tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="a8d30-463">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="a8d30-464">Egy új Location paraméter hozzáadása a Get-AzDeletedWebApp és a Restore-AzDeletedWebApp parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-464">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="a8d30-465">A webalkalmazás-tárhelyek New-AzWebApp -IncludeSourceWebAppSlots használatával történő klónozásakor jelentkező hiba javítása</span><span class="sxs-lookup"><span data-stu-id="a8d30-465">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="a8d30-466">2.4.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="a8d30-466">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a8d30-467">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a8d30-467">Az.Accounts</span></span>
* <span data-ttu-id="a8d30-468">Profilparancsmagok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="a8d30-468">Add support for profile cmdlets</span></span>
* <span data-ttu-id="a8d30-469">A létrehozott parancsmagokban lévő környezetek és adatsíkok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="a8d30-469">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="a8d30-470">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen végpontot használt az adatsík parancsmagjaihoz Windows PowerShellben</span><span class="sxs-lookup"><span data-stu-id="a8d30-470">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="a8d30-471">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="a8d30-471">Az.Advisor</span></span>
* <span data-ttu-id="a8d30-472">Az Az.Advisor GA-kiadása</span><span class="sxs-lookup"><span data-stu-id="a8d30-472">GA release of Az.Advisor</span></span>
* <span data-ttu-id="a8d30-473">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="a8d30-473">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="a8d30-474">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a8d30-474">Az.ApiManagement</span></span>
* <span data-ttu-id="a8d30-475">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="a8d30-475">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="a8d30-476">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="a8d30-476">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="a8d30-477">Előfizetések felhasználó és termék szerinti lekérdezésének támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a8d30-477">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="a8d30-478">„/”, „/apis”, „/apis/echo-api” hatókör használatával történő lekérdezés támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a8d30-478">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="a8d30-479">A következő hibák ki lettek javítva: https://github.com/Azure/azure-powershell/issues/9307 és https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="a8d30-479">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="a8d30-480">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="a8d30-480">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="a8d30-481">Az „ApiVersion” és az „ApiVersionSetId” megadhatóvá vált az API-k importálásakor</span><span class="sxs-lookup"><span data-stu-id="a8d30-481">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a8d30-482">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a8d30-482">Az.Automation</span></span>
* <span data-ttu-id="a8d30-483">A Set-AzAutomationConnectionFieldValue parancsmag sztringértékek kezelése esetén fellépő hibája javítva lett.</span><span class="sxs-lookup"><span data-stu-id="a8d30-483">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a8d30-484">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a8d30-484">Az.Compute</span></span>
* <span data-ttu-id="a8d30-485">A HyperVGeneration paraméter hozzáadása a New-AzImageConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-485">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a8d30-486">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a8d30-486">Az.DataFactory</span></span>
* <span data-ttu-id="a8d30-487">A tevékenység-, folyamat- és eseményindító-futtatási kimenetek lekérdezési ADF-parancsmagjainak frissítése a Select-Object folyamat támogatásához.</span><span class="sxs-lookup"><span data-stu-id="a8d30-487">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a8d30-488">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a8d30-488">Az.EventGrid</span></span>
* <span data-ttu-id="a8d30-489">Az elgépelés ki lett javítva a New-AzEventGridSubscription dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="a8d30-489">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a8d30-490">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a8d30-490">Az.IotHub</span></span>
* <span data-ttu-id="a8d30-491">Az engedélyezési szabályzati kulcsok újragenerálásának támogatása hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="a8d30-491">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a8d30-492">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a8d30-492">Az.Network</span></span>
* <span data-ttu-id="a8d30-493">A „RoutingPreference” hozzáadva a nyilvános IP-címkékhez</span><span class="sxs-lookup"><span data-stu-id="a8d30-493">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="a8d30-494">Javítottuk a példákat a „Get-AzNetworkServiceTag” referenciadokumentációban</span><span class="sxs-lookup"><span data-stu-id="a8d30-494">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a8d30-495">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a8d30-495">Az.PolicyInsights</span></span>
* <span data-ttu-id="a8d30-496">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyState parancsmagban</span><span class="sxs-lookup"><span data-stu-id="a8d30-496">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="a8d30-497">További információ: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="a8d30-497">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a8d30-498">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a8d30-498">Az.OperationalInsights</span></span>
* <span data-ttu-id="a8d30-499">Javítottuk a Get-AzOperationalInsightsDataSource parancsmagban visszaadott CustomLog adatforrásmodellt</span><span class="sxs-lookup"><span data-stu-id="a8d30-499">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a8d30-500">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a8d30-500">Az.RecoveryServices</span></span>
* <span data-ttu-id="a8d30-501">Az IaaSVMs get-policy parancsának javítása</span><span class="sxs-lookup"><span data-stu-id="a8d30-501">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="a8d30-502">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a8d30-502">Az.Resources</span></span>
    - <span data-ttu-id="a8d30-503">A Get-AzPolicyState -Top paraméter súgószövegének javítása</span><span class="sxs-lookup"><span data-stu-id="a8d30-503">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="a8d30-504">Ügyféloldali lapozás támogatásának hozzáadása a Get-AzPolicyAlias parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-504">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="a8d30-505">Új (-PolicyParameters és -PolicyParametersObject) paraméterek hozzáadása a Set-AzPolicyAssignment parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-505">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="a8d30-506">A Policy-parancsmagok néhány dokumentumának és példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="a8d30-506">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a8d30-507">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a8d30-507">Az.ServiceBus</span></span>
* <span data-ttu-id="a8d30-508">A 4938-as hiba javítása – A New-AzureRmServiceBusQueue parancsmag BadRequest értéket ad vissza a MaxSizeInMegabytes megadásakor</span><span class="sxs-lookup"><span data-stu-id="a8d30-508">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="a8d30-509">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a8d30-509">Az.Sql</span></span>
* <span data-ttu-id="a8d30-510">A példány-feladatátvételi csoportok parancsmagjainak hozzáadása az előzetes kiadásból a nyilvános kiadáshoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-510">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="a8d30-511">Az Azure SQL Server\Database Auditing támogatása új parancsmagokkal.</span><span class="sxs-lookup"><span data-stu-id="a8d30-511">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="a8d30-512">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="a8d30-512">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="a8d30-513">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="a8d30-513">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="a8d30-514">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="a8d30-514">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="a8d30-515">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="a8d30-515">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="a8d30-516">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="a8d30-516">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="a8d30-517">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="a8d30-517">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="a8d30-518">E-mailes korlátozások eltávolítása a sebezhetőségi felmérés beállításaiból</span><span class="sxs-lookup"><span data-stu-id="a8d30-518">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a8d30-519">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a8d30-519">Az.Storage</span></span>
* <span data-ttu-id="a8d30-520">Az „-IndexDocument” és „-ErrorDocument404Path” paraméter módosítása kötelezőről opcionálisra a következő parancsmagban:</span><span class="sxs-lookup"><span data-stu-id="a8d30-520">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="a8d30-521">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a8d30-521">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="a8d30-522">A Get-AzStorageBlobContent súgójának frissítése egy példa hozzáadásával</span><span class="sxs-lookup"><span data-stu-id="a8d30-522">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="a8d30-523">További hibaadatok megjelenítése, ha a parancsmag futtatása StorageException miatt meghiúsul</span><span class="sxs-lookup"><span data-stu-id="a8d30-523">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="a8d30-524">Storage-fiók létrehozásának és frissítésének támogatása Azure Files AAD DS-hitelesítéssel</span><span class="sxs-lookup"><span data-stu-id="a8d30-524">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="a8d30-525">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a8d30-525">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="a8d30-526">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a8d30-526">Set-AzStorageAccount</span></span>
* <span data-ttu-id="a8d30-527">Támogatás a fájlmegosztások, fájlkönyvtárak vagy fájlok fájlleíróinak listázásához vagy bezárásához</span><span class="sxs-lookup"><span data-stu-id="a8d30-527">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="a8d30-528">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="a8d30-528">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="a8d30-529">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="a8d30-529">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="a8d30-530">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="a8d30-530">Az.StorageSync</span></span>
* <span data-ttu-id="a8d30-531">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="a8d30-531">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="a8d30-532">2.3.2 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="a8d30-532">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a8d30-533">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a8d30-533">Az.Accounts</span></span>
* <span data-ttu-id="a8d30-534">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen URL-címeket használt a Functions-hívásokhoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-534">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="a8d30-535">További információ: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="a8d30-535">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="a8d30-536">Javítva lett az aliasok hibája az AzureRM–Az parancsmagok közötti átvitel esetében</span><span class="sxs-lookup"><span data-stu-id="a8d30-536">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="a8d30-537">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="a8d30-537">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="a8d30-538">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="a8d30-538">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a8d30-539">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a8d30-539">Az.Compute</span></span>
* <span data-ttu-id="a8d30-540">A „New-AzVm” és „New-AzVmss” egyszerű paraméterkészletek mostantól elfogadják a „ProximityPlacementGroup” paramétert.</span><span class="sxs-lookup"><span data-stu-id="a8d30-540">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="a8d30-541">Az elgépelés ki lett javítva a „New-AzVM” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="a8d30-541">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="a8d30-542">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="a8d30-542">Az.Dns</span></span>
* <span data-ttu-id="a8d30-543">Az elgépelés ki lett javítva a „Set-AzDnsZone” súgópéldáinál.</span><span class="sxs-lookup"><span data-stu-id="a8d30-543">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a8d30-544">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a8d30-544">Az.EventGrid</span></span>
* <span data-ttu-id="a8d30-545">Frissítve a 2019-06-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="a8d30-545">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="a8d30-546">Új parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="a8d30-546">New cmdlets:</span></span>
    - <span data-ttu-id="a8d30-547">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="a8d30-547">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="a8d30-548">Létrehoz egy új Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="a8d30-548">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="a8d30-549">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="a8d30-549">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="a8d30-550">Lekéri egy Event Grid-tartomány részleteit, vagy az aktuális Azure-előfizetéshez tartozó összes Event Grid-tartomány listáját.</span><span class="sxs-lookup"><span data-stu-id="a8d30-550">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="a8d30-551">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="a8d30-551">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="a8d30-552">Eltávolít egy Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="a8d30-552">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="a8d30-553">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="a8d30-553">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="a8d30-554">Újra létrehozza a megosztott hozzáférési kulcsot az Azure Event Grid-tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="a8d30-554">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="a8d30-555">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="a8d30-555">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="a8d30-556">Lekéri az Event Grid-tartományban való esemény-közzétételhez használt megosztott hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="a8d30-556">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="a8d30-557">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="a8d30-557">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="a8d30-558">Új Azure Event Grid-tartományi témakört hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a8d30-558">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="a8d30-559">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="a8d30-559">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="a8d30-560">Lekéri egy Event Grid-tartományi témakör részleteit, vagy az aktuális Azure-előfizetés adott Event Grid-tartományához tartozó Event Grid-tartományi témakörök listáját</span><span class="sxs-lookup"><span data-stu-id="a8d30-560">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="a8d30-561">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="a8d30-561">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="a8d30-562">Eltávolít egy meglévő Azure Event Grid-tartományi témakört.</span><span class="sxs-lookup"><span data-stu-id="a8d30-562">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="a8d30-563">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="a8d30-563">Updated cmdlets:</span></span>
    - <span data-ttu-id="a8d30-564">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="a8d30-564">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="a8d30-565">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="a8d30-565">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="a8d30-566">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="a8d30-566">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="a8d30-567">Új paraméterkészletek lettek hozzáadva tartományok és tartományi témakörök esetében, lehetővé téve a meglévő paraméterek (például EndPointType, SubjectBeginsWith stb.) újbóli felhasználását.</span><span class="sxs-lookup"><span data-stu-id="a8d30-567">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="a8d30-568">Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="a8d30-568">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="a8d30-569">Esemény-előfizetés lejárati dátuma,</span><span class="sxs-lookup"><span data-stu-id="a8d30-569">Event subscription expiration date,</span></span>
            - <span data-ttu-id="a8d30-570">Speciális szűrési paraméterek.</span><span class="sxs-lookup"><span data-stu-id="a8d30-570">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="a8d30-571">Új felsorolási érték lett hozzáadva a servicebusqueue elem célértékeként.</span><span class="sxs-lookup"><span data-stu-id="a8d30-571">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="a8d30-572">Nem engedélyezett az -IncludedEventType beállításnál az „All” érték használata és a következővel való helyettesítése:</span><span class="sxs-lookup"><span data-stu-id="a8d30-572">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="a8d30-573">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="a8d30-573">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="a8d30-574">Új opcionális paraméterek (Top, ODataQuery és NextLink) az eredmények tördelésének és szűrésének támogatásához.</span><span class="sxs-lookup"><span data-stu-id="a8d30-574">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="a8d30-575">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="a8d30-575">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="a8d30-576">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="a8d30-576">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="a8d30-577">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="a8d30-577">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a8d30-578">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a8d30-578">Az.FrontDoor</span></span>
* <span data-ttu-id="a8d30-579">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="a8d30-579">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="a8d30-580">Hozzá lett adva az átalakítások támogatása és az új operátorértékek automatikus kitöltése (RegEx)</span><span class="sxs-lookup"><span data-stu-id="a8d30-580">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="a8d30-581">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="a8d30-581">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="a8d30-582">Hozzá lett adva az új értékek automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="a8d30-582">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a8d30-583">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a8d30-583">Az.Network</span></span>
* <span data-ttu-id="a8d30-584">Virtuális hálózati átjárók erőforrás-támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a8d30-584">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="a8d30-585">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a8d30-585">New cmdlets</span></span>
        - <span data-ttu-id="a8d30-586">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="a8d30-586">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="a8d30-587">AvailablePrivateEndpointType hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a8d30-587">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="a8d30-588">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a8d30-588">New cmdlets</span></span> 
        - <span data-ttu-id="a8d30-589">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="a8d30-589">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="a8d30-590">PrivatePrivateLinkService hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a8d30-590">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="a8d30-591">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a8d30-591">New cmdlets</span></span> 
        - <span data-ttu-id="a8d30-592">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a8d30-592">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="a8d30-593">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a8d30-593">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="a8d30-594">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a8d30-594">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="a8d30-595">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a8d30-595">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="a8d30-596">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a8d30-596">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="a8d30-597">PrivateEndpoint hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a8d30-597">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="a8d30-598">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a8d30-598">New cmdlets</span></span>
        - <span data-ttu-id="a8d30-599">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a8d30-599">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a8d30-600">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a8d30-600">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a8d30-601">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a8d30-601">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="a8d30-602">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="a8d30-602">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="a8d30-603">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: UseLocalAzureIpAddress jelző a VpnConnection elemen</span><span class="sxs-lookup"><span data-stu-id="a8d30-603">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="a8d30-604">Frissítve lett a New-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="a8d30-604">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="a8d30-605">Frissítve lett a Set-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="a8d30-605">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="a8d30-606">Hozzá lett adva az írásvédett PeeredConnections mező az ExpressRoute-társhálózatlétesítések esetében.</span><span class="sxs-lookup"><span data-stu-id="a8d30-606">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="a8d30-607">Hozzá lett adva az írásvédett GlobalReachEnabled mező az ExpressRoute esetében.</span><span class="sxs-lookup"><span data-stu-id="a8d30-607">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="a8d30-608">Kompatibilitástörő változást okozó attribútum lett hozzáadva, amely jelzi az AllowGlobalReach mező elavulását az ExpressRouteCircuit-modellben</span><span class="sxs-lookup"><span data-stu-id="a8d30-608">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="a8d30-609">Javítva lett a 8756-os hiba a TargetListenerID AzApplicationGatewayRedirectConfiguration-parancsmagokkal való használata során</span><span class="sxs-lookup"><span data-stu-id="a8d30-609">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="a8d30-610">Javítva lett a hiba a New-AzApplicationGatewayPathRuleConfig parancsmagban, amely megakadályozta az átírási szabálykészlet beállítását.</span><span class="sxs-lookup"><span data-stu-id="a8d30-610">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="a8d30-611">Javítva lett a VirtualNetworkTaps megjelenítése a NetworkInterfaceIpConfiguration esetében</span><span class="sxs-lookup"><span data-stu-id="a8d30-611">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="a8d30-612">Javítva lettek a Cortex Get-parancsmagok az összes rész felsorolásához</span><span class="sxs-lookup"><span data-stu-id="a8d30-612">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="a8d30-613">Javítva lett a VirtualHub-hivatkozás létrehozása az ExpressRouteGateways, VpnGateway esetében</span><span class="sxs-lookup"><span data-stu-id="a8d30-613">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="a8d30-614">Hozzá lett adva a rendelkezésreállási zónák támogatása az AzureFirewall és a NatGateway esetében</span><span class="sxs-lookup"><span data-stu-id="a8d30-614">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="a8d30-615">Hozzá lett adva a Get-AzNetworkServiceTag parancsmag</span><span class="sxs-lookup"><span data-stu-id="a8d30-615">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="a8d30-616">Hozzá lett adva a több nyilvános IP-cím támogatása az Azure Firewall esetében</span><span class="sxs-lookup"><span data-stu-id="a8d30-616">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="a8d30-617">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="a8d30-617">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="a8d30-618">Hozzá lett adva a -PublicIpAddress paraméter, amely egy vagy több nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="a8d30-618">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="a8d30-619">Hozzá lett adva a -VirtualNetwork paraméter, amely virtuális hálózati objektumokat fogad el</span><span class="sxs-lookup"><span data-stu-id="a8d30-619">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="a8d30-620">Hozzá lett adva az AddPublicIpAddress és RemovePublicIpAddress metódus a tűzfalobjektumok esetében, és nyilvános IP-cím-objektumokat fogadnak el bemeneti adatként</span><span class="sxs-lookup"><span data-stu-id="a8d30-620">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="a8d30-621">Elavult a -PublicIpName és a -VirtualNetworkName paraméter</span><span class="sxs-lookup"><span data-stu-id="a8d30-621">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="a8d30-622">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: VpnClient AAD-alapú hitelesítési beállítások megadása a virtuális hálózati átjárók erőforrásaihoz.</span><span class="sxs-lookup"><span data-stu-id="a8d30-622">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="a8d30-623">Frissült a New-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="a8d30-623">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="a8d30-624">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="a8d30-624">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="a8d30-625">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva a RemoveAadAuthentication opcionális kapcsolóparaméter a VpnClient AAD-alapú hitelesítési beállítások eltávolításához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="a8d30-625">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a8d30-626">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a8d30-626">Az.OperationalInsights</span></span>
* <span data-ttu-id="a8d30-627">Engedélyezve lett a **pergb2018** tarifacsomag a „New-AzureRmOperationalInsightsWorkspace” parancs esetében</span><span class="sxs-lookup"><span data-stu-id="a8d30-627">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="a8d30-628">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a8d30-628">Az.Resources</span></span>
* <span data-ttu-id="a8d30-629">További sablonexportálási beállítások támogatása</span><span class="sxs-lookup"><span data-stu-id="a8d30-629">Support for additional Template Export options</span></span>
    - <span data-ttu-id="a8d30-630">Hozzá lett adva a „-SkipResourceNameParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="a8d30-630">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="a8d30-631">Hozzá lett adva a „-SkipAllParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="a8d30-631">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="a8d30-632">Hozzá lett adva a „-Resource” paraméter az Export-AzResourceGroup esetében az exportált erőforrások szűréséhez</span><span class="sxs-lookup"><span data-stu-id="a8d30-632">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a8d30-633">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a8d30-633">Az.ServiceFabric</span></span>
* <span data-ttu-id="a8d30-634">Ki lett javítva az a hiba, hogy a ByExistingKeyVault tanúsítvány hozzáadása bizonyos esetekben helytelen ujjlenyomatot kért le</span><span class="sxs-lookup"><span data-stu-id="a8d30-634">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="a8d30-635">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a8d30-635">Az.Sql</span></span>
* <span data-ttu-id="a8d30-636">Javítva lett az Advanced Threat Protection Storage-végpontjának utótagja</span><span class="sxs-lookup"><span data-stu-id="a8d30-636">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="a8d30-637">Javítva lett, hogy az Advanced Data Security engedélyezése felülbírálja az Advanced Threat Protection-szabályzatot</span><span class="sxs-lookup"><span data-stu-id="a8d30-637">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="a8d30-638">Új parancsmagok lettek hozzáadva a Management.Sql esetében, amelyek lehetővé teszik az ügyfelek számára TDE-kulcsok hozzáadását és TDE-védő beállítását a felügyelt példányokhoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-638">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="a8d30-639">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a8d30-639">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="a8d30-640">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a8d30-640">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="a8d30-641">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a8d30-641">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="a8d30-642">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="a8d30-642">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="a8d30-643">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="a8d30-643">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a8d30-644">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a8d30-644">Az.Storage</span></span>
* <span data-ttu-id="a8d30-645">A FileStorage és az SkuName Premium_ZRS altípus támogatása Storage-fiókok létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="a8d30-645">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="a8d30-646">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a8d30-646">New-AzStorageAccount</span></span>
* <span data-ttu-id="a8d30-647">Egyértelműsítve lett a blobmódosíthatatlansági parancsmag leírása</span><span class="sxs-lookup"><span data-stu-id="a8d30-647">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="a8d30-648">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a8d30-648">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a8d30-649">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a8d30-649">Az.Websites</span></span>
* <span data-ttu-id="a8d30-650">Optimalizálva lett a Get-AzWebAppCertificate parancsmag, hogy erőforráscsoport szerint szűrjön a kiszolgálón, ne ügyfél szerint</span><span class="sxs-lookup"><span data-stu-id="a8d30-650">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="a8d30-651">Hozzá lett adva a -UseDisasterRecovery kapcsolóparaméter a Get-AzWebAppSnapshot parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-651">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="a8d30-652">2.2.0 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="a8d30-652">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="a8d30-653">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a8d30-653">Az.Cdn</span></span>
* <span data-ttu-id="a8d30-654">Frissített parancsmagok a rulesEngine szolgáltatás támogatásához a 2019. 04. 15. API-verzión</span><span class="sxs-lookup"><span data-stu-id="a8d30-654">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a8d30-655">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a8d30-655">Az.Compute</span></span>
* <span data-ttu-id="a8d30-656">A `NoWait` paraméter hozzáadása, amely elindítja a műveletet, és azonnal visszatér, még a művelet befejezése előtt.</span><span class="sxs-lookup"><span data-stu-id="a8d30-656">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="a8d30-657">Frissített parancsmagok:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="a8d30-657">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a8d30-658">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a8d30-658">Az.EventHub</span></span>
* <span data-ttu-id="a8d30-659">A 9231-es hiba javítása – a Get-AzEventHubNamespace nem ad vissza címkéket</span><span class="sxs-lookup"><span data-stu-id="a8d30-659">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="a8d30-660">A 9230-as hiba javítása – a Get-AzEventHubNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="a8d30-660">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a8d30-661">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a8d30-661">Az.Network</span></span>
* <span data-ttu-id="a8d30-662">ResourceID és InputObject frissítése a Nat-átjárón</span><span class="sxs-lookup"><span data-stu-id="a8d30-662">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="a8d30-663">ResourceID és InputObject aliasának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="a8d30-663">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a8d30-664">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a8d30-664">Az.PolicyInsights</span></span>
* <span data-ttu-id="a8d30-665">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyEvent parancsmagban</span><span class="sxs-lookup"><span data-stu-id="a8d30-665">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a8d30-666">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a8d30-666">Az.RecoveryServices</span></span>
* <span data-ttu-id="a8d30-667">Az IaaSVM szabályzat minimális megőrzési ideje 7 napról 1-re módosult</span><span class="sxs-lookup"><span data-stu-id="a8d30-667">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a8d30-668">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a8d30-668">Az.ServiceBus</span></span>
* <span data-ttu-id="a8d30-669">A 9182-es hiba javítása – a Get-AzServiceBusNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="a8d30-669">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a8d30-670">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a8d30-670">Az.ServiceFabric</span></span>
* <span data-ttu-id="a8d30-671">Az Update-AzServiceFabricReliability hibaüzenetében lévő gépelési hiba kijavítása</span><span class="sxs-lookup"><span data-stu-id="a8d30-671">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="a8d30-672">A Service Fabric parancssorok hiányzó karakterének pótlása</span><span class="sxs-lookup"><span data-stu-id="a8d30-672">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="a8d30-673">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a8d30-673">Az.Sql</span></span>
* <span data-ttu-id="a8d30-674">A DnsZonePartner paraméter hozzáadása a New-AzureSqlInstance parancsmaghoz az AutoDr képesség a felügyelt példányon való támogatásához.</span><span class="sxs-lookup"><span data-stu-id="a8d30-674">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="a8d30-675">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag kivezetése</span><span class="sxs-lookup"><span data-stu-id="a8d30-675">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="a8d30-676">Threat Detection parancsmagok átnevezése Advanced Threat Protection névre</span><span class="sxs-lookup"><span data-stu-id="a8d30-676">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="a8d30-677">A New-AzSqlInstance, - StorageSizeInGB és - LicenseType paraméterek mostantól nem kötelezőek.</span><span class="sxs-lookup"><span data-stu-id="a8d30-677">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a8d30-678">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a8d30-678">Az.Websites</span></span>
* <span data-ttu-id="a8d30-679">javítja azt a hibát, amely miatt a Set-AzWebApp és a Set-AzWebAppSlot a -WebApp tulajdonsággal való használata eltávolította a címkéket</span><span class="sxs-lookup"><span data-stu-id="a8d30-679">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="a8d30-680">2.1.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="a8d30-680">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="a8d30-681">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a8d30-681">Az.ApiManagement</span></span>
* <span data-ttu-id="a8d30-682">Új parancsmagok a globális és API-szintű diagnosztika kezeléshez</span><span class="sxs-lookup"><span data-stu-id="a8d30-682">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="a8d30-683">**Get-AzApiManagementDiagnostic** – A globális vagy API hatókörre konfigurált diagnosztika beolvasása</span><span class="sxs-lookup"><span data-stu-id="a8d30-683">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="a8d30-684">**New-AzApiManagementDiagnostic** – Új diagnosztika létrehozása a globális vagy API szintű hatókörhöz</span><span class="sxs-lookup"><span data-stu-id="a8d30-684">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="a8d30-685">**New-AzApiManagementHttpMessageDiagnostic** – Diagnosztikai beállítás létrehozása arra vonatkozóan, hogy mely fejléceknél naplózzon a rendszer, és mekkora legyen a törzs mérete bájtban</span><span class="sxs-lookup"><span data-stu-id="a8d30-685">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="a8d30-686">**New-AzApiManagementPipelineDiagnosticSetting** – Diagnosztikai beállítások létrehozása az átjáróra érkező és onnan induló HTTP-üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="a8d30-686">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="a8d30-687">**New-AzApiManagementSamplingSetting** – Mintavételezési beállítások létrehozása diagnosztikai kérésekhez/válaszokhoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-687">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="a8d30-688">**Remove-AzApiManagementDiagnostic** – Diagnosztikai entitás eltávolítása globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="a8d30-688">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="a8d30-689">**Set-AzApiManagementDiagnostic** – Diagnosztikai entitás frissítése globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="a8d30-689">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="a8d30-690">Új parancsmagok az ApiManagement szolgáltatás gyorsítótárának kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="a8d30-690">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="a8d30-691">**Get-AzApiManagementCache** – Az azonosító által megadott vagy az összes gyorsítótár részleteinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="a8d30-691">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="a8d30-692">**New-AzApiManagementCache** – Új alapértelmezett gyorsítótár létrehozása vagy gyorsítótár létrehozása adott Azure-régióban</span><span class="sxs-lookup"><span data-stu-id="a8d30-692">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="a8d30-693">**Remove-AzApiManagementCache** – Gyorsítótár eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a8d30-693">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="a8d30-694">**Update-AzApiManagementCache** – Gyorsítótár frissítése</span><span class="sxs-lookup"><span data-stu-id="a8d30-694">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="a8d30-695">Új parancsmagok az API-séma kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="a8d30-695">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="a8d30-696">**New-AzApiManagementSchema** – Új séma létrehozása egy API-hoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-696">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="a8d30-697">**Get-AzApiManagementSchema** – Az API-ban konfigurált sémák beolvasása</span><span class="sxs-lookup"><span data-stu-id="a8d30-697">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="a8d30-698">**Remove-AzApiManagementSchema** – Az API-ban konfigurált sémák eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a8d30-698">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="a8d30-699">**Set-AzApiManagementSchema** – Az API-ban konfigurált séma frissítése</span><span class="sxs-lookup"><span data-stu-id="a8d30-699">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="a8d30-700">Új parancsmag a felhasználói jogkivonat létrehozásához</span><span class="sxs-lookup"><span data-stu-id="a8d30-700">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="a8d30-701">**New-AzApiManagementUserToken** – Új, alapértelmezés szerint 8 órán át érvényes felhasználói jogkivonat létrehozása. Ezen parancsmag használatával lehet a „GIT” felhasználó számára jogkivonatot létrehozni.</span><span class="sxs-lookup"><span data-stu-id="a8d30-701">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="a8d30-702">Új parancsmag a hálózat állapotának lekérdezéséhez</span><span class="sxs-lookup"><span data-stu-id="a8d30-702">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="a8d30-703">**Get-AzApiManagementNetworkStatus** – Azon erőforrások hálózati állapotának beolvasása, amelyektől az API Management szolgáltatás függ.</span><span class="sxs-lookup"><span data-stu-id="a8d30-703">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="a8d30-704">Ez hasznos lehet, ha az ApiManagement szolgáltatást virtuális hálózatra telepíti, és ellenőrizni kell, hogy rendben működnek-e a függőségek.</span><span class="sxs-lookup"><span data-stu-id="a8d30-704">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="a8d30-705">A **New-AzApiManagement** parancsmag frissítése az ApiManagement szolgáltatás kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="a8d30-705">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="a8d30-706">Mostantól az új „Consumption” SKU is támogatott</span><span class="sxs-lookup"><span data-stu-id="a8d30-706">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="a8d30-707">Mostantól az „EnableClientCertificate” jelző a „Consumption” SKU-hoz is bekapcsolható</span><span class="sxs-lookup"><span data-stu-id="a8d30-707">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="a8d30-708">Az új **New-AzApiManagementSslSetting** parancsmag lehetővé teszi a „TLS/SSL” beállítás konfigurálását a „Háttér” és „Előtér” esetén is.</span><span class="sxs-lookup"><span data-stu-id="a8d30-708">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="a8d30-709">Ez egy ApiManagement szolgáltatás előterén a titkosítások, mint például a 3DES, valamint a szerverprotokollok, mint például a Http2 konfigurálására is alkalmas.</span><span class="sxs-lookup"><span data-stu-id="a8d30-709">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="a8d30-710">Mostantól támogatott a „DeveloperPortal” gazdanév ApiManagement szolgáltatáson történő konfigurálása.</span><span class="sxs-lookup"><span data-stu-id="a8d30-710">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="a8d30-711">A **Get-AzApiManagementSsoToken** parancsmagok frissítése a „PsApiManagement” objektum bemenetként való használatához</span><span class="sxs-lookup"><span data-stu-id="a8d30-711">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="a8d30-712">A parancsmag frissítése a hibaüzenetek beágyazott megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="a8d30-712">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="a8d30-713">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hibakód: ValidationError Hibaüzenet: Egy vagy több mező hibás értéket tartalmaz: Hiba részletei:    [Kód=ValidationError, Üzenet=Hiba a log-to-eventhub elemben, 3. sor, 10. oszlop: A naplózó nem található, Cél=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="a8d30-713">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="a8d30-714">Az **Export-AzApiManagementApi** parancsmag frissítse az API-k OpenApi 3.0 formátumban való exportálásához</span><span class="sxs-lookup"><span data-stu-id="a8d30-714">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="a8d30-715">Az **Import-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="a8d30-715">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="a8d30-716">API importálása az OpenApi 3.0 dokumentumspecifikációból</span><span class="sxs-lookup"><span data-stu-id="a8d30-716">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="a8d30-717">A bármely (Swagger, Wadl, Wsdl, OpenAPI) dokumentumban megadott PsApiManagementSchema tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="a8d30-717">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="a8d30-718">A bármely dokumentumban megadott ServiceUrl tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="a8d30-718">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="a8d30-719">A **Get-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) való visszaadásához</span><span class="sxs-lookup"><span data-stu-id="a8d30-719">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="a8d30-720">A **Set-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) és XML-nek megfelelő feloldójeles formátumban (xml használatával) való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="a8d30-720">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="a8d30-721">A **New-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="a8d30-721">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="a8d30-722">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="a8d30-722">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="a8d30-723">API létrehozása ApiVersionSet tulajdonságban</span><span class="sxs-lookup"><span data-stu-id="a8d30-723">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="a8d30-724">API klónozása SourceApiId és SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="a8d30-724">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="a8d30-725">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="a8d30-725">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="a8d30-726">A **Set-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="a8d30-726">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="a8d30-727">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="a8d30-727">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="a8d30-728">API frissítése ApiVersionSet tulajdonságba</span><span class="sxs-lookup"><span data-stu-id="a8d30-728">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="a8d30-729">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="a8d30-729">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="a8d30-730">A **New-AzApiManagementRevision** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="a8d30-730">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="a8d30-731">Létező változat klónozása (címkék, termékek, műveletek és szabályzatok másolása) a SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="a8d30-731">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="a8d30-732">Az új változat a szülő ApiId értékét veszi át</span><span class="sxs-lookup"><span data-stu-id="a8d30-732">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="a8d30-733">ApiRevisionDescription biztosítása</span><span class="sxs-lookup"><span data-stu-id="a8d30-733">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="a8d30-734">A „ServiceUrl” felülírása API klónozáskor</span><span class="sxs-lookup"><span data-stu-id="a8d30-734">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="a8d30-735">A **New-AzApiManagementIdentityProvider** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="a8d30-735">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="a8d30-736">AAD vagy AADB2C konfigurálása hitelesítésszolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="a8d30-736">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="a8d30-737">SignupPolicy, SigninPolicy, ProfileEditingPolicy és PasswordResetPolicy beállítása</span><span class="sxs-lookup"><span data-stu-id="a8d30-737">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="a8d30-738">A **New-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="a8d30-738">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="a8d30-739">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-739">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="a8d30-740">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-740">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="a8d30-741">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="a8d30-741">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="a8d30-742">A **Set-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="a8d30-742">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="a8d30-743">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-743">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="a8d30-744">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-744">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="a8d30-745">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="a8d30-745">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="a8d30-746">Az alábbi parancsmagok frissültek a ResourceID bemenetként való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="a8d30-746">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="a8d30-747">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a8d30-747">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="a8d30-748">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="a8d30-748">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="a8d30-749">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a8d30-749">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="a8d30-750">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="a8d30-750">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="a8d30-751">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="a8d30-751">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="a8d30-752">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="a8d30-752">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="a8d30-753">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="a8d30-753">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="a8d30-754">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a8d30-754">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="a8d30-755">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="a8d30-755">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="a8d30-756">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="a8d30-756">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="a8d30-757">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="a8d30-757">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="a8d30-758">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a8d30-758">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a8d30-759">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a8d30-759">Az.Automation</span></span>
* <span data-ttu-id="a8d30-760">A Get-AzAutomationJobOutputRecord frissítése a JSON- és a szövegrekordértékek kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="a8d30-760">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="a8d30-761">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="a8d30-761">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="a8d30-762">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="a8d30-762">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="a8d30-763">A Start-AzAutomationDscCompilationJob viselkedésének módosítása a munka elindítására a befejezésre való várakozás helyett</span><span class="sxs-lookup"><span data-stu-id="a8d30-763">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="a8d30-764">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="a8d30-764">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="a8d30-765">A Get-AzAutomationDscNode azon hibájának javítása, amely miatt a -Name használatakor az összes csomópontot visszaadta.</span><span class="sxs-lookup"><span data-stu-id="a8d30-765">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="a8d30-766">Most már csak az egyező csomópontot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="a8d30-766">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a8d30-767">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a8d30-767">Az.Compute</span></span>
* <span data-ttu-id="a8d30-768">A ProtectFromScaleIn és a ProtectFromScaleSetAction paraméterek hozzáadása az Update-AzVmssVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-768">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="a8d30-769">A New-azvm fedőparaméter-készlet mostantól alapértelmezetten egy elérhető helyet használ, ha az USA keleti régiója nem támogatott</span><span class="sxs-lookup"><span data-stu-id="a8d30-769">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a8d30-770">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a8d30-770">Az.DataLakeStore</span></span>
* <span data-ttu-id="a8d30-771">Az ADLS SDK frissítése a httpclient használatához, integrált adatsíkteszteléssel az Azure-keretrendszerben</span><span class="sxs-lookup"><span data-stu-id="a8d30-771">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a8d30-772">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a8d30-772">Az.Monitor</span></span>
* <span data-ttu-id="a8d30-773">A hibás paraméternevek kijavítása a súgópéldákban</span><span class="sxs-lookup"><span data-stu-id="a8d30-773">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a8d30-774">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a8d30-774">Az.Network</span></span>
* <span data-ttu-id="a8d30-775">DisableBgpRoutePropagation jelölő hozzáadása az érvényes útválasztási táblázathoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-775">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="a8d30-776">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="a8d30-776">Updated cmdlet:</span></span>
        - <span data-ttu-id="a8d30-777">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="a8d30-777">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="a8d30-778">A dupla kötőjel kijavítása a New-AzApplicationGatewayTrustedRootCertificate dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="a8d30-778">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="a8d30-779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a8d30-779">Az.Resources</span></span>
* <span data-ttu-id="a8d30-780">Új Get-AzureRmDenyAssignment parancsmag hozzáadása a megtagadási hozzárendelések lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="a8d30-780">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="a8d30-781">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a8d30-781">Az.Sql</span></span>
* <span data-ttu-id="a8d30-782">Advanced Threat Protection parancsmagok átnevezése Advanced Data Security névre és a sebezhetőségi felmérés alapértelmezett engedélyezése</span><span class="sxs-lookup"><span data-stu-id="a8d30-782">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="a8d30-783">2.0.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="a8d30-783">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a8d30-784">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a8d30-784">Az.Accounts</span></span>
* <span data-ttu-id="a8d30-785">Az Authentication Library frissítése a felhasználóneves/jelszavas hitelesítéssel kapcsolatos ADFS-problémák kijavításához</span><span class="sxs-lookup"><span data-stu-id="a8d30-785">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a8d30-786">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a8d30-786">Az.CognitiveServices</span></span>
* <span data-ttu-id="a8d30-787">Csak a Bing jogi nyilatkozat jelenik meg a Bing Search-szolgáltatásoknál.</span><span class="sxs-lookup"><span data-stu-id="a8d30-787">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="a8d30-788">A sikertelen fióklétrehozás hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="a8d30-788">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a8d30-789">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a8d30-789">Az.Compute</span></span>
* <span data-ttu-id="a8d30-790">Közelségi elhelyezési csoport szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="a8d30-790">Proximity placement group feature.</span></span>
    - <span data-ttu-id="a8d30-791">A következő új parancsmagok lettek hozzáadva:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="a8d30-791">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="a8d30-792">Az új ProximityPlacementGroupId paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="a8d30-792">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="a8d30-793">A StorageAccountType paraméter hozzá lett adva a New-AzGalleryImageVersion parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="a8d30-793">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="a8d30-794">A New-AzGalleryImageVersion TargetRegion paramétere tartalmazhatja a következőt: StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="a8d30-794">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="a8d30-795">A SkipShutdown kapcsolóparaméter hozzá lett adva a Stop-AzVM és Stop-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-795">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="a8d30-796">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="a8d30-796">Breaking changes</span></span>
    - <span data-ttu-id="a8d30-797">A Set-AzVMBootDiagnostics parancsmag új neve: Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="a8d30-797">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="a8d30-798">Az Export-AzLogAnalyticThrottledRequests parancsmag új neve: Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="a8d30-798">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="a8d30-799">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="a8d30-799">Az.DeploymentManager</span></span>
* <span data-ttu-id="a8d30-800">Az Azure Deployment Manager-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="a8d30-800">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="a8d30-801">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="a8d30-801">Az.Dns</span></span>
* <span data-ttu-id="a8d30-802">Automatikus DNS NameServer-delegálás</span><span class="sxs-lookup"><span data-stu-id="a8d30-802">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="a8d30-803">A DNS-zóna létrehozási parancsmag további opcionális paraméterként elfogadja a szülőzóna nevét.</span><span class="sxs-lookup"><span data-stu-id="a8d30-803">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="a8d30-804">Névkiszolgálói rekordokat ad hozzá a szülőzónában az újonnan létrehozott gyermekzóna számára.</span><span class="sxs-lookup"><span data-stu-id="a8d30-804">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a8d30-805">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a8d30-805">Az.FrontDoor</span></span>
* <span data-ttu-id="a8d30-806">Az Azure FrontDoor-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="a8d30-806">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="a8d30-807">A WAF-parancsmagok új neve tartalmazza a „Waf” sztringet</span><span class="sxs-lookup"><span data-stu-id="a8d30-807">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="a8d30-808">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a8d30-808">Az.HDInsight</span></span>
* <span data-ttu-id="a8d30-809">A következő két parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="a8d30-809">Removed two cmdlets:</span></span>
    - <span data-ttu-id="a8d30-810">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a8d30-810">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="a8d30-811">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a8d30-811">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="a8d30-812">Egy új, Set-AzHDInsightGatewayCredential nevű parancsmag lett hozzáadva a Grant-AzHDInsightHttpServicesAccess helyett</span><span class="sxs-lookup"><span data-stu-id="a8d30-812">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="a8d30-813">A Get-AzHDInsightJobOutput parancsmag frissítve lett, hogy különbséget tegyen az olvasói és a HDInsight-operátori szerepkör között:</span><span class="sxs-lookup"><span data-stu-id="a8d30-813">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="a8d30-814">Az olvasói szerepkörrel rendelkező felhasználóknak explicit módon meg kell adniuk a DefaultStorageAccountKey paramétert, ellenkező esetben hiba történik.</span><span class="sxs-lookup"><span data-stu-id="a8d30-814">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="a8d30-815">A HDInsight-operátori szerepkörrel rendelkező felhasználókat ez nem érinti.</span><span class="sxs-lookup"><span data-stu-id="a8d30-815">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a8d30-816">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a8d30-816">Az.Monitor</span></span>
* <span data-ttu-id="a8d30-817">Az SQR API (ütemezett lekérdezési szabály) új parancsmagjai</span><span class="sxs-lookup"><span data-stu-id="a8d30-817">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="a8d30-818">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="a8d30-818">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="a8d30-819">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="a8d30-819">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="a8d30-820">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="a8d30-820">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="a8d30-821">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="a8d30-821">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="a8d30-822">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="a8d30-822">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="a8d30-823">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="a8d30-823">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="a8d30-824">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a8d30-824">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a8d30-825">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a8d30-825">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a8d30-826">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a8d30-826">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a8d30-827">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a8d30-827">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a8d30-828">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a8d30-828">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a8d30-829">[További](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) információk az SQR API-ról</span><span class="sxs-lookup"><span data-stu-id="a8d30-829">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="a8d30-830">A frissített Az.Monitor.md tartalmazza a GenV2 (nem klasszikus) metrikaalapú riasztási szabály parancsmagjait</span><span class="sxs-lookup"><span data-stu-id="a8d30-830">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a8d30-831">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a8d30-831">Az.Network</span></span>
* <span data-ttu-id="a8d30-832">A NAT-átjáró erőforrás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a8d30-832">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="a8d30-833">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a8d30-833">New cmdlets</span></span>
        - <span data-ttu-id="a8d30-834">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a8d30-834">New-AzNatGateway</span></span>
        - <span data-ttu-id="a8d30-835">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a8d30-835">Get-AzNatGateway</span></span>
        - <span data-ttu-id="a8d30-836">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a8d30-836">Set-AzNatGateway</span></span>
        - <span data-ttu-id="a8d30-837">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a8d30-837">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="a8d30-838">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a8d30-838">Updated cmdlets</span></span>
        - <span data-ttu-id="a8d30-839">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="a8d30-839">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="a8d30-840">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="a8d30-840">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="a8d30-841">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: Egyéni útvonalak beállítása/eltávolítása a Brooklyn Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="a8d30-841">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="a8d30-842">Frissült a New-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="a8d30-842">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="a8d30-843">Frissült a Set-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="a8d30-843">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a8d30-844">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a8d30-844">Az.PolicyInsights</span></span>
* <span data-ttu-id="a8d30-845">A szabályzat-kiértékelési adatok lekérdezésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="a8d30-845">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="a8d30-846">Az -Expand paraméter hozzá lett adva a Get-AzPolicyState parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="a8d30-846">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="a8d30-847">Az -Expand PolicyEvaluationDetails támogatása.</span><span class="sxs-lookup"><span data-stu-id="a8d30-847">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a8d30-848">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a8d30-848">Az.RecoveryServices</span></span>
* <span data-ttu-id="a8d30-849">Az előfizetések közötti Azure–Azure Site Recovery átvitel támogatása.</span><span class="sxs-lookup"><span data-stu-id="a8d30-849">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="a8d30-850">Az Azure Site Recovery jövőbeni kompatibilitástörő változásainak jelölése.</span><span class="sxs-lookup"><span data-stu-id="a8d30-850">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="a8d30-851">Ki lett javítva az Azure Site Recovery helyreállítási és műveletterve.</span><span class="sxs-lookup"><span data-stu-id="a8d30-851">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="a8d30-852">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure hálózatleképezés.</span><span class="sxs-lookup"><span data-stu-id="a8d30-852">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="a8d30-853">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure védelemirány felügyelt lemezek esetében.</span><span class="sxs-lookup"><span data-stu-id="a8d30-853">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="a8d30-854">További kisebb javítások.</span><span class="sxs-lookup"><span data-stu-id="a8d30-854">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="a8d30-855">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="a8d30-855">Az.Relay</span></span>
* <span data-ttu-id="a8d30-856">Az elgépelések ki lettek javítva az ügyféloldali üzenetekben</span><span class="sxs-lookup"><span data-stu-id="a8d30-856">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a8d30-857">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a8d30-857">Az.ServiceBus</span></span>
* <span data-ttu-id="a8d30-858">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="a8d30-858">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a8d30-859">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a8d30-859">Az.Storage</span></span>
* <span data-ttu-id="a8d30-860">A Storage ügyféloldali kódtárának frissítése a 10.0.1-es verziójára (az SDK összes objektuma esetében módosul a névtér a Microsoft.WindowsAzure.Storage. *névtérről a Microsoft.Azure.Storage.* névtérre)</span><span class="sxs-lookup"><span data-stu-id="a8d30-860">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="a8d30-861">Frissítés a Microsoft.Azure.Management.Storage 11.0.0-s verziójára az új API-verzió (2019. 04. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="a8d30-861">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="a8d30-862">A Tárfiók létrehozása parancs esetében az alapértelmezett Storage-fiókaltípus a Storage helyett mostantól a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="a8d30-862">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="a8d30-863">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a8d30-863">New-AzStorageAccount</span></span>
* <span data-ttu-id="a8d30-864">A Storage-fiók Sku.Name parancsmagkimenete módosul, hogy igazodjon a bemeneti SkuName paraméterhez, egy aláhúzásjel („_”) hozzáadásával – például a StandardLRS a Standard_LRS névre módosul</span><span class="sxs-lookup"><span data-stu-id="a8d30-864">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="a8d30-865">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a8d30-865">New-AzStorageAccount</span></span>
    - <span data-ttu-id="a8d30-866">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a8d30-866">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="a8d30-867">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a8d30-867">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a8d30-868">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a8d30-868">Az.Websites</span></span>
* <span data-ttu-id="a8d30-869">Az Altípus tulajdonság mostantól meg lesz adva a Get-AzWebApp által visszaadott PSSite objektumokhoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-869">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="a8d30-870">A Get-AzWebApp\*Metrics és a Get-AzAppServicePlanMetrics megjelölve elavultként</span><span class="sxs-lookup"><span data-stu-id="a8d30-870">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="a8d30-871">1.8.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="a8d30-871">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a8d30-872">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="a8d30-872">Highlights since the last major release</span></span>
* <span data-ttu-id="a8d30-873">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="a8d30-873">General availability of `Az` module</span></span>
* <span data-ttu-id="a8d30-874">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="a8d30-874">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a8d30-875">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="a8d30-875">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a8d30-876">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="a8d30-876">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a8d30-877">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="a8d30-877">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a8d30-878">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="a8d30-878">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a8d30-879">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-879">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a8d30-880">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a8d30-880">Az.Accounts</span></span>
* <span data-ttu-id="a8d30-881">Eltávolítás-AzureRm megfelelően törölni a Mac modulok frissítése</span><span class="sxs-lookup"><span data-stu-id="a8d30-881">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a8d30-882">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a8d30-882">Az.Batch</span></span>
* <span data-ttu-id="a8d30-883">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a8d30-883">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a8d30-884">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a8d30-884">Az.Cdn</span></span>
* <span data-ttu-id="a8d30-885">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a8d30-885">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a8d30-886">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a8d30-886">Az.CognitiveServices</span></span>
* <span data-ttu-id="a8d30-887">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a8d30-887">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a8d30-888">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a8d30-888">Az.Compute</span></span>
* <span data-ttu-id="a8d30-889">Az AEM telepítési kapcsolatos problémák megoldásához, ha a lemezek erőforrás-azonosítók kisbetűs resourcegroups volt az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="a8d30-889">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="a8d30-890">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a8d30-890">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a8d30-891">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="a8d30-891">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a8d30-892">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a8d30-892">Az.DataFactory</span></span>
* <span data-ttu-id="a8d30-893">Adjon hozzá SsisProperties, ha a NodeCount felügyelt integrációs modul nem null értékű.</span><span class="sxs-lookup"><span data-stu-id="a8d30-893">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a8d30-894">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a8d30-894">Az.DataLakeStore</span></span>
* <span data-ttu-id="a8d30-895">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a8d30-895">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a8d30-896">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a8d30-896">Az.EventGrid</span></span>
* <span data-ttu-id="a8d30-897">A Súgó szöveg jelzi, hogy erőforrásokat kell létrehozni a create/update eseményt előfizetés parancsmagok használata előtt végpont frissítése.</span><span class="sxs-lookup"><span data-stu-id="a8d30-897">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a8d30-898">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a8d30-898">Az.EventHub</span></span>
* <span data-ttu-id="a8d30-899">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="a8d30-899">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="a8d30-900">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a8d30-900">Az.HDInsight</span></span>
* <span data-ttu-id="a8d30-901">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a8d30-901">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a8d30-902">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a8d30-902">Az.IotHub</span></span>
* <span data-ttu-id="a8d30-903">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a8d30-903">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a8d30-904">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a8d30-904">Az.KeyVault</span></span>
* <span data-ttu-id="a8d30-905">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a8d30-905">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a8d30-906">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="a8d30-906">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="a8d30-907">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a8d30-907">Az.MachineLearning</span></span>
* <span data-ttu-id="a8d30-908">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a8d30-908">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="a8d30-909">Az.Media</span><span class="sxs-lookup"><span data-stu-id="a8d30-909">Az.Media</span></span>
* <span data-ttu-id="a8d30-910">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a8d30-910">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a8d30-911">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a8d30-911">Az.Monitor</span></span>
  * <span data-ttu-id="a8d30-912">Riasztási szabály (nem klasszikus) GenV2 mérőszám-alapú új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a8d30-912">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="a8d30-913">Új AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="a8d30-913">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="a8d30-914">Új AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="a8d30-914">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="a8d30-915">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a8d30-915">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="a8d30-916">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a8d30-916">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="a8d30-917">Adjon hozzá AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a8d30-917">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="a8d30-918">Frissített verzió 0.22.0-preview figyelő SDK</span><span class="sxs-lookup"><span data-stu-id="a8d30-918">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a8d30-919">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a8d30-919">Az.Network</span></span>
* <span data-ttu-id="a8d30-920">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a8d30-920">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a8d30-921">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="a8d30-921">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="a8d30-922">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="a8d30-922">Az.NotificationHubs</span></span>
* <span data-ttu-id="a8d30-923">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a8d30-923">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a8d30-924">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a8d30-924">Az.OperationalInsights</span></span>
* <span data-ttu-id="a8d30-925">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a8d30-925">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="a8d30-926">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a8d30-926">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="a8d30-927">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a8d30-927">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a8d30-928">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a8d30-928">Az.RecoveryServices</span></span>
* <span data-ttu-id="a8d30-929">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a8d30-929">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a8d30-930">Frissített táblázatos formában az SQL azure-beli virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="a8d30-930">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="a8d30-931">A hozzáadott alternatív módszert AzureFileShare hely beolvasása</span><span class="sxs-lookup"><span data-stu-id="a8d30-931">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="a8d30-932">Frissített ScheduleRunDays SchedulePolicy objektumban időzóna szerint</span><span class="sxs-lookup"><span data-stu-id="a8d30-932">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a8d30-933">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a8d30-933">Az.RedisCache</span></span>
* <span data-ttu-id="a8d30-934">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a8d30-934">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a8d30-935">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a8d30-935">Az.Resources</span></span>
* <span data-ttu-id="a8d30-936">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="a8d30-936">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="a8d30-937">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a8d30-937">Az.Sql</span></span>
* <span data-ttu-id="a8d30-938">Cserélje le a függőségi figyelő SDK közös kód</span><span class="sxs-lookup"><span data-stu-id="a8d30-938">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="a8d30-939">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a8d30-939">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a8d30-940">Továbbfejlesztett folyamat, amely több oszlop osztályozási.</span><span class="sxs-lookup"><span data-stu-id="a8d30-940">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="a8d30-941">Termékváltozat tulajdonságok (termékváltozat neve, családi, kapacitás) válasz a Get-AzSqlServerServiceObjective és formátum táblaként alapértelmezés szerint tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="a8d30-941">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="a8d30-942">Lehetővé teszi a Get-AzSqlServerServiceObjective anélkül, hogy a régióban egy már létező kiszolgáló hely alapján.</span><span class="sxs-lookup"><span data-stu-id="a8d30-942">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="a8d30-943">Hozzon létre felügyelt példányt az időzóna-paraméter támogatása.</span><span class="sxs-lookup"><span data-stu-id="a8d30-943">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="a8d30-944">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="a8d30-944">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a8d30-945">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a8d30-945">Az.Websites</span></span>
* <span data-ttu-id="a8d30-946">a Set-AzWebApp és a Set-AzWebAppSlot távolítja el a címkék a végrehajtási javítások</span><span class="sxs-lookup"><span data-stu-id="a8d30-946">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="a8d30-947">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="a8d30-947">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a8d30-948">A webhelyek SDK frissítése.</span><span class="sxs-lookup"><span data-stu-id="a8d30-948">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="a8d30-949">A AdminSiteName tulajdonság PSAppServicePlan eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="a8d30-949">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="a8d30-950">1.7.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="a8d30-950">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a8d30-951">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="a8d30-951">Highlights since the last major release</span></span>
* <span data-ttu-id="a8d30-952">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="a8d30-952">General availability of `Az` module</span></span>
* <span data-ttu-id="a8d30-953">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="a8d30-953">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a8d30-954">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="a8d30-954">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a8d30-955">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="a8d30-955">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a8d30-956">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="a8d30-956">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a8d30-957">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="a8d30-957">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a8d30-958">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-958">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a8d30-959">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a8d30-959">Az.Accounts</span></span>
* <span data-ttu-id="a8d30-960">Frissített Add-AzEnvironment és Set-AzEnvironment parancsmag az AzureAnalysisServicesEndpointResourceId paraméter elfogadásához</span><span class="sxs-lookup"><span data-stu-id="a8d30-960">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a8d30-961">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a8d30-961">Az.AnalysisServices</span></span>
* <span data-ttu-id="a8d30-962">ServiceClient használata DataPlane-parancsmagokban és az eredeti hitelesítési logika eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a8d30-962">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="a8d30-963">Az Add-AzureASAccount burkolóként való megadása a Connect-AzAccount számára a kompatibilitástörő változás elkerüléséhez</span><span class="sxs-lookup"><span data-stu-id="a8d30-963">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a8d30-964">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a8d30-964">Az.Automation</span></span>
* <span data-ttu-id="a8d30-965">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag belefoglalásokat érintő hibája.</span><span class="sxs-lookup"><span data-stu-id="a8d30-965">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="a8d30-966">Az IncludedKbNumber és az IncludedPackageNameMask paraméter mostantól működőképes.</span><span class="sxs-lookup"><span data-stu-id="a8d30-966">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="a8d30-967">Hibajavítás az Azure Automation frissítéskezelési dinamikus csoportja esetében</span><span class="sxs-lookup"><span data-stu-id="a8d30-967">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a8d30-968">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a8d30-968">Az.Compute</span></span>
* <span data-ttu-id="a8d30-969">HyperVGeneration paraméter hozzáadása a New-AzDiskConfig és a New-AzSnapshotConfig parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-969">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="a8d30-970">Virtuális gépek más bérlők katalógus-rendszerképével való létrehozásának engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="a8d30-970">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="a8d30-971">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a8d30-971">Az.ContainerInstance</span></span>
* <span data-ttu-id="a8d30-972">Ki lett javítva a New-AzContainerGroup üres záró argumentumot hozzáadó -Command paraméterével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="a8d30-972">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a8d30-973">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a8d30-973">Az.DataFactory</span></span>
* <span data-ttu-id="a8d30-974">Az ADF .Net SDK verziója 3.0.2-re frissült.</span><span class="sxs-lookup"><span data-stu-id="a8d30-974">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="a8d30-975">A Set-AzDataFactoryV2 parancsmag a RepoConfiguration beállításaihoz tartozó kiegészítő paraméterekkel lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="a8d30-975">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a8d30-976">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a8d30-976">Az.Resources</span></span>
* <span data-ttu-id="a8d30-977">Továbbfejlesztett szolgáltatókezelés a Get-AzResource esetében, -ResourceId vagy -ResourceGroupName, -Name és -ResourceType paraméterek megadásakor</span><span class="sxs-lookup"><span data-stu-id="a8d30-977">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="a8d30-978">Továbbfejlesztett hibakezelés a Test-AzDeployment és a Test-AzResourceGroupDeployment esetében</span><span class="sxs-lookup"><span data-stu-id="a8d30-978">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="a8d30-979">A hibákat nem a telepítés ellenőrzése során kezeli, hanem a parancs kimenetébe foglalja bele</span><span class="sxs-lookup"><span data-stu-id="a8d30-979">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="a8d30-980">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="a8d30-980">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="a8d30-981">-IgnoreDynamicParameters kapcsolóparaméter hozzáadása telepítési parancsmagokhoz a rendszer által feltett kérdések szkriptekben és feladatokban való mellőzéséhez</span><span class="sxs-lookup"><span data-stu-id="a8d30-981">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="a8d30-982">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="a8d30-982">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="a8d30-983">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a8d30-983">Az.Sql</span></span>
* <span data-ttu-id="a8d30-984">Adatbázisadat-besorolás támogatása.</span><span class="sxs-lookup"><span data-stu-id="a8d30-984">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a8d30-985">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a8d30-985">Az.Storage</span></span>
* <span data-ttu-id="a8d30-986">Részletes hibaüzenet megjelenítése Storage-környezet -UseConnectedAccount paraméterrel történő létrehozásakor az Azure-fiókba való bejelentkezés nélkül</span><span class="sxs-lookup"><span data-stu-id="a8d30-986">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="a8d30-987">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a8d30-987">New-AzStorageContext</span></span>
* <span data-ttu-id="a8d30-988">Adott Storage-fiók Blob service-tulajdonságai kezelésének támogatása Management plane API-val</span><span class="sxs-lookup"><span data-stu-id="a8d30-988">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="a8d30-989">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a8d30-989">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="a8d30-990">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a8d30-990">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="a8d30-991">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a8d30-991">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="a8d30-992">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a8d30-992">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="a8d30-993">Az -AsJob támogatása blobok és fájlok feltöltéséhez, valamint parancsmagok letöltéséhez</span><span class="sxs-lookup"><span data-stu-id="a8d30-993">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="a8d30-994">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a8d30-994">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="a8d30-995">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a8d30-995">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="a8d30-996">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a8d30-996">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="a8d30-997">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a8d30-997">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="a8d30-998">1.6.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="a8d30-998">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a8d30-999">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="a8d30-999">Highlights since the last major release</span></span>
* <span data-ttu-id="a8d30-1000">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="a8d30-1000">General availability of `Az` module</span></span>
* <span data-ttu-id="a8d30-1001">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="a8d30-1001">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a8d30-1002">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="a8d30-1002">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a8d30-1003">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="a8d30-1003">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a8d30-1004">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="a8d30-1004">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a8d30-1005">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="a8d30-1005">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a8d30-1006">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-1006">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a8d30-1007">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a8d30-1007">Az.Automation</span></span>
* <span data-ttu-id="a8d30-1008">Az Azure Automation frissítéskezelése módosult, hogy támogassa az alábbi új funkciókat:</span><span class="sxs-lookup"><span data-stu-id="a8d30-1008">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="a8d30-1009">Dinamikus csoportosítás</span><span class="sxs-lookup"><span data-stu-id="a8d30-1009">Dynamic grouping</span></span>
    * <span data-ttu-id="a8d30-1010">Előzetesen és utólagosan futtatandó szkriptek</span><span class="sxs-lookup"><span data-stu-id="a8d30-1010">Pre-Post script</span></span>
    * <span data-ttu-id="a8d30-1011">Újraindítási beállítás</span><span class="sxs-lookup"><span data-stu-id="a8d30-1011">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a8d30-1012">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a8d30-1012">Az.Compute</span></span>
* <span data-ttu-id="a8d30-1013">Ki lett javítva az elérési útvonal feloldásával kapcsolatos hiba a Get-AzVmBootDiagnosticsData esetében</span><span class="sxs-lookup"><span data-stu-id="a8d30-1013">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="a8d30-1014">A Compute ügyfélkódtár frissült a 25.0.0 verzióra</span><span class="sxs-lookup"><span data-stu-id="a8d30-1014">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a8d30-1015">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a8d30-1015">Az.KeyVault</span></span>
* <span data-ttu-id="a8d30-1016">Helyettesítő karakterek támogatásának hozzáadása a KeyVault-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-1016">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a8d30-1017">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a8d30-1017">Az.Network</span></span>
* <span data-ttu-id="a8d30-1018">Az Intelligens veszélyforrás-felderítés támogatásának hozzáadása az Azure Firewallhoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-1018">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="a8d30-1019">Az Application Gateway-tűzfalszabályzat legfelső szintű erőforrása és egyéni szabályok hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a8d30-1019">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a8d30-1020">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a8d30-1020">Az.RecoveryServices</span></span>
* <span data-ttu-id="a8d30-1021">A SnapshotRetentionInDays hozzáadása az Azure-beli virtuális gépek szabályzatához az azonnali RP támogatása érdekében</span><span class="sxs-lookup"><span data-stu-id="a8d30-1021">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="a8d30-1022">Folyamat támogatásának hozzáadása a regisztrációtörlési tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-1022">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="a8d30-1023">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a8d30-1023">Az.Resources</span></span>
* <span data-ttu-id="a8d30-1024">Helyettesítő karakterek támogatásának hozzáadása a Get-AzResource és Get-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="a8d30-1024">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="a8d30-1025">Az ARM általános hívása esetén használt hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="a8d30-1025">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="a8d30-1026">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a8d30-1026">Az.Sql</span></span>
* <span data-ttu-id="a8d30-1027">A Fenyegetésészlelés parancsmagjainak paramétere (ExcludeDetectionType) a DetectionType helyett string[] lett, hogy a jövőben is használható legyen az új DetectionType-ok hozzáadásakor, valamint az automatikus kitöltés támogatása érdekében.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1027">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a8d30-1028">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a8d30-1028">Az.Storage</span></span>
* <span data-ttu-id="a8d30-1029">Tárfiók felügyeleti szabályzata lekérésének/beállításának/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="a8d30-1029">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="a8d30-1030">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a8d30-1030">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a8d30-1031">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a8d30-1031">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a8d30-1032">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a8d30-1032">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a8d30-1033">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="a8d30-1033">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="a8d30-1034">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="a8d30-1034">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="a8d30-1035">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="a8d30-1035">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a8d30-1036">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a8d30-1036">Az.Websites</span></span>
* <span data-ttu-id="a8d30-1037">Ki lett javítva az ARM-sablon azon hibája, amely miatt meghiúsul az összes tárolóhely a New-AzWebApp - IncludeSourceWebAppSlots használatával történő klónozása</span><span class="sxs-lookup"><span data-stu-id="a8d30-1037">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="a8d30-1038">1.5.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="a8d30-1038">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a8d30-1039">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a8d30-1039">Az.Accounts</span></span>
* <span data-ttu-id="a8d30-1040">A Register-AzModule parancs hozzáadása az AutoRest által létrehozott parancsmagok támogatásához</span><span class="sxs-lookup"><span data-stu-id="a8d30-1040">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="a8d30-1041">A Connect-AzAccount példáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="a8d30-1041">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a8d30-1042">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a8d30-1042">Az.Automation</span></span>
* <span data-ttu-id="a8d30-1043">A bizonyos havi ütemezések lekérésekor jelentkező hiba kijavítva számos Azure Automation-parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="a8d30-1043">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="a8d30-1044">Ki lett javítva a hiba, amely miatt a Get-AzAutomationDscNode csak az első 20 csomópontot adta vissza.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1044">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="a8d30-1045">Most már az összes csomópontot visszaadja</span><span class="sxs-lookup"><span data-stu-id="a8d30-1045">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a8d30-1046">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a8d30-1046">Az.Cdn</span></span>
* <span data-ttu-id="a8d30-1047">Új Powershell-parancsmagok hozzáadva az Egyéni tartományi Https engedélyezése/letiltása szolgáltatáshoz, a régiek elavultak</span><span class="sxs-lookup"><span data-stu-id="a8d30-1047">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a8d30-1048">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a8d30-1048">Az.Compute</span></span>
* <span data-ttu-id="a8d30-1049">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-1049">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a8d30-1050">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a8d30-1050">Az.DataFactory</span></span>
* <span data-ttu-id="a8d30-1051">Az ADF .Net SDK verziója 3.0.1-re frissült</span><span class="sxs-lookup"><span data-stu-id="a8d30-1051">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a8d30-1052">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a8d30-1052">Az.LogicApp</span></span>
* <span data-ttu-id="a8d30-1053">Ki lett javítva a hiba, amely miatt a ListWorkflows csak az eredmények első oldalát kérte le</span><span class="sxs-lookup"><span data-stu-id="a8d30-1053">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a8d30-1054">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a8d30-1054">Az.Network</span></span>
* <span data-ttu-id="a8d30-1055">Helyettesítő karakterek támogatásának hozzáadása a Network-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-1055">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a8d30-1056">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a8d30-1056">Az.RecoveryServices</span></span>
* <span data-ttu-id="a8d30-1057">Azure-beli virtuális gépen futtatott SQL Server támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="a8d30-1057">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="a8d30-1058">SDK-frissítés</span><span class="sxs-lookup"><span data-stu-id="a8d30-1058">SDK Update</span></span>
* <span data-ttu-id="a8d30-1059">VMappContainer ellenőrzés eltávolítva a Get-ProtectableItem parancsmagból</span><span class="sxs-lookup"><span data-stu-id="a8d30-1059">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="a8d30-1060">Name és ServerName paraméterek hozzáadva a Get-ProtectableItem parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-1060">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="a8d30-1061">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a8d30-1061">Az.Resources</span></span>
* <span data-ttu-id="a8d30-1062">`-TemplateObject` paraméter hozzáadva az üzembe helyező parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-1062">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="a8d30-1063">További információ: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="a8d30-1063">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="a8d30-1064">Ki lett javítva a hiba, amely akkor jelentkezett, amikor a(z) `Get-AzResource` eredménye át lett irányítva a következőbe: `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="a8d30-1064">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="a8d30-1065">További információ: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="a8d30-1065">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="a8d30-1066">Ki lett javítva a JSON-adattípus módosításával kapcsolatos probléma, amely a(z) `Set-AzResource` futtatásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="a8d30-1066">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="a8d30-1067">További információ: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="a8d30-1067">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="a8d30-1068">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a8d30-1068">Az.Sql</span></span>
* <span data-ttu-id="a8d30-1069">Az AuditingEndpointsCommunicator frissítése.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1069">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="a8d30-1070">Ki lett javítva az új diagnosztikai beállítások létrehozásakor jelentkező ritka eset viselkedése.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1070">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a8d30-1071">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a8d30-1071">Az.Storage</span></span>
* <span data-ttu-id="a8d30-1072">A BlockBlobStorage altípus támogatása a Storage-fiók létrehozásakor      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a8d30-1072">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="a8d30-1073">1.4.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="a8d30-1073">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="a8d30-1074">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a8d30-1074">Az.AnalysisServices</span></span>
* <span data-ttu-id="a8d30-1075">Az AddAzureASAccount parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="a8d30-1075">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a8d30-1076">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a8d30-1076">Az.Automation</span></span>
* <span data-ttu-id="a8d30-1077">Az Import-AzAutomationDscNodeConfiguration súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="a8d30-1077">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="a8d30-1078">A konfigurációnév-ellenőrzés hozzáadva az Import-AzAutomationDscConfiguration parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-1078">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="a8d30-1079">Továbbfejlesztett hibakezelés az Import-AzAutomationDscConfiguration parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="a8d30-1079">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a8d30-1080">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a8d30-1080">Az.CognitiveServices</span></span>
* <span data-ttu-id="a8d30-1081">A CustomSubdomainName új választható paraméterként hozzáadva a New-AzCognitiveServicesAccount parancsmaghoz, amellyel altartomány adható meg az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1081">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a8d30-1082">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a8d30-1082">Az.Compute</span></span>
* <span data-ttu-id="a8d30-1083">Kijavítva az azonosító paraméterkészleteivel kapcsolatos probléma</span><span class="sxs-lookup"><span data-stu-id="a8d30-1083">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="a8d30-1084">Frissült a Get-AzVMExtension parancsmag, hogy az összes telepített bővítményt listázza, ha a Name paraméter nincs megadva</span><span class="sxs-lookup"><span data-stu-id="a8d30-1084">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="a8d30-1085">A Tag és a ResourceId paraméterek hozzáadva az Update-AzImage parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-1085">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="a8d30-1086">A Get-AzVmssVM példányazonosító nélkül, az InstanceView használatával példánynézetben listázni tudja a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1086">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a8d30-1087">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a8d30-1087">Az.DataLakeStore</span></span>
* <span data-ttu-id="a8d30-1088">Parancsmagok hozzáadása a törölt ADL-elemek enumerálásához és visszaállításához</span><span class="sxs-lookup"><span data-stu-id="a8d30-1088">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a8d30-1089">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a8d30-1089">Az.EventHub</span></span>
* <span data-ttu-id="a8d30-1090">Új SkipEmptyArchives logikai tulajdonság hozzáadva az üres archívumok kihagyásához az Eventhub CaptureDescription osztályában</span><span class="sxs-lookup"><span data-stu-id="a8d30-1090">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="a8d30-1091">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a8d30-1091">Az.KeyVault</span></span>
* <span data-ttu-id="a8d30-1092">A Set-AzKeyVaultSecret címkézésének kijavítása</span><span class="sxs-lookup"><span data-stu-id="a8d30-1092">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a8d30-1093">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a8d30-1093">Az.LogicApp</span></span>
* <span data-ttu-id="a8d30-1094">Hozzáadva az integrációs fiókok alapszintű termékváltozatában</span><span class="sxs-lookup"><span data-stu-id="a8d30-1094">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="a8d30-1095">Hozzáadva az XSLT 2.0-ban, az XSLT 3.0-ban és a Liquid leképezéstípusok esetén</span><span class="sxs-lookup"><span data-stu-id="a8d30-1095">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="a8d30-1096">Új parancsmagok az integrációs fiók szerelvényeihez</span><span class="sxs-lookup"><span data-stu-id="a8d30-1096">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="a8d30-1097">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a8d30-1097">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a8d30-1098">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a8d30-1098">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a8d30-1099">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a8d30-1099">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a8d30-1100">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a8d30-1100">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="a8d30-1101">Új parancsmagok az integrációs fiók kötegkonfigurációjához</span><span class="sxs-lookup"><span data-stu-id="a8d30-1101">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="a8d30-1102">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8d30-1102">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a8d30-1103">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8d30-1103">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a8d30-1104">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8d30-1104">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a8d30-1105">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8d30-1105">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="a8d30-1106">A Logic Apps SDK frissítése a 4.1.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="a8d30-1106">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a8d30-1107">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a8d30-1107">Az.Monitor</span></span>
* <span data-ttu-id="a8d30-1108">A Get-AzMetric súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="a8d30-1108">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a8d30-1109">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a8d30-1109">Az.Network</span></span>
* <span data-ttu-id="a8d30-1110">Az Add-AzApplicationGatewayCustomError súgójában lévő példa frissítése</span><span class="sxs-lookup"><span data-stu-id="a8d30-1110">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a8d30-1111">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a8d30-1111">Az.OperationalInsights</span></span>
* <span data-ttu-id="a8d30-1112">Kibővített támogatás a New és a Get ApplicationInsights adatforráshoz.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1112">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="a8d30-1113">Új „ApplicationInsights” altípus hozzáadva az adott munkaterület Get specific és Get all Application Insights-adatforrásainak támogatásához.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1113">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="a8d30-1114">A New-AzOperationalInsightsApplicationInsightsDataSource parancsmag hozzáadva adatforrás létrehozásához a következő Application Insights-erőforrásparaméterekkel: subscriptionId, resourceGroupName és name.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1114">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="a8d30-1115">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a8d30-1115">Az.Resources</span></span>
* <span data-ttu-id="a8d30-1116">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="a8d30-1116">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="a8d30-1117">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="a8d30-1117">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="a8d30-1118">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="a8d30-1118">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="a8d30-1119">Ki lett javítva a KeyCredentials ismételt létrehozását megakadályozó hiba</span><span class="sxs-lookup"><span data-stu-id="a8d30-1119">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="a8d30-1120">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a8d30-1120">Az.Sql</span></span>
* <span data-ttu-id="a8d30-1121">Rugalmas SQL DB-skálázási szint támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a8d30-1121">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="a8d30-1122">Ki lett javítva az a hiba, hogy a visszaállítási kérésben szereplő szükségtelen tulajdonságok megadása miatt a visszaállítás esetenként meghiúsult</span><span class="sxs-lookup"><span data-stu-id="a8d30-1122">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a8d30-1123">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a8d30-1123">Az.Websites</span></span>
* <span data-ttu-id="a8d30-1124">A Get-AzWebAppSlotMetrics példájának javítása</span><span class="sxs-lookup"><span data-stu-id="a8d30-1124">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="a8d30-1125">1.3.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="a8d30-1125">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a8d30-1126">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a8d30-1126">Az.Accounts</span></span>
* <span data-ttu-id="a8d30-1127">Frissítés a ClientRuntime legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="a8d30-1127">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a8d30-1128">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a8d30-1128">Az.AnalysisServices</span></span>
<span data-ttu-id="a8d30-1129">Az Az.AnalysisServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1129">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a8d30-1130">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a8d30-1130">Az.Compute</span></span>
* <span data-ttu-id="a8d30-1131">AEM-bővítmény: Mostantól az UltraSSD, valamint a P60, P70 és P80 lemezek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1131">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="a8d30-1132">A Set-AzVMBootDiagnostics súgóleírása frissült.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1132">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="a8d30-1133">Az Update-AzImage súgóleírása és példája frissült.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1133">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a8d30-1134">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a8d30-1134">Az.RecoveryServices</span></span>
<span data-ttu-id="a8d30-1135">Az Az.RecoveryServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1135">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a8d30-1136">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a8d30-1136">Az.Resources</span></span>
* <span data-ttu-id="a8d30-1137">Az erőforráscsoportok címkézése ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1137">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="a8d30-1138">További információ: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="a8d30-1138">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="a8d30-1139">Ki lett javítva az a hiba, amikor a `Get-AzureRmRoleAssignment` nem vette figyelembe az -ErrorAction paramétert.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1139">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="a8d30-1140">További információ: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="a8d30-1140">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="a8d30-1141">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a8d30-1141">Az.Sql</span></span>
* <span data-ttu-id="a8d30-1142">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a8d30-1142">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="a8d30-1143">Ki lett javítva az a hiba, amikor az Azure-fiókba való bejelentkezés hiánya nullref kivételt eredményezett az SQL-parancsmagok végrehajtásakor.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1143">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="a8d30-1144">A nullref kivétel ki lett javítva a Get-AzSqlCapabilityben.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1144">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="a8d30-1145">1.2.1 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="a8d30-1145">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a8d30-1146">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a8d30-1146">Az.Accounts</span></span>
* <span data-ttu-id="a8d30-1147">A hitelesítés megfelelő verziójával rendelkező kiadás</span><span class="sxs-lookup"><span data-stu-id="a8d30-1147">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a8d30-1148">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a8d30-1148">Az.AnalysisServices</span></span>
* <span data-ttu-id="a8d30-1149">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="a8d30-1149">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a8d30-1150">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a8d30-1150">Az.RecoveryServices</span></span>
* <span data-ttu-id="a8d30-1151">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="a8d30-1151">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="a8d30-1152">1.2.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="a8d30-1152">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a8d30-1153">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a8d30-1153">Az.Accounts</span></span>
* <span data-ttu-id="a8d30-1154">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="a8d30-1154">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a8d30-1155">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1155">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a8d30-1156">Az Uninstall-AzureRm figyelmeztető üzenete hozzáadva a PS Core-ban</span><span class="sxs-lookup"><span data-stu-id="a8d30-1156">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="a8d30-1157">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a8d30-1157">Az.Aks</span></span>
* <span data-ttu-id="a8d30-1158">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1158">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a8d30-1159">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a8d30-1159">Az.Automation</span></span>
* <span data-ttu-id="a8d30-1160">Mostantól támogatottak a Python 2-runbookok.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1160">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="a8d30-1161">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1161">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a8d30-1162">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a8d30-1162">Az.Cdn</span></span>
* <span data-ttu-id="a8d30-1163">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1163">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a8d30-1164">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a8d30-1164">Az.Compute</span></span>
* <span data-ttu-id="a8d30-1165">Az Invoke-AzVMReimage parancsmag hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1165">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="a8d30-1166">A TempDisk paraméter hozzá lett adva a Set-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1166">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="a8d30-1167">A New-AzVM figyelmeztető üzenete ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1167">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="a8d30-1168">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a8d30-1168">Az.ContainerRegistry</span></span>
* <span data-ttu-id="a8d30-1169">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1169">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a8d30-1170">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a8d30-1170">Az.DataFactory</span></span>
* <span data-ttu-id="a8d30-1171">Az ADF .Net SDK verziója 3.0.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1171">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a8d30-1172">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a8d30-1172">Az.DataLakeStore</span></span>
* <span data-ttu-id="a8d30-1173">Ki lett javítva az ADLS-végponttal kapcsolatos probléma az MSI használatakor.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1173">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="a8d30-1174">További információ: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="a8d30-1174">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="a8d30-1175">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1175">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a8d30-1176">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a8d30-1176">Az.IotHub</span></span>
* <span data-ttu-id="a8d30-1177">Az Encoding formátum hozzá lett adva az Add-IotHubRoutingEndpoint parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1177">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a8d30-1178">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a8d30-1178">Az.KeyVault</span></span>
* <span data-ttu-id="a8d30-1179">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1179">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a8d30-1180">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a8d30-1180">Az.Network</span></span>
* <span data-ttu-id="a8d30-1181">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1181">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="a8d30-1182">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a8d30-1182">Az.Resources</span></span>
* <span data-ttu-id="a8d30-1183">A helytelen példák ki lettek javítva a New-AzADAppCredential és a New-AzADSpCredential referenciadokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1183">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="a8d30-1184">Ki lett javítva az a hiba, amikor a -TemplateFile paraméter nem lett feloldva az erőforráscsoportokat üzembe helyező parancsmagok végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1184">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="a8d30-1185">Az.Resources: A New-AzureRmPolicyDefinition -Mode alapértelmezett értékének dokumentációja ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1185">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="a8d30-1186">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="a8d30-1186">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="a8d30-1187">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="a8d30-1187">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="a8d30-1188">Ki lett javítva a „PSResourceGroupDeployment” objektum formázásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1188">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="a8d30-1189">További információ: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="a8d30-1189">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a8d30-1190">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a8d30-1190">Az.ServiceFabric</span></span>
* <span data-ttu-id="a8d30-1191">Visszaállítás a VMSS-modell tanúsítványának hozzáadásakor bekövetkező kivétel-visszaadás esetén; javított hiba: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1191">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="a8d30-1192">Bizonyos hibaüzenetek ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1192">Fix some error messages.</span></span>
* <span data-ttu-id="a8d30-1193">Ki lett javítva az alapértelmezett ARM-sablonnal való fürtlétrehozás a New-AzServiceFabriCluster esetében, amely nem működött az Az-ba történő migrálással.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1193">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="a8d30-1194">Ki lett javítva a fürt-/alkalmazástanúsítvány létrehozása, így mostantól csak a fürtnek megfelelő virtuálisgép-méretezési csoportokhoz (Virtual Machine Scale Sets) lesznek hozzáadva, a fürtazonosító bővítményben való ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1194">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a8d30-1195">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a8d30-1195">Az.SignalR</span></span>
* <span data-ttu-id="a8d30-1196">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1196">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="a8d30-1197">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a8d30-1197">Az.Sql</span></span>
* <span data-ttu-id="a8d30-1198">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1198">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a8d30-1199">A LicenseType paraméter paraméterleírása frissítve lett a lehetséges értékekkel.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1199">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="a8d30-1200">Ki lett javítva az a hiba, amikor egy felügyelt példány identitásának frissítése nem működött, ha az volt az egyetlen frissített tulajdonság.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1200">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="a8d30-1201">Egyéni rendezések támogatása a felügyelt példányokon</span><span class="sxs-lookup"><span data-stu-id="a8d30-1201">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a8d30-1202">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a8d30-1202">Az.Storage</span></span>
* <span data-ttu-id="a8d30-1203">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1203">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a8d30-1204">Részletes hibaüzenet megjelenítése klasszikus naplózás/metrika get/set műveletei esetében a prémium szintű Storage-fiókon, mivel a prémium szintű Storage-fiók nem támogatja a klasszikus naplózást/metrikát.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1204">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="a8d30-1205">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="a8d30-1205">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="a8d30-1206">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="a8d30-1206">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="a8d30-1207">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a8d30-1207">Az.TrafficManager</span></span>
* <span data-ttu-id="a8d30-1208">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1208">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a8d30-1209">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a8d30-1209">Az.Websites</span></span>
* <span data-ttu-id="a8d30-1210">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1210">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a8d30-1211">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól a megfelelő erőforráscsoportba és helyre tölti fel a tanúsítványt, ha az alkalmazás ASE-n üzemel.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1211">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="a8d30-1212">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól nem írja felül a címkéket SSL-tanúsítvány alkalmazáshoz való kötésekor.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1212">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="a8d30-1213">1.1.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="a8d30-1213">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a8d30-1214">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a8d30-1214">Az.Accounts</span></span>
* <span data-ttu-id="a8d30-1215">A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-1215">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a8d30-1216">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a8d30-1216">Az.Compute</span></span>
* <span data-ttu-id="a8d30-1217">A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni</span><span class="sxs-lookup"><span data-stu-id="a8d30-1217">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="a8d30-1218">Frissült az azonosító leírása a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="a8d30-1218">Updated the description of ID in help files</span></span>
* <span data-ttu-id="a8d30-1219">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="a8d30-1219">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a8d30-1220">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a8d30-1220">Az.DataLakeStore</span></span>
* <span data-ttu-id="a8d30-1221">A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1221">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="a8d30-1222">A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva</span><span class="sxs-lookup"><span data-stu-id="a8d30-1222">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a8d30-1223">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a8d30-1223">Az.EventGrid</span></span>
* <span data-ttu-id="a8d30-1224">Frissítve a 2019-01-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1224">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="a8d30-1225">A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához</span><span class="sxs-lookup"><span data-stu-id="a8d30-1225">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="a8d30-1226">New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="a8d30-1226">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="a8d30-1227">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="a8d30-1227">Event Time-To-Live,</span></span>
        - <span data-ttu-id="a8d30-1228">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="a8d30-1228">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="a8d30-1229">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1229">Dead letter endpoint.</span></span>
    - <span data-ttu-id="a8d30-1230">Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="a8d30-1230">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="a8d30-1231">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="a8d30-1231">Event Time-To-Live,</span></span>
        - <span data-ttu-id="a8d30-1232">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="a8d30-1232">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="a8d30-1233">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1233">Dead letter endpoint.</span></span>
* <span data-ttu-id="a8d30-1234">Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1234">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="a8d30-1235">Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1235">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a8d30-1236">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a8d30-1236">Az.IotHub</span></span>
* <span data-ttu-id="a8d30-1237">Frissítve az IoT Hub SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="a8d30-1237">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a8d30-1238">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a8d30-1238">Az.LogicApp</span></span>
* <span data-ttu-id="a8d30-1239">A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel</span><span class="sxs-lookup"><span data-stu-id="a8d30-1239">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="a8d30-1240">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a8d30-1240">Az.Resources</span></span>
* <span data-ttu-id="a8d30-1241">Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="a8d30-1241">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="a8d30-1242">További információ: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="a8d30-1242">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="a8d30-1243">Ki lett javítva a -Custom paraméter kezelése a New/Set-AzPolicyDefinition parancsban</span><span class="sxs-lookup"><span data-stu-id="a8d30-1243">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="a8d30-1244">Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="a8d30-1244">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="a8d30-1245">A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében</span><span class="sxs-lookup"><span data-stu-id="a8d30-1245">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="a8d30-1246">További információ: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="a8d30-1246">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a8d30-1247">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a8d30-1247">Az.SignalR</span></span>
* <span data-ttu-id="a8d30-1248">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="a8d30-1248">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="a8d30-1249">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a8d30-1249">Az.Sql</span></span>
* <span data-ttu-id="a8d30-1250">A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1250">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a8d30-1251">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a8d30-1251">Az.Storage</span></span>
* <span data-ttu-id="a8d30-1252">A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva</span><span class="sxs-lookup"><span data-stu-id="a8d30-1252">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="a8d30-1253">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a8d30-1253">New-AzStorageContext</span></span>
* <span data-ttu-id="a8d30-1254">A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz</span><span class="sxs-lookup"><span data-stu-id="a8d30-1254">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="a8d30-1255">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="a8d30-1255">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a8d30-1256">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a8d30-1256">Az.Websites</span></span>
* <span data-ttu-id="a8d30-1257">Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban</span><span class="sxs-lookup"><span data-stu-id="a8d30-1257">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="a8d30-1258">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="a8d30-1258">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="a8d30-1259">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="a8d30-1259">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="a8d30-1260">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="a8d30-1260">General</span></span>

- <span data-ttu-id="a8d30-1261">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="a8d30-1261">General Availability of Az Module</span></span>
- <span data-ttu-id="a8d30-1262">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-1262">Online help for each module</span></span>
- <span data-ttu-id="a8d30-1263">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="a8d30-1263">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="a8d30-1264">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a8d30-1264">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="a8d30-1265">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a8d30-1265">Az.Accounts</span></span>
- <span data-ttu-id="a8d30-1266">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="a8d30-1266">Changed from Az.Profile</span></span>
- <span data-ttu-id="a8d30-1267">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-1267">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="a8d30-1268">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a8d30-1268">Az.ApiManagement</span></span>
- <span data-ttu-id="a8d30-1269">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="a8d30-1269">Fixes for #7002</span></span>
- <span data-ttu-id="a8d30-1270">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a8d30-1270">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="a8d30-1271">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a8d30-1271">Az.Batch</span></span>
- <span data-ttu-id="a8d30-1272">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1272">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="a8d30-1273">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1273">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="a8d30-1274">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a8d30-1274">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="a8d30-1275">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="a8d30-1275">Az.Billing</span></span>
- <span data-ttu-id="a8d30-1276">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1276">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="a8d30-1277">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="a8d30-1277">Az.CognitivServices</span></span>
- <span data-ttu-id="a8d30-1278">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1278">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="a8d30-1279">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1279">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="a8d30-1280">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a8d30-1280">Az.ContainerInstance</span></span>
- <span data-ttu-id="a8d30-1281">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="a8d30-1281">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="a8d30-1282">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="a8d30-1282">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="a8d30-1283">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a8d30-1283">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="a8d30-1284">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a8d30-1284">Az.DataLakeStore</span></span>
- <span data-ttu-id="a8d30-1285">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a8d30-1285">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="a8d30-1286">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a8d30-1286">Az.Monitor</span></span>
- <span data-ttu-id="a8d30-1287">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a8d30-1287">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="a8d30-1288">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a8d30-1288">Az.KeyVault</span></span>
- <span data-ttu-id="a8d30-1289">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1289">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="a8d30-1290">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a8d30-1290">Az.MachineLearning</span></span>
- <span data-ttu-id="a8d30-1291">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="a8d30-1291">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="a8d30-1292">Az.Media</span><span class="sxs-lookup"><span data-stu-id="a8d30-1292">Az.Media</span></span>
- <span data-ttu-id="a8d30-1293">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="a8d30-1293">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="a8d30-1294">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a8d30-1294">Az.Network</span></span>
<span data-ttu-id="a8d30-1295">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1295">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="a8d30-1296">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="a8d30-1296">New cmdlets added:</span></span>
        - <span data-ttu-id="a8d30-1297">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a8d30-1297">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a8d30-1298">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a8d30-1298">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a8d30-1299">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a8d30-1299">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a8d30-1300">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a8d30-1300">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a8d30-1301">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a8d30-1301">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a8d30-1302">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="a8d30-1302">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="a8d30-1303">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="a8d30-1303">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="a8d30-1304">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8d30-1304">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="a8d30-1305">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a8d30-1305">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="a8d30-1306">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a8d30-1306">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="a8d30-1307">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a8d30-1307">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="a8d30-1308">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a8d30-1308">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="a8d30-1309">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a8d30-1309">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="a8d30-1310">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a8d30-1310">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="a8d30-1311">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1311">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="a8d30-1312">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a8d30-1312">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="a8d30-1313">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a8d30-1313">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="a8d30-1314">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a8d30-1314">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="a8d30-1315">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a8d30-1315">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="a8d30-1316">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="a8d30-1316">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="a8d30-1317">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a8d30-1317">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="a8d30-1318">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a8d30-1318">Az.OperationalInsights</span></span>
- <span data-ttu-id="a8d30-1319">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a8d30-1319">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="a8d30-1320">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a8d30-1320">Az.Profile</span></span>
- <span data-ttu-id="a8d30-1321">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a8d30-1321">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="a8d30-1322">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a8d30-1322">Az.RecoveryServices</span></span>
- <span data-ttu-id="a8d30-1323">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a8d30-1323">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="a8d30-1324">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a8d30-1324">Az.Resources</span></span>
- <span data-ttu-id="a8d30-1325">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a8d30-1325">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="a8d30-1326">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a8d30-1326">Az.ServiceFabric</span></span>
- <span data-ttu-id="a8d30-1327">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="a8d30-1327">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="a8d30-1328">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a8d30-1328">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="a8d30-1329">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="a8d30-1329">Az.SIgnalR</span></span>
- <span data-ttu-id="a8d30-1330">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="a8d30-1330">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="a8d30-1331">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a8d30-1331">Az.Sql</span></span>
- <span data-ttu-id="a8d30-1332">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-1332">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="a8d30-1333">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="a8d30-1333">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="a8d30-1334">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a8d30-1334">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="a8d30-1335">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a8d30-1335">Az.Storage</span></span>
- <span data-ttu-id="a8d30-1336">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a8d30-1336">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="a8d30-1337">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a8d30-1337">Az.Websites</span></span>
- <span data-ttu-id="a8d30-1338">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="a8d30-1338">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="a8d30-1339">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="a8d30-1339">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="a8d30-1340">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="a8d30-1340">General</span></span>

* <span data-ttu-id="a8d30-1341">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="a8d30-1341">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="a8d30-1342">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a8d30-1342">Az.Compute</span></span>

* <span data-ttu-id="a8d30-1343">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1343">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="a8d30-1344">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a8d30-1344">Az.DataLakeStore</span></span>

* <span data-ttu-id="a8d30-1345">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="a8d30-1345">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="a8d30-1346">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a8d30-1346">Az.FrontDoor</span></span>

* <span data-ttu-id="a8d30-1347">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="a8d30-1347">Fixed some broken links</span></span>
    - <span data-ttu-id="a8d30-1348">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1348">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="a8d30-1349">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1349">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="a8d30-1350">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a8d30-1350">Az.RecoveryServices</span></span>

* <span data-ttu-id="a8d30-1351">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1351">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="a8d30-1352">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1352">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="a8d30-1353">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a8d30-1353">Az.Resources</span></span>

* <span data-ttu-id="a8d30-1354">https://github.com/Azure/azure-powershell/issues/7679 javítása</span><span class="sxs-lookup"><span data-stu-id="a8d30-1354">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="a8d30-1355">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1355">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="a8d30-1356">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a8d30-1356">Az.Sql</span></span>

* <span data-ttu-id="a8d30-1357">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="a8d30-1357">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="a8d30-1358">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="a8d30-1358">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="a8d30-1359">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1359">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="a8d30-1360">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a8d30-1360">Az.Storage</span></span>

* <span data-ttu-id="a8d30-1361">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-1361">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="a8d30-1362">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1362">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="a8d30-1363">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a8d30-1363">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="a8d30-1364">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="a8d30-1364">Support Static Website configuration</span></span>
    - <span data-ttu-id="a8d30-1365">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a8d30-1365">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="a8d30-1366">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a8d30-1366">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="a8d30-1367">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a8d30-1367">Az.Websites</span></span>

* <span data-ttu-id="a8d30-1368">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a8d30-1368">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="a8d30-1369">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1369">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="a8d30-1370">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1370">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="a8d30-1371">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="a8d30-1371">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="a8d30-1372">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a8d30-1372">Az.ApiManagement</span></span>
* <span data-ttu-id="a8d30-1373">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1373">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="a8d30-1374">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a8d30-1374">Az.Automation</span></span>
* <span data-ttu-id="a8d30-1375">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1375">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="a8d30-1376">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1376">Added Update Management cmdlets</span></span>
* <span data-ttu-id="a8d30-1377">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1377">Added Source Control cmdlets</span></span>
* <span data-ttu-id="a8d30-1378">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1378">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="a8d30-1379">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1379">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="a8d30-1380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a8d30-1380">Az.Compute</span></span>
* <span data-ttu-id="a8d30-1381">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1381">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="a8d30-1382">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1382">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="a8d30-1383">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a8d30-1383">Az.ContainerInstance</span></span>
* <span data-ttu-id="a8d30-1384">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1384">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="a8d30-1385">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a8d30-1385">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="a8d30-1386">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1386">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="a8d30-1387">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a8d30-1387">Az.Network</span></span>
* <span data-ttu-id="a8d30-1388">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1388">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="a8d30-1389">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1389">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="a8d30-1390">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1390">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="a8d30-1391">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1391">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="a8d30-1392">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a8d30-1392">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a8d30-1393">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1393">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="a8d30-1394">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1394">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="a8d30-1395">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="a8d30-1395">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="a8d30-1396">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1396">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="a8d30-1397">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1397">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="a8d30-1398">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="a8d30-1398">Az.Relay</span></span>
* <span data-ttu-id="a8d30-1399">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1399">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="a8d30-1400">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a8d30-1400">Az.Resources</span></span>
* <span data-ttu-id="a8d30-1401">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1401">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="a8d30-1402">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1402">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="a8d30-1403">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1403">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="a8d30-1404">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a8d30-1404">Az.ServiceFabric</span></span>
* <span data-ttu-id="a8d30-1405">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1405">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="a8d30-1406">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a8d30-1406">Az.Sql</span></span>
* <span data-ttu-id="a8d30-1407">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1407">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="a8d30-1408">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a8d30-1408">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a8d30-1409">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a8d30-1409">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a8d30-1410">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a8d30-1410">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a8d30-1411">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a8d30-1411">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a8d30-1412">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a8d30-1412">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a8d30-1413">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a8d30-1413">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a8d30-1414">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a8d30-1414">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a8d30-1415">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a8d30-1415">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="a8d30-1416">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1416">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="a8d30-1417">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1417">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="a8d30-1418">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1418">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="a8d30-1419">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1419">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="a8d30-1420">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1420">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="a8d30-1421">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1421">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="a8d30-1422">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1422">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="a8d30-1423">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1423">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="a8d30-1424">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="a8d30-1424">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a8d30-1425">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="a8d30-1425">General</span></span>
* <span data-ttu-id="a8d30-1426">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1426">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="a8d30-1427">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a8d30-1427">Az.Profile</span></span>
* <span data-ttu-id="a8d30-1428">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1428">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="a8d30-1429">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="a8d30-1429">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="a8d30-1430">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="a8d30-1430">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="a8d30-1431">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="a8d30-1431">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="a8d30-1432">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="a8d30-1432">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="a8d30-1433">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="a8d30-1433">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="a8d30-1434">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="a8d30-1434">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="a8d30-1435">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a8d30-1435">Az.CognitiveServices</span></span>
* <span data-ttu-id="a8d30-1436">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1436">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a8d30-1437">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a8d30-1437">Az.Compute</span></span>
* <span data-ttu-id="a8d30-1438">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="a8d30-1438">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="a8d30-1439">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="a8d30-1439">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="a8d30-1440">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1440">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a8d30-1441">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a8d30-1441">Az.DataLakeStore</span></span>
* <span data-ttu-id="a8d30-1442">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1442">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="a8d30-1443">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1443">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="a8d30-1444">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="a8d30-1444">Az.Insights</span></span>
* <span data-ttu-id="a8d30-1445">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="a8d30-1445">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="a8d30-1446">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="a8d30-1446">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="a8d30-1447">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="a8d30-1447">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="a8d30-1448">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="a8d30-1448">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a8d30-1449">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a8d30-1449">Az.Network</span></span>
* <span data-ttu-id="a8d30-1450">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="a8d30-1450">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="a8d30-1451">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="a8d30-1451">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="a8d30-1452">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="a8d30-1452">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="a8d30-1453">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a8d30-1453">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="a8d30-1454">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="a8d30-1454">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="a8d30-1455">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="a8d30-1455">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="a8d30-1456">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a8d30-1456">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a8d30-1457">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a8d30-1457">Az.PolicyInsights</span></span>
* <span data-ttu-id="a8d30-1458">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a8d30-1458">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="a8d30-1459">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a8d30-1459">Az.Resources</span></span>
* <span data-ttu-id="a8d30-1460">https://github.com/Azure/azure-powershell/issues/7402 javítása</span><span class="sxs-lookup"><span data-stu-id="a8d30-1460">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="a8d30-1461">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="a8d30-1461">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a8d30-1462">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a8d30-1462">Az.ServiceBus</span></span>
* <span data-ttu-id="a8d30-1463">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1463">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a8d30-1464">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a8d30-1464">Az.ServiceFabric</span></span>
* <span data-ttu-id="a8d30-1465">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1465">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="a8d30-1466">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="a8d30-1466">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="a8d30-1467">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="a8d30-1467">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="a8d30-1468">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="a8d30-1468">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="a8d30-1469">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1469">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="a8d30-1470">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="a8d30-1470">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="a8d30-1471">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a8d30-1471">Az.Profile</span></span>
* <span data-ttu-id="a8d30-1472">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1472">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="a8d30-1473">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1473">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a8d30-1474">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a8d30-1474">Az.Compute</span></span>
* <span data-ttu-id="a8d30-1475">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1475">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="a8d30-1476">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1476">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a8d30-1477">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a8d30-1477">Az.DataLakeStore</span></span>
* <span data-ttu-id="a8d30-1478">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="a8d30-1478">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="a8d30-1479">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1479">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="a8d30-1480">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1480">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a8d30-1481">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1481">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a8d30-1482">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1482">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a8d30-1483">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a8d30-1483">Az.Network</span></span>
* <span data-ttu-id="a8d30-1484">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1484">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="a8d30-1485">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1485">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a8d30-1486">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a8d30-1486">Az.Resources</span></span>
* <span data-ttu-id="a8d30-1487">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="a8d30-1487">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="a8d30-1488">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1488">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="a8d30-1489">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="a8d30-1489">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="a8d30-1490">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a8d30-1490">Azure.Storage</span></span>
* <span data-ttu-id="a8d30-1491">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="a8d30-1491">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="a8d30-1492">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a8d30-1492">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="a8d30-1493">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a8d30-1493">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="a8d30-1494">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1494">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="a8d30-1495">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="a8d30-1495">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="a8d30-1496">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a8d30-1496">Az.CognitiveServices</span></span>
* <span data-ttu-id="a8d30-1497">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1497">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a8d30-1498">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a8d30-1498">Az.Compute</span></span>
* <span data-ttu-id="a8d30-1499">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1499">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="a8d30-1500">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1500">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="a8d30-1501">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="a8d30-1501">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="a8d30-1502">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a8d30-1502">Az.DataFactoryV2</span></span>
* <span data-ttu-id="a8d30-1503">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1503">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a8d30-1504">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a8d30-1504">Az.Network</span></span>
* <span data-ttu-id="a8d30-1505">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1505">Added NetworkProfile functionality.</span></span> <span data-ttu-id="a8d30-1506">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a8d30-1506">new cmdlets added</span></span>
    - <span data-ttu-id="a8d30-1507">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a8d30-1507">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="a8d30-1508">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a8d30-1508">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="a8d30-1509">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a8d30-1509">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="a8d30-1510">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a8d30-1510">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="a8d30-1511">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="a8d30-1511">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="a8d30-1512">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="a8d30-1512">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="a8d30-1513">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="a8d30-1513">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="a8d30-1514">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="a8d30-1514">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="a8d30-1515">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="a8d30-1515">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a8d30-1516">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a8d30-1516">Az.RedisCache</span></span>
* <span data-ttu-id="a8d30-1517">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="a8d30-1517">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="a8d30-1518">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-1518">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="a8d30-1519">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a8d30-1519">Az.Resources</span></span>
* <span data-ttu-id="a8d30-1520">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a8d30-1520">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="a8d30-1521">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="a8d30-1521">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="a8d30-1522">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a8d30-1522">Az.Sql</span></span>
* <span data-ttu-id="a8d30-1523">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="a8d30-1523">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a8d30-1524">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a8d30-1524">Az.Websites</span></span>
* <span data-ttu-id="a8d30-1525">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="a8d30-1525">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="a8d30-1526">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="a8d30-1526">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="a8d30-1527">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="a8d30-1527">0.2.0 - September 2018</span></span>
 <span data-ttu-id="a8d30-1528">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="a8d30-1528">Initial Release</span></span>
