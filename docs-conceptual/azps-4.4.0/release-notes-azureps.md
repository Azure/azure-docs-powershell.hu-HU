---
title: Az Azure PowerShell kibocsátási megjegyzései
description: Megismerheti az Azure PowerShell-modulok legújabb frissítéseit.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: 88e9c622ef3608b17e6cd8d4ce8c193812a97520
ms.sourcegitcommit: 23e5b2b0751777ef0a5ca74e40c7772653e339a3
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/14/2020
ms.locfileid: "86382174"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="773db-103">Az Azure PowerShell kibocsátási megjegyzései</span><span class="sxs-lookup"><span data-stu-id="773db-103">Azure PowerShell release notes</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="773db-104">4.4.0 – 2020. július</span><span class="sxs-lookup"><span data-stu-id="773db-104">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="773db-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="773db-105">Az.Accounts</span></span>
* <span data-ttu-id="773db-106">Invoke-AzRestMethod új parancsmag hozzáadása</span><span class="sxs-lookup"><span data-stu-id="773db-106">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="773db-107">Kijavítottunk egy olyan problémát, amely hitelesítési hibákat okozhat az olyan többfolyamatos forgatókönyvekben, mint például több Azure PowerShell parancsmag futtatása a Start-Job paranccsal [#9448]</span><span class="sxs-lookup"><span data-stu-id="773db-107">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="773db-108">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="773db-108">Az.Aks</span></span>
* <span data-ttu-id="773db-109">Ki lett javítva az a hiba, amely miatt a Get-AzAks nem kér le minden fürtöt [#12296]</span><span class="sxs-lookup"><span data-stu-id="773db-109">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="773db-110">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="773db-110">Az.AnalysisServices</span></span>
* <span data-ttu-id="773db-111">A hitelesítés projekthivatkozása eltávolítva</span><span class="sxs-lookup"><span data-stu-id="773db-111">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="773db-112">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="773db-112">Az.Automation</span></span>
* <span data-ttu-id="773db-113">Ki lett javítva az a hiba, amely miatt a feloldójeleket tartalmazó sztringek nem alakíthatók át JSON-objektummá.</span><span class="sxs-lookup"><span data-stu-id="773db-113">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="773db-114">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-114">Az.Compute</span></span>
* <span data-ttu-id="773db-115">Figyelmeztetés jelenik meg a New-AzVmss a „latest” rendszerképverzió nélküli használatakor</span><span class="sxs-lookup"><span data-stu-id="773db-115">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="773db-116">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="773db-116">Az.DataFactory</span></span>
* <span data-ttu-id="773db-117">Globális paraméterek hozzáadva a Data Factoryhez.</span><span class="sxs-lookup"><span data-stu-id="773db-117">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="773db-118">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="773db-118">Az.EventGrid</span></span>
* <span data-ttu-id="773db-119">Frissítve a 2020-06-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="773db-119">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="773db-120">Új funkciók hozzáadva:</span><span class="sxs-lookup"><span data-stu-id="773db-120">Added new features:</span></span>
    - <span data-ttu-id="773db-121">Bemenetleképezés</span><span class="sxs-lookup"><span data-stu-id="773db-121">Input mapping</span></span>
    - <span data-ttu-id="773db-122">Eseménykézbesítési séma</span><span class="sxs-lookup"><span data-stu-id="773db-122">Event Delivery Schema</span></span>
    - <span data-ttu-id="773db-123">Privát kapcsolat</span><span class="sxs-lookup"><span data-stu-id="773db-123">Private Link</span></span>
    - <span data-ttu-id="773db-124">V10 felhő-eseményséma</span><span class="sxs-lookup"><span data-stu-id="773db-124">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="773db-125">Service Bus-témakör célértékként</span><span class="sxs-lookup"><span data-stu-id="773db-125">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="773db-126">Azure-függvény célértékként</span><span class="sxs-lookup"><span data-stu-id="773db-126">Azure Function As Destination</span></span>
    - <span data-ttu-id="773db-127">Webhookkötegelés</span><span class="sxs-lookup"><span data-stu-id="773db-127">WebHook Batching</span></span>
    - <span data-ttu-id="773db-128">Biztonságos webhook (AAD-támogatás)</span><span class="sxs-lookup"><span data-stu-id="773db-128">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="773db-129">IP-szűrés</span><span class="sxs-lookup"><span data-stu-id="773db-129">IpFiltering</span></span>
* <span data-ttu-id="773db-130">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="773db-130">Updated cmdlets:</span></span>
    - <span data-ttu-id="773db-131">New-AzEventGridSubscription/Update-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="773db-131">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="773db-132">Új választható paraméterek lettek hozzáadva a webhookkötegelés támogatásáért.</span><span class="sxs-lookup"><span data-stu-id="773db-132">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="773db-133">Új választható paraméterek lettek hozzáadva a biztonságos webhook AAD-vel való használatának támogatásáért.</span><span class="sxs-lookup"><span data-stu-id="773db-133">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="773db-134">Új felsorolási érték lett hozzáadva az EndpointType paraméterhez az Azure-függvény és a Service Bus-témakör új célértékként való támogatásáért.</span><span class="sxs-lookup"><span data-stu-id="773db-134">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="773db-135">Új választható paraméter lett hozzáadva a kézbesítési sémához.</span><span class="sxs-lookup"><span data-stu-id="773db-135">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="773db-136">New-AzEventGridTopic/Update-AzEventGridTopic és New-AzEventGridDomain/Update-AzEventGridDomain:</span><span class="sxs-lookup"><span data-stu-id="773db-136">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="773db-137">Új választható paraméterek lettek hozzáadva az IP-szűrés támogatásáért.</span><span class="sxs-lookup"><span data-stu-id="773db-137">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="773db-138">New-AzEventGridTopic/New-AzEventGridDomain:</span><span class="sxs-lookup"><span data-stu-id="773db-138">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="773db-139">Új választható paraméterek lettek hozzáadva a bemenetleképezés támogatásáért.</span><span class="sxs-lookup"><span data-stu-id="773db-139">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="773db-140">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="773db-140">Az.FrontDoor</span></span>
* <span data-ttu-id="773db-141">Modul frissítve a 2020-05-01-es API-verzió használatára</span><span class="sxs-lookup"><span data-stu-id="773db-141">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="773db-142">Privátkapcsolat-támogatás hozzáadva a Storage-, KeyVault- és Web App Service-erőforrásokhoz</span><span class="sxs-lookup"><span data-stu-id="773db-142">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="773db-143">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="773db-143">Az.HDInsight</span></span>
* <span data-ttu-id="773db-144">ADLSGen1/2-tárolóval rendelkező fürt országos felhőkben való létrehozásának támogatása.</span><span class="sxs-lookup"><span data-stu-id="773db-144">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="773db-145">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="773db-145">Az.Monitor</span></span>
* <span data-ttu-id="773db-146">Ki lett javítva a Get-AzDiagnosticSetting hibája, amely miatt a metrikák vagy naplók null értékűek [#12272]</span><span class="sxs-lookup"><span data-stu-id="773db-146">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="773db-147">Az.Network</span><span class="sxs-lookup"><span data-stu-id="773db-147">Az.Network</span></span>
* <span data-ttu-id="773db-148">A paraméterek felcserélése ki lett javítva a VWan–HubVnet kapcsolatban</span><span class="sxs-lookup"><span data-stu-id="773db-148">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="773db-149">Új parancsmagok lettek hozzáadva az Azure hálózati virtuális berendezések helyéhez</span><span class="sxs-lookup"><span data-stu-id="773db-149">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="773db-150">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="773db-150">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="773db-151">New-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="773db-151">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="773db-152">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="773db-152">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="773db-153">Update-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="773db-153">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="773db-154">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="773db-154">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="773db-155">Új parancsmagok lettek hozzáadva az Azure hálózati virtuális berendezésekhez</span><span class="sxs-lookup"><span data-stu-id="773db-155">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="773db-156">Get-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="773db-156">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="773db-157">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="773db-157">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="773db-158">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="773db-158">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="773db-159">Update-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="773db-159">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="773db-160">Get-AzNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="773db-160">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="773db-161">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="773db-161">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="773db-162">Application Gateway előkészítve a Private Link gyakori parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="773db-162">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="773db-163">StorageSync előkészítve a Private Link gyakori parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="773db-163">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="773db-164">SignalR előkészítve a Private Link gyakori parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="773db-164">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="773db-165">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="773db-165">Az.RecoveryServices</span></span>
* <span data-ttu-id="773db-166">A hitelesítés projekthivatkozása eltávolítva</span><span class="sxs-lookup"><span data-stu-id="773db-166">Removed project reference to Authentication</span></span>
* <span data-ttu-id="773db-167">Azure Backup-parancsmagok finomhangolása a pontosabb szövegért.</span><span class="sxs-lookup"><span data-stu-id="773db-167">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="773db-168">Az Azure Backup mostantól támogatott az MAB-ügynökfeladatok beolvasásához a Get-AzRecoveryServicesBackupJob parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="773db-168">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="773db-169">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-169">Az.Resources</span></span>
* <span data-ttu-id="773db-170">A Save-AzResourceGroupDeploymentTemplate frissítése az SDK használatához.</span><span class="sxs-lookup"><span data-stu-id="773db-170">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="773db-171">Unregister-AzResourceProvider parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="773db-171">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="773db-172">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-172">Az.Sql</span></span>
* <span data-ttu-id="773db-173">Szolgáltatásnév és vendégfelhasználók támogatása hozzáadva a Set-AzSqlInstanceActiveDirectoryAdministrator parancsmagban</span><span class="sxs-lookup"><span data-stu-id="773db-173">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="773db-174">Ki lett javítva egy hiba az adatbesorolási parancsmagokban.</span><span class="sxs-lookup"><span data-stu-id="773db-174">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="773db-175">A felügyelt Azure SQL-példány feladatátvétele mostantól támogatott: Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="773db-175">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="773db-176">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="773db-176">Az.Storage</span></span>
* <span data-ttu-id="773db-177">Ki lett javítva az a probléma, amely miatt a UserAgent nem adható hozzá egyes adatsíkparancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="773db-177">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="773db-178">Storage-fiók létrehozásának/frissítésének támogatása a MinimumTlsVersion és az AllowBlobPublicAccess használatával</span><span class="sxs-lookup"><span data-stu-id="773db-178">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="773db-179">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="773db-179">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="773db-180">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="773db-180">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="773db-181">A Storage-fiókok Blob service-beli verziószámozása engedélyezésének/letiltásának támogatása</span><span class="sxs-lookup"><span data-stu-id="773db-181">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="773db-182">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="773db-182">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="773db-183">Blobok blobverziókkal való listázásának támogatása</span><span class="sxs-lookup"><span data-stu-id="773db-183">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="773db-184">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="773db-184">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="773db-185">Egyetlen blobpillanatkép vagy blobverzió lekérésének/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="773db-185">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="773db-186">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="773db-186">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="773db-187">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="773db-187">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="773db-188">Az Azure.Storage.Blobs 12-es verziójában létrehozott blobobjektum folyamatának támogatása</span><span class="sxs-lookup"><span data-stu-id="773db-188">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="773db-189">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="773db-189">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="773db-190">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="773db-190">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="773db-191">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="773db-191">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="773db-192">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="773db-192">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="773db-193">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="773db-193">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="773db-194">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="773db-194">Az.StorageSync</span></span>
* <span data-ttu-id="773db-195">A 2020-03-01-es API-verziót célzó StorageSync SDK új verziója hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-195">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="773db-196">Tárolószinkronizálási szolgáltatás frissítési parancsmagja hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-196">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="773db-197">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="773db-197">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="773db-198">IncomingTrafficPolicy és PrivateEndpointConnections hozzáadva a StorageSyncService parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="773db-198">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="773db-199">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="773db-199">Az.Websites</span></span>
* <span data-ttu-id="773db-200">Támogatás hozzáadva az olyan Pontok műveleteinek elvégzéséhez, amelyek nem abban az erőforráscsoportban vannak, amelyben az App Service-csomag</span><span class="sxs-lookup"><span data-stu-id="773db-200">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="773db-201">4.3.0 – 2020. június</span><span class="sxs-lookup"><span data-stu-id="773db-201">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="773db-202">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="773db-202">Az.Accounts</span></span>
* <span data-ttu-id="773db-203">A környezetfelderítés beállítása és a környezet hozzáadása az Add-AzEnvironment használatával alapértelmezés szerint támogatott</span><span class="sxs-lookup"><span data-stu-id="773db-203">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="773db-204">Előre betöltött szerelvények frissítése [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="773db-204">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="773db-205">Az Azure.Core szerelvény frissült</span><span class="sxs-lookup"><span data-stu-id="773db-205">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="773db-206">Ki lett javítva egy probléma, amely a Connect-AzAccount meghiúsulását okozhatta többszálas végrehajtás esetében [#11201]</span><span class="sxs-lookup"><span data-stu-id="773db-206">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="773db-207">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="773db-207">Az.Aks</span></span>
* <span data-ttu-id="773db-208">A régi [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) használata helyébe a [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) és a [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) API-k meghívása lépett</span><span class="sxs-lookup"><span data-stu-id="773db-208">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="773db-209">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="773db-209">Az.Batch</span></span>
* <span data-ttu-id="773db-210">Frissítve lett az Az.Batch a Microsoft.Azure.Management.Batch SDK 11.0.0-s verziójának használatára</span><span class="sxs-lookup"><span data-stu-id="773db-210">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="773db-211">Hozzá lett adva a BatchAccount identitás beállításának lehetősége a New-AzBatchAccount parancsmagban</span><span class="sxs-lookup"><span data-stu-id="773db-211">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="773db-212">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="773db-212">Az.CognitiveServices</span></span>
* <span data-ttu-id="773db-213">A fiók képességeinek megjelenítése támogatott.</span><span class="sxs-lookup"><span data-stu-id="773db-213">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="773db-214">Támogatott a PublicNetworkAccess paraméter módosítása.</span><span class="sxs-lookup"><span data-stu-id="773db-214">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="773db-215">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-215">Az.Compute</span></span>
* <span data-ttu-id="773db-216">A SimulateEviction paraméter hozzá lett adva a Set-AzVm és a Set-AzVmssVM parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="773db-216">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="773db-217">A Premium_LRS hozzá lett adva a StorageAccountType paraméter argumentumbefejezőjéhez a New-AzGalleryImageVersion parancsmagban.</span><span class="sxs-lookup"><span data-stu-id="773db-217">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="773db-218">Alállapotok lettek hozzáadva a VMCustomScriptExtension bővítményhez [#11297]</span><span class="sxs-lookup"><span data-stu-id="773db-218">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="773db-219">A Törlés lehetőség hozzá lett adva az EvictionPolicy paraméter argumentumbefejezőjéhez a New-AzVM és a New-AzVMConfig parancsmagokban.</span><span class="sxs-lookup"><span data-stu-id="773db-219">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="773db-220">Az új virtuálisgép-bővítmény neve ki lett javítva az SAP esetében</span><span class="sxs-lookup"><span data-stu-id="773db-220">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="773db-221">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="773db-221">Az.DataFactory</span></span>
* <span data-ttu-id="773db-222">Az ADF .Net SDK a 4.9.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="773db-222">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="773db-223">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="773db-223">Az.EventHub</span></span>
* <span data-ttu-id="773db-224">Managed Identity-paraméterek lettek hozzáadva a New-AzEventHubNamespace és a Set-AzEventHubNamespace parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="773db-224">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="773db-225">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="773db-225">Az.Functions</span></span>
* <span data-ttu-id="773db-226">A PowerShell 7.0- és a Java 11-függvényalkalmazások létrehozása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="773db-226">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="773db-227">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="773db-227">Az.HDInsight</span></span>
* <span data-ttu-id="773db-228">Támogatott a gazdagépek listázása és a HDInsight-fürt adott gazdagépeinek újraindítása.</span><span class="sxs-lookup"><span data-stu-id="773db-228">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="773db-229">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="773db-229">Az.HealthcareApis</span></span>
* <span data-ttu-id="773db-230">Az SDK a 1.1.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="773db-230">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="773db-231">Az exportálási beállítások és a Managed Identity mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="773db-231">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="773db-232">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="773db-232">Az.Monitor</span></span>
* <span data-ttu-id="773db-233">Ki lett javítva a bemeneti objektumparaméter a Set-AzActivityLogAlert parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="773db-233">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="773db-234">Ki lett javítva az InputObject paraméter a Set-AzActionGroup parancsmag esetében [#10868]</span><span class="sxs-lookup"><span data-stu-id="773db-234">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="773db-235">Az.Network</span><span class="sxs-lookup"><span data-stu-id="773db-235">Az.Network</span></span>
* <span data-ttu-id="773db-236">Az AddressPrefixType paraméter mostantól támogatott a Remove-AzExpressRouteCircuitConnectionConfig esetében</span><span class="sxs-lookup"><span data-stu-id="773db-236">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="773db-237">Új parancsmagok lettek hozzáadva az Azure FirewallPolicy szabályzathoz</span><span class="sxs-lookup"><span data-stu-id="773db-237">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="773db-238">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="773db-238">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="773db-239">A tűzfalszabályzathoz tartozó hálózati szabályok céltartományneveinek támogatása</span><span class="sxs-lookup"><span data-stu-id="773db-239">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="773db-240">A háttércímkészlet műveletei mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="773db-240">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="773db-241">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="773db-241">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="773db-242">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="773db-242">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="773db-243">Set-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="773db-243">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="773db-244">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="773db-244">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="773db-245">Get-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="773db-245">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="773db-246">A New-AzIpGroup névérvényesítése hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-246">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="773db-247">Új parancsmagok lettek hozzáadva az Azure FirewallPolicy szabályzathoz</span><span class="sxs-lookup"><span data-stu-id="773db-247">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="773db-248">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="773db-248">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="773db-249">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: Egyéni DNS-kiszolgálók beállítása/eltávolítása a VirtualWan-P2SVpnGateway átjárón.</span><span class="sxs-lookup"><span data-stu-id="773db-249">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="773db-250">Frissült a New-AzP2sVpnGateway: A -CustomDnsServer opcionális paraméter hozzá lett adva az ügyfelek számára, hogy megadhassák a P2SVpnGateway átjárón beállítani kívánt DNS-kiszolgálókat (ezeket pont–hely ügyfelek is használhatják).</span><span class="sxs-lookup"><span data-stu-id="773db-250">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="773db-251">Frissült az AzP2sVpnGateway: A -CustomDnsServer opcionális paraméter hozzá lett adva az ügyfelek számára, hogy megadhassák a P2SVpnGateway átjárón beállítani kívánt DNS-kiszolgálókat (ezeket pont–hely ügyfelek is használhatják).</span><span class="sxs-lookup"><span data-stu-id="773db-251">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="773db-252">Frissült az Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="773db-252">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="773db-253">A -BgpPeeringAddress opcionális paraméter hozzá lett adva az ügyfelek számára a VPN Gateway átjárón beállítani kívánt egyéni bgps megadásához.</span><span class="sxs-lookup"><span data-stu-id="773db-253">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="773db-254">Új parancsmag lett hozzáadva a VirtualHub-erőforrás útválasztási állapota visszaállításának támogatásához:</span><span class="sxs-lookup"><span data-stu-id="773db-254">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="773db-255">Reset-AzHubRouter</span><span class="sxs-lookup"><span data-stu-id="773db-255">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="773db-256">A tűzfalszabályzat legutóbbi Swagger-módosításának megfelelően frissültek az alábbi tételek</span><span class="sxs-lookup"><span data-stu-id="773db-256">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="773db-257">A RuleGroup, a RuleCollectionGroup és a RuleType neve megváltozott</span><span class="sxs-lookup"><span data-stu-id="773db-257">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="773db-258">Mostantól támogatott a tűzfalszabályzat NAT-szabálygyűjteménye esetében több NAT-szabálygyűjtemény használata</span><span class="sxs-lookup"><span data-stu-id="773db-258">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="773db-259">[Kompatibilitástörő változás] Kötelező SourceIpGroup paraméter lett hozzáadva a New-AzFirewallPolicyApplicationRule és a New-AzFirewallPolicyNetworkRule esetében.</span><span class="sxs-lookup"><span data-stu-id="773db-259">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="773db-260">[Kompatibilitástörő változás] A New-AzFirewallPolicyApplicationRule ki lett javítva, a SourceAddress paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="773db-260">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="773db-261">[Kompatibilitástörő változás] A New-AzFirewallPolicyApplicationRule ki lett javítva, a SourceAddress paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="773db-261">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="773db-262">[Kompatibilitástörő változás] Eltávolított kötelező paraméterek: TranslatedAddress, TranslatedPort a New-AzFirewallPolicyNatRuleCollection esetében.</span><span class="sxs-lookup"><span data-stu-id="773db-262">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="773db-263">Új parancsmagok lettek hozzáadva a PrivateLink támogatásához az Application Gatewayen</span><span class="sxs-lookup"><span data-stu-id="773db-263">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="773db-264">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="773db-264">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="773db-265">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="773db-265">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="773db-266">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="773db-266">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="773db-267">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="773db-267">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="773db-268">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="773db-268">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="773db-269">New-AzApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="773db-269">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="773db-270">Új parancsmagok lettek hozzáadva a VirtualHub HubRouteTables gyermekerőforrásai esetében.</span><span class="sxs-lookup"><span data-stu-id="773db-270">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="773db-271">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="773db-271">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="773db-272">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="773db-272">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="773db-273">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="773db-273">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="773db-274">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="773db-274">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="773db-275">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="773db-275">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="773db-276">Frissültek a meglévő parancsmagok az opcionális RoutingConfiguration bemeneti paraméter támogatásához az egyéni útválasztás esetében a VirtualWanban.</span><span class="sxs-lookup"><span data-stu-id="773db-276">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="773db-277">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="773db-277">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="773db-278">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="773db-278">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="773db-279">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="773db-279">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="773db-280">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="773db-280">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="773db-281">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="773db-281">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="773db-282">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="773db-282">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="773db-283">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="773db-283">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="773db-284">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="773db-284">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="773db-285">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="773db-285">Az.OperationalInsights</span></span>
* <span data-ttu-id="773db-286">Ki lett javítva az a PSWorkspace-hiba, amely miatt meghiúsult az IOperationalInsightsWorkspace implementálása [#12135]</span><span class="sxs-lookup"><span data-stu-id="773db-286">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="773db-287">A pergb2018 hozzá lett adva az SKU paraméter érvényes értékéhez a Set-AzOperationalInsightsWorkspace esetében</span><span class="sxs-lookup"><span data-stu-id="773db-287">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="773db-288">A FunctionParameters alias hozzá lett adva a FunctionParameter paraméterhez a következők esetében:</span><span class="sxs-lookup"><span data-stu-id="773db-288">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="773db-289">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="773db-289">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="773db-290">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="773db-290">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="773db-291">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="773db-291">Az.RecoveryServices</span></span>
* <span data-ttu-id="773db-292">Az Azure Backup mostantól támogatott az MAB-elemek beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="773db-292">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="773db-293">Az Azure Site Recovery támogatja a StandardSSD_LRS lemeztípust</span><span class="sxs-lookup"><span data-stu-id="773db-293">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="773db-294">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-294">Az.Resources</span></span>
* <span data-ttu-id="773db-295">A UsageLocation, GivenName, Surname, AccountEnabled, MailNickname, Mail paraméterek hozzá lettek adva a PSADUser esetében [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="773db-295">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="773db-296">Ki lett javítva az a hiba, hogy a -Mail nem működött a Get-AzADUser esetében [#11981]</span><span class="sxs-lookup"><span data-stu-id="773db-296">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="773db-297">Az -ExcludeChangeType paraméter hozzá lett adva a következőkhöz: Get-AzDeploymentWhatIfResult és Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="773db-297">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="773db-298">A -WhatIfExcludeChangeType paraméter hozzá lett adva a következőkhöz: New-AzDeployment és New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="773db-298">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="773db-299">A Test-Az\*Deployment parancsmagok frissültek a megfelelőbb hibaüzenetek megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="773db-299">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="773db-300">Ki lett javítva az üzemelő példány -Name paraméterének súgóüzenete a create és a What-If parancsmagok esetében</span><span class="sxs-lookup"><span data-stu-id="773db-300">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="773db-301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-301">Az.Sql</span></span>
* <span data-ttu-id="773db-302">Szolgáltatásnév támogatása hozzáadva a Set SQL Server Azure Active Directory Admin parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="773db-302">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="773db-303">Ki lett javítva a szinkronizálási probléma az adatbesorolási parancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="773db-303">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="773db-304">Támogatott az e-mail-cím alapján történő felhasználókeresés a következő esetében: Set-AzSqlServerActiveDirectoryAdministrator [#12192]</span><span class="sxs-lookup"><span data-stu-id="773db-304">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="773db-305">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="773db-305">Az.Storage</span></span>
* <span data-ttu-id="773db-306">Támogatott a tárfiók RequireInfrastructureEncryption használatával való létrehozása</span><span class="sxs-lookup"><span data-stu-id="773db-306">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="773db-307">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="773db-307">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="773db-308">Át lett helyezve az Azure.Core betöltési logikája Az.Accounts modulba</span><span class="sxs-lookup"><span data-stu-id="773db-308">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="773db-309">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="773db-309">Az.Websites</span></span>
* <span data-ttu-id="773db-310">Hozzáadott védelem a létrehozott webalkalmazás törléséhez, ha a visszaállítás nem sikerült a Restore-AzDeletedWebApp esetében</span><span class="sxs-lookup"><span data-stu-id="773db-310">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="773db-311">A SourceWebApp.Location paraméter hozzá lett adva a New-AzWebApp és a New-AzWebAppSlot esetében</span><span class="sxs-lookup"><span data-stu-id="773db-311">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="773db-312">Ki lett javítva az a hiba, amely megakadályozta a tárolóbeállítások módosítását a Set-AzWebApp és a Set-AzWebAppSlot esetében</span><span class="sxs-lookup"><span data-stu-id="773db-312">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="773db-313">Ki lett javítva a SiteConfig lekérésének hibája, ha a -Name nem lett megadva a Get-AzWebApp esetében</span><span class="sxs-lookup"><span data-stu-id="773db-313">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="773db-314">Támogatás hozzáadva ASP létráhozásához Linux-alkalmazások esetében</span><span class="sxs-lookup"><span data-stu-id="773db-314">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="773db-315">Kivételek hozzáadva az erőforráscsoportok közötti klónozás esetében</span><span class="sxs-lookup"><span data-stu-id="773db-315">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="773db-316">4.2.0 – 2020. június</span><span class="sxs-lookup"><span data-stu-id="773db-316">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="773db-317">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="773db-317">Az.Accounts</span></span>
* <span data-ttu-id="773db-318">Kijavítottunk egy problémát, amely miatt az Az Azure Automation-naplókat vagy PowerShell-feladatokat hagyott ki [#11492]</span><span class="sxs-lookup"><span data-stu-id="773db-318">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="773db-319">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="773db-319">Az.AnalysisServices</span></span>
* <span data-ttu-id="773db-320">Frissítettük az adatsík parancsmagjainak szerelvényverzióját</span><span class="sxs-lookup"><span data-stu-id="773db-320">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="773db-321">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="773db-321">Az.ApiManagement</span></span>
* <span data-ttu-id="773db-322">Frissítettük a szolgáltatásfelügyeleti parancsmagok szerelvényverzióját</span><span class="sxs-lookup"><span data-stu-id="773db-322">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="773db-323">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="773db-323">Az.Billing</span></span>
* <span data-ttu-id="773db-324">Frissítettük a felhasználási parancsmagok szerelvényverzióját</span><span class="sxs-lookup"><span data-stu-id="773db-324">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="773db-325">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="773db-325">Az.CognitiveServices</span></span>
* <span data-ttu-id="773db-326">A PrivateEndpoint és a PublicNetworkAccess vezérlők támogatása.</span><span class="sxs-lookup"><span data-stu-id="773db-326">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="773db-327">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="773db-327">Az.DataFactory</span></span>
* <span data-ttu-id="773db-328">Frissítettük a Data Factory V2 parancsmagjainak szerelvényverzióját</span><span class="sxs-lookup"><span data-stu-id="773db-328">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="773db-329">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="773db-329">Az.DataShare</span></span>
* <span data-ttu-id="773db-330">Az Az.DataShare modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="773db-330">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="773db-331">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="773db-331">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="773db-332">Az „Az.DesktopVirtualization” modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="773db-332">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="773db-333">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="773db-333">Az.OperationalInsights</span></span>
* <span data-ttu-id="773db-334">SDK frissítve a 0.21.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="773db-334">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="773db-335">Választható paraméterek hozzáadva a következőkhöz:</span><span class="sxs-lookup"><span data-stu-id="773db-335">Added optional parameters to</span></span> 
    - <span data-ttu-id="773db-336">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="773db-336">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="773db-337">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="773db-337">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="773db-338">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="773db-338">Az.PolicyInsights</span></span>
* <span data-ttu-id="773db-339">Javítottuk a Start-AzPolicyComplianceScan 3. példáját</span><span class="sxs-lookup"><span data-stu-id="773db-339">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="773db-340">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="773db-340">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="773db-341">Frissítettük a PowerBI-parancsmagok szerelvényverzióját</span><span class="sxs-lookup"><span data-stu-id="773db-341">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="773db-342">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="773db-342">Az.PrivateDns</span></span>
* <span data-ttu-id="773db-343">Javítottuk a Remove-AzPrivateDnsRecordSet kimeneti sztringjének formázását</span><span class="sxs-lookup"><span data-stu-id="773db-343">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="773db-344">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="773db-344">Az.RecoveryServices</span></span>
* <span data-ttu-id="773db-345">Azure Site Recovery-támogatás helyreállítási terv létrehozásához az xml-bemenetből kezdeményezett, zónák közötti replikáció esetében.</span><span class="sxs-lookup"><span data-stu-id="773db-345">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="773db-346">Frissítettük a SiteRecovery és a Backup parancsmagok szerelvényverzióját</span><span class="sxs-lookup"><span data-stu-id="773db-346">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="773db-347">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-347">Az.Resources</span></span>
* <span data-ttu-id="773db-348">Szélsőérték paraméter hozzáadva a Get-AzDeploymentScriptLog és a Save-AzDeploymentScriptLog parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="773db-348">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="773db-349">Kimeneti tulajdonság formázása és megjelenítése a Get-AzDeploymentScript parancsmag kimenetén</span><span class="sxs-lookup"><span data-stu-id="773db-349">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="773db-350">A -DeploymentScriptInputObject paraméter új neve -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="773db-350">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="773db-351">Javítottuk a parancsmagüzenetek hiányzó fájl-/célnevét.</span><span class="sxs-lookup"><span data-stu-id="773db-351">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="773db-352">Frissítettük a Resource Manager és a címkék parancsmagjainak szerelvényverzióját</span><span class="sxs-lookup"><span data-stu-id="773db-352">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="773db-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-353">Az.Sql</span></span>
* <span data-ttu-id="773db-354">UsePrivateLinkConnection hozzáadva a következőkhöz: New-AzSqlSyncGroup, Update-AzSqlSyncGroup, New-AzSqlSyncMember és Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="773db-354">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="773db-355">SyncMemberAzureDatabaseResourceId hozzáadva a következőkhöz: New-AzSqlSyncMember és Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="773db-355">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="773db-356">Vendégfelhasználó-keresés támogatása hozzáadva a Set SQL Server Azure Active Directory Admin parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="773db-356">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="773db-357">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="773db-357">Az.Storage</span></span>
* <span data-ttu-id="773db-358">Frissítettük az adatsík parancsmagjainak szerelvényverzióját</span><span class="sxs-lookup"><span data-stu-id="773db-358">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="773db-359">4.1.0 – 2020. május</span><span class="sxs-lookup"><span data-stu-id="773db-359">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="773db-360">A legutóbbi kiadás óta bevezetett újdonságok</span><span class="sxs-lookup"><span data-stu-id="773db-360">Highlights since the last release</span></span>
* <span data-ttu-id="773db-361">Támogatott PowerShell-verziók: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="773db-361">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="773db-362">Az Az.Functions általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="773db-362">General availability of Az.Functions</span></span> 
* <span data-ttu-id="773db-363">A következők rendelkeznek nagyobb kiadással: Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources és Az.Storage</span><span class="sxs-lookup"><span data-stu-id="773db-363">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="773db-364">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="773db-364">Az.Accounts</span></span>
* <span data-ttu-id="773db-365">Frissítve lett az Add-AzEnvironment és a Set-AzEnvironment parancsmag, amelyek mostantól elfogadják az AzureSynapseAnalyticsEndpointResourceId és az AzureSynapseAnalyticsEndpointSuffix paramétereket</span><span class="sxs-lookup"><span data-stu-id="773db-365">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="773db-366">Hozzá lettek adva az Azure.Core-hoz kapcsolódó szerelvények az Az.Accounts-hoz, a támogatott platformok a Windows PowerShell 5.1, a PowerShell Core 6.2.4 és a PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="773db-366">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="773db-367">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="773db-367">Az.Aks</span></span>
* <span data-ttu-id="773db-368">Az API-verzió frissítve lett a 2019-10-01-es verzióra</span><span class="sxs-lookup"><span data-stu-id="773db-368">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="773db-369">Az AKS Windows-tárolókkal történő létrehozásának támogatása</span><span class="sxs-lookup"><span data-stu-id="773db-369">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="773db-370">Elérhető új parancsmagok: New-AzAksNodePool, Update-AzAksNodePool, Remove-AzAksNodePool,        Get-AzAksNodePool, Install-AzAksKubectl, Get-AzAksVersion</span><span class="sxs-lookup"><span data-stu-id="773db-370">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="773db-371">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="773db-371">Az.ApiManagement</span></span>
* <span data-ttu-id="773db-372">New-AzApiManagement és Set-AzApiManagement: az [-AssignIdentity] paraméter új neve [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="773db-372">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="773db-373">New-AzApiManagement és Set-AzApiManagement: Új paraméter lett hozzáadva: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="773db-373">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="773db-374">A Get-AzApiManagementProperty át lett nevezve a következőre: Get-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="773db-374">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="773db-375">A PropertyId paraméter át lett nevezve a következőre: NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="773db-375">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="773db-376">A New-AzApiManagementProperty át lett nevezve a következőre: New-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="773db-376">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="773db-377">A PropertyId paraméter át lett nevezve a következőre: NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="773db-377">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="773db-378">A Set-AzApiManagementProperty át lett nevezve a következőre: Set-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="773db-378">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="773db-379">A PropertyId paraméter át lett nevezve a következőre: NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="773db-379">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="773db-380">A Remove-AzApiManagementProperty át lett nevezve a következőre: Remove-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="773db-380">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="773db-381">A PropertyId paraméter át lett nevezve a következőre: NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="773db-381">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="773db-382">Hozzá lett adva az új Get-AzApiManagementAuthorizationServerClientSecret parancsmag, valamint a Get-AzApiManagementAuthorizationServer már nem ad vissza titkos ügyfélkulcsot.</span><span class="sxs-lookup"><span data-stu-id="773db-382">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="773db-383">Hozzá lett adva az új Get-AzApiManagementNamedValueSecretValue parancsmag, és a Get-AzApiManagementNamedValue nem ad vissza titkos kulcsot.</span><span class="sxs-lookup"><span data-stu-id="773db-383">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="773db-384">Hozzá lett adva az új Get-AzApiManagementOpenIdConnectProviderClientSecret parancsmag, valamint a Get-AzApiManagementOpenIdConnectProvider már nem ad vissza titkos ügyfélkulcsot.</span><span class="sxs-lookup"><span data-stu-id="773db-384">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="773db-385">Hozzá lett adva az új Get-AzApiManagementSubscriptionKey parancsmag, és a Get-AzApiManagementSubscription már nem ad vissza előfizetési azonosítót.</span><span class="sxs-lookup"><span data-stu-id="773db-385">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="773db-386">Hozzá lett adva az új Get-AzApiManagementTenantAccessSecret parancsmag, és a Get-AzApiManagementTenantAccess már nem ad vissza kulcsot.</span><span class="sxs-lookup"><span data-stu-id="773db-386">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="773db-387">Hozzá lett adva az új Get-AzApiManagementTenantGitAccessSecret parancsmag, és a Get-AzApiManagementTenantGitAccess már nem ad vissza kulcsot.</span><span class="sxs-lookup"><span data-stu-id="773db-387">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="773db-388">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="773db-388">Az.ApplicationInsights</span></span>
* <span data-ttu-id="773db-389">Hozzáadott paraméterek: A New-AzApplicationInsights esetében: RetentionInDays, PublicNetworkAccessForIngestion, PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="773db-389">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="773db-390">Létre lett hozva az Update-AzApplicationInsights parancsmag</span><span class="sxs-lookup"><span data-stu-id="773db-390">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="773db-391">Parancsmagok lettek létrehozva a társított tárfiókhoz</span><span class="sxs-lookup"><span data-stu-id="773db-391">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="773db-392">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="773db-392">Az.Batch</span></span>
* <span data-ttu-id="773db-393">Frissítve lett az Az.Batch a Microsoft.Azure.Batch SDK 13.0.0.-s verziójának és a Microsoft.Azure.Management.Batch SDK 9.0.0-s verziójának használatára.</span><span class="sxs-lookup"><span data-stu-id="773db-393">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="773db-394">Kiválaszthatóvá vált a hozzáadni kívánt tanúsítvány típusa a New-AzBatchCertificate új -CertificateKind paraméterének használatával.</span><span class="sxs-lookup"><span data-stu-id="773db-394">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="773db-395">El lett távolítva az ApplicationPackages tulajdonság a PSApplicationből, amelynek típusa eddig mindig '' volt.</span><span class="sxs-lookup"><span data-stu-id="773db-395">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="773db-396">Most már lekérhetők az alkalmazásokon belüli adott csomagok a Get-AzBatchApplicationPackage használatával.</span><span class="sxs-lookup"><span data-stu-id="773db-396">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="773db-397">Például: Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication.</span><span class="sxs-lookup"><span data-stu-id="773db-397">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="773db-398">Egy készlet New-AzBatchPool használatával történő létrehozásakor a PSImageReference VirtualMachineImageId tulajdonsága már csak a Shared Image Gallery-ben található rendszerképre hivatkozhat.</span><span class="sxs-lookup"><span data-stu-id="773db-398">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="773db-399">Egy készlet New-AzBatchPool használatával történő létrehozásakor a készlet nyilvános IP-cím nélkül is létrehozható a PSNetworkConfiguration új PublicIPAddressConfiguration tulajdonságával.</span><span class="sxs-lookup"><span data-stu-id="773db-399">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="773db-400">A PSNetworkConfiguration PublicIPs tulajdonsága a PSPublicIPAddressConfiguration esetében is elérhető.</span><span class="sxs-lookup"><span data-stu-id="773db-400">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="773db-401">Ez a tulajdonság csak akkor adható meg, ha az IPAddressProvisioningType UserManaged típusú.</span><span class="sxs-lookup"><span data-stu-id="773db-401">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="773db-402">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-402">Az.Compute</span></span>
* <span data-ttu-id="773db-403">A HostId paraméter hozzá lett adva az Update-AzVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="773db-403">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="773db-404">Frissültek a New-AzVMConfig, New-AzVmssConfig, Update-AzVmss, Set-AzVMOperatingSystem és Set-AzVmssOsProfile parancsmagok súgódokumentumai.</span><span class="sxs-lookup"><span data-stu-id="773db-404">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="773db-405">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="773db-405">Breaking changes</span></span>
    - <span data-ttu-id="773db-406">A FilterExpression paraméter el lett távolítva a Get-AzVMImage parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="773db-406">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="773db-407">Az AssignIdentity paraméter el lett távolítva a New-AzVmssConfig, New-AzVMConfig és Update-AzVM parancsmagokból.</span><span class="sxs-lookup"><span data-stu-id="773db-407">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="773db-408">Az AutomaticRepairMaxInstanceRepairsPercent paraméter el lett távolítva a New-AzVmssConfig és az Update-AzVmss parancsmagokból.</span><span class="sxs-lookup"><span data-stu-id="773db-408">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="773db-409">Az AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus és VirtualMachineScaleSetsColocationStatus tulajdonságok el lettek távolítva a ProximityPlacementGroup paraméterből.</span><span class="sxs-lookup"><span data-stu-id="773db-409">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="773db-410">A MaxInstanceRepairsPercent tulajdonság el lett távolítva a következőből: AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="773db-410">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="773db-411">Az AvailabilitySets, VirtualMachines és VirtualMachineScaleSets típusa IList<SubResource> helyett mostantól IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="773db-411">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="773db-412">Frissült a Get-AzVM parancsmag leírása, hogy pontosabban ismertesse a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="773db-412">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="773db-413">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="773db-413">Az.DataFactory</span></span>
* <span data-ttu-id="773db-414">Adatfolyam futtatókörnyezeti tulajdonságaihoz tartozó CRUD támogatása a felügyelt IR-ben.</span><span class="sxs-lookup"><span data-stu-id="773db-414">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="773db-415">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="773db-415">Az.FrontDoor</span></span>
* <span data-ttu-id="773db-416">Új parancsmagok lettek hozzáadva a Front Door szabálymotor-objektumának létrehozására, frissítésére, lekérésére és törlésére.</span><span class="sxs-lookup"><span data-stu-id="773db-416">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="773db-417">Hozzá lettek adva segítő parancsmagok a Front Door szabálymotor-objektumának létrehozásához</span><span class="sxs-lookup"><span data-stu-id="773db-417">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="773db-418">Hozzá lett adva a szabálymotor-referencia a Front Door útválasztásiszabály-objektumához.</span><span class="sxs-lookup"><span data-stu-id="773db-418">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="773db-419">Hozzá lettek adva privát kapcsolati paraméterek a Front Door háttérobjektumához</span><span class="sxs-lookup"><span data-stu-id="773db-419">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="773db-420">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="773db-420">Az.Functions</span></span>
* <span data-ttu-id="773db-421">Az Az.Functions modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="773db-421">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="773db-422">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="773db-422">Az.HDInsight</span></span>
* <span data-ttu-id="773db-423">Az ügyfél által felügyelt kulcson alapuló lemeztitkosítás mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="773db-423">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="773db-424">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="773db-424">Az.HealthcareApis</span></span>
* <span data-ttu-id="773db-425">A hozzáférési szabályzatok már nem tartoznak alapértelmezés szerint az aktuális rendszerbiztonsági taghoz</span><span class="sxs-lookup"><span data-stu-id="773db-425">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="773db-426">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="773db-426">Az.IotHub</span></span>
* <span data-ttu-id="773db-427">Hozzá lett adva egy parancsmag, amellyel egy SQL-szerű nyelv használatával végzett, információkat lekérő lekérdezés indítható el az IoT Hubban.</span><span class="sxs-lookup"><span data-stu-id="773db-427">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="773db-428">Javítva a hiba, amely miatt az Add-AzIotHubDevice gyermekeszköz nélkül nem tudott Edge-kompatibilis eszközt létrehozni [#11597]</span><span class="sxs-lookup"><span data-stu-id="773db-428">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="773db-429">Hozzá lett adva egy parancsmag egy SAS-token létrehozásához az IoT Hub, eszköz vagy modul számára.</span><span class="sxs-lookup"><span data-stu-id="773db-429">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="773db-430">Hozzá lett adva egy parancsmag a konfiguráció-metrikák lekérdezésének meghívásához.</span><span class="sxs-lookup"><span data-stu-id="773db-430">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="773db-431">Az IoT Edge nagy léptékű automatikus üzembe helyezésének kezelése.</span><span class="sxs-lookup"><span data-stu-id="773db-431">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="773db-432">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="773db-432">New cmdlets are:</span></span>
    - <span data-ttu-id="773db-433">Add-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="773db-433">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="773db-434">Get-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="773db-434">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="773db-435">Remove-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="773db-435">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="773db-436">Set-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="773db-436">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="773db-437">Hozzá lett adva egy parancsmag, amellyel az IoT Edge üzembehelyezési metrikáit lekérő lekérdezést hívható meg.</span><span class="sxs-lookup"><span data-stu-id="773db-437">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="773db-438">Hozzá lett adva egy parancsmag a konfiguráció tartalmának egy adott Edge-eszközre történő alkalmazásához.</span><span class="sxs-lookup"><span data-stu-id="773db-438">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="773db-439">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="773db-439">Az.KeyVault</span></span>
* <span data-ttu-id="773db-440">A következő két alias el lett távolítva: New-AzKeyVaultCertificateAdministratorDetails és New-AzKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="773db-440">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="773db-441">Alapértelmezés szerint engedélyezve lett a helyreállítható törlés egy kulcstartó létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="773db-441">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="773db-442">Kulcstartó létrehozásakor a hálózati szabályok beállíthatók a megadott hálózati helyekről való hozzáférés szabályozására</span><span class="sxs-lookup"><span data-stu-id="773db-442">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="773db-443">A saját kulcs használata (BYOK) már támogatott</span><span class="sxs-lookup"><span data-stu-id="773db-443">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="773db-444">Az Add-AzKeyVaultKey támogatja a kulcscserekulcsok létrehozását</span><span class="sxs-lookup"><span data-stu-id="773db-444">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="773db-445">A Get-AzKeyVaultKey támogatja a nyilvános kulcsok PEM formátumban való letöltését</span><span class="sxs-lookup"><span data-stu-id="773db-445">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="773db-446">Frissült az Add-AzKeyVaultKey súgódokumentációjának KeyOps része</span><span class="sxs-lookup"><span data-stu-id="773db-446">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="773db-447">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="773db-447">Az.Monitor</span></span>
* <span data-ttu-id="773db-448">Javítva a Set-AzDiagnosticSettings hibája, amely miatt a megtartási szabályzat nem vonatkozott minden kategóriára [#11589]</span><span class="sxs-lookup"><span data-stu-id="773db-448">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="773db-449">A WebTest rendelkezésre állási feltételeinek támogatása a 2-es verziójú metrikariasztás esetében</span><span class="sxs-lookup"><span data-stu-id="773db-449">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="773db-450">New-AzMetricAlertRuleV2Criteria: mostantól megadhatók a webteszt rendelkezésre állási feltételei</span><span class="sxs-lookup"><span data-stu-id="773db-450">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="773db-451">Add-AzMetricAlertRuleV2: támogatja a webteszt új rendelkezésre állási feltételeit</span><span class="sxs-lookup"><span data-stu-id="773db-451">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="773db-452">El lett távolítva a RetentionPolicy redundáns definíciója a PSLogProfile-ból [#7608]</span><span class="sxs-lookup"><span data-stu-id="773db-452">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="773db-453">El lettek távolítva a PSEventData objektumban meghatározott redundáns tulajdonságok [#11353]</span><span class="sxs-lookup"><span data-stu-id="773db-453">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="773db-454">A Get-Azlog át lett nevezve a következőre: Get-AzActivityLog</span><span class="sxs-lookup"><span data-stu-id="773db-454">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="773db-455">Az.Network</span><span class="sxs-lookup"><span data-stu-id="773db-455">Az.Network</span></span>
* <span data-ttu-id="773db-456">Kompatibilitástörő változást okozó attribútum lett hozzáadva, amely figyelmeztet a Zone alapértelmezett viselkedésének változásáról</span><span class="sxs-lookup"><span data-stu-id="773db-456">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="773db-457">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="773db-457">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="773db-458">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="773db-458">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="773db-459">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="773db-459">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="773db-460">Hozzá lett adva az új, SecurityPartnerProvider legfelsőbb szintű erőforrás támogatása</span><span class="sxs-lookup"><span data-stu-id="773db-460">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="773db-461">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="773db-461">New cmdlets added:</span></span>
        - <span data-ttu-id="773db-462">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="773db-462">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="773db-463">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="773db-463">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="773db-464">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="773db-464">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="773db-465">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="773db-465">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="773db-466">Hozzá lett adva a RequiredZoneNames tulajdonság a PSPrivateLinkResource esetében, és a GroupId a PSPrivateEndpointConnection esetében</span><span class="sxs-lookup"><span data-stu-id="773db-466">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="773db-467">Kijavítva a SuccessThresholdRoundTripTimeMs paraméter típusa a New-AzNetworkWatcherConnectionMonitorTestConfigurationObject esetében</span><span class="sxs-lookup"><span data-stu-id="773db-467">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="773db-468">Frissítve lettek a VirtualWan parancsmagok az AllowVnetToVnetTraffic argumentum True értékre való állításához.</span><span class="sxs-lookup"><span data-stu-id="773db-468">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="773db-469">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="773db-469">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="773db-470">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="773db-470">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="773db-471">Új parancsmagok lettek hozzáadva a privát végpontok DNS-zónacsoportjainak támogatásához</span><span class="sxs-lookup"><span data-stu-id="773db-471">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="773db-472">New-AzPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="773db-472">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="773db-473">Get-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="773db-473">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="773db-474">New-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="773db-474">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="773db-475">Set-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="773db-475">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="773db-476">Remove-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="773db-476">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="773db-477">Hozzá lett adva a DNSEnableProxy, a DNSRequireProxyForNetworkRules és a DNSServers paraméter az AzureFirewall-hoz</span><span class="sxs-lookup"><span data-stu-id="773db-477">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="773db-478">Hozzá lett adva az EnableDnsProxy, a DnsProxyNotRequiredForNetworkRule és a DnsServer paraméter az AzureFirewall-hoz</span><span class="sxs-lookup"><span data-stu-id="773db-478">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="773db-479">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="773db-479">Updated cmdlet:</span></span>
        - <span data-ttu-id="773db-480">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="773db-480">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="773db-481">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="773db-481">Az.OperationalInsights</span></span>
* <span data-ttu-id="773db-482">Frissítve lett a régi kód az újonnan létrehozott SDK alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="773db-482">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="773db-483">Az elavult API-k miatt törölt parancsmagok</span><span class="sxs-lookup"><span data-stu-id="773db-483">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="773db-484">Get-AzOperationalInsightsSavedSearchResult (alias: Get-AzOperationalInsightsSavedSearchResults)</span><span class="sxs-lookup"><span data-stu-id="773db-484">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="773db-485">Get-AzOperationalInsightsSearchResult (alias: Get-AzOperationalInsightsSearchResults)</span><span class="sxs-lookup"><span data-stu-id="773db-485">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="773db-486">Get-AzOperationalInsightsLinkTarget (alias: Get-AzOperationalInsightsLinkTargets)</span><span class="sxs-lookup"><span data-stu-id="773db-486">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="773db-487">Paraméterek lettek hozzáadva a Set-AzOperationalInsightsWorkspace és New-AzOperationalInsightsWorkspace parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="773db-487">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="773db-488">Parancsmagok lettek létrehozva a társított tárfiókhoz</span><span class="sxs-lookup"><span data-stu-id="773db-488">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="773db-489">Parancsmagok lettek létrehozva a fürtökhöz és a társított szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="773db-489">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="773db-490">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="773db-490">Az.RecoveryServices</span></span>
* <span data-ttu-id="773db-491">Hozzá lett adva az Azure Site Recovery-támogatás a közelségi elhelyezési csoportokban lévő virtuális gépek védelme érdekében, az Azure–Azure szolgáltatók esetében.</span><span class="sxs-lookup"><span data-stu-id="773db-491">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="773db-492">Hozzá lett adva az Azure Site Recovery-támogatás a zónák közötti replikáció esetében.</span><span class="sxs-lookup"><span data-stu-id="773db-492">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="773db-493">Az Azure Backup már támogatja a hosszú távú megőrzést az Azure FileShare helyreállítási pontok esetében.</span><span class="sxs-lookup"><span data-stu-id="773db-493">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="773db-494">Hozzá lettek adva az Azure Backup lemezkizárási tulajdonságok a Get-AzRecoveryServicesBackupItem parancsmag kimenetéhez.</span><span class="sxs-lookup"><span data-stu-id="773db-494">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="773db-495">Hozzá lett adva a privát végpont a Vault hitelesítési fájljaihoz a Site Recovery szolgáltatás esetében.</span><span class="sxs-lookup"><span data-stu-id="773db-495">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="773db-496">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-496">Az.Resources</span></span>
* <span data-ttu-id="773db-497">Hozzá lett adva a megtekintés késéséről figyelmeztető üzenet az új szerepkör-definíció létrehozása során</span><span class="sxs-lookup"><span data-stu-id="773db-497">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="773db-498">Módosítva lettek a szabályzat-parancsmagok a szigorú típusmegadású objektumok megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="773db-498">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="773db-499">El lett távolítva a Get-AzResourceLock parancsmaghoz használt -TenantLevel paraméter [#11335]</span><span class="sxs-lookup"><span data-stu-id="773db-499">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="773db-500">Javítva a Remove-AzResourceGroup -Id ResourceId parancsmag [#9882]</span><span class="sxs-lookup"><span data-stu-id="773db-500">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="773db-501">Hozzá lett adva egy új parancsmag az ARM-sablon What-If típusú eredményeinek lekéréséhez az erőforráscsoport hatókörében: Get-AzDeploymentResourceGroupWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="773db-501">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="773db-502">Hozzá lett adva egy új parancsmag az ARM-sablonok What-If típusú eredményeinek lekéréséhez az előfizetés hatókörében: Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="773db-502">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="773db-503">Alias: Get-AzSubscriptionDeploymentWhatIf</span><span class="sxs-lookup"><span data-stu-id="773db-503">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="773db-504">A -WhatIf és a -Confirm paraméter felül lett írva a New-AzDeployment és a New-AzResourceGroupDeployment parancsmagok esetében az ARM-sablon What-If típusú eredményeinek használata érdekében</span><span class="sxs-lookup"><span data-stu-id="773db-504">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="773db-505">Hozzá lett adva az elavulási üzenet az ApiVersion paraméterhez az üzembehelyezési parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="773db-505">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="773db-506">Hozzá lett adva egy képesség, amely lehetővé teszi, hogy fejlettebb hibaüzenetek jelenjenek meg az üzembehelyezési hibák esetén</span><span class="sxs-lookup"><span data-stu-id="773db-506">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="773db-507">Hozzá lett adva a correlationId-naplózása az üzembehelyezési hibák esetében</span><span class="sxs-lookup"><span data-stu-id="773db-507">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="773db-508">Hozzá lett adva az error tulajdonság az üzembehelyezési szkript kimenetéhez</span><span class="sxs-lookup"><span data-stu-id="773db-508">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="773db-509">A Microsoft.Azure.Management.ResourceManager NuGet frissítve lett a 3.7.1-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="773db-509">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="773db-510">El lettek távolítva adott tesztesetek, mivel a DeploymentValidateResult Error tulajdonsága csak olvasható állapotúra változott a NuGet 3.7.1-preview verziójától kezdődően</span><span class="sxs-lookup"><span data-stu-id="773db-510">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="773db-511">A GenericResourceExpanded át lett hozva a ResourceManager SDK 3.7.1-preview verziójából</span><span class="sxs-lookup"><span data-stu-id="773db-511">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="773db-512">Hozzá lett adva a címketámogatás az összes, üzembe helyezéshez használt Get parancsmaghoz, valamint a következőkhöz:</span><span class="sxs-lookup"><span data-stu-id="773db-512">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="773db-513">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="773db-513">'New-AzDeployment'</span></span>
    - <span data-ttu-id="773db-514">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="773db-514">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="773db-515">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="773db-515">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="773db-516">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="773db-516">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="773db-517">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="773db-517">Az.ServiceFabric</span></span>
* <span data-ttu-id="773db-518">Javítva a hiba, amely hibás tanúsítvány-ujjlenyomatot kért le a tanúsítvány --SecretIdentifier használatával történő hozzáadásakor</span><span class="sxs-lookup"><span data-stu-id="773db-518">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="773db-519">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-519">Az.Sql</span></span>
* <span data-ttu-id="773db-520">Javult a következők teljesítménye:</span><span class="sxs-lookup"><span data-stu-id="773db-520">Enhance performance of:</span></span>
    - <span data-ttu-id="773db-521">Set-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="773db-521">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="773db-522">Set-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="773db-522">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="773db-523">Remove-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="773db-523">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="773db-524">Remove-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="773db-524">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="773db-525">Enable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="773db-525">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="773db-526">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="773db-526">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="773db-527">Disable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="773db-527">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="773db-528">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="773db-528">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="773db-529">El lett távolítva a RetentionDays paraméter ügyféloldali érvényesítése a Set-AzSqlDatabaseBackupShortTermRetentionPolicy parancsmagból</span><span class="sxs-lookup"><span data-stu-id="773db-529">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="773db-530">A Vnet-ben található tárfiók naplózása, javítva a Storage Blob-adatok közreműködői szerepkörének létrehozásakor fellépő hiba.</span><span class="sxs-lookup"><span data-stu-id="773db-530">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="773db-531">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="773db-531">Az.Storage</span></span>
* <span data-ttu-id="773db-532">Hozzá lett adva az -AsJob a fiók Get-AzStorageAccount parancsmagjának lekéréséhez vagy listázásához</span><span class="sxs-lookup"><span data-stu-id="773db-532">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="773db-533">A KeyVersion választható lett a Storage-fiók KeyvaultEncryption használatával történő frissítésekor a kulcs automatikus rotálásának támogatásához</span><span class="sxs-lookup"><span data-stu-id="773db-533">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="773db-534">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="773db-534">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="773db-535">Javítva a hiba, amely során az Azure File Directory eltávolítása egy folyamattal meghiúsult</span><span class="sxs-lookup"><span data-stu-id="773db-535">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="773db-536">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="773db-536">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="773db-537">[#9880] javítva: Módosítva lett a NetWorkRule DefaultAction értékdefiníciója, hogy megfeleljen a Swaggernek.</span><span class="sxs-lookup"><span data-stu-id="773db-537">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="773db-538">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="773db-538">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="773db-539">Get-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="773db-539">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="773db-540">[#11624] javítva: Duplikált szabályok kihagyása NetworkRules hozzáadásakor a kiszolgáló meghibásodásának elkerülése érdekében</span><span class="sxs-lookup"><span data-stu-id="773db-540">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="773db-541">Add-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="773db-541">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="773db-542">A Microsoft.Azure.Cosmos.Table SDK verziója 1.0.7-re frissült</span><span class="sxs-lookup"><span data-stu-id="773db-542">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="773db-543">Hozzá lett adva egy figyelmeztető üzenet, amely emlékezteti a felhasználót, hogy listázzon újra a ContinuationToken használatával, ha csak részleges elemeket ad vissza a rendszer a Data Lake Gen2 elemek listáján</span><span class="sxs-lookup"><span data-stu-id="773db-543">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="773db-544">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="773db-544">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="773db-545">Storage-fiók létrehozásának és frissítésének támogatása Azure Files Active Directory Domain Service-hitelesítéssel</span><span class="sxs-lookup"><span data-stu-id="773db-545">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="773db-546">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="773db-546">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="773db-547">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="773db-547">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="773db-548">Storage-fiók Kerberos-kulcsai listázásának vagy új Kerberos-kulcsok létrehozásának támogatása</span><span class="sxs-lookup"><span data-stu-id="773db-548">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="773db-549">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="773db-549">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="773db-550">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="773db-550">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="773db-551">Feladatátvételi Storage-fiók támogatása</span><span class="sxs-lookup"><span data-stu-id="773db-551">Supported failover Storage account</span></span>
    - <span data-ttu-id="773db-552">Invoke-AzStorageAccountFailover</span><span class="sxs-lookup"><span data-stu-id="773db-552">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="773db-553">Frissítve a Get-AzStorageBlobCopyState súgója</span><span class="sxs-lookup"><span data-stu-id="773db-553">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="773db-554">Frissítve a Get-AzStorageFileCopyState és a Start-AzStorageBlobCopy súgója</span><span class="sxs-lookup"><span data-stu-id="773db-554">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="773db-555">A Storage-ügyfélkódtár 12-es verziója integrálva lett a Queue és a File parancsmagokba</span><span class="sxs-lookup"><span data-stu-id="773db-555">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="773db-556">A kimenet típusa CloudFile helyett mostantól AzureStorageFile, az eredeti kimenet az új kimenet gyermektulajdonsága lesz</span><span class="sxs-lookup"><span data-stu-id="773db-556">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="773db-557">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="773db-557">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="773db-558">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="773db-558">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="773db-559">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="773db-559">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="773db-560">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="773db-560">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="773db-561">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="773db-561">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="773db-562">A kimenet típusa CloudFileDirectory helyett mostantól AzureStorageFileDirectory, az eredeti kimenet az új kimenet gyermektulajdonsága lesz</span><span class="sxs-lookup"><span data-stu-id="773db-562">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="773db-563">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="773db-563">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="773db-564">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="773db-564">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="773db-565">A kimenet típusa CloudFileShare helyett mostantól AzureStorageFileShare, az eredeti kimenet az új kimenet gyermektulajdonsága lesz</span><span class="sxs-lookup"><span data-stu-id="773db-565">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="773db-566">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="773db-566">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="773db-567">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="773db-567">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="773db-568">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="773db-568">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="773db-569">A kimenet típusa FileShareProperties helyett mostantól AzureStorageFileShare, az eredeti kimenet az új kimenet gyermek-altulajdonsága lesz</span><span class="sxs-lookup"><span data-stu-id="773db-569">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="773db-570">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="773db-570">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="773db-571">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="773db-571">Az.TrafficManager</span></span>
* <span data-ttu-id="773db-572">Javítva a hibás profilnév a DisableAzureTrafficManagerEndpoint részletes kimenetében</span><span class="sxs-lookup"><span data-stu-id="773db-572">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="773db-573">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="773db-573">Az.Websites</span></span>
* <span data-ttu-id="773db-574">Javítva az elgépelés az Update-AzWebAppAccessRestrictionConfig súgójában.</span><span class="sxs-lookup"><span data-stu-id="773db-574">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="773db-575">3.8.0 – 2020. április</span><span class="sxs-lookup"><span data-stu-id="773db-575">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="773db-576">A legutóbbi kiadás óta bevezetett újdonságok</span><span class="sxs-lookup"><span data-stu-id="773db-576">Highlights since the last release</span></span>
* <span data-ttu-id="773db-577">Az Az.Storage által támogatott PowerShell-verziók: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="773db-577">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="773db-578">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="773db-578">Az.Accounts</span></span>
* <span data-ttu-id="773db-579">Frissítve lett az Azure PowerShell-felmérés URL-címe a következő helyen: Resolve-AzError [#11507]</span><span class="sxs-lookup"><span data-stu-id="773db-579">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="773db-580">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="773db-580">Az.ApiManagement</span></span>
* <span data-ttu-id="773db-581">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó értesítés az Azure File parancsmagok kimenetére vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="773db-581">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="773db-582">Set-AzApiManagementGroup – Frissítve lett a dokumentáció a GroupId paraméter meghatározása érdekében</span><span class="sxs-lookup"><span data-stu-id="773db-582">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="773db-583">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="773db-583">Az.Cdn</span></span>
* <span data-ttu-id="773db-584">Ki lett javítva a díjszabási termékváltozat megjelenítése a ChinaCDN kapcsán</span><span class="sxs-lookup"><span data-stu-id="773db-584">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="773db-585">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="773db-585">Az.CognitiveServices</span></span>
* <span data-ttu-id="773db-586">Támogatott identitás, Titkosítás, UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="773db-586">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="773db-587">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-587">Az.Compute</span></span>
* <span data-ttu-id="773db-588">Hozzá lett adva a Set-AzVmssOrchestrationServiceState parancsmag.</span><span class="sxs-lookup"><span data-stu-id="773db-588">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="773db-589">A Get-AzVmss az InstanceView használatával az OrchestrationService állapotait mutatja.</span><span class="sxs-lookup"><span data-stu-id="773db-589">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="773db-590">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="773db-590">Az.IotHub</span></span>
* <span data-ttu-id="773db-591">Az IoT-ikereszköz konfigurációjának kezelése, Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="773db-591">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="773db-592">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="773db-592">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="773db-593">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="773db-593">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="773db-594">Hozzá lett adva egy parancsmag a közvetlen metódusok az IoT Hubban lévő eszközökön való meghívásához.</span><span class="sxs-lookup"><span data-stu-id="773db-594">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="773db-595">Az IoT-ikereszköz modulja konfigurációjának kezelése, Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="773db-595">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="773db-596">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="773db-596">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="773db-597">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="773db-597">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="773db-598">Nagy méretekben történő automatikus IoT-eszközfelügyelet konfigurációjának kezelése.</span><span class="sxs-lookup"><span data-stu-id="773db-598">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="773db-599">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="773db-599">New cmdlets are:</span></span>
    - <span data-ttu-id="773db-600">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="773db-600">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="773db-601">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="773db-601">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="773db-602">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="773db-602">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="773db-603">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="773db-603">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="773db-604">Hozzá lett adva egy parancsmag az Edge-modul metódusok az IoT Hubban való meghívásához.</span><span class="sxs-lookup"><span data-stu-id="773db-604">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="773db-605">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="773db-605">Az.KeyVault</span></span>
* <span data-ttu-id="773db-606">Hozzá lett adva egy új Update-AzKeyVault parancsmag a helyreállító törlés és végleges törlés elleni védelem tárolón való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="773db-606">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="773db-607">Támogatás a következőhöz: Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="773db-607">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="773db-608">Ki lettek javítva a Remove-AzKeyVaultManagedStorageSasDefinition [#11479] példáinak hibái</span><span class="sxs-lookup"><span data-stu-id="773db-608">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="773db-609">Támogatás a privát végponthoz</span><span class="sxs-lookup"><span data-stu-id="773db-609">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="773db-610">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="773db-610">Az.Maintenance</span></span>
* <span data-ttu-id="773db-611">Karbantartási parancsmagok végleges verziójának közzététele az általánosan elérhető kiadás számára</span><span class="sxs-lookup"><span data-stu-id="773db-611">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="773db-612">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="773db-612">Az.Monitor</span></span>
* <span data-ttu-id="773db-613">Parancsmagok hozzáadva a privát kapcsolat hatóköréhez</span><span class="sxs-lookup"><span data-stu-id="773db-613">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="773db-614">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="773db-614">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="773db-615">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="773db-615">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="773db-616">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="773db-616">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="773db-617">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="773db-617">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="773db-618">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="773db-618">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="773db-619">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="773db-619">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="773db-620">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="773db-620">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="773db-621">Az.Network</span><span class="sxs-lookup"><span data-stu-id="773db-621">Az.Network</span></span>
* <span data-ttu-id="773db-622">Frissítve lettek a parancsmagok a virtuális hálózati átjáróhoz való csatlakozás engedélyezéséhez magánhálózati IP-cím esetében.</span><span class="sxs-lookup"><span data-stu-id="773db-622">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="773db-623">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="773db-623">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="773db-624">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="773db-624">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="773db-625">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="773db-625">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="773db-626">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="773db-626">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="773db-627">Frissítve lettek a parancsmagok az FQDN-alapú LocalNetworkGateways és VpnSites engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="773db-627">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="773db-628">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="773db-628">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="773db-629">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="773db-629">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="773db-630">Az IPv6-címcsalád támogatása a következőben: ExpressRouteCircuitConnectionConfig (Global Reach)</span><span class="sxs-lookup"><span data-stu-id="773db-630">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="773db-631">Hozzá lett adva a Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="773db-631">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="773db-632">lehetővé teszi az összes meglévő tulajdonság beállítását, beleértve a következőt is: IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="773db-632">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="773db-633">Frissítve lett az Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="773db-633">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="773db-634">Hozzá lett adva egy másik opcionális AddressPrefixType paraméter a címelőtag címcsaládjának meghatározásához</span><span class="sxs-lookup"><span data-stu-id="773db-634">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="773db-635">Frissítve lettek a parancsmagok a DPD-időtúllépés beállításának engedélyezéséhez a virtuális hálózati átjáró kapcsolatain.</span><span class="sxs-lookup"><span data-stu-id="773db-635">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="773db-636">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="773db-636">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="773db-637">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="773db-637">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="773db-638">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="773db-638">Az.PolicyInsights</span></span>
* <span data-ttu-id="773db-639">Hozzá lett adva a Start-AzPolicyComplianceScan parancsmag a szabályzatok megfelelőségi vizsgálatának elindításához</span><span class="sxs-lookup"><span data-stu-id="773db-639">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="773db-640">Szabályzatdefiníció, készletdefiníció és hozzárendelési verziók hozzáadva a Get-AzPolicyState kimenetéhez</span><span class="sxs-lookup"><span data-stu-id="773db-640">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="773db-641">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="773db-641">Az.ServiceFabric</span></span>
* <span data-ttu-id="773db-642">Tovább lett fejlesztve a kódok formázása és a használhatóság a New-AzServiceFabricCluster példái esetében</span><span class="sxs-lookup"><span data-stu-id="773db-642">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="773db-643">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-643">Az.Sql</span></span>
* <span data-ttu-id="773db-644">Hozzá lettek adva a Get-AzSqlInstanceOperation és a Stop-AzSqlInstanceOperation parancsmagok</span><span class="sxs-lookup"><span data-stu-id="773db-644">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="773db-645">Naplózás támogatása egy VNet-ben található tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="773db-645">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="773db-646">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="773db-646">Az.Storage</span></span>
* <span data-ttu-id="773db-647">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó értesítés az Azure File parancsmagok kimenetére vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="773db-647">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="773db-648">Támogatott új SkuName StandardGZRS, StandardRAGZRS a Storage-fiók létrehozása/frissítése során</span><span class="sxs-lookup"><span data-stu-id="773db-648">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="773db-649">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="773db-649">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="773db-650">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="773db-650">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="773db-651">Támogatott Data Lake Gen2</span><span class="sxs-lookup"><span data-stu-id="773db-651">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="773db-652">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="773db-652">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="773db-653">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="773db-653">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="773db-654">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="773db-654">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="773db-655">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="773db-655">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="773db-656">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="773db-656">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="773db-657">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="773db-657">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="773db-658">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="773db-658">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="773db-659">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="773db-659">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="773db-660">0.10.0-s előzetes verzió – 2020. április</span><span class="sxs-lookup"><span data-stu-id="773db-660">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="773db-661">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="773db-661">General</span></span>
* <span data-ttu-id="773db-662">Az Az modulok előzetes verziója mostantól elérhető az Azure Stack Hubon.</span><span class="sxs-lookup"><span data-stu-id="773db-662">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="773db-663">Ez lehetővé teszi a platformok közötti kompatibilitást a Linux és a macOs rendszerekkel.</span><span class="sxs-lookup"><span data-stu-id="773db-663">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="773db-664">A Azure Stack Hub mostantól támogatja a PowerShell Core-t az Az modulokkal, további információt [itt](https://aka.ms/az4AzureStack) talál</span><span class="sxs-lookup"><span data-stu-id="773db-664">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="773db-665">Az Az modulok támogatják a 2019-03-01-hybrid profilt:</span><span class="sxs-lookup"><span data-stu-id="773db-665">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="773db-666">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="773db-666">Az.Billing</span></span>
  - <span data-ttu-id="773db-667">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-667">Az.Compute</span></span>
  - <span data-ttu-id="773db-668">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="773db-668">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="773db-669">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="773db-669">Az.EventHub</span></span>
  - <span data-ttu-id="773db-670">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="773db-670">Az.IotHub</span></span>
  - <span data-ttu-id="773db-671">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="773db-671">Az.KeyVault</span></span>
  - <span data-ttu-id="773db-672">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="773db-672">Az.Monitor</span></span>
  - <span data-ttu-id="773db-673">Az.Network</span><span class="sxs-lookup"><span data-stu-id="773db-673">Az.Network</span></span>
  - <span data-ttu-id="773db-674">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-674">Az.Resources</span></span>
  - <span data-ttu-id="773db-675">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="773db-675">Az.Storage</span></span>
  - <span data-ttu-id="773db-676">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="773db-676">Az.Websites</span></span>
* <span data-ttu-id="773db-677">A következő három új PowerShell-modul lett bevezetve, amelyek használhatók az Azure Stack Hubbal: Az.Databox, Az.IotHub és Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="773db-677">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="773db-678">A parancsok viszonylag változatlanok maradnak, kisebb módosításokkal. Például az Az helyébe az AzureRM lép.</span><span class="sxs-lookup"><span data-stu-id="773db-678">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="773db-679">Az Azure Stack Hubhoz kapcsolódó PowerShell-dokumentáció frissített hivatkozását [itt](https://aka.ms/InstallASHPowerShell) találja</span><span class="sxs-lookup"><span data-stu-id="773db-679">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="773db-680">3.7.0 – 2020. március</span><span class="sxs-lookup"><span data-stu-id="773db-680">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="773db-681">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="773db-681">Az.Accounts</span></span>
* <span data-ttu-id="773db-682">Ki lett javítva az a hiba, hogy a Get-AzTenant/Get-AzDefault/Set-AzDefault parancs NullReferenceException hibát ad vissza kijelentkezett állapotban [#10292]</span><span class="sxs-lookup"><span data-stu-id="773db-682">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="773db-683">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-683">Az.Compute</span></span>
* <span data-ttu-id="773db-684">A következő paraméterek lettek hozzáadva a New-AzDiskConfig parancsmaghoz:</span><span class="sxs-lookup"><span data-stu-id="773db-684">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="773db-685">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="773db-685">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="773db-686">Engedélyezve lett a New-AzGalleryImageVersion parancsmag célparaméterének titkosítási tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="773db-686">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="773db-687">Ki lett javítva a tempDisk hibája a Set-AzVmss -Reimage és az Invoke-AzVMReimage parancsmag esetében.</span><span class="sxs-lookup"><span data-stu-id="773db-687">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="773db-688">[#11354]</span><span class="sxs-lookup"><span data-stu-id="773db-688">[#11354]</span></span>
* <span data-ttu-id="773db-689">Az alábbi parancsmagok mostantól támogatottak az új SAP-bővítmény esetében</span><span class="sxs-lookup"><span data-stu-id="773db-689">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="773db-690">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="773db-690">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="773db-691">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="773db-691">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="773db-692">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="773db-692">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="773db-693">Update-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="773db-693">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="773db-694">Ki lettek javítva a súgódokumentáció példáinak hibái</span><span class="sxs-lookup"><span data-stu-id="773db-694">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="773db-695">Táblázatos formátumban jelenítette meg a sztring pontos értékét a PowerState virtuális gép esetében.</span><span class="sxs-lookup"><span data-stu-id="773db-695">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="773db-696">New-AzVmssConfig: ki lett javítva az AutomaticRepairs tulajdonság szerializálása a SinglePlacementGroup letiltott állapota esetén.</span><span class="sxs-lookup"><span data-stu-id="773db-696">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="773db-697">[#11257]</span><span class="sxs-lookup"><span data-stu-id="773db-697">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="773db-698">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="773db-698">Az.DataFactory</span></span>
* <span data-ttu-id="773db-699">Az ADF .Net SDK a 4.8.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="773db-699">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="773db-700">Opcionális paraméterek lettek hozzáadva az Invoke-AzDataFactoryV2Pipeline parancshoz az újrafuttatás támogatásához</span><span class="sxs-lookup"><span data-stu-id="773db-700">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="773db-701">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="773db-701">Az.DataLakeStore</span></span>
* <span data-ttu-id="773db-702">Hozzá lett adva a kompatibilitástörő változás leírása az Export-AzDataLakeStoreItem és az Import-AzDataLakeStoreItem parancsok esetében</span><span class="sxs-lookup"><span data-stu-id="773db-702">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="773db-703">A bájtkódolási lehetőség hozzá lett adva a New-AzDataLakeStoreItem, az Add-AzDAtaLakeStoreItemContent és a Get-AzDAtaLakeStoreItemContent parancsok esetében</span><span class="sxs-lookup"><span data-stu-id="773db-703">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="773db-704">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="773db-704">Az.HDInsight</span></span>
* <span data-ttu-id="773db-705">Fürt létrehozásakor a minimálisan támogatott TLS-verzió megadása támogatott.</span><span class="sxs-lookup"><span data-stu-id="773db-705">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="773db-706">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="773db-706">Az.IotHub</span></span>
* <span data-ttu-id="773db-707">Hozzá lett adva az elosztott beállítások eszközönkénti felügyeletének támogatása.</span><span class="sxs-lookup"><span data-stu-id="773db-707">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="773db-708">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="773db-708">New Cmdlets are:</span></span>
    - <span data-ttu-id="773db-709">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="773db-709">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="773db-710">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="773db-710">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="773db-711">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="773db-711">Az.KeyVault</span></span>
* <span data-ttu-id="773db-712">Kompatibilitástörő változást okozó attribútumok lettek hozzáadva a New-AzKeyVault parancshoz</span><span class="sxs-lookup"><span data-stu-id="773db-712">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="773db-713">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="773db-713">Az.Monitor</span></span>
* <span data-ttu-id="773db-714">Frissült a New-AzScheduledQueryRuleLogMetricTrigger dokumentációja</span><span class="sxs-lookup"><span data-stu-id="773db-714">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="773db-715">Az.Network</span><span class="sxs-lookup"><span data-stu-id="773db-715">Az.Network</span></span>
* <span data-ttu-id="773db-716">Frissültek a parancsmagok a több-bérlős VirtualHubVnetConnections engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="773db-716">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="773db-717">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="773db-717">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="773db-718">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="773db-718">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="773db-719">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="773db-719">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="773db-720">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="773db-720">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="773db-721">Az SQL Management SDK-függőség el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="773db-721">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="773db-722">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="773db-722">Az.PolicyInsights</span></span>
* <span data-ttu-id="773db-723">Továbbfejlesztett hibaüzenetek</span><span class="sxs-lookup"><span data-stu-id="773db-723">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="773db-724">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="773db-724">Az.RecoveryServices</span></span>
* <span data-ttu-id="773db-725">Hozzá lett adva az Azure Site Recovery-támogatás az Azure Diskkel titkosított virtuális gépek védelmének újbóli beállítása és frissített virtuálisgép-tulajdonságai esetében.</span><span class="sxs-lookup"><span data-stu-id="773db-725">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="773db-726">Hozzá lett adva az Azure Site Recovery VmwareToAzure tulajdonságainak vészhelyreállítási monitorozása</span><span class="sxs-lookup"><span data-stu-id="773db-726">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="773db-727">Hozzá lett adva az Azure Backup-támogatás a sikertelen elemekre vonatkozó szabályzatfrissítés újbóli végrehajtása esetében.</span><span class="sxs-lookup"><span data-stu-id="773db-727">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="773db-728">Hozzá lett adva az Azure Backup-támogatás a lemezkizárási beállításokhoz a biztonsági mentés és a visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="773db-728">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="773db-729">Hozzá lett adva az Azure Backup-támogatás több fájl/mappa visszaállításához az AzureFileShare-ben</span><span class="sxs-lookup"><span data-stu-id="773db-729">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="773db-730">Hozzá lett adva az Azure Backup-támogatás a felhasználó által megadott erőforráscsoport támogatásához az IaasVM-szabályzat frissítésekor</span><span class="sxs-lookup"><span data-stu-id="773db-730">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="773db-731">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-731">Az.Resources</span></span>
* <span data-ttu-id="773db-732">Ki lett javítva a Get-AzResource-ResourceGroupName-Name-ExpandProperties-ResourceType parancs, hogy ezentúl az erőforrások aktuális API-verzióját használja az alapértelmezett verzió helyett [#11267]</span><span class="sxs-lookup"><span data-stu-id="773db-732">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="773db-733">Hozzá lett adva a CorrelationId-naplózás a hibaforgatókönyvek esetében</span><span class="sxs-lookup"><span data-stu-id="773db-733">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="773db-734">A Get-AzResourceLock dokumentációjában kisebb módosítás történt.</span><span class="sxs-lookup"><span data-stu-id="773db-734">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="773db-735">Példa hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="773db-735">Added example.</span></span>
* <span data-ttu-id="773db-736">A szimpla idézőjel fel lett oldva a Get-AzADUser paraméterértékében [#11317]</span><span class="sxs-lookup"><span data-stu-id="773db-736">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="773db-737">Új parancsmagok lettek hozzáadva az üzembehelyezési szkriptekhez (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript)</span><span class="sxs-lookup"><span data-stu-id="773db-737">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="773db-738">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-738">Az.Sql</span></span>
* <span data-ttu-id="773db-739">Olvasható másodlagos paraméter lett hozzáadva az Invoke-AzSqlDatabaseFailover parancshoz</span><span class="sxs-lookup"><span data-stu-id="773db-739">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="773db-740">A Disable-AzSqlServerActiveDirectoryOnlyAuthentication parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="773db-740">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="773db-741">Az érzékenységi besorolás mentése megtörténik az adatbázis oszlopainak osztályozásakor.</span><span class="sxs-lookup"><span data-stu-id="773db-741">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="773db-742">Az.Support</span><span class="sxs-lookup"><span data-stu-id="773db-742">Az.Support</span></span>
* <span data-ttu-id="773db-743">Az Az.Support modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="773db-743">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="773db-744">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="773db-744">Az.Websites</span></span>
* <span data-ttu-id="773db-745">Mostantól támogatott a webalkalmazások forgalom-útválasztási szabályainak az alábbi új parancsmagokkal történő használata</span><span class="sxs-lookup"><span data-stu-id="773db-745">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="773db-746">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="773db-746">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="773db-747">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="773db-747">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="773db-748">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="773db-748">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="773db-749">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="773db-749">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="773db-750">3.6.1 – 2020. március</span><span class="sxs-lookup"><span data-stu-id="773db-750">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="773db-751">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="773db-751">Az.Accounts</span></span>
* <span data-ttu-id="773db-752">Azure PowerShell felmérési oldal megnyitása itt: Send-Feedback [#11020]</span><span class="sxs-lookup"><span data-stu-id="773db-752">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="773db-753">Azure PowerShell-felmérés URL-címének megjelenítése itt: Resolve-Error [#11021]</span><span class="sxs-lookup"><span data-stu-id="773db-753">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="773db-754">Az-verzió hozzáadva az UserAgenthez</span><span class="sxs-lookup"><span data-stu-id="773db-754">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="773db-755">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="773db-755">Az.ApiManagement</span></span>
* <span data-ttu-id="773db-756">Mostantól támogatott az egyéni tartomány lekérése és konfigurálása a DeveloperPortal végpontján [#11007]</span><span class="sxs-lookup"><span data-stu-id="773db-756">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="773db-757">Export-AzApiManagementAPi – Mostantól támogatott az Api-definíció Json formátumban való letöltése [#9987]</span><span class="sxs-lookup"><span data-stu-id="773db-757">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="773db-758">Import-AzApiManagementApi – Az OpenAPI 3.0-definíció Json-dokumentumokból való importálása mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="773db-758">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="773db-759">New-AzApiManagementIdentityProvider és Set-AzApiManagementIdentityProvider – A Signin Tenant konfigurálása az AAD B2C-szolgáltató esetében mostantól támogatott. [#9784]</span><span class="sxs-lookup"><span data-stu-id="773db-759">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="773db-760">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="773db-760">Az.DataLakeStore</span></span>
* <span data-ttu-id="773db-761">A System.Buffershez hivatkozásának explicit hozzáadása a következőkben: csproj és psd1</span><span class="sxs-lookup"><span data-stu-id="773db-761">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="773db-762">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="773db-762">Az.IotHub</span></span>
* <span data-ttu-id="773db-763">Az eszközök az IoT Hubban való kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="773db-763">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="773db-764">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="773db-764">New Cmdlets are:</span></span>
    - <span data-ttu-id="773db-765">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="773db-765">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="773db-766">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="773db-766">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="773db-767">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="773db-767">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="773db-768">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="773db-768">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="773db-769">A cél IoT-eszközökön lévő modulok IoT Hubban való kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="773db-769">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="773db-770">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="773db-770">New Cmdlets are:</span></span>
    - <span data-ttu-id="773db-771">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="773db-771">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="773db-772">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="773db-772">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="773db-773">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="773db-773">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="773db-774">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="773db-774">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="773db-775">Parancsmag hozzáadva egy IoT Hubban lévő cél IoT-eszköz kapcsolati sztringjének lekéréséhez.</span><span class="sxs-lookup"><span data-stu-id="773db-775">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="773db-776">Parancsmag hozzáadva egy IoT Hubban lévő cél IoT-eszköz modulja kapcsolati sztringjének lekéréséhez.</span><span class="sxs-lookup"><span data-stu-id="773db-776">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="773db-777">Az IoT-eszközök szülő eszközének lekérése/beállítása mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="773db-777">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="773db-778">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="773db-778">New Cmdlets are:</span></span>
    - <span data-ttu-id="773db-779">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="773db-779">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="773db-780">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="773db-780">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="773db-781">Az eszközök szülő-gyermek kapcsolatainak kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="773db-781">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="773db-782">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="773db-782">Az.Monitor</span></span>
* <span data-ttu-id="773db-783">A Get-AzMetricDefinition kimeneti értéke javítva [#9714]</span><span class="sxs-lookup"><span data-stu-id="773db-783">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="773db-784">Az.Network</span><span class="sxs-lookup"><span data-stu-id="773db-784">Az.Network</span></span>
* <span data-ttu-id="773db-785">SQL Management SDK frissítve.</span><span class="sxs-lookup"><span data-stu-id="773db-785">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="773db-786">Kijavítottuk a PrivateLinkServiceConnectionState osztály eltérő elnevezéssel kapcsolatos hibáját.</span><span class="sxs-lookup"><span data-stu-id="773db-786">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="773db-787">Az ActionsRequired mező leképezése a követezőre: ActionRequired</span><span class="sxs-lookup"><span data-stu-id="773db-787">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="773db-788">PublicNetworkAccess hozzáadva a következőhöz: New-AzSqlServer és Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="773db-788">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="773db-789">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-789">Az.Resources</span></span>
* <span data-ttu-id="773db-790">A Get-AzRoleAssignment null értékű hivatkozásra vonatkozó hibája javítva</span><span class="sxs-lookup"><span data-stu-id="773db-790">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="773db-791">A -Force és a -PassThru kapcsoló nem kötelezőként lett megjelölve a Remove-AzADGroup esetében [#10849]</span><span class="sxs-lookup"><span data-stu-id="773db-791">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="773db-792">Javítva a hiba, amely miatt a MailNickname nem lett visszaadva Remove-AzADGroup esetében [#11167]</span><span class="sxs-lookup"><span data-stu-id="773db-792">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="773db-793">A Remove-AzADGroup folyamatművelet működési hibája kijavítva [#11171]</span><span class="sxs-lookup"><span data-stu-id="773db-793">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="773db-794">A GetAzureRoleAssignmentCommand null értékű hivatkozásra vonatkozó hibája javítva</span><span class="sxs-lookup"><span data-stu-id="773db-794">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="773db-795">Kompatibilitástörő változás hozzáadva a szabályzati parancsmagok soron következő változásaihoz</span><span class="sxs-lookup"><span data-stu-id="773db-795">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="773db-796">Frissült a Get-AzResourceGroup az erőforráscsoport-címke kiszolgálóoldali szűrésének elvégzéséhez</span><span class="sxs-lookup"><span data-stu-id="773db-796">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="773db-797">A címkeparancsmagok kiterjesztése a -ResourceID elfogadása érdekében</span><span class="sxs-lookup"><span data-stu-id="773db-797">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="773db-798">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="773db-798">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="773db-799">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="773db-799">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="773db-800">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="773db-800">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="773db-801">Új címkeparancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-801">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="773db-802">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="773db-802">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="773db-803">A ScopedDeployment áthozva az SDK 3.3.0-ból</span><span class="sxs-lookup"><span data-stu-id="773db-803">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="773db-804">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-804">Az.Sql</span></span>
* <span data-ttu-id="773db-805">PublicNetworkAccess hozzáadva a következőhöz: New-AzSqlServer és Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="773db-805">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="773db-806">Támogatás hozzáadva a biztonsági másolatok hosszú távú megőrzési konfigurációjához a felügyelt adatbázisok esetében</span><span class="sxs-lookup"><span data-stu-id="773db-806">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="773db-807">LTR-szabályzat lekérése/beállítása felügyelt adatbázison</span><span class="sxs-lookup"><span data-stu-id="773db-807">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="773db-808">LTR biztonsági másolat(ok) lekérése felügyelt adatbázis, felügyelt példány vagy hely szerint</span><span class="sxs-lookup"><span data-stu-id="773db-808">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="773db-809">LTR biztonsági másolat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="773db-809">Remove an LTR backup</span></span>
    - <span data-ttu-id="773db-810">LTR biztonsági másolat visszaállítása új felügyelt adatbázis létrehozásához</span><span class="sxs-lookup"><span data-stu-id="773db-810">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="773db-811">MinimalTlsVersion hozzáadva a következőkhöz: New-AzSqlServer és Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="773db-811">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="773db-812">MinimalTlsVersion hozzáadva a következőkhöz: New-AzSqlInstance és Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="773db-812">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="773db-813">Az SQL SDK-verzió felléptetése a következőhöz: AZ.Network</span><span class="sxs-lookup"><span data-stu-id="773db-813">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="773db-814">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="773db-814">Az.Storage</span></span>
* <span data-ttu-id="773db-815">Támogatott AllowProtectedAppendWrite a következőben: ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="773db-815">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="773db-816">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="773db-816">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="773db-817">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó figyelmeztető üzenet az AzureStorageTable típusának módosítására vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="773db-817">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="773db-818">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="773db-818">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="773db-819">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="773db-819">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="773db-820">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="773db-820">Az.Websites</span></span>
* <span data-ttu-id="773db-821">Címke paraméter hozzáadva a következőkhöz: New-AzAppServicePlan és Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="773db-821">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="773db-822">A parancsmag végrehajtásának leállítása, ha egy egyéni tartomány webhelyhez történő hozzáadásakor a rendszer kivételt ad vissza</span><span class="sxs-lookup"><span data-stu-id="773db-822">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="773db-823">Támogatás hozzáadva az olyan App Services műveletek elvégzéséhez, amelyek nem abban az erőforráscsoportban vannak, amelyben az App Service-csomag</span><span class="sxs-lookup"><span data-stu-id="773db-823">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="773db-824">Hozzáférési korlátozás alkalmazva a különböző erőforráscsoportokban lévő webalkalmazásokra/függvényekre</span><span class="sxs-lookup"><span data-stu-id="773db-824">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="773db-825">Az egyéni WebAppSlots-gazdanevek beállítására vonatkozó hiba kijavítva</span><span class="sxs-lookup"><span data-stu-id="773db-825">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="773db-826">3.5.0 – 2020. február</span><span class="sxs-lookup"><span data-stu-id="773db-826">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="773db-827">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="773db-827">Highlights since the last major release</span></span>
* <span data-ttu-id="773db-828">Frissült az ügyféloldali telemetria.</span><span class="sxs-lookup"><span data-stu-id="773db-828">Updated client side telemetry.</span></span>
* <span data-ttu-id="773db-829">Az.IotHub: parancsmagok hozzáadva az eszközkezelés támogatásához.</span><span class="sxs-lookup"><span data-stu-id="773db-829">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="773db-830">Az.SqlVirtualMachine: parancsmagok hozzáadva a rendelkezésreállási csoport figyelőjéhez.</span><span class="sxs-lookup"><span data-stu-id="773db-830">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="773db-831">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="773db-831">Az.Accounts</span></span>
* <span data-ttu-id="773db-832">A SubscriptionId, a TenantId és a végrehajtási idő hozzáadva az ügyféloldali telemetria adataihoz.</span><span class="sxs-lookup"><span data-stu-id="773db-832">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="773db-833">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="773db-833">Az.Automation</span></span>
* <span data-ttu-id="773db-834">Ki lett javítva a „New-AzAutomationSoftwareUpdateConfiguration” referenciadokumentációjának 1. példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="773db-834">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="773db-835">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="773db-835">Az.CognitiveServices</span></span>
* <span data-ttu-id="773db-836">Az SDK a 7.0-ás verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="773db-836">Updated SDK to 7.0</span></span>
* <span data-ttu-id="773db-837">Tovább lett fejlesztve a hibaüzenet, amely akkor jelenik meg, ha a kiszolgáló üres törzset ad vissza válaszként</span><span class="sxs-lookup"><span data-stu-id="773db-837">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="773db-838">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-838">Az.Compute</span></span>
* <span data-ttu-id="773db-839">A ProximityPlacementGroupId mostantól üres értékkel is rendelkezhet a frissítés során</span><span class="sxs-lookup"><span data-stu-id="773db-839">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="773db-840">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="773db-840">Az.FrontDoor</span></span>
* <span data-ttu-id="773db-841">Új parancsmag hozzáadva a WAF-ban használható felügyelt szabálydefiníciók lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="773db-841">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="773db-842">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="773db-842">Az.IotHub</span></span>
* <span data-ttu-id="773db-843">Az eszközök az IoT Hubban való kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="773db-843">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="773db-844">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="773db-844">New Cmdlets are:</span></span>
    - <span data-ttu-id="773db-845">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="773db-845">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="773db-846">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="773db-846">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="773db-847">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="773db-847">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="773db-848">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="773db-848">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="773db-849">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="773db-849">Az.KeyVault</span></span>
* <span data-ttu-id="773db-850">Ki lett javítva az Add-AzKeyVaultKey.md duplikált szövege</span><span class="sxs-lookup"><span data-stu-id="773db-850">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="773db-851">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="773db-851">Az.Monitor</span></span>
* <span data-ttu-id="773db-852">Ki lett javítva a Get-AzLog parancsmag leírása.</span><span class="sxs-lookup"><span data-stu-id="773db-852">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="773db-853">Egy új, ActionGroupId nevű paraméter lett hozzáadva a „New-AzMetricAlertRuleV2” parancshoz.</span><span class="sxs-lookup"><span data-stu-id="773db-853">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="773db-854">A felhasználó a következőket adhatja meg: ActionGroupId(string) vagy ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="773db-854">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="773db-855">Az.Network</span><span class="sxs-lookup"><span data-stu-id="773db-855">Az.Network</span></span>
* <span data-ttu-id="773db-856">Hozzá lett adva egy extra paramétermegjegyzés a „New-AzPrivateLinkService” parancsmag „-EnableProxyProtocol” paraméteréhez.</span><span class="sxs-lookup"><span data-stu-id="773db-856">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="773db-857">A Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és a Start-AzVirtualnetworkGatewayPacketCapture.md FilterData kapcsolójának példái ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="773db-857">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="773db-858">Hozzá lett adva egy csomagrögzítési példa a Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és Start-AzVirtualnetworkGatewayPacketCapture.md minden belső és külső csomagjának rögzítéséhez.</span><span class="sxs-lookup"><span data-stu-id="773db-858">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="773db-859">Az Azure Firewall-szabályzat mostantól támogatott a Vnet-tűzfalakon</span><span class="sxs-lookup"><span data-stu-id="773db-859">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="773db-860">Nem lettek hozzáadva új parancsmagok.</span><span class="sxs-lookup"><span data-stu-id="773db-860">No new cmdlets are added.</span></span> <span data-ttu-id="773db-861">Enyhítve lettek a tűzfalszabályzat korlátozásai a Vnet-tűzfalak esetében</span><span class="sxs-lookup"><span data-stu-id="773db-861">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="773db-862">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="773db-862">Az.RecoveryServices</span></span>
* <span data-ttu-id="773db-863">A fájlokként történő visszaállítás mostantól támogatott az SQL-adatbázisok esetében.</span><span class="sxs-lookup"><span data-stu-id="773db-863">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="773db-864">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-864">Az.Resources</span></span>
* <span data-ttu-id="773db-865">Újra lettek tervezve a sablonalapú üzembehelyezési parancsmagok</span><span class="sxs-lookup"><span data-stu-id="773db-865">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="773db-866">Új parancsmagok lettek hozzáadva a felügyeleti csoportban való üzembe helyezés kezeléséhez: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="773db-866">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="773db-867">Új parancsmagok lettek hozzáadva a bérlői hatókörben való üzembe helyezés kezeléséhez: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="773db-867">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="773db-868">Az \*-AzDeployment parancsmagok kifejezetten az előfizetési hatókörben való működéshez lettek újratervezve</span><span class="sxs-lookup"><span data-stu-id="773db-868">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="773db-869">Az \*-AzSubscriptionDeployment aliasok lettek létrehozva az \*-AzDeployment parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="773db-869">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="773db-870">Ki lett javítva az „Update-AzADApplication” nem beállított „AvailableToOtherTenants” paraméter esetében</span><span class="sxs-lookup"><span data-stu-id="773db-870">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="773db-871">Az ApplicationObjectWithoutCredentialParameterSet el lett távolítva az AmbiguousParameterSetException elkerülése érdekében.</span><span class="sxs-lookup"><span data-stu-id="773db-871">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="773db-872">A súgófájlok újra létre lettek hozva</span><span class="sxs-lookup"><span data-stu-id="773db-872">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="773db-873">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-873">Az.Sql</span></span>
* <span data-ttu-id="773db-874">Az előfizetések közötti időponthoz kötött visszaállítás mostantól támogatott a felügyelt példányokon.</span><span class="sxs-lookup"><span data-stu-id="773db-874">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="773db-875">A már meglévő felügyelt SQL-példány hardvergenerációjának módosítása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="773db-875">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="773db-876">Ki lettek javítva az „Update-AzSqlServerVulnerabilityAssessmentSetting” súgópéldái: paraméter/tulajdonságkimenet – EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="773db-876">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="773db-877">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="773db-877">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="773db-878">Parancsmagokat hozzáadva a rendelkezésreállási csoport figyelőjéhez</span><span class="sxs-lookup"><span data-stu-id="773db-878">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="773db-879">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="773db-879">Az.StorageSync</span></span>
* <span data-ttu-id="773db-880">Frissültek az „Invoke-AzStorageSyncCompatibilityCheck” támogatott karakterkészletei.</span><span class="sxs-lookup"><span data-stu-id="773db-880">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="773db-881">3.4.0 – 2020. február</span><span class="sxs-lookup"><span data-stu-id="773db-881">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="773db-882">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="773db-882">Highlights since the last major release</span></span>
* <span data-ttu-id="773db-883">Megjelent az Az.CosmosDB 0.1.0-s kezdeti verziója</span><span class="sxs-lookup"><span data-stu-id="773db-883">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="773db-884">Az.Network ConnectionMonitor V2 támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="773db-884">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="773db-885">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="773db-885">Az.Accounts</span></span>
* <span data-ttu-id="773db-886">A környezet automatikus mentésének letiltása, ha az AzureRmContext.json nem érhető el</span><span class="sxs-lookup"><span data-stu-id="773db-886">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="773db-887">Az Azure Powershell Common referenciájának frissítése 1.3.5-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="773db-887">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="773db-888">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="773db-888">Az.ApiManagement</span></span>
* <span data-ttu-id="773db-889">**Get-AzApiManagementApiSchema** Az API-val társított Open-API séma kijavítása   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="773db-889">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="773db-890">**New-AzApiManagementProduct**\* és **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="773db-890">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="773db-891">https://github.com/Azure/azure-powershell/issues/10472 dokumentációja kijavítva</span><span class="sxs-lookup"><span data-stu-id="773db-891">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="773db-892">**Set-AzApiManagementApi** A ServiceUrl parancsmaggal való frissítését bemutató példa hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-892">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="773db-893">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-893">Az.Compute</span></span>
* <span data-ttu-id="773db-894">A virtuális gép állapotának korlátozása 100 értékre, hogy ne legyen szabályozás, ha a Get-AzVM -Status a virtuális gép neve nélkül lett végrehajtva.</span><span class="sxs-lookup"><span data-stu-id="773db-894">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="773db-895">Update-AzDiskEncryptionSet parancsmagok hozzáadása</span><span class="sxs-lookup"><span data-stu-id="773db-895">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="773db-896">Az EncryptionType és a DiskEncryptionSetId paraméterek hozzáadása a következő parancsmagokhoz:</span><span class="sxs-lookup"><span data-stu-id="773db-896">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="773db-897">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="773db-897">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="773db-898">A ColocationStatus paraméter hozzáadva a Get-AzProximityPlacementGroup parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="773db-898">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="773db-899">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="773db-899">Az.DataFactory</span></span>
* <span data-ttu-id="773db-900">Az ADF .Net SDK frissítve lett a 4.7.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="773db-900">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="773db-901">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="773db-901">Az.DeploymentManager</span></span>
* <span data-ttu-id="773db-902">LIST műveletek hozzáadása az erőforrásokhoz</span><span class="sxs-lookup"><span data-stu-id="773db-902">Adds LIST operations for resources</span></span>
* <span data-ttu-id="773db-903">Műveletek végrehajtásának lehetősége az állapotellenőrzés lépésein</span><span class="sxs-lookup"><span data-stu-id="773db-903">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="773db-904">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="773db-904">Az.HDInsight</span></span>
* <span data-ttu-id="773db-905">A New-AzHDInsightCluster dokumentációs hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="773db-905">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="773db-906">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="773db-906">Az.KeyVault</span></span>
* <span data-ttu-id="773db-907">Name alias hozzáadása a VaultName attribútumhoz, hogy a Remove-AzureKeyVault konzisztens legyen a New-AzureKeyVault paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="773db-907">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="773db-908">Az.Network</span><span class="sxs-lookup"><span data-stu-id="773db-908">Az.Network</span></span>
* <span data-ttu-id="773db-909">Új példa hozzáadva a Set-AzNetworkWatcherConfigFlowLog.md fájlhoz a Traffic Analytics-letiltási forgatókönyv szemléltetésére.</span><span class="sxs-lookup"><span data-stu-id="773db-909">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="773db-910">Felügyeleti IP-konfiguráció támogatás hozzáadva az Azure Firewallhoz – egy dedikált alhálózat és nyilvános IP-cím, amelyet a tűzfal a forgalom felügyeléséhez használni fog</span><span class="sxs-lookup"><span data-stu-id="773db-910">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="773db-911">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="773db-911">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="773db-912">Hozzá lett adva a (nem kötelező) -PublicIpAddress-ManagementPublicIpAddress paraméter, amely egy nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="773db-912">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="773db-913">Hozzá lett adva a SetManagementIpConfiguration metódus a tűzfalobjektumok esetében – nyilvános IP-cím-objektumokat fogad el bemeneti adatként – az alhálózat nevének AzureFirewallManagementSubnet értéknek kell lennie</span><span class="sxs-lookup"><span data-stu-id="773db-913">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="773db-914">A Get-AzNetworkSecurityGroup példái javítva, hogy hálózati biztonsági csoportok példáit tartalmazzák hálózati adapterek helyett.</span><span class="sxs-lookup"><span data-stu-id="773db-914">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="773db-915">Javítottunk egy elírást a New-AzVpnSite parancsban, amely megakadályozta, hogy az erőforrásazonosító-kiegészítő kiegészítsen egy paramétert.</span><span class="sxs-lookup"><span data-stu-id="773db-915">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="773db-916">Az Application Gateway szabály-újraírási műveletkészletének URL-konfigurálása mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="773db-916">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="773db-917">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="773db-917">New cmdlets added:</span></span>
        - <span data-ttu-id="773db-918">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="773db-918">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="773db-919">A parancsmagok frissültek a nem kötelező UrlConfiguration paraméterrel</span><span class="sxs-lookup"><span data-stu-id="773db-919">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="773db-920">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="773db-920">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="773db-921">A Network Watcher Connection Monitor 2-es verziójú erőforrások támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-921">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="773db-922">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="773db-922">Az.PolicyInsights</span></span>
* <span data-ttu-id="773db-923">A javítandó erőforrások azonosítása előtti megfelelőségértékelés támogatása</span><span class="sxs-lookup"><span data-stu-id="773db-923">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="773db-924">-ResourceDiscoverMode paraméter hozzáadása a Start-AzPolicyRemediation parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="773db-924">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="773db-925">A szabályzatok metaadat-erőforrásainak elérésére szolgáló Get-AzPolicyMetadata parancsmag hozzáadása</span><span class="sxs-lookup"><span data-stu-id="773db-925">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="773db-926">A Get-AzPolicyState és a Get-AzPolicyStateSummary frissült a 2019-10-01 API-verzióhoz</span><span class="sxs-lookup"><span data-stu-id="773db-926">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="773db-927">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="773db-927">Az.RecoveryServices</span></span>
* <span data-ttu-id="773db-928">Azure Site Recovery-támogatás a replikált lemezek eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="773db-928">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="773db-929">Hozzáadott Azure Backup-támogatás a helyreállítási tárak létrehozása közbeni címkehozzáadáshoz.</span><span class="sxs-lookup"><span data-stu-id="773db-929">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="773db-930">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-930">Az.Resources</span></span>
* <span data-ttu-id="773db-931">A -Scope választható a \*-AzPolicyAssignment parancsmagokban; az alapértelmezett érték a környezeti előfizetés</span><span class="sxs-lookup"><span data-stu-id="773db-931">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="773db-932">Az ADServicePrincipal jelszó és kulcs típusú hitelesítő adatokkal való létrehozását szemléltető példák hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-932">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="773db-933">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-933">Az.Sql</span></span>
<span data-ttu-id="773db-934">A New-AzSqlDatabaseSecondary parancsmag javítva, hogy a PartnerDatabaseName létezését ellenőrizze a DatabaseName létezése helyett.</span><span class="sxs-lookup"><span data-stu-id="773db-934">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="773db-935">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="773db-935">Az.Storage</span></span>
* <span data-ttu-id="773db-936">A Table/Queue Encryption Keytype készlet beállításának támogatása Storage-fiók létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="773db-936">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="773db-937">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="773db-937">New-AzStorageAccount</span></span>
* <span data-ttu-id="773db-938">RequestId megjelenítése, ha a StorageException nem rendelkezik ExtendedErrorInformation paraméterrel</span><span class="sxs-lookup"><span data-stu-id="773db-938">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="773db-939">A Start-AzStorageBlobCopy parancsmag 6. példájának kijavítása</span><span class="sxs-lookup"><span data-stu-id="773db-939">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="773db-940">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="773db-940">Az.Websites</span></span>
* <span data-ttu-id="773db-941">A Set-AzWebapp és a Set-AzWebappSlot támogatja az AlwaysOn, a MinTls és a FtpsState tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="773db-941">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="773db-942">Javítva a hiba, amely miatt a HttpsOnly és az AppservicePlan Set-AzWebApp paranccsal történő egyidejű módosításakor a HttpsOnly paraméter alaphelyzetbe állt.</span><span class="sxs-lookup"><span data-stu-id="773db-942">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="773db-943">3.3.0 – 2020. január</span><span class="sxs-lookup"><span data-stu-id="773db-943">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="773db-944">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="773db-944">Az.Accounts</span></span>
* <span data-ttu-id="773db-945">Frissítve lettek az Add-AzEnvironment és Set-AzEnvironment parancsmagok, amelyek mostantól elfogadják az AzureAttestationServiceEndpointResourceId és AzureAttestationServiceEndpointSuffix paramétereket</span><span class="sxs-lookup"><span data-stu-id="773db-945">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="773db-946">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="773db-946">Az.Cdn</span></span>
* <span data-ttu-id="773db-947">A hibaválasz részleteinek láthatóvá tétele a New-AzCdnEndpoint parancsmagban</span><span class="sxs-lookup"><span data-stu-id="773db-947">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="773db-948">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-948">Az.Compute</span></span>
* <span data-ttu-id="773db-949">Javítva lett a Set-AzVMCustomScriptExtension parancsmag az olyan virtuális gépek esetében, amelyek felügyelt operációsrendszer-lemeze nem rendelkezik operációsrendszer-profillal.</span><span class="sxs-lookup"><span data-stu-id="773db-949">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="773db-950">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="773db-950">Az.ContainerInstance</span></span>
* <span data-ttu-id="773db-951">Javítva lettek a New-AzContainerGroup parancsmagpélda által használt paraméternevek</span><span class="sxs-lookup"><span data-stu-id="773db-951">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="773db-952">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="773db-952">Az.DataBoxEdge</span></span>
* <span data-ttu-id="773db-953">Hozzá lett adva a Get-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="773db-953">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="773db-954">Az Edge Storage-tároló lekérése</span><span class="sxs-lookup"><span data-stu-id="773db-954">Get the Edge Storage Container</span></span>
* <span data-ttu-id="773db-955">Hozzá lett adva a New-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="773db-955">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="773db-956">Új Edge Storage-tároló létrehozása</span><span class="sxs-lookup"><span data-stu-id="773db-956">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="773db-957">Hozzá lett adva a Remove-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="773db-957">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="773db-958">Az Edge Storage-tároló eltávolítása</span><span class="sxs-lookup"><span data-stu-id="773db-958">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="773db-959">Hozzá lett adva az Invoke-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="773db-959">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="773db-960">Meghívási művelet az Edge Storage-tárolóban lévő adatok frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="773db-960">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="773db-961">Hozzá lett adva a Get-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="773db-961">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="773db-962">Az Edge Storage-fiók lekérése</span><span class="sxs-lookup"><span data-stu-id="773db-962">Get the Edge Storage Account</span></span>
* <span data-ttu-id="773db-963">Hozzá lett adva a New-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="773db-963">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="773db-964">Új Edge Storage-fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="773db-964">Create new Edge Storage Account</span></span>
* <span data-ttu-id="773db-965">Hozzá lett adva a Remove-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="773db-965">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="773db-966">Az Edge Storage-fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="773db-966">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="773db-967">Hozzá lett adva az Invoke-AzDataBoxEdgeShare parancsmag</span><span class="sxs-lookup"><span data-stu-id="773db-967">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="773db-968">Meghívási művelet a megosztott adatok frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="773db-968">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="773db-969">Hozzá lett adva a Set-AzDataBoxEdgeStorageAccountCredential parancsmag</span><span class="sxs-lookup"><span data-stu-id="773db-969">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="773db-970">Az Az.DataBoxEdge tárfiók hitelesítő adatainak beállítása</span><span class="sxs-lookup"><span data-stu-id="773db-970">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="773db-971">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="773db-971">Az.DataFactory</span></span>
* <span data-ttu-id="773db-972">Hozzá lettek adva az AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId és VersionStatus tulajdonságok a Get-AzDataFactoryV2IntegrationRuntime parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="773db-972">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="773db-973">Az ADF .Net SDK frissítve lett a 4.6.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="773db-973">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="773db-974">A PublicIPs paraméter hozzá lett adva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz statikus nyilvános IP-címekkel rendelkező Azure-SSIS IR létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="773db-974">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="773db-975">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="773db-975">Az.DevTestLabs</span></span>
* <span data-ttu-id="773db-976">A hibás hivatkozás el lett távolítva a Get-AzDtlAllowedVMSizesPolicy.md parancsmagból</span><span class="sxs-lookup"><span data-stu-id="773db-976">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="773db-977">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="773db-977">Az.EventHub</span></span>
* <span data-ttu-id="773db-978">A 10634-es hiba javítása: Ki lett javítva a nullértékű objektumhivatkozás a remove eventhubnamespace esetében</span><span class="sxs-lookup"><span data-stu-id="773db-978">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="773db-979">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="773db-979">Az.HDInsight</span></span>
* <span data-ttu-id="773db-980">Ki lett javítva az Invoke-AzHDInsightHiveJob.md hibája.</span><span class="sxs-lookup"><span data-stu-id="773db-980">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="773db-981">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="773db-981">Az.MachineLearning</span></span>
* <span data-ttu-id="773db-982">El lettek távolítva az alábbi parancsmagok, mivel a MachineLearningCompute már nem érhető el</span><span class="sxs-lookup"><span data-stu-id="773db-982">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="773db-983">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="773db-983">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="773db-984">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="773db-984">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="773db-985">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="773db-985">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="773db-986">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="773db-986">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="773db-987">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="773db-987">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="773db-988">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="773db-988">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="773db-989">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="773db-989">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="773db-990">Az.Network</span><span class="sxs-lookup"><span data-stu-id="773db-990">Az.Network</span></span>
* <span data-ttu-id="773db-991">Frissítve lett a Microsoft.Azure.Management.Sql függősége: 1.36-preview helyett 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="773db-991">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="773db-992">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="773db-992">Az.RecoveryServices</span></span>
* <span data-ttu-id="773db-993">Módosított Azure Site Recovery-támogatás azon felügyelt lemezeken található, inaktív állapotban titkosított virtuális gépeknél, amelyekhez felhasználó által kezelt kulcsok tartoznak a következő esetében: Azure – Azure-szolgáltató.</span><span class="sxs-lookup"><span data-stu-id="773db-993">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="773db-994">Azure Site Recovery-támogatás a lemeztitkosítási csoportazonosító megadásának opcionálissá tételéhez a védelem engedélyezése során a következő esetében: VMware – Azure.</span><span class="sxs-lookup"><span data-stu-id="773db-994">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="773db-995">Azure Site Recovery-támogatás a lemeztitkosítási csoportazonosító megadásának opcionálissá tételéhez a lemez szintjén a védelem engedélyezéséhez a következő esetében: VMware – Azure.</span><span class="sxs-lookup"><span data-stu-id="773db-995">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="773db-996">Azure Site Recovery-támogatás a Replikációval védett, lemeztitkosítási csoportleképezéssel ellátott elemek frissítéséhez a következő esetében: HyperV – Azure.</span><span class="sxs-lookup"><span data-stu-id="773db-996">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="773db-997">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-997">Az.Resources</span></span>
* <span data-ttu-id="773db-998">Javítva lett egy hiba a Remove-AzTag súgódokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="773db-998">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="773db-999">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-999">Az.Sql</span></span>
* <span data-ttu-id="773db-1000">Javítva lett a sebezhetőségi felmérés csoportszintű alapkonfigurációs parancsmagjainak működése: az Azure-adatbázis főadatbázisában használható, a felügyelt példányok rendszeradatbázisaiban korlátozott.</span><span class="sxs-lookup"><span data-stu-id="773db-1000">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="773db-1001">Ki lett javítva egy hiba az SQL-példányok feladatátvételi csoportjainak létrehozása esetében</span><span class="sxs-lookup"><span data-stu-id="773db-1001">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="773db-1002">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="773db-1002">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="773db-1003">Hozzá lett adva a DR, mint új érvényes licenctípus</span><span class="sxs-lookup"><span data-stu-id="773db-1003">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="773db-1004">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="773db-1004">Az.Storage</span></span>
* <span data-ttu-id="773db-1005">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó figyelmeztető üzenet a DefaultAction értékének módosítására vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="773db-1005">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="773db-1006">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="773db-1006">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="773db-1007">Támogatott a tárfiók legutóbbi szinkronizálási időpontjának lekérése a get-AzureRMStorageAccount parancsmag -IncludeGeoReplicationStats paraméterrel való futtatásával</span><span class="sxs-lookup"><span data-stu-id="773db-1007">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="773db-1008">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="773db-1008">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="773db-1009">3.2.0 – 2019. december</span><span class="sxs-lookup"><span data-stu-id="773db-1009">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="773db-1010">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="773db-1010">General</span></span>
* <span data-ttu-id="773db-1011">A .psd1 hivatkozásai frissítve, hogy minden modulhoz a relatív elérési utat használják</span><span class="sxs-lookup"><span data-stu-id="773db-1011">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="773db-1012">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="773db-1012">Az.Accounts</span></span>
* <span data-ttu-id="773db-1013">A megfelelő felhasználói ügynök beállítva az ügyféloldali telemetriához az Az 4.0 előzetes verziójában</span><span class="sxs-lookup"><span data-stu-id="773db-1013">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="773db-1014">Felhasználóbarát hibaüzenet megjelenítése, ha az Az 4.0 előzetes verziójában a környezet null értékű</span><span class="sxs-lookup"><span data-stu-id="773db-1014">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="773db-1015">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="773db-1015">Az.Batch</span></span>
* <span data-ttu-id="773db-1016">Ki lett javítva a [10602-es](https://github.com/Azure/azure-powershell/issues/10602) számú hiba, amely miatt a **New-AzBatchPool** nem megfelelően küldte el a „VirtualMachineConfiguration.ContainerConfiguration” és a „VirtualMachineConfiguration.DataDisks” paramétereket a kiszolgálónak.</span><span class="sxs-lookup"><span data-stu-id="773db-1016">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="773db-1017">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="773db-1017">Az.DataFactory</span></span>
* <span data-ttu-id="773db-1018">Az ADF .Net SDK a 4.5.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="773db-1018">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="773db-1019">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="773db-1019">Az.FrontDoor</span></span>
* <span data-ttu-id="773db-1020">A WAF felügyeleti szabályok kizárása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="773db-1020">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="773db-1021">Hozzá lett adva a SocketAddr automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="773db-1021">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="773db-1022">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="773db-1022">Az.HealthcareApis</span></span>
* <span data-ttu-id="773db-1023">Kivételkezelés</span><span class="sxs-lookup"><span data-stu-id="773db-1023">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="773db-1024">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="773db-1024">Az.KeyVault</span></span>
* <span data-ttu-id="773db-1025">Ki lett javítva az esetleg nem beállított értékek hozzáférésével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="773db-1025">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="773db-1026">Az elliptikus görbéjű titkosítási tanúsítványok kezelése</span><span class="sxs-lookup"><span data-stu-id="773db-1026">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="773db-1027">A görbe tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="773db-1027">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="773db-1028">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="773db-1028">Az.Monitor</span></span>
* <span data-ttu-id="773db-1029">Opcionális argumentum hozzáadva a Diagnosztikai beállítások hozzáadása parancshoz.</span><span class="sxs-lookup"><span data-stu-id="773db-1029">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="773db-1030">Ez egy kapcsoló argumentum, amely megléte esetén azt jelzi, hogy a Log Analyticsbe történő exportálást egy rögzített séma (más néven</span><span class="sxs-lookup"><span data-stu-id="773db-1030">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="773db-1031">dedikált adattípus) szerint kell végrehajtani</span><span class="sxs-lookup"><span data-stu-id="773db-1031">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="773db-1032">Az.Network</span><span class="sxs-lookup"><span data-stu-id="773db-1032">Az.Network</span></span>
* <span data-ttu-id="773db-1033">Támogatás az Ip-csoportok számára az AzureFirewall alkalmazás, valamint a Nat- és a hálózati szabályok esetében.</span><span class="sxs-lookup"><span data-stu-id="773db-1033">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="773db-1034">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-1034">Az.Resources</span></span>
* <span data-ttu-id="773db-1035">Ki lett javítva az a hiba, amely miatt a sablonalapú üzembe helyezés során a sablonparamétert nem lehet olvasni, ha a sablonparaméter és egy beépített paraméter neve között névütközés áll fenn.</span><span class="sxs-lookup"><span data-stu-id="773db-1035">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="773db-1036">Frissültek a szabályzat parancsmagjai a 2019. 09. 01. dátumú új API-verzió használatára, amely bevezeti a szabályzatkészlet-definíciókon belüli csoportos támogatást.</span><span class="sxs-lookup"><span data-stu-id="773db-1036">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="773db-1037">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-1037">Az.Sql</span></span>
* <span data-ttu-id="773db-1038">Frissítve lett a sebezhetőségi felmérés automatikus engedélyezéséhez szükséges tárterület létrehozása a Storagev2-ben</span><span class="sxs-lookup"><span data-stu-id="773db-1038">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="773db-1039">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="773db-1039">Az.Storage</span></span>
* <span data-ttu-id="773db-1040">A blob-/tárolóidentitás-alapú SAS-token Oauth-hitelesítésen alapuló Storage-környezettel való létrehozásának támogatása</span><span class="sxs-lookup"><span data-stu-id="773db-1040">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="773db-1041">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="773db-1041">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="773db-1042">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="773db-1042">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="773db-1043">Támogatott lett a tárfiókhoz tartozó felhasználódelegálási kulcsok visszavonása, így minden identitásalapú SAS-token visszavonható</span><span class="sxs-lookup"><span data-stu-id="773db-1043">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="773db-1044">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="773db-1044">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="773db-1045">Frissítés a Microsoft.Azure.Management.Storage 14.2.0-s verziójára az új API-verzió (2019. 06. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="773db-1045">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="773db-1046">A QuotaGiB (gigabájtban megadott megosztási kvóta) esetében támogatottak az 5120-nál nagyobb értékek a fájlmegosztási parancsmagok felügyeleti síkján, és hozzá lett adva a Quota paraméteralias a QuotaGiB paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="773db-1046">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="773db-1047">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="773db-1047">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="773db-1048">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="773db-1048">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="773db-1049">A „QuotaGiB” paraméteralias hozzáadva a „kvóta” paraméterhez</span><span class="sxs-lookup"><span data-stu-id="773db-1049">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="773db-1050">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="773db-1050">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="773db-1051">Ki lett javítva az a hiba, amely miatt a Set-AzStorageContainerAcl parancsmag el tudta távolítani a tárolt hozzáférési szabályzatot</span><span class="sxs-lookup"><span data-stu-id="773db-1051">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="773db-1052">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="773db-1052">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="773db-1053">3.1.0 – 2019. november</span><span class="sxs-lookup"><span data-stu-id="773db-1053">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="773db-1054">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="773db-1054">Highlights since the last major release</span></span>
* <span data-ttu-id="773db-1055">Az.DataBoxEdge 1.0.0 kiadva</span><span class="sxs-lookup"><span data-stu-id="773db-1055">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="773db-1056">Az.SqlVirtualMachine 1.0.0 kiadva</span><span class="sxs-lookup"><span data-stu-id="773db-1056">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="773db-1057">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-1057">Az.Compute</span></span>
* <span data-ttu-id="773db-1058">A virtuális gépek Reapply funkciója</span><span class="sxs-lookup"><span data-stu-id="773db-1058">VM Reapply feature</span></span>
    - <span data-ttu-id="773db-1059">A Reapply paraméter hozzá lett adva a Set-AzVM parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="773db-1059">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="773db-1060">A virtuálisgép-méretezési csoportok AutomaticRepairs funkciója:</span><span class="sxs-lookup"><span data-stu-id="773db-1060">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="773db-1061">Az EnableAutomaticRepair, az AutomaticRepairGracePeriod és az AutomaticRepairMaxInstanceRepairsPercent paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="773db-1061">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="773db-1062">Több-bérlős katalógus-rendszerkép támogatása a New-AzVM parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="773db-1062">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="773db-1063">A Spot hozzá lett adva a New-AzVM, a New-AzVMConfig és a New-AzVmss parancsmag Priority paraméterének argumentumbefejezőjéhez</span><span class="sxs-lookup"><span data-stu-id="773db-1063">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="773db-1064">A DiskIOPSReadWrite és a DiskMBpsReadWrite paraméter hozzá lett adva az Add-AzVmssDataDisk parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="773db-1064">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="773db-1065">A New-AzGalleryImageVersion parancsmag SourceImageId paramétere mostantól nem kötelező</span><span class="sxs-lookup"><span data-stu-id="773db-1065">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="773db-1066">A New-AzGalleryImageVersion parancsmag az OSDiskImage és a DataDiskImage paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="773db-1066">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="773db-1067">A HyperVGeneration paraméter mostantól elérhető a New-AzGalleryImageDefinition parancsmagban</span><span class="sxs-lookup"><span data-stu-id="773db-1067">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="773db-1068">A SkipExtensionsOnOverprovisionedVMs paraméter hozzá lett adva a New-AzVmss, a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="773db-1068">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="773db-1069">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="773db-1069">Az.DataBoxEdge</span></span>
* <span data-ttu-id="773db-1070">A(z) `Get-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="773db-1070">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="773db-1071">Megrendelés lekérése</span><span class="sxs-lookup"><span data-stu-id="773db-1071">Get the Order</span></span>
* <span data-ttu-id="773db-1072">A(z) `New-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="773db-1072">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="773db-1073">Új megrendelés létrehozása</span><span class="sxs-lookup"><span data-stu-id="773db-1073">Create new Order</span></span>
* <span data-ttu-id="773db-1074">A(z) `Remove-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="773db-1074">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="773db-1075">Megrendelés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="773db-1075">Remove the Order</span></span>
* <span data-ttu-id="773db-1076">`New-AzDataBoxEdgeShare` parancsmag módosítása</span><span class="sxs-lookup"><span data-stu-id="773db-1076">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="773db-1077">Mostantól helyi megosztást hoz létre</span><span class="sxs-lookup"><span data-stu-id="773db-1077">Now creates Local Share</span></span>
* <span data-ttu-id="773db-1078">A(z) `Set-AzDataBoxEdgeRole` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="773db-1078">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="773db-1079">Mostantól az IotRole leképezhető a Share-re</span><span class="sxs-lookup"><span data-stu-id="773db-1079">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="773db-1080">A(z) `Invoke-AzDataBoxEdgeDevice` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="773db-1080">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="773db-1081">Frissítések keresésének, letöltésének, telepítésének indítása az eszközön</span><span class="sxs-lookup"><span data-stu-id="773db-1081">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="773db-1082">A(z) `Get-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="773db-1082">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="773db-1083">Triggerek információinak lekérdezése</span><span class="sxs-lookup"><span data-stu-id="773db-1083">Gets the information about Triggers</span></span>
* <span data-ttu-id="773db-1084">A(z) `New-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="773db-1084">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="773db-1085">Új triggerek létrehozása</span><span class="sxs-lookup"><span data-stu-id="773db-1085">Create new Triggers</span></span>
* <span data-ttu-id="773db-1086">A(z) `Remove-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="773db-1086">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="773db-1087">Triggerek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="773db-1087">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="773db-1088">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="773db-1088">Az.DataFactory</span></span>
* <span data-ttu-id="773db-1089">Az ADF .Net SDK a 4.4.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="773db-1089">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="773db-1090">Az ExpressCustomSetup paraméter hozzá lett adva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz a beállítási konfigurációk és külső összetevők egyéni beállítási szkript nélkül történő engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="773db-1090">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="773db-1091">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="773db-1091">Az.DataLakeStore</span></span>
* <span data-ttu-id="773db-1092">Frissült a Get-AzDataLakeStoreDeletedItem és a Restore-AzDataLakeStoreDeletedItem dokumentációja</span><span class="sxs-lookup"><span data-stu-id="773db-1092">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="773db-1093">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="773db-1093">Az.EventHub</span></span>
* <span data-ttu-id="773db-1094">A 10301-es hiba javítása: Az SAS-token dátumformátumának javítása</span><span class="sxs-lookup"><span data-stu-id="773db-1094">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="773db-1095">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="773db-1095">Az.FrontDoor</span></span>
* <span data-ttu-id="773db-1096">Az Enable-AzFrontDoorCustomDomainHttps és a New-AzFrontDoorFrontendEndpointObject a MinimumTlsVersion paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="773db-1096">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="773db-1097">A New-AzFrontDoorHealthProbeSettingObject a HealthProbeMethod és az EnabledState paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="773db-1097">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="773db-1098">Új parancsmag érhető el a Front Door létrehozásakor/frissítésekor megadandó BackendPoolsSettings objektum létrehozásához</span><span class="sxs-lookup"><span data-stu-id="773db-1098">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="773db-1099">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="773db-1099">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="773db-1100">Az.Network</span><span class="sxs-lookup"><span data-stu-id="773db-1100">Az.Network</span></span>
* <span data-ttu-id="773db-1101">A Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és a Start-AzVirtualnetworkGatewayPacketCapture.md FilterData kapcsolójának példái módosultak.</span><span class="sxs-lookup"><span data-stu-id="773db-1101">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="773db-1102">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="773db-1102">Az.PrivateDns</span></span>
* <span data-ttu-id="773db-1103">A PrivateDns .net sdk frissült az 1.0.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="773db-1103">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="773db-1104">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="773db-1104">Az.RecoveryServices</span></span>
* <span data-ttu-id="773db-1105">Mostantól Azure Site Recovery-támogatás érhető el a lemeztípus kiválasztásához a védelem engedélyezésekor.</span><span class="sxs-lookup"><span data-stu-id="773db-1105">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="773db-1106">Azure Site Recovery-hibajavítás a visszaállítási terv műveletének szerkesztéséhez.</span><span class="sxs-lookup"><span data-stu-id="773db-1106">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="773db-1107">SQL-visszaállítási támogatás az Azure Backuphoz a fájlstream-adatbázisok elfogadása érdekében.</span><span class="sxs-lookup"><span data-stu-id="773db-1107">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="773db-1108">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="773db-1108">Az.RedisCache</span></span>
* <span data-ttu-id="773db-1109">A MinimumTlsVersion paraméter hozzá lett adva a New-AzRedisCache és a Set-AzRedisCache parancsmagban.</span><span class="sxs-lookup"><span data-stu-id="773db-1109">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="773db-1110">Emellett a MinimumTlsVersion hozzá lett adva a Get-AzRedisCache parancsmag kimenetéhez.</span><span class="sxs-lookup"><span data-stu-id="773db-1110">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="773db-1111">Mostantól elérhető a -Size paraméter érvényesítése a Set-AzRedisCache és a New-AzRedisCache parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="773db-1111">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="773db-1112">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-1112">Az.Resources</span></span>
- <span data-ttu-id="773db-1113">Frissültek a szabályzat parancsmagjai a 2019. 06. 01. dátumú új API-verzió használatára, amely tartalmazza az új EnforcementMode tulajdonságot a szabályzat-hozzárendelésekben.</span><span class="sxs-lookup"><span data-stu-id="773db-1113">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="773db-1114">Frissült a létrehozási szabályzat definíciójának súgóbeli példája</span><span class="sxs-lookup"><span data-stu-id="773db-1114">Updated create policy definition help example</span></span>
- <span data-ttu-id="773db-1115">Kijavítottuk azt a hibát, amikor a Remove-AZADServicePrincipal -ServicePrincipalName null értékű hivatkozást ad vissza, ha az egyszerű szolgáltatásnév nem található.</span><span class="sxs-lookup"><span data-stu-id="773db-1115">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="773db-1116">Kijavítottuk azt a hibát, amikor a New-AZADServicePrincipal null értékű hivatkozást ad vissza, ha a bérlőnek nincs előfizetése.</span><span class="sxs-lookup"><span data-stu-id="773db-1116">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="773db-1117">A New-AzAdServicePrincipal módosult, és már csak a társított alkalmazáshoz ad hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="773db-1117">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="773db-1118">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-1118">Az.Sql</span></span>
* <span data-ttu-id="773db-1119">Az adatbázisbeli ReadReplicaCount mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="773db-1119">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="773db-1120">A Set-AzSqlDatabase ki lett javítva nem beállított zónaredundancia esetén</span><span class="sxs-lookup"><span data-stu-id="773db-1120">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="773db-1121">3.0.0 – 2019. november</span><span class="sxs-lookup"><span data-stu-id="773db-1121">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="773db-1122">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="773db-1122">General</span></span>
* <span data-ttu-id="773db-1123">Megjelent az Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="773db-1123">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="773db-1124">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="773db-1124">Az.Accounts</span></span>
* <span data-ttu-id="773db-1125">A Resolve-Error aliast érintő elavulási üzenet hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="773db-1125">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="773db-1126">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="773db-1126">Az.Advisor</span></span>
* <span data-ttu-id="773db-1127">Új Működésbeli kiválóság kategória hozzáadva a Get-AzAdvisorRecommendation parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="773db-1127">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="773db-1128">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="773db-1128">Az.Batch</span></span>
* <span data-ttu-id="773db-1129">A `CoreQuota` átnevezve `BatchAccountContext` értékre a következőn: `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="773db-1129">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="773db-1130">Emellett egy új `LowPriorityCoreQuota` elem is található.</span><span class="sxs-lookup"><span data-stu-id="773db-1130">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="773db-1131">Ez hatással van a következőre: **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="773db-1131">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="773db-1132">A **New-AzBatchTask** `-ResourceFile` paraméter most már `PSResourceFile` objektumok gyűjteményét használja, amely az új **New-AzBatchResourceFile** parancsmaggal hozható létre.</span><span class="sxs-lookup"><span data-stu-id="773db-1132">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="773db-1133">Új **New-AzBatchResourceFile** parancsfájl a szükséges `PSResourceFile` objektumok létrehozásának elősegítéséhez.</span><span class="sxs-lookup"><span data-stu-id="773db-1133">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="773db-1134">Ezek az **New-AzBatchTask**`-ResourceFile` paraméterénél adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="773db-1134">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="773db-1135">Ez két új típusú erőforrásfájlt támogat a meglévő `HttpUrl` mód mellett:</span><span class="sxs-lookup"><span data-stu-id="773db-1135">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="773db-1136">Az `AutoStorageContainerName`-alapú erőforrásfájlok egy teljes automatikus tárolót töltenek le a Batch-csomópontra.</span><span class="sxs-lookup"><span data-stu-id="773db-1136">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="773db-1137">A `StorageContainerUrl`-alapú erőforrásfájlok az URL-címben megadott tárolót töltik le a Batch-csomópontra.</span><span class="sxs-lookup"><span data-stu-id="773db-1137">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="773db-1138">A `PSApplication`**Get-AzBatchApplication** által visszaadott `ApplicationPackages` tulajdonsága eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="773db-1138">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="773db-1139">Most már lekérhetők az alkalmazásokon belüli adott csomagok a **Get-AzBatchApplicationPackage** használatával.</span><span class="sxs-lookup"><span data-stu-id="773db-1139">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="773db-1140">Például: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="773db-1140">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="773db-1141">Az `ApplicationId` átnevezve `ApplicationName` értékre a **Get-AzBatchApplicationPackage**, a **New-AzBatchApplicationPackage**, a **Remove-AzBatchApplicationPackage**, a **Get-AzBatchApplication**, a **New-AzBatchApplication**, a **Remove-AzBatchApplication** és a **Set-AzBatchApplication** esetében.</span><span class="sxs-lookup"><span data-stu-id="773db-1141">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="773db-1142">Az `ApplicationId` mostantól az `ApplicationName` aliasa.</span><span class="sxs-lookup"><span data-stu-id="773db-1142">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="773db-1143">Az új `PSWindowsUserConfiguration` tulajdonság hozzáadva a következőhöz: `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="773db-1143">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="773db-1144">A `Version` átnevezve `Name` értékre a `PSApplicationPackage` esetében.</span><span class="sxs-lookup"><span data-stu-id="773db-1144">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="773db-1145">A `BlobSource` átnevezve `HttpUrl` értékre a `PSResourceFile` esetében.</span><span class="sxs-lookup"><span data-stu-id="773db-1145">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="773db-1146">Az `OSDisk` tulajdonság eltávolítva a következőből: `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="773db-1146">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="773db-1147">A **Set-AzBatchPoolOSVersion** eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="773db-1147">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="773db-1148">Ez a művelet már nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="773db-1148">This operation is no longer supported.</span></span>
* <span data-ttu-id="773db-1149">`PSCloudServiceConfiguration``TargetOSVersion` eleme eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="773db-1149">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="773db-1150">A `CurrentOSVersion` átnevezve `OSVersion` értékre a `PSCloudServiceConfiguration` esetében.</span><span class="sxs-lookup"><span data-stu-id="773db-1150">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="773db-1151">`DataEgressGiB` és `DataIngressGiB` eltávolítva a következőből: `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="773db-1151">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="773db-1152">A **Get-AzBatchNodeAgentSku** eltávolítva és a **Get-AzBatchSupportedImage** parancsmaggal helyettesítve.</span><span class="sxs-lookup"><span data-stu-id="773db-1152">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="773db-1153">A **Get-AzBatchSupportedImage** ugyanazokat az adatokat jeleníti meg, mint a **Get-AzBatchNodeAgentSku**, csak egyszerűbb formátumban.</span><span class="sxs-lookup"><span data-stu-id="773db-1153">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="773db-1154">Most már új, nem ellenőrzött rendszerképeket is visszaad a rendszer.</span><span class="sxs-lookup"><span data-stu-id="773db-1154">New non-verified images are also now returned.</span></span> <span data-ttu-id="773db-1155">Minden rendszerképről további, `Capabilities` és `BatchSupportEndOfLife` típusú információk is szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="773db-1155">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="773db-1156">Lehetőség arra, hogy távoli fájlrendszereket lehessen csatlakoztatni egy készlet minden csomópontjára a **New-AzBatchPool** új `MountConfiguration` paraméterével.</span><span class="sxs-lookup"><span data-stu-id="773db-1156">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="773db-1157">Most már támogatja a hálózati biztonsági szabályokat, amelyek a letiltják a készletekhez való hozzáférést a forgalom forrásportja alapján.</span><span class="sxs-lookup"><span data-stu-id="773db-1157">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="773db-1158">Ez a `PSNetworkSecurityGroupRule``SourcePortRanges` tulajdonsága alapján történik.</span><span class="sxs-lookup"><span data-stu-id="773db-1158">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="773db-1159">Tároló futtatásakor a Batch támogatja a feladat végrehajtását a tároló munkakönyvtárában vagy a Batch-feladat munkakönyvtárában.</span><span class="sxs-lookup"><span data-stu-id="773db-1159">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="773db-1160">Ezt a `PSTaskContainerSettings``WorkingDirectory` tulajdonsága szabályozza.</span><span class="sxs-lookup"><span data-stu-id="773db-1160">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="773db-1161">Új lehetőség nyilvános IP-gyűjtemény megadására az érintett `PSNetworkConfiguration` elemen az új `PublicIPs` tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="773db-1161">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="773db-1162">Ez garantálja, hogy a készletben található csomópontok rendelkeznek majd IP-címmel a felhasználó által megadott IP-listáról.</span><span class="sxs-lookup"><span data-stu-id="773db-1162">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="773db-1163">Ha nincs megadva, a `PSSTartTask` alapértelmezett `WaitForSuccess` értéke `$True` (korábban `$False` volt).</span><span class="sxs-lookup"><span data-stu-id="773db-1163">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="773db-1164">Ha nincs megadva, a `PSAutoUserSpecification` alapértelmezett `Scope` értéke `Pool` (korábban Windowson `Task`, Linuxon pedig `Pool` volt).</span><span class="sxs-lookup"><span data-stu-id="773db-1164">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="773db-1165">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="773db-1165">Az.Cdn</span></span>
* <span data-ttu-id="773db-1166">A RulesEngine tartalmazza az új UrlRewriteAction és a CacheKeyQueryStringAction műveleteket.</span><span class="sxs-lookup"><span data-stu-id="773db-1166">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="773db-1167">Javítva számos olyan hiba, mint a New-AzDeliveryRuleCondition parancsmag hiányzó Selector bemenete.</span><span class="sxs-lookup"><span data-stu-id="773db-1167">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="773db-1168">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-1168">Az.Compute</span></span>
* <span data-ttu-id="773db-1169">Lemeztitkosítási készlet funkció</span><span class="sxs-lookup"><span data-stu-id="773db-1169">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="773db-1170">Új parancsmagok:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="773db-1170">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="773db-1171">A DiskEncryptionSetId paraméter hozzá lett adva a következő parancsmagokhoz:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="773db-1171">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="773db-1172">A DiskEncryptionSetId és az EncryptionType paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="773db-1172">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="773db-1173">A PublicIPAddressVersion paraméter hozzá lett adva a New-AzVmssIPConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="773db-1173">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="773db-1174">Egyéni szkriptbővítmény FileUris tulajdonságának módosítása nyilvánosról védett beállításra</span><span class="sxs-lookup"><span data-stu-id="773db-1174">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="773db-1175">ScaleInPolicy hozzáadva a New-AzVmss, New-AzVmssConfig és Update-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="773db-1175">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="773db-1176">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="773db-1176">Breaking changes</span></span>
    - <span data-ttu-id="773db-1177">A New-AzDiskConfig esetében a DiskSizeGB helyett az UploadSizeInBytes paramétert kell használni, ha a CreateOption értéke Upload</span><span class="sxs-lookup"><span data-stu-id="773db-1177">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="773db-1178">A PublishingProfile.Source.ManagedImage.Id elemet a StorageProfile.Source.Id helyettesíti a GalleryImageVersion objektumban</span><span class="sxs-lookup"><span data-stu-id="773db-1178">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="773db-1179">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="773db-1179">Az.DataFactory</span></span>
* <span data-ttu-id="773db-1180">Az ADF .Net SDK a 4.3.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="773db-1180">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="773db-1181">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="773db-1181">Az.DataLakeStore</span></span>
* <span data-ttu-id="773db-1182">Az ADLS SDK-verziójának frissítése (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) , a következő javításokkal</span><span class="sxs-lookup"><span data-stu-id="773db-1182">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="773db-1183">Kivétel jelzésének elkerülése, amikor a lomtár vagy a könyvtár bejegyzésének CreationTime tulajdonsága nem deszerializálható.</span><span class="sxs-lookup"><span data-stu-id="773db-1183">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="773db-1184">Beállítás megjelenítése minden kérelem-időtúllépés esetén az adlsclient objektumban</span><span class="sxs-lookup"><span data-stu-id="773db-1184">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="773db-1185">Az eredeti syncflag átadásának javítása a badoffset helyreállításához</span><span class="sxs-lookup"><span data-stu-id="773db-1185">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="773db-1186">Az EnumerateDirectory javítása a folytatási token válaszellenőrzés utáni lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="773db-1186">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="773db-1187">Concat-hiba javítása</span><span class="sxs-lookup"><span data-stu-id="773db-1187">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="773db-1188">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="773db-1188">Az.FrontDoor</span></span>
* <span data-ttu-id="773db-1189">Különféle elgépelések kijavítva a modulban</span><span class="sxs-lookup"><span data-stu-id="773db-1189">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="773db-1190">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="773db-1190">Az.HDInsight</span></span>
* <span data-ttu-id="773db-1191">Kijavítva az a hiba, amely miatt az ügyfél a Nem érvényes Base-64-sztring hibát kapta, amikor a Get-AzHDInsightCluster használatával próbálta lekérni a fürtöt az ADLSGen1 tároló esetében.</span><span class="sxs-lookup"><span data-stu-id="773db-1191">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="773db-1192">Új, ApplicationId nevű paraméter hozzáadva az Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig és New-AzHDInsightCluster nevű három parancsmaghoz, hogy az ügyfél megadhassa a szolgáltatásnév alkalmazásazonosítóját az Azure Data Lake eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="773db-1192">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="773db-1193">A Microsoft.Azure.Management.HDInsight 2.1.0 módosítva a következőre: 5.1.0</span><span class="sxs-lookup"><span data-stu-id="773db-1193">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="773db-1194">Öt parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="773db-1194">Removed five cmdlets:</span></span>
    - <span data-ttu-id="773db-1195">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="773db-1195">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="773db-1196">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="773db-1196">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="773db-1197">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="773db-1197">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="773db-1198">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="773db-1198">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="773db-1199">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="773db-1199">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="773db-1200">Három parancsmag hozzáadva:</span><span class="sxs-lookup"><span data-stu-id="773db-1200">Added three cmdlets:</span></span>
    - <span data-ttu-id="773db-1201">Get-AzHDInsightMonitoring a Get-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="773db-1201">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="773db-1202">Enable-AzHDInsightMonitoring az Enable-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="773db-1202">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="773db-1203">Disable-AzHDInsightMonitoring a Disable-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="773db-1203">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="773db-1204">A Get-AzHDInsightProperties javítva, hogy támogassa a képességinformációk adott helyről történő beszerzését.</span><span class="sxs-lookup"><span data-stu-id="773db-1204">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="773db-1205">Paraméterkészletek (Spark1, Spark2) eltávolítva a következőből: Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="773db-1205">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="773db-1206">Az Add-AzHDInsightSecurityProfile parancsmag súgódokumentumai példákkal bővültek.</span><span class="sxs-lookup"><span data-stu-id="773db-1206">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="773db-1207">A következő parancsmagok kimeneti típusa megváltozott:</span><span class="sxs-lookup"><span data-stu-id="773db-1207">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="773db-1208">A Get-AzHDInsightProperties kimeneti típusa CapabilitiesResponse értékről AzureHDInsightCapabilities értékre változott.</span><span class="sxs-lookup"><span data-stu-id="773db-1208">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="773db-1209">A Remove-AzHDInsightCluster kimeneti típusa ClusterGetResponse értékről logikai értékre változott.</span><span class="sxs-lookup"><span data-stu-id="773db-1209">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="773db-1210">A Set-AzHDInsightGatewaySettings HttpConnectivitySettings kimeneti típusa GatewaySettings értékre változott.</span><span class="sxs-lookup"><span data-stu-id="773db-1210">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="773db-1211">Néhány forgatókönyvi teszteset hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="773db-1211">Added some scenario test cases.</span></span>
* <span data-ttu-id="773db-1212">Néhány alias eltávolítva: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="773db-1212">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="773db-1213">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="773db-1213">Az.IotHub</span></span>
* <span data-ttu-id="773db-1214">Kompatibilitástörő változások:</span><span class="sxs-lookup"><span data-stu-id="773db-1214">Breaking changes:</span></span>
    - <span data-ttu-id="773db-1215">Az Add-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="773db-1215">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="773db-1216">Az Add-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="773db-1216">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="773db-1217">A Get-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="773db-1217">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="773db-1218">A Get-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="773db-1218">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="773db-1219">A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="773db-1219">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="773db-1220">A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="773db-1220">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="773db-1221">A New-AzIotHubExportDevice parancsmag már nem támogatja a New-AzIotHubExportDevices aliast.</span><span class="sxs-lookup"><span data-stu-id="773db-1221">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="773db-1222">A New-AzIotHubImportDevice parancsmag már nem támogatja a New-AzIotHubImportDevices aliast.</span><span class="sxs-lookup"><span data-stu-id="773db-1222">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="773db-1223">A Remove-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="773db-1223">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="773db-1224">A Remove-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="773db-1224">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="773db-1225">A Set-AzIotHub parancsmag a továbbiakban nem támogatja az OperationsMonitoringProperties paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="773db-1225">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="773db-1226">A Set-AzIotHub parancsmaghoz tartozó UpdateOperationsMonitoringProperties paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="773db-1226">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="773db-1227">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="773db-1227">Az.RecoveryServices</span></span>
* <span data-ttu-id="773db-1228">Azure Site Recovery-támogatás az olyan hálózati erőforrások konfigurálásához, mint a hálózati biztonsági csoportok, a nyilvános IP-címek és az Azure–Azure belső terheléselosztók.</span><span class="sxs-lookup"><span data-stu-id="773db-1228">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="773db-1229">Azure Site Recovery-támogatás felügyelt lemezekre történő íráshoz VMware-ről az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="773db-1229">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="773db-1230">Azure Site Recovery-támogatás hálózati adapter csökkentéséhez VMware-ről az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="773db-1230">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="773db-1231">Azure Site Recovery-támogatás a hálózat felgyorsításához Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="773db-1231">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="773db-1232">Azure Site Recovery-támogatás az automatikus frissítési ügynök biztosításához Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="773db-1232">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="773db-1233">Azure Site Recovery-támogatás standard SSD-meghajtóhoz Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="773db-1233">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="773db-1234">Azure Site Recovery-támogatás az Azure Disk Encryption kétlépéses hitelesítéséhez Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="773db-1234">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="773db-1235">Azure Site Recovery-támogatás az újonnan hozzáadott lemez védelméhez Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="773db-1235">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="773db-1236">SoftDelete funkció hozzáadva a virtuális géphez, továbbá a softdelete-hez hozzáadott tesztek</span><span class="sxs-lookup"><span data-stu-id="773db-1236">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="773db-1237">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-1237">Az.Resources</span></span>
* <span data-ttu-id="773db-1238">A Microsoft.Extensions.Caching.Memory függőségi szerelvény frissítése 1.1.1-esről 2.2-es verzióra</span><span class="sxs-lookup"><span data-stu-id="773db-1238">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="773db-1239">Az.Network</span><span class="sxs-lookup"><span data-stu-id="773db-1239">Az.Network</span></span>
* <span data-ttu-id="773db-1240">A PrivateEndpointConnection összes parancsmagjának módosítása az általános szolgáltató támogatásához.</span><span class="sxs-lookup"><span data-stu-id="773db-1240">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="773db-1241">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="773db-1241">Updated cmdlet:</span></span>
        - <span data-ttu-id="773db-1242">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="773db-1242">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="773db-1243">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="773db-1243">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="773db-1244">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="773db-1244">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="773db-1245">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="773db-1245">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="773db-1246">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="773db-1246">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="773db-1247">Új parancsmag hozzáadása a PrivateLinkResource-hoz, valamint az általános szolgáltató támogatása.</span><span class="sxs-lookup"><span data-stu-id="773db-1247">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="773db-1248">Új parancsmag:</span><span class="sxs-lookup"><span data-stu-id="773db-1248">New cmdlet:</span></span>
        - <span data-ttu-id="773db-1249">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="773db-1249">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="773db-1250">Új mezőket és paramétereket ad a Proxy Protocol V2 funkcióhoz.</span><span class="sxs-lookup"><span data-stu-id="773db-1250">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="773db-1251">Hozzáadja az EnableProxyProtocol tulajdonságot a PrivateLinkService osztályban</span><span class="sxs-lookup"><span data-stu-id="773db-1251">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="773db-1252">Hozzáadja a LinkIdentifier tulajdonságot a PrivateEndpointConnection osztályban</span><span class="sxs-lookup"><span data-stu-id="773db-1252">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="773db-1253">New-AzPrivateLinkService frissítve az új, választható EnableProxyProtocol paraméter hozzáadásával.</span><span class="sxs-lookup"><span data-stu-id="773db-1253">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="773db-1254">Ki lett javítva a New-AzApplicationGatewaySku referenciadokumentációjában található helytelen paraméterleírás</span><span class="sxs-lookup"><span data-stu-id="773db-1254">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="773db-1255">Új parancsmagok az Azure Firewall-szabályzat támogatásához</span><span class="sxs-lookup"><span data-stu-id="773db-1255">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="773db-1256">A VirtualHub RouteTables gyermekerőforrásának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-1256">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="773db-1257">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="773db-1257">New cmdlets added:</span></span>
        - <span data-ttu-id="773db-1258">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="773db-1258">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="773db-1259">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="773db-1259">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="773db-1260">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="773db-1260">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="773db-1261">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="773db-1261">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="773db-1262">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="773db-1262">Set-AzVirtualHub</span></span>
* <span data-ttu-id="773db-1263">Az új termékváltozat és VirtualWANType tulajdonság támogatásának hozzáadása a VirtualHub, illetve a VirtualWan esetében</span><span class="sxs-lookup"><span data-stu-id="773db-1263">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="773db-1264">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="773db-1264">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="773db-1265">New-AzVirtualHub: Sku paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-1265">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="773db-1266">Update-AzVirtualHub: Sku paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-1266">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="773db-1267">New-AzVirtualWan: VirtualWANType paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-1267">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="773db-1268">Update-AzVirtualWan: VirtualWANType paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-1268">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="773db-1269">Az EnableInternetSecurity tulajdonság támogatásának hozzáadása a HubVnetConnection, a VpnConnection és az ExpressRouteConnection esetében</span><span class="sxs-lookup"><span data-stu-id="773db-1269">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="773db-1270">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="773db-1270">New cmdlets added:</span></span>
        - <span data-ttu-id="773db-1271">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="773db-1271">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="773db-1272">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="773db-1272">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="773db-1273">New-AzureRmVirtualHubVnetConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-1273">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="773db-1274">New-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-1274">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="773db-1275">Update-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-1275">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="773db-1276">New-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-1276">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="773db-1277">Set-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-1277">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="773db-1278">TopLevel WebApplicationFirewall-szabályzat beállításának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-1278">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="773db-1279">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="773db-1279">New cmdlets added:</span></span>
        - <span data-ttu-id="773db-1280">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="773db-1280">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="773db-1281">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="773db-1281">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="773db-1282">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="773db-1282">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="773db-1283">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="773db-1283">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="773db-1284">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="773db-1284">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="773db-1285">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="773db-1285">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="773db-1286">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="773db-1286">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="773db-1287">New-AzApplicationGatewayFirewallPolicy: PolicySetting, ManagedRule paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-1287">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="773db-1288">A CustomRule Geo-Match operátorának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-1288">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="773db-1289">A GeoMatch hozzáadva a FirewallCondition operátorához</span><span class="sxs-lookup"><span data-stu-id="773db-1289">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="773db-1290">perListener és a perSite tűzfalszabályzat támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-1290">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="773db-1291">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="773db-1291">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="773db-1292">New-AzApplicationGatewayHttpListener: FirewallPolicy, FirewallPolicyId paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-1292">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="773db-1293">New-AzApplicationGatewayPathRuleConfig: FirewallPolicy, FirewallPolicyId paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-1293">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="773db-1294">Javítva: a PSBastion esetében a szükséges AzureBastionSubnet alhálózat nevében nem kell megkülönböztetni a kis- és nagybetűket</span><span class="sxs-lookup"><span data-stu-id="773db-1294">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="773db-1295">A hálózati szabályok céltartományneveinek és a NAT-szabályok lefordított tartományneveinek támogatása az Azure Firewallban</span><span class="sxs-lookup"><span data-stu-id="773db-1295">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="773db-1296">Az IpGroup legfelsőbb szintű RouteTables erőforrásának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-1296">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="773db-1297">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="773db-1297">New cmdlets added:</span></span>
        - <span data-ttu-id="773db-1298">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="773db-1298">New-AzIpGroup</span></span>
        - <span data-ttu-id="773db-1299">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="773db-1299">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="773db-1300">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="773db-1300">Get-AzIpGroup</span></span>
        - <span data-ttu-id="773db-1301">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="773db-1301">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="773db-1302">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="773db-1302">Az.ServiceFabric</span></span>
* <span data-ttu-id="773db-1303">Az Add-AzServiceFabricApplicationCertificate parancsmag el lett távolítva, mivel az Add-AzVmssSecret lefedi ezt a forgatókönyvet.</span><span class="sxs-lookup"><span data-stu-id="773db-1303">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="773db-1304">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-1304">Az.Sql</span></span>
* <span data-ttu-id="773db-1305">Törölt adatbázisok visszaállításának támogatása hozzáadva a felügyelt példányokon.</span><span class="sxs-lookup"><span data-stu-id="773db-1305">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="773db-1306">A régi naplózási parancsmagok elavulttá váltak a kódban.</span><span class="sxs-lookup"><span data-stu-id="773db-1306">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="773db-1307">A következő elavult aliasok el lettek távolítva:</span><span class="sxs-lookup"><span data-stu-id="773db-1307">Removed deprecated aliases:</span></span>
* <span data-ttu-id="773db-1308">Get-AzSqlDatabaseIndexRecommendations (a Get-AzSqlDatabaseIndexRecommendation használata javasolt helyette)</span><span class="sxs-lookup"><span data-stu-id="773db-1308">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="773db-1309">Get-AzSqlDatabaseRestorePoints (a Get-AzSqlDatabaseRestorePoint használata javasolt helyette)</span><span class="sxs-lookup"><span data-stu-id="773db-1309">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="773db-1310">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag eltávolítva</span><span class="sxs-lookup"><span data-stu-id="773db-1310">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="773db-1311">Az elavult sebezhetőség-felmérési beállítások parancsmagjainak aliasai eltávolítva</span><span class="sxs-lookup"><span data-stu-id="773db-1311">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="773db-1312">A fejlett fenyegetésészlelési beállítások parancsmagjai elavulttá váltak</span><span class="sxs-lookup"><span data-stu-id="773db-1312">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="773db-1313">Parancsmagok hozzáadása egy adatbázis oszlopait érintő érzékenységi javaslatok letiltása és engedélyezése céljából.</span><span class="sxs-lookup"><span data-stu-id="773db-1313">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="773db-1314">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="773db-1314">Az.Storage</span></span>
* <span data-ttu-id="773db-1315">Nagy fájlok megosztásának engedélyezése Storage-fiók létrehozása vagy frissítése esetén</span><span class="sxs-lookup"><span data-stu-id="773db-1315">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="773db-1316">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="773db-1316">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="773db-1317">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="773db-1317">Set-AzStorageAccount</span></span>
* <span data-ttu-id="773db-1318">Fájlkezelő bezárása/lekérése esetén a fájlkönyvtár vagy fájl bemeneti elérési út ellenőrzése kimarad, hogy a DeletePending állapotban lévő objektum ne okozhasson hibát</span><span class="sxs-lookup"><span data-stu-id="773db-1318">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="773db-1319">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="773db-1319">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="773db-1320">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="773db-1320">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="773db-1321">2.8.0 – 2019. október</span><span class="sxs-lookup"><span data-stu-id="773db-1321">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="773db-1322">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="773db-1322">General</span></span>
* <span data-ttu-id="773db-1323">Az.HealthcareApis 1.0.0-s kiadás</span><span class="sxs-lookup"><span data-stu-id="773db-1323">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="773db-1324">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="773db-1324">Az.Accounts</span></span>
* <span data-ttu-id="773db-1325">A telemetria és az URL-címek újraírásának frissítése a létrehozott modulok esetében, a Windows-egységek tesztelésének javítása.</span><span class="sxs-lookup"><span data-stu-id="773db-1325">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="773db-1326">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="773db-1326">Az.ApiManagement</span></span>
* <span data-ttu-id="773db-1327">**Set-AzApiManagementApi** – Az API a következőre való frissítésének támogatása: ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="773db-1327">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="773db-1328">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="773db-1328">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="773db-1329">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="773db-1329">Az.Automation</span></span>
* <span data-ttu-id="773db-1330">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag a Linux újraindítási beállítási paramétere kapcsán.</span><span class="sxs-lookup"><span data-stu-id="773db-1330">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="773db-1331">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="773db-1331">Az.Batch</span></span>
* <span data-ttu-id="773db-1332">A **Get-AzBatchNodeAgentSku** elavult, így a 2.0.0-ás verziótól a **Get-AzBatchSupportImage** váltja fel.</span><span class="sxs-lookup"><span data-stu-id="773db-1332">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="773db-1333">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-1333">Az.Compute</span></span>
* <span data-ttu-id="773db-1334">A Priority, EvictionPolicy és MaxPrice paraméterek hozzáadása a New-AzVM és a New-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="773db-1334">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="773db-1335">Az Add-AzVMAdditionalUnattendContent és az Add-AzVMSshPublicKey parancsmagok figyelmeztető üzenetének és súgójának kijavítása</span><span class="sxs-lookup"><span data-stu-id="773db-1335">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="773db-1336">A -skipVmBackup kivétel kijavítása felügyelt lemezekkel rendelkező Linux rendszerű virtuális gépek esetében a Set-AzVMDiskEncryptionExtension kapcsán.</span><span class="sxs-lookup"><span data-stu-id="773db-1336">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="773db-1337">A titkosítási beállítások frissítési hibájának kijavítása a Set-AzVMDiskEncryptionExtension kétmenetes forgatókönyvében.</span><span class="sxs-lookup"><span data-stu-id="773db-1337">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="773db-1338">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="773db-1338">Az.DataFactory</span></span>
* <span data-ttu-id="773db-1339">CRUD-parancsok lettek hozzáadva az ADF V2-adatfolyamhoz: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow és Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="773db-1339">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="773db-1340">Műveleti parancsok lettek hozzáadva az ADF V2-adatfolyam hibakeresési munkamenetéhez: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand és Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="773db-1340">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="773db-1341">Az ADF .Net SDK a 4.2.0-ás verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="773db-1341">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="773db-1342">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="773db-1342">Az.DataLakeStore</span></span>
* <span data-ttu-id="773db-1343">A fiókérvényesítés javítása, hogy a "-" jelölésű fiókok tartomány nélkül is továbbíthatók legyenek</span><span class="sxs-lookup"><span data-stu-id="773db-1343">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="773db-1344">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="773db-1344">Az.HealthcareApis</span></span>
* <span data-ttu-id="773db-1345">A PowerShell az 1.0.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="773db-1345">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="773db-1346">Az SDK a 1.0.2-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="773db-1346">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="773db-1347">Frissítés a tesztekben az új SDK-verzióra való hivatkozáshoz</span><span class="sxs-lookup"><span data-stu-id="773db-1347">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="773db-1348">A kimeneti struktúra beágyazottról simítottra frissült.</span><span class="sxs-lookup"><span data-stu-id="773db-1348">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="773db-1349">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="773db-1349">Az.IotHub</span></span>
* <span data-ttu-id="773db-1350">Új útválasztási forrás hozzáadása: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="773db-1350">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="773db-1351">Kisebb hibajavítás: A Get-AzIothub nem adja vissza a következőt: subscriptionId</span><span class="sxs-lookup"><span data-stu-id="773db-1351">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="773db-1352">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="773db-1352">Az.Monitor</span></span>
* <span data-ttu-id="773db-1353">Új műveleticsoport-fogadók hozzáadva a következő műveleti csoporthoz:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="773db-1353">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="773db-1354">Az általános riasztási séma használata engedélyezve a fogadók számára.</span><span class="sxs-lookup"><span data-stu-id="773db-1354">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="773db-1355">Ez nem vonatkozik az SMS, az Azure App leküldéses üzenetei, az ITSM és a Voice fogadóira.</span><span class="sxs-lookup"><span data-stu-id="773db-1355">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="773db-1356">A webhookok mostantól az Azure Active Directory-hitelesítés használatát is támogatják.</span><span class="sxs-lookup"><span data-stu-id="773db-1356">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="773db-1357">Az.Network</span><span class="sxs-lookup"><span data-stu-id="773db-1357">Az.Network</span></span>
* <span data-ttu-id="773db-1358">Új Get-AzAvailableServiceAlias parancsmag hozzáadva, amely a szolgáltatásvégpont-szabályzatokhoz használható aliasok beszerzéséhez hívható meg.</span><span class="sxs-lookup"><span data-stu-id="773db-1358">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="773db-1359">Forgalomválasztók hozzáadásának támogatása a virtuális hálózati átjáró kapcsolataihoz</span><span class="sxs-lookup"><span data-stu-id="773db-1359">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="773db-1360">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="773db-1360">New cmdlets added:</span></span>
        - <span data-ttu-id="773db-1361">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="773db-1361">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="773db-1362">Parancsmagok frissítve választható paraméterekkel -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="773db-1362">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="773db-1363">Az ESP és AH protokollok támogatása a hálózati biztonsági szabályzati konfigurációkban</span><span class="sxs-lookup"><span data-stu-id="773db-1363">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="773db-1364">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="773db-1364">Updated cmdlets:</span></span>
        - <span data-ttu-id="773db-1365">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="773db-1365">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="773db-1366">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="773db-1366">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="773db-1367">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="773db-1367">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="773db-1368">Tovább javult a Cortex-parancsmagok kivételeinek kezelése</span><span class="sxs-lookup"><span data-stu-id="773db-1368">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="773db-1369">A VirtualNetworkGateways új generációi és termékváltozatai</span><span class="sxs-lookup"><span data-stu-id="773db-1369">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="773db-1370">A VirtualNetworkGateways új generációinak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="773db-1370">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="773db-1371">A VirtualNetworkGateways új, nagy átviteli sebességű termékváltozatainak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="773db-1371">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="773db-1372">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="773db-1372">Az.RedisCache</span></span>
* <span data-ttu-id="773db-1373">Frissült a Set-AzRedisCache referenciadokumentációja, amely most már tartalmazza a -Size paraméter hiányzó értékeit.</span><span class="sxs-lookup"><span data-stu-id="773db-1373">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="773db-1374">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-1374">Az.Sql</span></span>
* <span data-ttu-id="773db-1375">Az Active Directory-rendszergazda a felügyelt példányon való beállításának támogatása</span><span class="sxs-lookup"><span data-stu-id="773db-1375">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="773db-1376">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="773db-1376">Az.Storage</span></span>
* <span data-ttu-id="773db-1377">Az Storage-ügyfélkódtár a 11.1.0-s verzióra frissült.</span><span class="sxs-lookup"><span data-stu-id="773db-1377">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="773db-1378">A Management plane API-val rendelkező tárolók listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="773db-1378">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="773db-1379">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="773db-1379">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="773db-1380">A tárfiókok előfizetésből történő listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="773db-1380">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="773db-1381">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="773db-1381">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="773db-1382">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="773db-1382">Az.StorageSync</span></span>
* <span data-ttu-id="773db-1383">A Reset-AzStorageSyncServerCertificate 9810-es hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="773db-1383">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="773db-1384">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="773db-1384">Az.Websites</span></span>
* <span data-ttu-id="773db-1385">Egy alkalmazáshoz tartozó ASP Set-AzWebApp általi frissítése sikertelen volt</span><span class="sxs-lookup"><span data-stu-id="773db-1385">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="773db-1386">2.7.0 – 2019. szeptember</span><span class="sxs-lookup"><span data-stu-id="773db-1386">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="773db-1387">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="773db-1387">Az.ApiManagement</span></span>
* <span data-ttu-id="773db-1388">Frissítve lett a „-Format” paraméter leírása a „Set-AzApiManagementPolicy” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="773db-1388">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="773db-1389">El lettek távolítva az elavult „Update-AzApiManagementDeployment” parancsmag referenciái a referenciadokumentációból.</span><span class="sxs-lookup"><span data-stu-id="773db-1389">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="773db-1390">A „Set-AzApiManagement” használható helyette.</span><span class="sxs-lookup"><span data-stu-id="773db-1390">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="773db-1391">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="773db-1391">Az.Automation</span></span>
* <span data-ttu-id="773db-1392">Ki lett javítva a „Register-AzAutomationDscNode” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="773db-1392">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="773db-1393">Hozzá lett adva az operációs rendszerrel kapcsolatos korlátozások pontosítása a Register-AzAutomationDSCNode parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="773db-1393">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="773db-1394">Ki lett javítva a Start-AzAutomationRunbook parancsmag null értékű hivatkozás okozta kivétele a -Wait paraméter esetén.</span><span class="sxs-lookup"><span data-stu-id="773db-1394">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="773db-1395">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-1395">Az.Compute</span></span>
* <span data-ttu-id="773db-1396">Hozzá lett adva az UploadSizeInBytes paraméter a New-AzDiskConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="773db-1396">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="773db-1397">Hozzá lett adva az Incremental paraméter a New-AzSnapshotConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="773db-1397">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="773db-1398">Alacsony prioritású virtuálisgép-funkció hozzáadása:</span><span class="sxs-lookup"><span data-stu-id="773db-1398">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="773db-1399">Hozzá lett adva a MaxPrice, az EvictionPolicy és a Priority paraméter a New-AzVMConfig parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="773db-1399">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="773db-1400">Hozzá lett adva a MaxPrice paraméter a New-AzVmssConfig, az Update-AzVM és az Update-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="773db-1400">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="773db-1401">Ki lett javítva a Get-AzAvailabilitySet parancsmag virtuálisgép-hivatkozással kapcsolatos hibája, amely miatt a parancsmag az előfizetésben található összes rendelkezésreállási csoportot listázta.</span><span class="sxs-lookup"><span data-stu-id="773db-1401">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="773db-1402">Ki lett javítva a Get-AzRemoteDesktopFile parancsmag esetében jelentkező null kivétel.</span><span class="sxs-lookup"><span data-stu-id="773db-1402">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="773db-1403">Ki lett javítva virtuális merevlemezek Seek metódusa a végrelatív pozíció esetében.</span><span class="sxs-lookup"><span data-stu-id="773db-1403">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="773db-1404">Ki lett javítva az UltraSSD hibája a New-AzVM és az Update-AzVM parancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="773db-1404">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="773db-1405">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="773db-1405">Az.DataFactory</span></span>
* <span data-ttu-id="773db-1406">Hozzá lett adva 3 új parancs (az Add-AzDataFactoryV2TriggerSubscription, a Remove-AzDataFactoryV2TriggerSubscription és a Get-AzDataFactoryV2TriggerSubscriptionStatus) az ADF V2-höz</span><span class="sxs-lookup"><span data-stu-id="773db-1406">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="773db-1407">Az ADF .Net SDK a 4.1.3-as verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="773db-1407">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="773db-1408">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="773db-1408">Az.HDInsight</span></span>
* <span data-ttu-id="773db-1409">Kompatibilitástörő változások a meghívással kapcsolatban</span><span class="sxs-lookup"><span data-stu-id="773db-1409">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="773db-1410">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="773db-1410">Az.IotHub</span></span>
* <span data-ttu-id="773db-1411">Hozzá lett adva az IoTHubok földrajzilag párosított vészhelyreállítási régiójába történő feladatátvétel meghívásának támogatása.</span><span class="sxs-lookup"><span data-stu-id="773db-1411">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="773db-1412">Hozzá lett adva az IoTHubok üzenetbővítés-kezelésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="773db-1412">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="773db-1413">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="773db-1413">New cmdlets are:</span></span>
    - <span data-ttu-id="773db-1414">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="773db-1414">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="773db-1415">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="773db-1415">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="773db-1416">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="773db-1416">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="773db-1417">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="773db-1417">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="773db-1418">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="773db-1418">Az.Monitor</span></span>
* <span data-ttu-id="773db-1419">A legújabb Monitor SDK-ra mutat, azaz a 0.24.1-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="773db-1419">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="773db-1420">Nem kompatibilitástörő változásokkal bővíti a Metrics parancsmagokat, így az egységek számbavétele számos új értéket támogat.</span><span class="sxs-lookup"><span data-stu-id="773db-1420">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="773db-1421">Ezek írásvédett parancsmagok, ezért a parancsmagok bemenetében nem történik változás.</span><span class="sxs-lookup"><span data-stu-id="773db-1421">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="773db-1422">Az **ActionGroups**-kérések api-version értéke mostantól **2019-06-01**, korábban **2018-03-01** volt.</span><span class="sxs-lookup"><span data-stu-id="773db-1422">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="773db-1423">A forgatókönyvtesztek frissültek, így igazodnak a változáshoz.</span><span class="sxs-lookup"><span data-stu-id="773db-1423">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="773db-1424">Az **EmailReceiver** és a **WebhookReceiver** osztályok konstruktoraihoz hozzá lett adva egy új kötelező argumentum, a **useCommonAlertSchema** nevű logikai érték.</span><span class="sxs-lookup"><span data-stu-id="773db-1424">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="773db-1425">A kompatibilitástörő változás parancsmagok elől való elrejtése érdekében a rögzített érték jelenleg a **false** (hamis).</span><span class="sxs-lookup"><span data-stu-id="773db-1425">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="773db-1426">**MEGJEGYZÉS**: Ez egy átmeneti módosítás, amelyet a Riasztások csapatnak érvényesítenie kell.</span><span class="sxs-lookup"><span data-stu-id="773db-1426">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="773db-1427">A **Source** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="773db-1427">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="773db-1428">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="773db-1428">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="773db-1429">Az **AlertingAction** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="773db-1429">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="773db-1430">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="773db-1430">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="773db-1431">A dinamikus küszöbérték kritériumainak támogatása a 2-es verziójú metrikariasztás esetében</span><span class="sxs-lookup"><span data-stu-id="773db-1431">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="773db-1432">New-AzMetricAlertRuleV2Criteria: mostantól a dinamikus küszöbértékek kritériumait is létrehozza</span><span class="sxs-lookup"><span data-stu-id="773db-1432">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="773db-1433">Add-AzMetricAlertRuleV2: mostantól a dinamikus küszöbértékek kritériumait is elfogadja</span><span class="sxs-lookup"><span data-stu-id="773db-1433">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="773db-1434">Az ütemezett lekérdezési szabályok parancsmagjainak (SQR) fejlesztései</span><span class="sxs-lookup"><span data-stu-id="773db-1434">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="773db-1435">A parancsmagok a „Location” paraméter mindkét formátumát elfogadják: a helyet (például eastus) és a hely megjelenített nevét is (például USA keleti régiója)</span><span class="sxs-lookup"><span data-stu-id="773db-1435">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="773db-1436">Megfelelően ábrázolva lett az „Enabled” paraméter a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="773db-1436">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="773db-1437">Példák lettek hozzáadva az „ActionGroup” opcionális paraméterhez</span><span class="sxs-lookup"><span data-stu-id="773db-1437">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="773db-1438">Általánosan továbbfejlesztett súgófájlok</span><span class="sxs-lookup"><span data-stu-id="773db-1438">Overall improved help files</span></span>
* <span data-ttu-id="773db-1439">Ki lett javítva a „Set-AzActionRule” hatókörtípusának meghatározásával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="773db-1439">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="773db-1440">Az.Network</span><span class="sxs-lookup"><span data-stu-id="773db-1440">Az.Network</span></span>
* <span data-ttu-id="773db-1441">Ki lett javítva a „New-AzApplicationGateway” referenciadokumentációjában található helytelen példa</span><span class="sxs-lookup"><span data-stu-id="773db-1441">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="773db-1442">Hozzá lett adva egy csomagrögzítés összes tulajdonságának lekérésével kapcsolatos megjegyzés a „Get-AzNetworkWatcherPacketCapture” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="773db-1442">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="773db-1443">Ki lett javítva a „Test-AzNetworkWatcherIPFlow” referenciadokumentációjában található példa a hálózati adapterek megfelelő számbavétele érdekében</span><span class="sxs-lookup"><span data-stu-id="773db-1443">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="773db-1444">Tovább lett fejlesztve a felhőkivétel-elemzés az esetleges további részletek megjelenítése érdekében</span><span class="sxs-lookup"><span data-stu-id="773db-1444">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="773db-1445">Tovább lett fejlesztve a felhőkivétel-elemzés az SDK-kivételek további típusainak kezelése érdekében</span><span class="sxs-lookup"><span data-stu-id="773db-1445">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="773db-1446">Ki lett javítva a biztonságiszabály-modellek helytelen leképezése</span><span class="sxs-lookup"><span data-stu-id="773db-1446">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="773db-1447">Hozzá lettek adva a privát IP-cím funkcióval kapcsolatos tulajdonságok a hálózati adapterhez</span><span class="sxs-lookup"><span data-stu-id="773db-1447">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="773db-1448">Hozzá lett adva a „PrivateEndpoint” tulajdonság PSResourceId típusúként a PSNetworkInterface osztályhoz</span><span class="sxs-lookup"><span data-stu-id="773db-1448">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="773db-1449">Hozzá lett adva a „PrivateLinkConnectionProperties” tulajdonság PSIpConfigurationConnectivityInformation típusúként a PSNetworkInterfaceIPConfiguration osztályhoz</span><span class="sxs-lookup"><span data-stu-id="773db-1449">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="773db-1450">Hozzá lett adva a PSIpConfigurationConnectivityInformation nevű új modellosztály</span><span class="sxs-lookup"><span data-stu-id="773db-1450">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="773db-1451">Hozzá lett adva az új ApplicationRuleProtocolType „mssql” az Azure Firewall-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="773db-1451">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="773db-1452">MultiLink-támogatás a Virtuális WAN-ben</span><span class="sxs-lookup"><span data-stu-id="773db-1452">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="773db-1453">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="773db-1453">New cmdlets</span></span>
        - <span data-ttu-id="773db-1454">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="773db-1454">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="773db-1455">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="773db-1455">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="773db-1456">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="773db-1456">Updated cmdlet:</span></span>
        - <span data-ttu-id="773db-1457">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="773db-1457">New-VpnSite</span></span>
        - <span data-ttu-id="773db-1458">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="773db-1458">Update-VpnSite</span></span>
        - <span data-ttu-id="773db-1459">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="773db-1459">New-VpnConnection</span></span>
        - <span data-ttu-id="773db-1460">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="773db-1460">Update-VpnConnection</span></span>
* <span data-ttu-id="773db-1461">Ki lettek javítva bizonyos PowerShell-példák dokumentumai, hogy az AzureRM-parancsmagok helyett az Az-parancsmagokat használják</span><span class="sxs-lookup"><span data-stu-id="773db-1461">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="773db-1462">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="773db-1462">Az.RecoveryServices</span></span>
* <span data-ttu-id="773db-1463">Frissítve lett az AzureVMpolicy objektum a ProtectedItemsCount attribútummal</span><span class="sxs-lookup"><span data-stu-id="773db-1463">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="773db-1464">Tesztek lettek hozzáadva a virtuális gép szabályzatához és az eredeti Storage-fiók visszaállításához</span><span class="sxs-lookup"><span data-stu-id="773db-1464">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="773db-1465">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-1465">Az.Resources</span></span>
* <span data-ttu-id="773db-1466">Ki lett javítva a hiba, amely miatt a New-AzRoleAssignment parancsot nem lehetett meghívni a Scope paraméter nélkül.</span><span class="sxs-lookup"><span data-stu-id="773db-1466">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="773db-1467">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="773db-1467">Az.ServiceFabric</span></span>
* <span data-ttu-id="773db-1468">Ki lett javítva az „Update-AzServiceFabricReliability” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="773db-1468">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="773db-1469">Új parancsmagok lettek hozzáadva az alkalmazás és a szolgáltatások felügyeletéhez:</span><span class="sxs-lookup"><span data-stu-id="773db-1469">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="773db-1470">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="773db-1470">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="773db-1471">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="773db-1471">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="773db-1472">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="773db-1472">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="773db-1473">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="773db-1473">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="773db-1474">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="773db-1474">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="773db-1475">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="773db-1475">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="773db-1476">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="773db-1476">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="773db-1477">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="773db-1477">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="773db-1478">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="773db-1478">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="773db-1479">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="773db-1479">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="773db-1480">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="773db-1480">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="773db-1481">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="773db-1481">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="773db-1482">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="773db-1482">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="773db-1483">A Service Fabric SDK az 1.2.0-s verzióra frissült, amely a Service Fabric erőforrás-szolgáltató 2019-03-01 api-versionjét használja.</span><span class="sxs-lookup"><span data-stu-id="773db-1483">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="773db-1484">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="773db-1484">Az.SignalR</span></span>
* <span data-ttu-id="773db-1485">Hozzá lettek adva az Update, Restart, CheckNameAvailability és GetUsage parancsmagok</span><span class="sxs-lookup"><span data-stu-id="773db-1485">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="773db-1486">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-1486">Az.Sql</span></span>
* <span data-ttu-id="773db-1487">Frissítve lett a „Get-AzSqlElasticPool” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="773db-1487">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="773db-1488">Hozzá lett adva egy rugalmas készlet létrehozását bemutató virtuálismag-példa (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="773db-1488">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="773db-1489">El lett távolítva az EmailAddresses érvényesítése és annak ellenőrzése, hogy az EmailAdmins értéke hamis-e abban az esetben, ha az EmailAddresses üres a Set-AzSqlServerAdvancedThreatProtectionPolicy és a Set-AzSqlDatabaseAdvancedThreatProtectionPolicy parancsmagban</span><span class="sxs-lookup"><span data-stu-id="773db-1489">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="773db-1490">Engedélyezve lettek a kiszolgáló-/adatbázis-naplózási beállítások abban az esetben, ha több olyan diagnosztikai beállítás létezik, amelyek engedélyezik a naplózási kategóriát.</span><span class="sxs-lookup"><span data-stu-id="773db-1490">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="773db-1491">Ki lett javítva az e-mail-címek ellenőrzése több, SQL-sebezhetőségi felméréshez használt parancsmagban (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting és Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="773db-1491">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="773db-1492">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="773db-1492">Az.Storage</span></span>
* <span data-ttu-id="773db-1493">Frissítve lett a „Get-AzStorageAccountKey” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="773db-1493">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="773db-1494">A forrásfájl SMB-tulajdonságai (fájlattribútumok, fájl létrehozásának ideje, fájl utolsó írásának ideje) célfájlban történő megtartásának támogatása az Azure File-beli feltöltés/letöltés esetében</span><span class="sxs-lookup"><span data-stu-id="773db-1494">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="773db-1495">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="773db-1495">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="773db-1496">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="773db-1496">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="773db-1497">Ki lett javítva a tulajdonság-/metaadathibával meghiúsuló blokkblobfeltöltés a tárolóképes ImmutabilityPolicy esetében.</span><span class="sxs-lookup"><span data-stu-id="773db-1497">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="773db-1498">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="773db-1498">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="773db-1499">Az Azure File-megosztások Management plane API-val történő kezelésének támogatása</span><span class="sxs-lookup"><span data-stu-id="773db-1499">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="773db-1500">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="773db-1500">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="773db-1501">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="773db-1501">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="773db-1502">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="773db-1502">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="773db-1503">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="773db-1503">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="773db-1504">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="773db-1504">Az.Websites</span></span>
* <span data-ttu-id="773db-1505">Ki lett javítva az a probléma, amely miatt a webalkalmazás Címkéi törölve lettek az alkalmazás új ASP-be történő migrálásakor</span><span class="sxs-lookup"><span data-stu-id="773db-1505">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="773db-1506">Ki lett javítva a Publish-AzureWebapp parancs a Linux és Windows rendszeren történő működés érdekében</span><span class="sxs-lookup"><span data-stu-id="773db-1506">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="773db-1507">Frissítve lett a „Get-AzWebAppPublishingProfile” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="773db-1507">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="773db-1508">2.6.0 – 2019. augusztus</span><span class="sxs-lookup"><span data-stu-id="773db-1508">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="773db-1509">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="773db-1509">General</span></span>
* <span data-ttu-id="773db-1510">Különféle elgépelések kijavítva több modulban</span><span class="sxs-lookup"><span data-stu-id="773db-1510">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="773db-1511">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="773db-1511">Az.Accounts</span></span>
* <span data-ttu-id="773db-1512">Felhasználó által hozzárendelt MSI támogatása az Azure Functions-hitelesítésben (#9479)</span><span class="sxs-lookup"><span data-stu-id="773db-1512">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="773db-1513">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="773db-1513">Az.Aks</span></span>
* <span data-ttu-id="773db-1514">A Get-AzAks kimenetével kapcsolatos probléma ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="773db-1514">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="773db-1515">További információ: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="773db-1515">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="773db-1516">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="773db-1516">Az.ApiManagement</span></span>
* <span data-ttu-id="773db-1517">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="773db-1517">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="773db-1518">Frissült a .net nuget verziója, amely nem kényszeríti ki a productId, az apiId, a groupId és a userId korlátozásait</span><span class="sxs-lookup"><span data-stu-id="773db-1518">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="773db-1519">**Get-AzApiManagementProduct** – A termékek API-val történő lekérdezése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="773db-1519">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="773db-1520">**New-AzApiManagementApiRevision** – Ki lett javítva az a probléma, amely miatt az ApiRevisionDescription nem lett beállítva az új API-változat létrehozásakor https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="773db-1520">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="773db-1521">Ki lett javítva a PsApiManagementOAuth2AuthrozationServer modell elírása PsApiManagementOAuth2AuthorizationServer értékre</span><span class="sxs-lookup"><span data-stu-id="773db-1521">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="773db-1522">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="773db-1522">Az.Batch</span></span>
* <span data-ttu-id="773db-1523">Ki lett javítva a súgóüzenetben és a dokumentációban található elgépelés, nagy kezdőbetűs Windows értékre</span><span class="sxs-lookup"><span data-stu-id="773db-1523">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="773db-1524">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="773db-1524">Az.Cdn</span></span>
* <span data-ttu-id="773db-1525">Ki lett javítva egy elgépelés CDN modulátalakító segédben</span><span class="sxs-lookup"><span data-stu-id="773db-1525">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="773db-1526">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-1526">Az.Compute</span></span>
* <span data-ttu-id="773db-1527">Új VmssId a New-AzVMConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="773db-1527">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="773db-1528">Új TerminateScheduledEvents és a TerminateScheduledEventNotBeforeTimeoutInMinutes paraméterek a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="773db-1528">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="773db-1529">Új HyperVGeneration tulajdonság a VM-rendszerképobjektumhoz</span><span class="sxs-lookup"><span data-stu-id="773db-1529">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="773db-1530">Új Host és HostGroup jellemzők</span><span class="sxs-lookup"><span data-stu-id="773db-1530">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="773db-1531">Új parancsmagok:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="773db-1531">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="773db-1532">Új HostId paraméter a New-AzVMConfig és a New-AzVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="773db-1532">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="773db-1533">Az Invoke-AzVMRunCommand dokumentációjában található példa frissítve lett a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="773db-1533">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="773db-1534">A -VolumeType leírása frissítve lett a set-AzVMDiskEncryptionExtension és a set-AzVmssDiskEncryptionExtension referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="773db-1534">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="773db-1535">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="773db-1535">Az.DataFactory</span></span>
* <span data-ttu-id="773db-1536">A New-AzDataFactoryEncryptValue dokumentációjában a Windows szó nagy kezdőbetűsre lett javítva</span><span class="sxs-lookup"><span data-stu-id="773db-1536">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="773db-1537">Az ADF .Net SDK a 4.1.2-es verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="773db-1537">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="773db-1538">Új DataProxyIntegrationRuntimeName, DataProxyIntegrationRuntimeName és DataProxyStagingPath paraméterek lettek hozzáadva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz, lehetővé téve a helyi integrációs modul SSIS integrációs modul proxyjaként való beállítását</span><span class="sxs-lookup"><span data-stu-id="773db-1538">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="773db-1539">Frissítve lett a PSTriggerRun, hogy megjelenítse az aktivált folyamatokat, üzeneteket és tulajdonságokat, illetve a PSActivityRun, hogy megjelenítse a tevékenységtípust</span><span class="sxs-lookup"><span data-stu-id="773db-1539">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="773db-1540">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="773db-1540">Az.DataLakeStore</span></span>
* <span data-ttu-id="773db-1541">Ki lett javítva a Get-DataLakeStoreDeletedItem lefagyása hibák vagy távoli kivételek esetén.</span><span class="sxs-lookup"><span data-stu-id="773db-1541">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="773db-1542">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="773db-1542">Az.EventHub</span></span>
* <span data-ttu-id="773db-1543">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNteworkRule paraméter a Set-AzEventHubNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="773db-1543">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="773db-1544">Ki lett javítva a 9558-as számú hiba: Set-AzEventHubNamespace a PUT helyett a PATCH kérést használta</span><span class="sxs-lookup"><span data-stu-id="773db-1544">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="773db-1545">új EnableKafka paraméter a Set-AzEventHubNamespace parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="773db-1545">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="773db-1546">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="773db-1546">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="773db-1547">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="773db-1547">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="773db-1548">Ki lett javítva egy elgépelés a dokumentációban, ahol az Azure csupa kisbetűvel szerepelt</span><span class="sxs-lookup"><span data-stu-id="773db-1548">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="773db-1549">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="773db-1549">Az.Monitor</span></span>
* <span data-ttu-id="773db-1550">Hibás paraméternév lett kijavítva a súgódokumentációban</span><span class="sxs-lookup"><span data-stu-id="773db-1550">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="773db-1551">Az.Network</span><span class="sxs-lookup"><span data-stu-id="773db-1551">Az.Network</span></span>
* <span data-ttu-id="773db-1552">Frissítve lett a New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="773db-1552">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="773db-1553">A PublicIpAddress elavult, mert a kiszolgálóoldalon nem használatos.</span><span class="sxs-lookup"><span data-stu-id="773db-1553">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="773db-1554">Hozzá lett adva egy opcionális Primary paraméter, amely azt jelzi, hogy a jelenlegi IP-konfiguráció elsődleges-e.</span><span class="sxs-lookup"><span data-stu-id="773db-1554">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="773db-1555">Javítva lett az SDK kérelemhiba-kivételének kezelése – kijavítja azt a problémát, amely miatt az SDK-kivételek kezelése korábban nem volt megfelelő, és a fontos hibarészletek nem jelentek meg</span><span class="sxs-lookup"><span data-stu-id="773db-1555">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="773db-1556">Be lett állítva, hogy az IPv6 IP-előtag ellenőrzési logikája ellenőrizze az IPv6-előtag hosszának megfelelőségét.</span><span class="sxs-lookup"><span data-stu-id="773db-1556">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="773db-1557">Frissült a Get-AzVirtualNetworkSubnetConfig: Új paraméterkészlet lett hozzáadva az alhálózat erőforrás-azonosítója szerinti lekéréshez.</span><span class="sxs-lookup"><span data-stu-id="773db-1557">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="773db-1558">Frissült az AzNetworkServiceTag Location paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="773db-1558">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="773db-1559">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="773db-1559">Az.OperationalInsights</span></span>
* <span data-ttu-id="773db-1560">Frissült a New-AzOperationalInsightsLinuxSyslogDataSource dokumentációja</span><span class="sxs-lookup"><span data-stu-id="773db-1560">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="773db-1561">Példa hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-1561">Added example</span></span>
    - <span data-ttu-id="773db-1562">A -Name paraméter leírása frissítve lett</span><span class="sxs-lookup"><span data-stu-id="773db-1562">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="773db-1563">Új példa lett hozzáadva a New-AzOperationalInsightsWindowsEventDataSource parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="773db-1563">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="773db-1564">Módosult a New-AzOperationalInsightsWindowsEventDataSource -Name paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="773db-1564">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="773db-1565">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="773db-1565">Az.RecoveryServices</span></span>
* <span data-ttu-id="773db-1566">Frissült a Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="773db-1566">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="773db-1567">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-1567">Az.Resources</span></span>
* <span data-ttu-id="773db-1568">A Microsoft.Resource mostantól támogatja a 2019-05-10-es új api-verziót</span><span class="sxs-lookup"><span data-stu-id="773db-1568">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="773db-1569">Mostantól támogatott a copy.count = 0 a változók, erőforrások és tulajdonságok esetében</span><span class="sxs-lookup"><span data-stu-id="773db-1569">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="773db-1570">A condition = false vagy copy.count = 0 tulajdonságú erőforrások teljes módban törölve lesznek</span><span class="sxs-lookup"><span data-stu-id="773db-1570">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="773db-1571">A súgódokumentációhoz hozzá lett adva egy példa a szabályzatok előfizetési szinten történő hozzárendeléséhez</span><span class="sxs-lookup"><span data-stu-id="773db-1571">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="773db-1572">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="773db-1572">Az.ServiceBus</span></span>
* <span data-ttu-id="773db-1573">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNetworkRule paraméter a Set-AzServiceBusNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="773db-1573">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="773db-1574">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="773db-1574">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="773db-1575">Új Test-AzServiceBusNameAvailability parancs lett hozzáadva annak ellenőrzésére, hogy az üzenetsor és a témakör neve elérhető-e</span><span class="sxs-lookup"><span data-stu-id="773db-1575">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="773db-1576">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="773db-1576">Az.ServiceFabric</span></span>
* <span data-ttu-id="773db-1577">Ki lettek javítva a csomóponttípus-hozzáadási parancsmag hibái:</span><span class="sxs-lookup"><span data-stu-id="773db-1577">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="773db-1578">NullReferenceException hiba történt, ha az erőforráscsoport más, a Service Fabric-fürthöz nem kapcsolódó VMSS-sel rendelkezett.</span><span class="sxs-lookup"><span data-stu-id="773db-1578">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="773db-1579">Kijavított hiba: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="773db-1579">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="773db-1580">Ki lett javítva egy hiba, amely miatt a parancsmag futása meghiúsult, ha a virtualNetwork a fürttől eltérő erőforráscsoportban volt.</span><span class="sxs-lookup"><span data-stu-id="773db-1580">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="773db-1581">kijavított hiba: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="773db-1581">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="773db-1582">Az Add-AzServiceFabricApplicationCertificate parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="773db-1582">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="773db-1583">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-1583">Az.Sql</span></span>
* <span data-ttu-id="773db-1584">Frissült a régi naplózási parancsmagok dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="773db-1584">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="773db-1585">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="773db-1585">Az.Storage</span></span>
* <span data-ttu-id="773db-1586">A Get/Close-AzStorageFileHandle súgója további parancsmagpélda-forgatókönyvek hozzáadásával és a paraméterek leírásának frissítésével változott</span><span class="sxs-lookup"><span data-stu-id="773db-1586">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="773db-1587">A StandardBlobTier mostantól támogatott a blobfeltöltési és -másolási műveletekhez</span><span class="sxs-lookup"><span data-stu-id="773db-1587">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="773db-1588">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="773db-1588">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="773db-1589">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="773db-1589">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="773db-1590">A rehidratálás prioritása mostantól támogatott a blobmásoláskor</span><span class="sxs-lookup"><span data-stu-id="773db-1590">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="773db-1591">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="773db-1591">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="773db-1592">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="773db-1592">Az.Websites</span></span>
* <span data-ttu-id="773db-1593">Magyarázat hozzáadva a Set-AzWebApp és a Set-AzWebAppSlot parancsmagok -AppSettings paraméteréhez</span><span class="sxs-lookup"><span data-stu-id="773db-1593">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="773db-1594">2.5.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="773db-1594">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="773db-1595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="773db-1595">Az.Accounts</span></span>
* <span data-ttu-id="773db-1596">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="773db-1596">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="773db-1597">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="773db-1597">Az.ApplicationInsights</span></span>
* <span data-ttu-id="773db-1598">A Remove-AzApplicationInsightsApiKey dokumentáció példájában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="773db-1598">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="773db-1599">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="773db-1599">Az.Automation</span></span>
* <span data-ttu-id="773db-1600">Az erőforrássztringben található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="773db-1600">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="773db-1601">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="773db-1601">Az.CognitiveServices</span></span>
* <span data-ttu-id="773db-1602">NetworkRuleSet támogatás hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="773db-1602">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="773db-1603">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-1603">Az.Compute</span></span>
* <span data-ttu-id="773db-1604">A virtuálisgép-példány nézetobjektumaiból hiányzó tulajdonságok (ComputerName, OsName, OsVersion és HyperVGeneration) hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="773db-1604">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="773db-1605">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="773db-1605">Az.ContainerRegistry</span></span>
* <span data-ttu-id="773db-1606">A Remove-AzContainerRegistryReplication Replikáció paraméterében lévő elírás javítása</span><span class="sxs-lookup"><span data-stu-id="773db-1606">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="773db-1607">További információ: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="773db-1607">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="773db-1608">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="773db-1608">Az.DataFactory</span></span>
* <span data-ttu-id="773db-1609">Az ADF .Net SDK a 4.1.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="773db-1609">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="773db-1610">A Get-AzDataFactoryV2PipelineRun dokumentációjában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="773db-1610">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="773db-1611">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="773db-1611">Az.EventHub</span></span>
* <span data-ttu-id="773db-1612">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="773db-1612">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="773db-1613">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="773db-1613">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="773db-1614">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="773db-1614">Az.KeyVault</span></span>
* <span data-ttu-id="773db-1615">A KeySize tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="773db-1615">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="773db-1616">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="773db-1616">Az.LogicApp</span></span>
* <span data-ttu-id="773db-1617">A Get-AzIntegrationAccountMap javítása, hogy minden leképezéstípust listázzon</span><span class="sxs-lookup"><span data-stu-id="773db-1617">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="773db-1618">Új MapType paraméter hozzáadva a szűréshez</span><span class="sxs-lookup"><span data-stu-id="773db-1618">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="773db-1619">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="773db-1619">Az.ManagedServices</span></span>
* <span data-ttu-id="773db-1620">Az API 2019. 06. 01-én kiadott (GA) verziójának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-1620">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="773db-1621">Az.Network</span><span class="sxs-lookup"><span data-stu-id="773db-1621">Az.Network</span></span>
* <span data-ttu-id="773db-1622">A privát végpont és privát kapcsolatszolgáltatás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-1622">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="773db-1623">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="773db-1623">New cmdlets</span></span>
        - <span data-ttu-id="773db-1624">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="773db-1624">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="773db-1625">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="773db-1625">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="773db-1626">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="773db-1626">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="773db-1627">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="773db-1627">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="773db-1628">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="773db-1628">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="773db-1629">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="773db-1629">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="773db-1630">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="773db-1630">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="773db-1631">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="773db-1631">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="773db-1632">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies jelző a VirtualNetwork alhálózatban</span><span class="sxs-lookup"><span data-stu-id="773db-1632">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="773db-1633">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig frissítve</span><span class="sxs-lookup"><span data-stu-id="773db-1633">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="773db-1634">Hozzá lett adva a -PrivateEndpointNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát végpont esetében.</span><span class="sxs-lookup"><span data-stu-id="773db-1634">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="773db-1635">Hozzá lett adva a -PrivateLinkServiceNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát kapcsolati szolgáltatás esetében.</span><span class="sxs-lookup"><span data-stu-id="773db-1635">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="773db-1636">Az AzPrivateLinkService parancsmag ServiceName paramétere átnevezve a Name névre a ServiceName aliasszal a visszamenőleges kompatibilitás érdekében</span><span class="sxs-lookup"><span data-stu-id="773db-1636">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="773db-1637">ICMP-protokoll engedélyezése a hálózati biztonsági szabályzati konfigurációkhoz</span><span class="sxs-lookup"><span data-stu-id="773db-1637">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="773db-1638">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="773db-1638">Updated cmdlets</span></span>
        - <span data-ttu-id="773db-1639">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="773db-1639">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="773db-1640">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="773db-1640">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="773db-1641">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="773db-1641">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="773db-1642">A ConnectionProtocolType (Ikev1/Ikev2) hozzáadva a New-AzVirtualNetworkGatewayConnection konfigurálható paramétereként</span><span class="sxs-lookup"><span data-stu-id="773db-1642">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="773db-1643">PrivateIpAddressVersion hozzáadva a LoadBalancerFrontendIpConfigurationhöz</span><span class="sxs-lookup"><span data-stu-id="773db-1643">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="773db-1644">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="773db-1644">Updated cmdlet:</span></span>
        - <span data-ttu-id="773db-1645">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="773db-1645">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="773db-1646">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="773db-1646">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="773db-1647">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="773db-1647">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="773db-1648">Application Gateway New-AzApplicationGatewayProbeConfig parancs frissítése a mintavétel egyéni portjának támogatásához</span><span class="sxs-lookup"><span data-stu-id="773db-1648">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="773db-1649">Frissített New-AzApplicationGatewayProbeConfig: A Port opcionális paraméter hozzáadva, amelyet a rendszer a háttérrendszer-kiszolgáló mintavételére használ.</span><span class="sxs-lookup"><span data-stu-id="773db-1649">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="773db-1650">Ez a paraméter a Standard_V2 és WAF_V2 termékváltozatokban használható.</span><span class="sxs-lookup"><span data-stu-id="773db-1650">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="773db-1651">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="773db-1651">Az.OperationalInsights</span></span>
* <span data-ttu-id="773db-1652">A mentett keresések alapértelmezett verziója 1 értékre frissítve.</span><span class="sxs-lookup"><span data-stu-id="773db-1652">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="773db-1653">Null reguláris kifejezések kezelése javítva az egyéni naplókban</span><span class="sxs-lookup"><span data-stu-id="773db-1653">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="773db-1654">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="773db-1654">Az.RecoveryServices</span></span>
* <span data-ttu-id="773db-1655">A Get-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="773db-1655">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="773db-1656">A Get-AzRecoveryServicesBackupContainer.md frissítése</span><span class="sxs-lookup"><span data-stu-id="773db-1656">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="773db-1657">A Get-AzRecoveryServicesVault.md frissítése</span><span class="sxs-lookup"><span data-stu-id="773db-1657">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="773db-1658">A Wait-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="773db-1658">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="773db-1659">A Set-AzRecoveryServicesVaultContext.md frissítése</span><span class="sxs-lookup"><span data-stu-id="773db-1659">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="773db-1660">A Get-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="773db-1660">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="773db-1661">A Get-AzRecoveryServicesBackupRecoveryPoint.md frissítése</span><span class="sxs-lookup"><span data-stu-id="773db-1661">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="773db-1662">A Restore-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="773db-1662">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="773db-1663">A tároló Azure-fájlmegosztásban való regisztrációjának törlésére szolgáló szolgáltatáshívás frissítése</span><span class="sxs-lookup"><span data-stu-id="773db-1663">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="773db-1664">A Set-AzRecoveryServicesAsrAlertSetting.md frissítése</span><span class="sxs-lookup"><span data-stu-id="773db-1664">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="773db-1665">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-1665">Az.Resources</span></span>
- <span data-ttu-id="773db-1666">A New-AzResourceGroupDeployment dokumentációban hivatkozott hiányzó parancsmag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="773db-1666">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="773db-1667">A szabályzat parancsmagjai frissítve a 2019. 01. 01. dátumú új API-verzió használatára</span><span class="sxs-lookup"><span data-stu-id="773db-1667">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="773db-1668">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="773db-1668">Az.ServiceBus</span></span>
* <span data-ttu-id="773db-1669">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="773db-1669">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="773db-1670">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="773db-1670">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="773db-1671">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-1671">Az.Sql</span></span>
* <span data-ttu-id="773db-1672">A Set-AzSqlDatabaseSecondary parancsmag hiányzó példáinak javítása</span><span class="sxs-lookup"><span data-stu-id="773db-1672">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="773db-1673">A biztonságirés-felmérés e-mail-cím megadása nélkül beállított ismétlődő vizsgálatának javítása</span><span class="sxs-lookup"><span data-stu-id="773db-1673">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="773db-1674">Egy kis elírás javítása egy figyelmeztető üzenetben.</span><span class="sxs-lookup"><span data-stu-id="773db-1674">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="773db-1675">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="773db-1675">Az.Storage</span></span>
* <span data-ttu-id="773db-1676">A Get-AzStorageAccount hivatkozási dokumentációjában található példa frissítése a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="773db-1676">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="773db-1677">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="773db-1677">Az.StorageSync</span></span>
* <span data-ttu-id="773db-1678">Az Invoke-AzStorageSyncChangeDetection parancsmag hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="773db-1678">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="773db-1679">A 9551-es hiba javítása a TierFilesOlderThanDays betartásához</span><span class="sxs-lookup"><span data-stu-id="773db-1679">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="773db-1680">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="773db-1680">Az.Websites</span></span>
* <span data-ttu-id="773db-1681">A hiba elhárítása, amely miatt a Get-AzWebApp és a Set-AzWebApp nem adott vissza egyes SiteConfig tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="773db-1681">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="773db-1682">Egy új Location paraméter hozzáadása a Get-AzDeletedWebApp és a Restore-AzDeletedWebApp parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="773db-1682">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="773db-1683">A webalkalmazás-tárhelyek New-AzWebApp -IncludeSourceWebAppSlots használatával történő klónozásakor jelentkező hiba javítása</span><span class="sxs-lookup"><span data-stu-id="773db-1683">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="773db-1684">2.4.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="773db-1684">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="773db-1685">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="773db-1685">Az.Accounts</span></span>
* <span data-ttu-id="773db-1686">Profilparancsmagok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="773db-1686">Add support for profile cmdlets</span></span>
* <span data-ttu-id="773db-1687">A létrehozott parancsmagokban lévő környezetek és adatsíkok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="773db-1687">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="773db-1688">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen végpontot használt az adatsík parancsmagjaihoz Windows PowerShellben</span><span class="sxs-lookup"><span data-stu-id="773db-1688">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="773db-1689">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="773db-1689">Az.Advisor</span></span>
* <span data-ttu-id="773db-1690">Az Az.Advisor GA-kiadása</span><span class="sxs-lookup"><span data-stu-id="773db-1690">GA release of Az.Advisor</span></span>
* <span data-ttu-id="773db-1691">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="773db-1691">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="773db-1692">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="773db-1692">Az.ApiManagement</span></span>
* <span data-ttu-id="773db-1693">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="773db-1693">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="773db-1694">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="773db-1694">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="773db-1695">Előfizetések felhasználó és termék szerinti lekérdezésének támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-1695">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="773db-1696">„/”, „/apis”, „/apis/echo-api” hatókör használatával történő lekérdezés támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-1696">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="773db-1697">A következő hibák ki lettek javítva: https://github.com/Azure/azure-powershell/issues/9307 és https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="773db-1697">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="773db-1698">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="773db-1698">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="773db-1699">Az „ApiVersion” és az „ApiVersionSetId” megadhatóvá vált az API-k importálásakor</span><span class="sxs-lookup"><span data-stu-id="773db-1699">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="773db-1700">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="773db-1700">Az.Automation</span></span>
* <span data-ttu-id="773db-1701">A Set-AzAutomationConnectionFieldValue parancsmag sztringértékek kezelése esetén fellépő hibája javítva lett.</span><span class="sxs-lookup"><span data-stu-id="773db-1701">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="773db-1702">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-1702">Az.Compute</span></span>
* <span data-ttu-id="773db-1703">A HyperVGeneration paraméter hozzáadása a New-AzImageConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="773db-1703">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="773db-1704">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="773db-1704">Az.DataFactory</span></span>
* <span data-ttu-id="773db-1705">A tevékenység-, folyamat- és eseményindító-futtatási kimenetek lekérdezési ADF-parancsmagjainak frissítése a Select-Object folyamat támogatásához.</span><span class="sxs-lookup"><span data-stu-id="773db-1705">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="773db-1706">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="773db-1706">Az.EventGrid</span></span>
* <span data-ttu-id="773db-1707">Az elgépelés ki lett javítva a New-AzEventGridSubscription dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="773db-1707">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="773db-1708">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="773db-1708">Az.IotHub</span></span>
* <span data-ttu-id="773db-1709">Az engedélyezési szabályzati kulcsok újragenerálásának támogatása hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="773db-1709">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="773db-1710">Az.Network</span><span class="sxs-lookup"><span data-stu-id="773db-1710">Az.Network</span></span>
* <span data-ttu-id="773db-1711">A „RoutingPreference” hozzáadva a nyilvános IP-címkékhez</span><span class="sxs-lookup"><span data-stu-id="773db-1711">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="773db-1712">Javítottuk a példákat a „Get-AzNetworkServiceTag” referenciadokumentációban</span><span class="sxs-lookup"><span data-stu-id="773db-1712">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="773db-1713">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="773db-1713">Az.PolicyInsights</span></span>
* <span data-ttu-id="773db-1714">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyState parancsmagban</span><span class="sxs-lookup"><span data-stu-id="773db-1714">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="773db-1715">További információ: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="773db-1715">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="773db-1716">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="773db-1716">Az.OperationalInsights</span></span>
* <span data-ttu-id="773db-1717">Javítottuk a Get-AzOperationalInsightsDataSource parancsmagban visszaadott CustomLog adatforrásmodellt</span><span class="sxs-lookup"><span data-stu-id="773db-1717">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="773db-1718">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="773db-1718">Az.RecoveryServices</span></span>
* <span data-ttu-id="773db-1719">Az IaaSVMs get-policy parancsának javítása</span><span class="sxs-lookup"><span data-stu-id="773db-1719">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="773db-1720">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-1720">Az.Resources</span></span>
    - <span data-ttu-id="773db-1721">A Get-AzPolicyState -Top paraméter súgószövegének javítása</span><span class="sxs-lookup"><span data-stu-id="773db-1721">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="773db-1722">Ügyféloldali lapozás támogatásának hozzáadása a Get-AzPolicyAlias parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="773db-1722">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="773db-1723">Új (-PolicyParameters és -PolicyParametersObject) paraméterek hozzáadása a Set-AzPolicyAssignment parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="773db-1723">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="773db-1724">A Policy-parancsmagok néhány dokumentumának és példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="773db-1724">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="773db-1725">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="773db-1725">Az.ServiceBus</span></span>
* <span data-ttu-id="773db-1726">A 4938-as hiba javítása – A New-AzureRmServiceBusQueue parancsmag BadRequest értéket ad vissza a MaxSizeInMegabytes megadásakor</span><span class="sxs-lookup"><span data-stu-id="773db-1726">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="773db-1727">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-1727">Az.Sql</span></span>
* <span data-ttu-id="773db-1728">A példány-feladatátvételi csoportok parancsmagjainak hozzáadása az előzetes kiadásból a nyilvános kiadáshoz</span><span class="sxs-lookup"><span data-stu-id="773db-1728">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="773db-1729">Az Azure SQL Server\Database Auditing támogatása új parancsmagokkal.</span><span class="sxs-lookup"><span data-stu-id="773db-1729">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="773db-1730">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="773db-1730">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="773db-1731">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="773db-1731">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="773db-1732">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="773db-1732">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="773db-1733">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="773db-1733">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="773db-1734">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="773db-1734">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="773db-1735">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="773db-1735">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="773db-1736">E-mailes korlátozások eltávolítása a sebezhetőségi felmérés beállításaiból</span><span class="sxs-lookup"><span data-stu-id="773db-1736">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="773db-1737">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="773db-1737">Az.Storage</span></span>
* <span data-ttu-id="773db-1738">Az „-IndexDocument” és „-ErrorDocument404Path” paraméter módosítása kötelezőről opcionálisra a következő parancsmagban:</span><span class="sxs-lookup"><span data-stu-id="773db-1738">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="773db-1739">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="773db-1739">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="773db-1740">A Get-AzStorageBlobContent súgójának frissítése egy példa hozzáadásával</span><span class="sxs-lookup"><span data-stu-id="773db-1740">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="773db-1741">További hibaadatok megjelenítése, ha a parancsmag futtatása StorageException miatt meghiúsul</span><span class="sxs-lookup"><span data-stu-id="773db-1741">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="773db-1742">Storage-fiók létrehozásának és frissítésének támogatása Azure Files AAD DS-hitelesítéssel</span><span class="sxs-lookup"><span data-stu-id="773db-1742">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="773db-1743">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="773db-1743">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="773db-1744">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="773db-1744">Set-AzStorageAccount</span></span>
* <span data-ttu-id="773db-1745">Támogatás a fájlmegosztások, fájlkönyvtárak vagy fájlok fájlleíróinak listázásához vagy bezárásához</span><span class="sxs-lookup"><span data-stu-id="773db-1745">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="773db-1746">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="773db-1746">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="773db-1747">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="773db-1747">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="773db-1748">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="773db-1748">Az.StorageSync</span></span>
* <span data-ttu-id="773db-1749">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="773db-1749">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="773db-1750">2.3.2 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="773db-1750">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="773db-1751">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="773db-1751">Az.Accounts</span></span>
* <span data-ttu-id="773db-1752">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen URL-címeket használt a Functions-hívásokhoz</span><span class="sxs-lookup"><span data-stu-id="773db-1752">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="773db-1753">További információ: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="773db-1753">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="773db-1754">Javítva lett az aliasok hibája az AzureRM–Az parancsmagok közötti átvitel esetében</span><span class="sxs-lookup"><span data-stu-id="773db-1754">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="773db-1755">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="773db-1755">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="773db-1756">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="773db-1756">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="773db-1757">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-1757">Az.Compute</span></span>
* <span data-ttu-id="773db-1758">A „New-AzVm” és „New-AzVmss” egyszerű paraméterkészletek mostantól elfogadják a „ProximityPlacementGroup” paramétert.</span><span class="sxs-lookup"><span data-stu-id="773db-1758">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="773db-1759">Az elgépelés ki lett javítva a „New-AzVM” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="773db-1759">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="773db-1760">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="773db-1760">Az.Dns</span></span>
* <span data-ttu-id="773db-1761">Az elgépelés ki lett javítva a „Set-AzDnsZone” súgópéldáinál.</span><span class="sxs-lookup"><span data-stu-id="773db-1761">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="773db-1762">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="773db-1762">Az.EventGrid</span></span>
* <span data-ttu-id="773db-1763">Frissítve a 2019-06-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="773db-1763">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="773db-1764">Új parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="773db-1764">New cmdlets:</span></span>
    - <span data-ttu-id="773db-1765">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="773db-1765">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="773db-1766">Létrehoz egy új Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="773db-1766">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="773db-1767">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="773db-1767">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="773db-1768">Lekéri egy Event Grid-tartomány részleteit, vagy az aktuális Azure-előfizetéshez tartozó összes Event Grid-tartomány listáját.</span><span class="sxs-lookup"><span data-stu-id="773db-1768">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="773db-1769">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="773db-1769">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="773db-1770">Eltávolít egy Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="773db-1770">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="773db-1771">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="773db-1771">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="773db-1772">Újra létrehozza a megosztott hozzáférési kulcsot az Azure Event Grid-tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="773db-1772">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="773db-1773">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="773db-1773">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="773db-1774">Lekéri az Event Grid-tartományban való esemény-közzétételhez használt megosztott hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="773db-1774">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="773db-1775">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="773db-1775">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="773db-1776">Új Azure Event Grid-tartományi témakört hoz létre.</span><span class="sxs-lookup"><span data-stu-id="773db-1776">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="773db-1777">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="773db-1777">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="773db-1778">Lekéri egy Event Grid-tartományi témakör részleteit, vagy az aktuális Azure-előfizetés adott Event Grid-tartományához tartozó Event Grid-tartományi témakörök listáját</span><span class="sxs-lookup"><span data-stu-id="773db-1778">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="773db-1779">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="773db-1779">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="773db-1780">Eltávolít egy meglévő Azure Event Grid-tartományi témakört.</span><span class="sxs-lookup"><span data-stu-id="773db-1780">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="773db-1781">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="773db-1781">Updated cmdlets:</span></span>
    - <span data-ttu-id="773db-1782">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="773db-1782">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="773db-1783">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="773db-1783">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="773db-1784">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="773db-1784">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="773db-1785">Új paraméterkészletek lettek hozzáadva tartományok és tartományi témakörök esetében, lehetővé téve a meglévő paraméterek (például EndPointType, SubjectBeginsWith stb.) újbóli felhasználását.</span><span class="sxs-lookup"><span data-stu-id="773db-1785">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="773db-1786">Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="773db-1786">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="773db-1787">Esemény-előfizetés lejárati dátuma,</span><span class="sxs-lookup"><span data-stu-id="773db-1787">Event subscription expiration date,</span></span>
            - <span data-ttu-id="773db-1788">Speciális szűrési paraméterek.</span><span class="sxs-lookup"><span data-stu-id="773db-1788">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="773db-1789">Új felsorolási érték lett hozzáadva a servicebusqueue elem célértékeként.</span><span class="sxs-lookup"><span data-stu-id="773db-1789">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="773db-1790">Nem engedélyezett az -IncludedEventType beállításnál az „All” érték használata és a következővel való helyettesítése:</span><span class="sxs-lookup"><span data-stu-id="773db-1790">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="773db-1791">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="773db-1791">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="773db-1792">Új opcionális paraméterek (Top, ODataQuery és NextLink) az eredmények tördelésének és szűrésének támogatásához.</span><span class="sxs-lookup"><span data-stu-id="773db-1792">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="773db-1793">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="773db-1793">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="773db-1794">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="773db-1794">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="773db-1795">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="773db-1795">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="773db-1796">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="773db-1796">Az.FrontDoor</span></span>
* <span data-ttu-id="773db-1797">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="773db-1797">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="773db-1798">Hozzá lett adva az átalakítások támogatása és az új operátorértékek automatikus kitöltése (RegEx)</span><span class="sxs-lookup"><span data-stu-id="773db-1798">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="773db-1799">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="773db-1799">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="773db-1800">Hozzá lett adva az új értékek automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="773db-1800">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="773db-1801">Az.Network</span><span class="sxs-lookup"><span data-stu-id="773db-1801">Az.Network</span></span>
* <span data-ttu-id="773db-1802">Virtuális hálózati átjárók erőforrás-támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-1802">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="773db-1803">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="773db-1803">New cmdlets</span></span>
        - <span data-ttu-id="773db-1804">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="773db-1804">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="773db-1805">AvailablePrivateEndpointType hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-1805">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="773db-1806">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="773db-1806">New cmdlets</span></span>
        - <span data-ttu-id="773db-1807">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="773db-1807">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="773db-1808">PrivatePrivateLinkService hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-1808">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="773db-1809">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="773db-1809">New cmdlets</span></span>
        - <span data-ttu-id="773db-1810">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="773db-1810">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="773db-1811">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="773db-1811">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="773db-1812">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="773db-1812">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="773db-1813">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="773db-1813">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="773db-1814">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="773db-1814">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="773db-1815">PrivateEndpoint hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-1815">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="773db-1816">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="773db-1816">New cmdlets</span></span>
        - <span data-ttu-id="773db-1817">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="773db-1817">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="773db-1818">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="773db-1818">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="773db-1819">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="773db-1819">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="773db-1820">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="773db-1820">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="773db-1821">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: UseLocalAzureIpAddress jelző a VpnConnection elemen</span><span class="sxs-lookup"><span data-stu-id="773db-1821">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="773db-1822">Frissítve lett a New-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="773db-1822">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="773db-1823">Frissítve lett a Set-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="773db-1823">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="773db-1824">Hozzá lett adva az írásvédett PeeredConnections mező az ExpressRoute-társhálózatlétesítések esetében.</span><span class="sxs-lookup"><span data-stu-id="773db-1824">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="773db-1825">Hozzá lett adva az írásvédett GlobalReachEnabled mező az ExpressRoute esetében.</span><span class="sxs-lookup"><span data-stu-id="773db-1825">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="773db-1826">Kompatibilitástörő változást okozó attribútum lett hozzáadva, amely jelzi az AllowGlobalReach mező elavulását az ExpressRouteCircuit-modellben</span><span class="sxs-lookup"><span data-stu-id="773db-1826">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="773db-1827">Javítva lett a 8756-os hiba a TargetListenerID AzApplicationGatewayRedirectConfiguration-parancsmagokkal való használata során</span><span class="sxs-lookup"><span data-stu-id="773db-1827">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="773db-1828">Javítva lett a hiba a New-AzApplicationGatewayPathRuleConfig parancsmagban, amely megakadályozta az átírási szabálykészlet beállítását.</span><span class="sxs-lookup"><span data-stu-id="773db-1828">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="773db-1829">Javítva lett a VirtualNetworkTaps megjelenítése a NetworkInterfaceIpConfiguration esetében</span><span class="sxs-lookup"><span data-stu-id="773db-1829">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="773db-1830">Javítva lettek a Cortex Get-parancsmagok az összes rész felsorolásához</span><span class="sxs-lookup"><span data-stu-id="773db-1830">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="773db-1831">Javítva lett a VirtualHub-hivatkozás létrehozása az ExpressRouteGateways, VpnGateway esetében</span><span class="sxs-lookup"><span data-stu-id="773db-1831">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="773db-1832">Hozzá lett adva a rendelkezésreállási zónák támogatása az AzureFirewall és a NatGateway esetében</span><span class="sxs-lookup"><span data-stu-id="773db-1832">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="773db-1833">Hozzá lett adva a Get-AzNetworkServiceTag parancsmag</span><span class="sxs-lookup"><span data-stu-id="773db-1833">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="773db-1834">Hozzá lett adva a több nyilvános IP-cím támogatása az Azure Firewall esetében</span><span class="sxs-lookup"><span data-stu-id="773db-1834">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="773db-1835">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="773db-1835">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="773db-1836">Hozzá lett adva a -PublicIpAddress paraméter, amely egy vagy több nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="773db-1836">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="773db-1837">Hozzá lett adva a -VirtualNetwork paraméter, amely virtuális hálózati objektumokat fogad el</span><span class="sxs-lookup"><span data-stu-id="773db-1837">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="773db-1838">Hozzá lett adva az AddPublicIpAddress és RemovePublicIpAddress metódus a tűzfalobjektumok esetében, és nyilvános IP-cím-objektumokat fogadnak el bemeneti adatként</span><span class="sxs-lookup"><span data-stu-id="773db-1838">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="773db-1839">Elavult a -PublicIpName és a -VirtualNetworkName paraméter</span><span class="sxs-lookup"><span data-stu-id="773db-1839">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="773db-1840">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: VpnClient AAD-alapú hitelesítési beállítások megadása a virtuális hálózati átjárók erőforrásaihoz.</span><span class="sxs-lookup"><span data-stu-id="773db-1840">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="773db-1841">Frissült a New-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="773db-1841">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="773db-1842">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="773db-1842">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="773db-1843">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva a RemoveAadAuthentication opcionális kapcsolóparaméter a VpnClient AAD-alapú hitelesítési beállítások eltávolításához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="773db-1843">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="773db-1844">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="773db-1844">Az.OperationalInsights</span></span>
* <span data-ttu-id="773db-1845">Engedélyezve lett a **pergb2018** tarifacsomag a „New-AzureRmOperationalInsightsWorkspace” parancs esetében</span><span class="sxs-lookup"><span data-stu-id="773db-1845">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="773db-1846">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-1846">Az.Resources</span></span>
* <span data-ttu-id="773db-1847">További sablonexportálási beállítások támogatása</span><span class="sxs-lookup"><span data-stu-id="773db-1847">Support for additional Template Export options</span></span>
    - <span data-ttu-id="773db-1848">Hozzá lett adva a „-SkipResourceNameParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="773db-1848">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="773db-1849">Hozzá lett adva a „-SkipAllParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="773db-1849">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="773db-1850">Hozzá lett adva a „-Resource” paraméter az Export-AzResourceGroup esetében az exportált erőforrások szűréséhez</span><span class="sxs-lookup"><span data-stu-id="773db-1850">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="773db-1851">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="773db-1851">Az.ServiceFabric</span></span>
* <span data-ttu-id="773db-1852">Ki lett javítva az a hiba, hogy a ByExistingKeyVault tanúsítvány hozzáadása bizonyos esetekben helytelen ujjlenyomatot kért le</span><span class="sxs-lookup"><span data-stu-id="773db-1852">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="773db-1853">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-1853">Az.Sql</span></span>
* <span data-ttu-id="773db-1854">Javítva lett az Advanced Threat Protection Storage-végpontjának utótagja</span><span class="sxs-lookup"><span data-stu-id="773db-1854">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="773db-1855">Javítva lett, hogy az Advanced Data Security engedélyezése felülbírálja az Advanced Threat Protection-szabályzatot</span><span class="sxs-lookup"><span data-stu-id="773db-1855">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="773db-1856">Új parancsmagok lettek hozzáadva a Management.Sql esetében, amelyek lehetővé teszik az ügyfelek számára TDE-kulcsok hozzáadását és TDE-védő beállítását a felügyelt példányokhoz</span><span class="sxs-lookup"><span data-stu-id="773db-1856">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="773db-1857">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="773db-1857">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="773db-1858">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="773db-1858">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="773db-1859">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="773db-1859">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="773db-1860">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="773db-1860">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="773db-1861">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="773db-1861">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="773db-1862">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="773db-1862">Az.Storage</span></span>
* <span data-ttu-id="773db-1863">A FileStorage és az SkuName Premium_ZRS altípus támogatása Storage-fiókok létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="773db-1863">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="773db-1864">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="773db-1864">New-AzStorageAccount</span></span>
* <span data-ttu-id="773db-1865">Egyértelműsítve lett a blobmódosíthatatlansági parancsmag leírása</span><span class="sxs-lookup"><span data-stu-id="773db-1865">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="773db-1866">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="773db-1866">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="773db-1867">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="773db-1867">Az.Websites</span></span>
* <span data-ttu-id="773db-1868">Optimalizálva lett a Get-AzWebAppCertificate parancsmag, hogy erőforráscsoport szerint szűrjön a kiszolgálón, ne ügyfél szerint</span><span class="sxs-lookup"><span data-stu-id="773db-1868">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="773db-1869">Hozzá lett adva a -UseDisasterRecovery kapcsolóparaméter a Get-AzWebAppSnapshot parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="773db-1869">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="773db-1870">2.2.0 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="773db-1870">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="773db-1871">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="773db-1871">Az.Cdn</span></span>
* <span data-ttu-id="773db-1872">Frissített parancsmagok a rulesEngine szolgáltatás támogatásához a 2019. 04. 15. API-verzión</span><span class="sxs-lookup"><span data-stu-id="773db-1872">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="773db-1873">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-1873">Az.Compute</span></span>
* <span data-ttu-id="773db-1874">A `NoWait` paraméter hozzáadása, amely elindítja a műveletet, és azonnal visszatér, még a művelet befejezése előtt.</span><span class="sxs-lookup"><span data-stu-id="773db-1874">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="773db-1875">Frissített parancsmagok:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="773db-1875">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="773db-1876">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="773db-1876">Az.EventHub</span></span>
* <span data-ttu-id="773db-1877">A 9231-es hiba javítása – a Get-AzEventHubNamespace nem ad vissza címkéket</span><span class="sxs-lookup"><span data-stu-id="773db-1877">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="773db-1878">A 9230-as hiba javítása – a Get-AzEventHubNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="773db-1878">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="773db-1879">Az.Network</span><span class="sxs-lookup"><span data-stu-id="773db-1879">Az.Network</span></span>
* <span data-ttu-id="773db-1880">ResourceID és InputObject frissítése a Nat-átjárón</span><span class="sxs-lookup"><span data-stu-id="773db-1880">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="773db-1881">ResourceID és InputObject aliasának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="773db-1881">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="773db-1882">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="773db-1882">Az.PolicyInsights</span></span>
* <span data-ttu-id="773db-1883">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyEvent parancsmagban</span><span class="sxs-lookup"><span data-stu-id="773db-1883">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="773db-1884">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="773db-1884">Az.RecoveryServices</span></span>
* <span data-ttu-id="773db-1885">Az IaaSVM szabályzat minimális megőrzési ideje 7 napról 1-re módosult</span><span class="sxs-lookup"><span data-stu-id="773db-1885">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="773db-1886">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="773db-1886">Az.ServiceBus</span></span>
* <span data-ttu-id="773db-1887">A 9182-es hiba javítása – a Get-AzServiceBusNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="773db-1887">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="773db-1888">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="773db-1888">Az.ServiceFabric</span></span>
* <span data-ttu-id="773db-1889">Az Update-AzServiceFabricReliability hibaüzenetében lévő gépelési hiba kijavítása</span><span class="sxs-lookup"><span data-stu-id="773db-1889">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="773db-1890">A Service Fabric parancssorok hiányzó karakterének pótlása</span><span class="sxs-lookup"><span data-stu-id="773db-1890">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="773db-1891">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-1891">Az.Sql</span></span>
* <span data-ttu-id="773db-1892">A DnsZonePartner paraméter hozzáadása a New-AzureSqlInstance parancsmaghoz az AutoDr képesség a felügyelt példányon való támogatásához.</span><span class="sxs-lookup"><span data-stu-id="773db-1892">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="773db-1893">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag kivezetése</span><span class="sxs-lookup"><span data-stu-id="773db-1893">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="773db-1894">Threat Detection parancsmagok átnevezése Advanced Threat Protection névre</span><span class="sxs-lookup"><span data-stu-id="773db-1894">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="773db-1895">A New-AzSqlInstance, - StorageSizeInGB és - LicenseType paraméterek mostantól nem kötelezőek.</span><span class="sxs-lookup"><span data-stu-id="773db-1895">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="773db-1896">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="773db-1896">Az.Websites</span></span>
* <span data-ttu-id="773db-1897">javítja azt a hibát, amely miatt a Set-AzWebApp és a Set-AzWebAppSlot a -WebApp tulajdonsággal való használata eltávolította a címkéket</span><span class="sxs-lookup"><span data-stu-id="773db-1897">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="773db-1898">2.1.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="773db-1898">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="773db-1899">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="773db-1899">Az.ApiManagement</span></span>
* <span data-ttu-id="773db-1900">Új parancsmagok a globális és API-szintű diagnosztika kezeléshez</span><span class="sxs-lookup"><span data-stu-id="773db-1900">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="773db-1901">**Get-AzApiManagementDiagnostic** – A globális vagy API hatókörre konfigurált diagnosztika beolvasása</span><span class="sxs-lookup"><span data-stu-id="773db-1901">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="773db-1902">**New-AzApiManagementDiagnostic** – Új diagnosztika létrehozása a globális vagy API szintű hatókörhöz</span><span class="sxs-lookup"><span data-stu-id="773db-1902">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="773db-1903">**New-AzApiManagementHttpMessageDiagnostic** – Diagnosztikai beállítás létrehozása arra vonatkozóan, hogy mely fejléceknél naplózzon a rendszer, és mekkora legyen a törzs mérete bájtban</span><span class="sxs-lookup"><span data-stu-id="773db-1903">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="773db-1904">**New-AzApiManagementPipelineDiagnosticSetting** – Diagnosztikai beállítások létrehozása az átjáróra érkező és onnan induló HTTP-üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="773db-1904">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="773db-1905">**New-AzApiManagementSamplingSetting** – Mintavételezési beállítások létrehozása diagnosztikai kérésekhez/válaszokhoz</span><span class="sxs-lookup"><span data-stu-id="773db-1905">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="773db-1906">**Remove-AzApiManagementDiagnostic** – Diagnosztikai entitás eltávolítása globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="773db-1906">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="773db-1907">**Set-AzApiManagementDiagnostic** – Diagnosztikai entitás frissítése globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="773db-1907">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="773db-1908">Új parancsmagok az ApiManagement szolgáltatás gyorsítótárának kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="773db-1908">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="773db-1909">**Get-AzApiManagementCache** – Az azonosító által megadott vagy az összes gyorsítótár részleteinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="773db-1909">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="773db-1910">**New-AzApiManagementCache** – Új alapértelmezett gyorsítótár létrehozása vagy gyorsítótár létrehozása adott Azure-régióban</span><span class="sxs-lookup"><span data-stu-id="773db-1910">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="773db-1911">**Remove-AzApiManagementCache** – Gyorsítótár eltávolítása</span><span class="sxs-lookup"><span data-stu-id="773db-1911">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="773db-1912">**Update-AzApiManagementCache** – Gyorsítótár frissítése</span><span class="sxs-lookup"><span data-stu-id="773db-1912">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="773db-1913">Új parancsmagok az API-séma kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="773db-1913">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="773db-1914">**New-AzApiManagementSchema** – Új séma létrehozása egy API-hoz</span><span class="sxs-lookup"><span data-stu-id="773db-1914">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="773db-1915">**Get-AzApiManagementSchema** – Az API-ban konfigurált sémák beolvasása</span><span class="sxs-lookup"><span data-stu-id="773db-1915">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="773db-1916">**Remove-AzApiManagementSchema** – Az API-ban konfigurált sémák eltávolítása</span><span class="sxs-lookup"><span data-stu-id="773db-1916">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="773db-1917">**Set-AzApiManagementSchema** – Az API-ban konfigurált séma frissítése</span><span class="sxs-lookup"><span data-stu-id="773db-1917">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="773db-1918">Új parancsmag a felhasználói jogkivonat létrehozásához</span><span class="sxs-lookup"><span data-stu-id="773db-1918">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="773db-1919">**New-AzApiManagementUserToken** – Új, alapértelmezés szerint 8 órán át érvényes felhasználói jogkivonat létrehozása. Ezen parancsmag használatával lehet a „GIT” felhasználó számára jogkivonatot létrehozni.</span><span class="sxs-lookup"><span data-stu-id="773db-1919">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="773db-1920">Új parancsmag a hálózat állapotának lekérdezéséhez</span><span class="sxs-lookup"><span data-stu-id="773db-1920">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="773db-1921">**Get-AzApiManagementNetworkStatus** – Azon erőforrások hálózati állapotának beolvasása, amelyektől az API Management szolgáltatás függ.</span><span class="sxs-lookup"><span data-stu-id="773db-1921">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="773db-1922">Ez hasznos lehet, ha az ApiManagement szolgáltatást virtuális hálózatra telepíti, és ellenőrizni kell, hogy rendben működnek-e a függőségek.</span><span class="sxs-lookup"><span data-stu-id="773db-1922">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="773db-1923">A **New-AzApiManagement** parancsmag frissítése az ApiManagement szolgáltatás kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="773db-1923">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="773db-1924">Mostantól az új „Consumption” SKU is támogatott</span><span class="sxs-lookup"><span data-stu-id="773db-1924">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="773db-1925">Mostantól az „EnableClientCertificate” jelző a „Consumption” SKU-hoz is bekapcsolható</span><span class="sxs-lookup"><span data-stu-id="773db-1925">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="773db-1926">Az új **New-AzApiManagementSslSetting** parancsmag lehetővé teszi a „TLS/SSL” beállítás konfigurálását a „Háttér” és „Előtér” esetén is.</span><span class="sxs-lookup"><span data-stu-id="773db-1926">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="773db-1927">Ez egy ApiManagement szolgáltatás előterén a titkosítások, mint például a 3DES, valamint a szerverprotokollok, mint például a Http2 konfigurálására is alkalmas.</span><span class="sxs-lookup"><span data-stu-id="773db-1927">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="773db-1928">Mostantól támogatott a „DeveloperPortal” gazdanév ApiManagement szolgáltatáson történő konfigurálása.</span><span class="sxs-lookup"><span data-stu-id="773db-1928">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="773db-1929">A **Get-AzApiManagementSsoToken** parancsmagok frissítése a „PsApiManagement” objektum bemenetként való használatához</span><span class="sxs-lookup"><span data-stu-id="773db-1929">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="773db-1930">A parancsmag frissítése a hibaüzenetek beágyazott megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="773db-1930">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="773db-1931">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hibakód: ValidationError Hibaüzenet: Egy vagy több mező hibás értéket tartalmaz: Hiba részletei:    [Kód=ValidationError, Üzenet=Hiba a log-to-eventhub elemben, 3. sor, 10. oszlop: A naplózó nem található, Cél=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="773db-1931">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="773db-1932">Az **Export-AzApiManagementApi** parancsmag frissítse az API-k OpenApi 3.0 formátumban való exportálásához</span><span class="sxs-lookup"><span data-stu-id="773db-1932">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="773db-1933">Az **Import-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="773db-1933">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="773db-1934">API importálása az OpenApi 3.0 dokumentumspecifikációból</span><span class="sxs-lookup"><span data-stu-id="773db-1934">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="773db-1935">A bármely (Swagger, Wadl, Wsdl, OpenAPI) dokumentumban megadott PsApiManagementSchema tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="773db-1935">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="773db-1936">A bármely dokumentumban megadott ServiceUrl tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="773db-1936">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="773db-1937">A **Get-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) való visszaadásához</span><span class="sxs-lookup"><span data-stu-id="773db-1937">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="773db-1938">A **Set-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) és XML-nek megfelelő feloldójeles formátumban (xml használatával) való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="773db-1938">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="773db-1939">A **New-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="773db-1939">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="773db-1940">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="773db-1940">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="773db-1941">API létrehozása ApiVersionSet tulajdonságban</span><span class="sxs-lookup"><span data-stu-id="773db-1941">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="773db-1942">API klónozása SourceApiId és SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="773db-1942">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="773db-1943">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="773db-1943">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="773db-1944">A **Set-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="773db-1944">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="773db-1945">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="773db-1945">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="773db-1946">API frissítése ApiVersionSet tulajdonságba</span><span class="sxs-lookup"><span data-stu-id="773db-1946">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="773db-1947">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="773db-1947">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="773db-1948">A **New-AzApiManagementRevision** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="773db-1948">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="773db-1949">Létező változat klónozása (címkék, termékek, műveletek és szabályzatok másolása) a SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="773db-1949">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="773db-1950">Az új változat a szülő ApiId értékét veszi át</span><span class="sxs-lookup"><span data-stu-id="773db-1950">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="773db-1951">ApiRevisionDescription biztosítása</span><span class="sxs-lookup"><span data-stu-id="773db-1951">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="773db-1952">A „ServiceUrl” felülírása API klónozáskor</span><span class="sxs-lookup"><span data-stu-id="773db-1952">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="773db-1953">A **New-AzApiManagementIdentityProvider** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="773db-1953">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="773db-1954">AAD vagy AADB2C konfigurálása hitelesítésszolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="773db-1954">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="773db-1955">SignupPolicy, SigninPolicy, ProfileEditingPolicy és PasswordResetPolicy beállítása</span><span class="sxs-lookup"><span data-stu-id="773db-1955">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="773db-1956">A **New-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="773db-1956">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="773db-1957">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="773db-1957">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="773db-1958">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="773db-1958">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="773db-1959">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="773db-1959">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="773db-1960">A **Set-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="773db-1960">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="773db-1961">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="773db-1961">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="773db-1962">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="773db-1962">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="773db-1963">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="773db-1963">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="773db-1964">Az alábbi parancsmagok frissültek a ResourceID bemenetként való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="773db-1964">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="773db-1965">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="773db-1965">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="773db-1966">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="773db-1966">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="773db-1967">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="773db-1967">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="773db-1968">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="773db-1968">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="773db-1969">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="773db-1969">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="773db-1970">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="773db-1970">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="773db-1971">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="773db-1971">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="773db-1972">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="773db-1972">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="773db-1973">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="773db-1973">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="773db-1974">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="773db-1974">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="773db-1975">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="773db-1975">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="773db-1976">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="773db-1976">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="773db-1977">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="773db-1977">Az.Automation</span></span>
* <span data-ttu-id="773db-1978">A Get-AzAutomationJobOutputRecord frissítése a JSON- és a szövegrekordértékek kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="773db-1978">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="773db-1979">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="773db-1979">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="773db-1980">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="773db-1980">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="773db-1981">A Start-AzAutomationDscCompilationJob viselkedésének módosítása a munka elindítására a befejezésre való várakozás helyett</span><span class="sxs-lookup"><span data-stu-id="773db-1981">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="773db-1982">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="773db-1982">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="773db-1983">A Get-AzAutomationDscNode azon hibájának javítása, amely miatt a -Name használatakor az összes csomópontot visszaadta.</span><span class="sxs-lookup"><span data-stu-id="773db-1983">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="773db-1984">Most már csak az egyező csomópontot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="773db-1984">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="773db-1985">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-1985">Az.Compute</span></span>
* <span data-ttu-id="773db-1986">A ProtectFromScaleIn és a ProtectFromScaleSetAction paraméterek hozzáadása az Update-AzVmssVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="773db-1986">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="773db-1987">A New-azvm fedőparaméter-készlet mostantól alapértelmezetten egy elérhető helyet használ, ha az USA keleti régiója nem támogatott</span><span class="sxs-lookup"><span data-stu-id="773db-1987">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="773db-1988">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="773db-1988">Az.DataLakeStore</span></span>
* <span data-ttu-id="773db-1989">Az ADLS SDK frissítése a httpclient használatához, integrált adatsíkteszteléssel az Azure-keretrendszerben</span><span class="sxs-lookup"><span data-stu-id="773db-1989">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="773db-1990">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="773db-1990">Az.Monitor</span></span>
* <span data-ttu-id="773db-1991">A hibás paraméternevek kijavítása a súgópéldákban</span><span class="sxs-lookup"><span data-stu-id="773db-1991">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="773db-1992">Az.Network</span><span class="sxs-lookup"><span data-stu-id="773db-1992">Az.Network</span></span>
* <span data-ttu-id="773db-1993">DisableBgpRoutePropagation jelölő hozzáadása az érvényes útválasztási táblázathoz</span><span class="sxs-lookup"><span data-stu-id="773db-1993">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="773db-1994">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="773db-1994">Updated cmdlet:</span></span>
        - <span data-ttu-id="773db-1995">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="773db-1995">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="773db-1996">A dupla kötőjel kijavítása a New-AzApplicationGatewayTrustedRootCertificate dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="773db-1996">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="773db-1997">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-1997">Az.Resources</span></span>
* <span data-ttu-id="773db-1998">Új Get-AzureRmDenyAssignment parancsmag hozzáadása a megtagadási hozzárendelések lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="773db-1998">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="773db-1999">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-1999">Az.Sql</span></span>
* <span data-ttu-id="773db-2000">Advanced Threat Protection parancsmagok átnevezése Advanced Data Security névre és a sebezhetőségi felmérés alapértelmezett engedélyezése</span><span class="sxs-lookup"><span data-stu-id="773db-2000">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="773db-2001">2.0.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="773db-2001">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="773db-2002">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="773db-2002">Az.Accounts</span></span>
* <span data-ttu-id="773db-2003">Az Authentication Library frissítése a felhasználóneves/jelszavas hitelesítéssel kapcsolatos ADFS-problémák kijavításához</span><span class="sxs-lookup"><span data-stu-id="773db-2003">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="773db-2004">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="773db-2004">Az.CognitiveServices</span></span>
* <span data-ttu-id="773db-2005">Csak a Bing jogi nyilatkozat jelenik meg a Bing Search-szolgáltatásoknál.</span><span class="sxs-lookup"><span data-stu-id="773db-2005">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="773db-2006">A sikertelen fióklétrehozás hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="773db-2006">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="773db-2007">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-2007">Az.Compute</span></span>
* <span data-ttu-id="773db-2008">Közelségi elhelyezési csoport szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="773db-2008">Proximity placement group feature.</span></span>
    - <span data-ttu-id="773db-2009">A következő új parancsmagok lettek hozzáadva:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="773db-2009">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="773db-2010">Az új ProximityPlacementGroupId paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="773db-2010">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="773db-2011">A StorageAccountType paraméter hozzá lett adva a New-AzGalleryImageVersion parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="773db-2011">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="773db-2012">A New-AzGalleryImageVersion TargetRegion paramétere tartalmazhatja a következőt: StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="773db-2012">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="773db-2013">A SkipShutdown kapcsolóparaméter hozzá lett adva a Stop-AzVM és Stop-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="773db-2013">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="773db-2014">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="773db-2014">Breaking changes</span></span>
    - <span data-ttu-id="773db-2015">A Set-AzVMBootDiagnostics parancsmag új neve: Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="773db-2015">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="773db-2016">Az Export-AzLogAnalyticThrottledRequests parancsmag új neve: Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="773db-2016">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="773db-2017">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="773db-2017">Az.DeploymentManager</span></span>
* <span data-ttu-id="773db-2018">Az Azure Deployment Manager-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="773db-2018">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="773db-2019">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="773db-2019">Az.Dns</span></span>
* <span data-ttu-id="773db-2020">Automatikus DNS NameServer-delegálás</span><span class="sxs-lookup"><span data-stu-id="773db-2020">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="773db-2021">A DNS-zóna létrehozási parancsmag további opcionális paraméterként elfogadja a szülőzóna nevét.</span><span class="sxs-lookup"><span data-stu-id="773db-2021">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="773db-2022">Névkiszolgálói rekordokat ad hozzá a szülőzónában az újonnan létrehozott gyermekzóna számára.</span><span class="sxs-lookup"><span data-stu-id="773db-2022">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="773db-2023">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="773db-2023">Az.FrontDoor</span></span>
* <span data-ttu-id="773db-2024">Az Azure FrontDoor-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="773db-2024">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="773db-2025">A WAF-parancsmagok új neve tartalmazza a „Waf” sztringet</span><span class="sxs-lookup"><span data-stu-id="773db-2025">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="773db-2026">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="773db-2026">Az.HDInsight</span></span>
* <span data-ttu-id="773db-2027">A következő két parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="773db-2027">Removed two cmdlets:</span></span>
    - <span data-ttu-id="773db-2028">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="773db-2028">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="773db-2029">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="773db-2029">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="773db-2030">Egy új, Set-AzHDInsightGatewayCredential nevű parancsmag lett hozzáadva a Grant-AzHDInsightHttpServicesAccess helyett</span><span class="sxs-lookup"><span data-stu-id="773db-2030">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="773db-2031">A Get-AzHDInsightJobOutput parancsmag frissítve lett, hogy különbséget tegyen az olvasói és a HDInsight-operátori szerepkör között:</span><span class="sxs-lookup"><span data-stu-id="773db-2031">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="773db-2032">Az olvasói szerepkörrel rendelkező felhasználóknak explicit módon meg kell adniuk a DefaultStorageAccountKey paramétert, ellenkező esetben hiba történik.</span><span class="sxs-lookup"><span data-stu-id="773db-2032">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="773db-2033">A HDInsight-operátori szerepkörrel rendelkező felhasználókat ez nem érinti.</span><span class="sxs-lookup"><span data-stu-id="773db-2033">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="773db-2034">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="773db-2034">Az.Monitor</span></span>
* <span data-ttu-id="773db-2035">Az SQR API (ütemezett lekérdezési szabály) új parancsmagjai</span><span class="sxs-lookup"><span data-stu-id="773db-2035">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="773db-2036">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="773db-2036">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="773db-2037">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="773db-2037">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="773db-2038">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="773db-2038">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="773db-2039">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="773db-2039">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="773db-2040">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="773db-2040">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="773db-2041">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="773db-2041">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="773db-2042">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="773db-2042">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="773db-2043">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="773db-2043">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="773db-2044">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="773db-2044">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="773db-2045">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="773db-2045">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="773db-2046">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="773db-2046">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="773db-2047">[További](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) információk az SQR API-ról</span><span class="sxs-lookup"><span data-stu-id="773db-2047">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="773db-2048">A frissített Az.Monitor.md tartalmazza a GenV2 (nem klasszikus) metrikaalapú riasztási szabály parancsmagjait</span><span class="sxs-lookup"><span data-stu-id="773db-2048">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="773db-2049">Az.Network</span><span class="sxs-lookup"><span data-stu-id="773db-2049">Az.Network</span></span>
* <span data-ttu-id="773db-2050">A NAT-átjáró erőforrás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-2050">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="773db-2051">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="773db-2051">New cmdlets</span></span>
        - <span data-ttu-id="773db-2052">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="773db-2052">New-AzNatGateway</span></span>
        - <span data-ttu-id="773db-2053">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="773db-2053">Get-AzNatGateway</span></span>
        - <span data-ttu-id="773db-2054">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="773db-2054">Set-AzNatGateway</span></span>
        - <span data-ttu-id="773db-2055">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="773db-2055">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="773db-2056">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="773db-2056">Updated cmdlets</span></span>
        - <span data-ttu-id="773db-2057">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="773db-2057">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="773db-2058">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="773db-2058">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="773db-2059">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: Egyéni útvonalak beállítása/eltávolítása a Brooklyn Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="773db-2059">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="773db-2060">Frissült a New-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="773db-2060">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="773db-2061">Frissült a Set-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="773db-2061">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="773db-2062">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="773db-2062">Az.PolicyInsights</span></span>
* <span data-ttu-id="773db-2063">A szabályzat-kiértékelési adatok lekérdezésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="773db-2063">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="773db-2064">Az -Expand paraméter hozzá lett adva a Get-AzPolicyState parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="773db-2064">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="773db-2065">Az -Expand PolicyEvaluationDetails támogatása.</span><span class="sxs-lookup"><span data-stu-id="773db-2065">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="773db-2066">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="773db-2066">Az.RecoveryServices</span></span>
* <span data-ttu-id="773db-2067">Az előfizetések közötti Azure–Azure Site Recovery átvitel támogatása.</span><span class="sxs-lookup"><span data-stu-id="773db-2067">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="773db-2068">Az Azure Site Recovery jövőbeni kompatibilitástörő változásainak jelölése.</span><span class="sxs-lookup"><span data-stu-id="773db-2068">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="773db-2069">Ki lett javítva az Azure Site Recovery helyreállítási és műveletterve.</span><span class="sxs-lookup"><span data-stu-id="773db-2069">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="773db-2070">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure hálózatleképezés.</span><span class="sxs-lookup"><span data-stu-id="773db-2070">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="773db-2071">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure védelemirány felügyelt lemezek esetében.</span><span class="sxs-lookup"><span data-stu-id="773db-2071">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="773db-2072">További kisebb javítások.</span><span class="sxs-lookup"><span data-stu-id="773db-2072">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="773db-2073">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="773db-2073">Az.Relay</span></span>
* <span data-ttu-id="773db-2074">Az elgépelések ki lettek javítva az ügyféloldali üzenetekben</span><span class="sxs-lookup"><span data-stu-id="773db-2074">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="773db-2075">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="773db-2075">Az.ServiceBus</span></span>
* <span data-ttu-id="773db-2076">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="773db-2076">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="773db-2077">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="773db-2077">Az.Storage</span></span>
* <span data-ttu-id="773db-2078">A Storage ügyféloldali kódtárának frissítése a 10.0.1-es verziójára (az SDK összes objektuma esetében módosul a névtér a Microsoft.WindowsAzure.Storage. *névtérről a Microsoft.Azure.Storage.* névtérre)</span><span class="sxs-lookup"><span data-stu-id="773db-2078">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="773db-2079">Frissítés a Microsoft.Azure.Management.Storage 11.0.0-s verziójára az új API-verzió (2019. 04. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="773db-2079">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="773db-2080">A Tárfiók létrehozása parancs esetében az alapértelmezett Storage-fiókaltípus a Storage helyett mostantól a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="773db-2080">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="773db-2081">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="773db-2081">New-AzStorageAccount</span></span>
* <span data-ttu-id="773db-2082">A Storage-fiók Sku.Name parancsmagkimenete módosul, hogy igazodjon a bemeneti SkuName paraméterhez, egy aláhúzásjel („_”) hozzáadásával – például a StandardLRS a Standard_LRS névre módosul</span><span class="sxs-lookup"><span data-stu-id="773db-2082">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="773db-2083">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="773db-2083">New-AzStorageAccount</span></span>
    - <span data-ttu-id="773db-2084">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="773db-2084">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="773db-2085">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="773db-2085">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="773db-2086">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="773db-2086">Az.Websites</span></span>
* <span data-ttu-id="773db-2087">Az Altípus tulajdonság mostantól meg lesz adva a Get-AzWebApp által visszaadott PSSite objektumokhoz</span><span class="sxs-lookup"><span data-stu-id="773db-2087">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="773db-2088">A Get-AzWebApp\*Metrics és a Get-AzAppServicePlanMetrics megjelölve elavultként</span><span class="sxs-lookup"><span data-stu-id="773db-2088">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="773db-2089">1.8.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="773db-2089">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="773db-2090">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="773db-2090">Highlights since the last major release</span></span>
* <span data-ttu-id="773db-2091">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="773db-2091">General availability of `Az` module</span></span>
* <span data-ttu-id="773db-2092">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="773db-2092">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="773db-2093">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="773db-2093">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="773db-2094">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="773db-2094">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="773db-2095">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="773db-2095">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="773db-2096">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="773db-2096">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="773db-2097">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="773db-2097">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="773db-2098">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="773db-2098">Az.Accounts</span></span>
* <span data-ttu-id="773db-2099">Eltávolítás-AzureRm megfelelően törölni a Mac modulok frissítése</span><span class="sxs-lookup"><span data-stu-id="773db-2099">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="773db-2100">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="773db-2100">Az.Batch</span></span>
* <span data-ttu-id="773db-2101">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="773db-2101">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="773db-2102">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="773db-2102">Az.Cdn</span></span>
* <span data-ttu-id="773db-2103">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="773db-2103">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="773db-2104">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="773db-2104">Az.CognitiveServices</span></span>
* <span data-ttu-id="773db-2105">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="773db-2105">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="773db-2106">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-2106">Az.Compute</span></span>
* <span data-ttu-id="773db-2107">Az AEM telepítési kapcsolatos problémák megoldásához, ha a lemezek erőforrás-azonosítók kisbetűs resourcegroups volt az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="773db-2107">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="773db-2108">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="773db-2108">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="773db-2109">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="773db-2109">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="773db-2110">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="773db-2110">Az.DataFactory</span></span>
* <span data-ttu-id="773db-2111">Adjon hozzá SsisProperties, ha a NodeCount felügyelt integrációs modul nem null értékű.</span><span class="sxs-lookup"><span data-stu-id="773db-2111">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="773db-2112">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="773db-2112">Az.DataLakeStore</span></span>
* <span data-ttu-id="773db-2113">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="773db-2113">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="773db-2114">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="773db-2114">Az.EventGrid</span></span>
* <span data-ttu-id="773db-2115">A Súgó szöveg jelzi, hogy erőforrásokat kell létrehozni a create/update eseményt előfizetés parancsmagok használata előtt végpont frissítése.</span><span class="sxs-lookup"><span data-stu-id="773db-2115">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="773db-2116">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="773db-2116">Az.EventHub</span></span>
* <span data-ttu-id="773db-2117">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="773db-2117">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="773db-2118">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="773db-2118">Az.HDInsight</span></span>
* <span data-ttu-id="773db-2119">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="773db-2119">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="773db-2120">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="773db-2120">Az.IotHub</span></span>
* <span data-ttu-id="773db-2121">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="773db-2121">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="773db-2122">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="773db-2122">Az.KeyVault</span></span>
* <span data-ttu-id="773db-2123">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="773db-2123">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="773db-2124">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="773db-2124">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="773db-2125">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="773db-2125">Az.MachineLearning</span></span>
* <span data-ttu-id="773db-2126">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="773db-2126">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="773db-2127">Az.Media</span><span class="sxs-lookup"><span data-stu-id="773db-2127">Az.Media</span></span>
* <span data-ttu-id="773db-2128">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="773db-2128">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="773db-2129">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="773db-2129">Az.Monitor</span></span>
  * <span data-ttu-id="773db-2130">Riasztási szabály (nem klasszikus) GenV2 mérőszám-alapú új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="773db-2130">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="773db-2131">Új AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="773db-2131">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="773db-2132">Új AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="773db-2132">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="773db-2133">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="773db-2133">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="773db-2134">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="773db-2134">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="773db-2135">Adjon hozzá AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="773db-2135">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="773db-2136">Frissített verzió 0.22.0-preview figyelő SDK</span><span class="sxs-lookup"><span data-stu-id="773db-2136">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="773db-2137">Az.Network</span><span class="sxs-lookup"><span data-stu-id="773db-2137">Az.Network</span></span>
* <span data-ttu-id="773db-2138">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="773db-2138">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="773db-2139">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="773db-2139">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="773db-2140">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="773db-2140">Az.NotificationHubs</span></span>
* <span data-ttu-id="773db-2141">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="773db-2141">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="773db-2142">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="773db-2142">Az.OperationalInsights</span></span>
* <span data-ttu-id="773db-2143">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="773db-2143">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="773db-2144">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="773db-2144">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="773db-2145">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="773db-2145">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="773db-2146">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="773db-2146">Az.RecoveryServices</span></span>
* <span data-ttu-id="773db-2147">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="773db-2147">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="773db-2148">Frissített táblázatos formában az SQL azure-beli virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="773db-2148">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="773db-2149">A hozzáadott alternatív módszert AzureFileShare hely beolvasása</span><span class="sxs-lookup"><span data-stu-id="773db-2149">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="773db-2150">Frissített ScheduleRunDays SchedulePolicy objektumban időzóna szerint</span><span class="sxs-lookup"><span data-stu-id="773db-2150">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="773db-2151">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="773db-2151">Az.RedisCache</span></span>
* <span data-ttu-id="773db-2152">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="773db-2152">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="773db-2153">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-2153">Az.Resources</span></span>
* <span data-ttu-id="773db-2154">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="773db-2154">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="773db-2155">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-2155">Az.Sql</span></span>
* <span data-ttu-id="773db-2156">Cserélje le a függőségi figyelő SDK közös kód</span><span class="sxs-lookup"><span data-stu-id="773db-2156">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="773db-2157">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="773db-2157">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="773db-2158">Továbbfejlesztett folyamat, amely több oszlop osztályozási.</span><span class="sxs-lookup"><span data-stu-id="773db-2158">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="773db-2159">Termékváltozat tulajdonságok (termékváltozat neve, családi, kapacitás) válasz a Get-AzSqlServerServiceObjective és formátum táblaként alapértelmezés szerint tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="773db-2159">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="773db-2160">Lehetővé teszi a Get-AzSqlServerServiceObjective anélkül, hogy a régióban egy már létező kiszolgáló hely alapján.</span><span class="sxs-lookup"><span data-stu-id="773db-2160">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="773db-2161">Hozzon létre felügyelt példányt az időzóna-paraméter támogatása.</span><span class="sxs-lookup"><span data-stu-id="773db-2161">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="773db-2162">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="773db-2162">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="773db-2163">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="773db-2163">Az.Websites</span></span>
* <span data-ttu-id="773db-2164">a Set-AzWebApp és a Set-AzWebAppSlot távolítja el a címkék a végrehajtási javítások</span><span class="sxs-lookup"><span data-stu-id="773db-2164">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="773db-2165">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="773db-2165">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="773db-2166">A webhelyek SDK frissítése.</span><span class="sxs-lookup"><span data-stu-id="773db-2166">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="773db-2167">A AdminSiteName tulajdonság PSAppServicePlan eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="773db-2167">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="773db-2168">1.7.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="773db-2168">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="773db-2169">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="773db-2169">Highlights since the last major release</span></span>
* <span data-ttu-id="773db-2170">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="773db-2170">General availability of `Az` module</span></span>
* <span data-ttu-id="773db-2171">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="773db-2171">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="773db-2172">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="773db-2172">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="773db-2173">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="773db-2173">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="773db-2174">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="773db-2174">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="773db-2175">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="773db-2175">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="773db-2176">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="773db-2176">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="773db-2177">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="773db-2177">Az.Accounts</span></span>
* <span data-ttu-id="773db-2178">Frissített Add-AzEnvironment és Set-AzEnvironment parancsmag az AzureAnalysisServicesEndpointResourceId paraméter elfogadásához</span><span class="sxs-lookup"><span data-stu-id="773db-2178">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="773db-2179">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="773db-2179">Az.AnalysisServices</span></span>
* <span data-ttu-id="773db-2180">ServiceClient használata DataPlane-parancsmagokban és az eredeti hitelesítési logika eltávolítása</span><span class="sxs-lookup"><span data-stu-id="773db-2180">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="773db-2181">Az Add-AzureASAccount burkolóként való megadása a Connect-AzAccount számára a kompatibilitástörő változás elkerüléséhez</span><span class="sxs-lookup"><span data-stu-id="773db-2181">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="773db-2182">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="773db-2182">Az.Automation</span></span>
* <span data-ttu-id="773db-2183">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag belefoglalásokat érintő hibája.</span><span class="sxs-lookup"><span data-stu-id="773db-2183">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="773db-2184">Az IncludedKbNumber és az IncludedPackageNameMask paraméter mostantól működőképes.</span><span class="sxs-lookup"><span data-stu-id="773db-2184">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="773db-2185">Hibajavítás az Azure Automation frissítéskezelési dinamikus csoportja esetében</span><span class="sxs-lookup"><span data-stu-id="773db-2185">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="773db-2186">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-2186">Az.Compute</span></span>
* <span data-ttu-id="773db-2187">HyperVGeneration paraméter hozzáadása a New-AzDiskConfig és a New-AzSnapshotConfig parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="773db-2187">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="773db-2188">Virtuális gépek más bérlők katalógus-rendszerképével való létrehozásának engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="773db-2188">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="773db-2189">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="773db-2189">Az.ContainerInstance</span></span>
* <span data-ttu-id="773db-2190">Ki lett javítva a New-AzContainerGroup üres záró argumentumot hozzáadó -Command paraméterével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="773db-2190">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="773db-2191">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="773db-2191">Az.DataFactory</span></span>
* <span data-ttu-id="773db-2192">Az ADF .Net SDK verziója 3.0.2-re frissült.</span><span class="sxs-lookup"><span data-stu-id="773db-2192">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="773db-2193">A Set-AzDataFactoryV2 parancsmag a RepoConfiguration beállításaihoz tartozó kiegészítő paraméterekkel lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="773db-2193">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="773db-2194">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-2194">Az.Resources</span></span>
* <span data-ttu-id="773db-2195">Továbbfejlesztett szolgáltatókezelés a Get-AzResource esetében, -ResourceId vagy -ResourceGroupName, -Name és -ResourceType paraméterek megadásakor</span><span class="sxs-lookup"><span data-stu-id="773db-2195">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="773db-2196">Továbbfejlesztett hibakezelés a Test-AzDeployment és a Test-AzResourceGroupDeployment esetében</span><span class="sxs-lookup"><span data-stu-id="773db-2196">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="773db-2197">A hibákat nem a telepítés ellenőrzése során kezeli, hanem a parancs kimenetébe foglalja bele</span><span class="sxs-lookup"><span data-stu-id="773db-2197">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="773db-2198">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="773db-2198">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="773db-2199">-IgnoreDynamicParameters kapcsolóparaméter hozzáadása telepítési parancsmagokhoz a rendszer által feltett kérdések szkriptekben és feladatokban való mellőzéséhez</span><span class="sxs-lookup"><span data-stu-id="773db-2199">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="773db-2200">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="773db-2200">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="773db-2201">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-2201">Az.Sql</span></span>
* <span data-ttu-id="773db-2202">Adatbázisadat-besorolás támogatása.</span><span class="sxs-lookup"><span data-stu-id="773db-2202">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="773db-2203">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="773db-2203">Az.Storage</span></span>
* <span data-ttu-id="773db-2204">Részletes hibaüzenet megjelenítése Storage-környezet -UseConnectedAccount paraméterrel történő létrehozásakor az Azure-fiókba való bejelentkezés nélkül</span><span class="sxs-lookup"><span data-stu-id="773db-2204">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="773db-2205">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="773db-2205">New-AzStorageContext</span></span>
* <span data-ttu-id="773db-2206">Adott Storage-fiók Blob service-tulajdonságai kezelésének támogatása Management plane API-val</span><span class="sxs-lookup"><span data-stu-id="773db-2206">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="773db-2207">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="773db-2207">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="773db-2208">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="773db-2208">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="773db-2209">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="773db-2209">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="773db-2210">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="773db-2210">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="773db-2211">Az -AsJob támogatása blobok és fájlok feltöltéséhez, valamint parancsmagok letöltéséhez</span><span class="sxs-lookup"><span data-stu-id="773db-2211">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="773db-2212">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="773db-2212">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="773db-2213">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="773db-2213">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="773db-2214">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="773db-2214">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="773db-2215">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="773db-2215">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="773db-2216">1.6.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="773db-2216">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="773db-2217">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="773db-2217">Highlights since the last major release</span></span>
* <span data-ttu-id="773db-2218">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="773db-2218">General availability of `Az` module</span></span>
* <span data-ttu-id="773db-2219">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="773db-2219">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="773db-2220">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="773db-2220">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="773db-2221">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="773db-2221">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="773db-2222">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="773db-2222">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="773db-2223">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="773db-2223">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="773db-2224">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="773db-2224">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="773db-2225">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="773db-2225">Az.Automation</span></span>
* <span data-ttu-id="773db-2226">Az Azure Automation frissítéskezelése módosult, hogy támogassa az alábbi új funkciókat:</span><span class="sxs-lookup"><span data-stu-id="773db-2226">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="773db-2227">Dinamikus csoportosítás</span><span class="sxs-lookup"><span data-stu-id="773db-2227">Dynamic grouping</span></span>
    * <span data-ttu-id="773db-2228">Előzetesen és utólagosan futtatandó szkriptek</span><span class="sxs-lookup"><span data-stu-id="773db-2228">Pre-Post script</span></span>
    * <span data-ttu-id="773db-2229">Újraindítási beállítás</span><span class="sxs-lookup"><span data-stu-id="773db-2229">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="773db-2230">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-2230">Az.Compute</span></span>
* <span data-ttu-id="773db-2231">Ki lett javítva az elérési útvonal feloldásával kapcsolatos hiba a Get-AzVmBootDiagnosticsData esetében</span><span class="sxs-lookup"><span data-stu-id="773db-2231">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="773db-2232">A Compute ügyfélkódtár frissült a 25.0.0 verzióra</span><span class="sxs-lookup"><span data-stu-id="773db-2232">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="773db-2233">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="773db-2233">Az.KeyVault</span></span>
* <span data-ttu-id="773db-2234">Helyettesítő karakterek támogatásának hozzáadása a KeyVault-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="773db-2234">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="773db-2235">Az.Network</span><span class="sxs-lookup"><span data-stu-id="773db-2235">Az.Network</span></span>
* <span data-ttu-id="773db-2236">Az Intelligens veszélyforrás-felderítés támogatásának hozzáadása az Azure Firewallhoz</span><span class="sxs-lookup"><span data-stu-id="773db-2236">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="773db-2237">Az Application Gateway-tűzfalszabályzat legfelső szintű erőforrása és egyéni szabályok hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-2237">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="773db-2238">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="773db-2238">Az.RecoveryServices</span></span>
* <span data-ttu-id="773db-2239">A SnapshotRetentionInDays hozzáadása az Azure-beli virtuális gépek szabályzatához az azonnali RP támogatása érdekében</span><span class="sxs-lookup"><span data-stu-id="773db-2239">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="773db-2240">Folyamat támogatásának hozzáadása a regisztrációtörlési tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="773db-2240">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="773db-2241">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-2241">Az.Resources</span></span>
* <span data-ttu-id="773db-2242">Helyettesítő karakterek támogatásának hozzáadása a Get-AzResource és Get-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="773db-2242">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="773db-2243">Az ARM általános hívása esetén használt hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="773db-2243">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="773db-2244">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-2244">Az.Sql</span></span>
* <span data-ttu-id="773db-2245">A Fenyegetésészlelés parancsmagjainak paramétere (ExcludeDetectionType) a DetectionType helyett string[] lett, hogy a jövőben is használható legyen az új DetectionType-ok hozzáadásakor, valamint az automatikus kitöltés támogatása érdekében.</span><span class="sxs-lookup"><span data-stu-id="773db-2245">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="773db-2246">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="773db-2246">Az.Storage</span></span>
* <span data-ttu-id="773db-2247">Tárfiók felügyeleti szabályzata lekérésének/beállításának/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="773db-2247">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="773db-2248">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="773db-2248">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="773db-2249">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="773db-2249">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="773db-2250">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="773db-2250">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="773db-2251">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="773db-2251">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="773db-2252">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="773db-2252">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="773db-2253">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="773db-2253">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="773db-2254">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="773db-2254">Az.Websites</span></span>
* <span data-ttu-id="773db-2255">Ki lett javítva az ARM-sablon azon hibája, amely miatt meghiúsul az összes tárolóhely a New-AzWebApp - IncludeSourceWebAppSlots használatával történő klónozása</span><span class="sxs-lookup"><span data-stu-id="773db-2255">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="773db-2256">1.5.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="773db-2256">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="773db-2257">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="773db-2257">Az.Accounts</span></span>
* <span data-ttu-id="773db-2258">A Register-AzModule parancs hozzáadása az AutoRest által létrehozott parancsmagok támogatásához</span><span class="sxs-lookup"><span data-stu-id="773db-2258">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="773db-2259">A Connect-AzAccount példáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="773db-2259">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="773db-2260">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="773db-2260">Az.Automation</span></span>
* <span data-ttu-id="773db-2261">A bizonyos havi ütemezések lekérésekor jelentkező hiba kijavítva számos Azure Automation-parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="773db-2261">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="773db-2262">Ki lett javítva a hiba, amely miatt a Get-AzAutomationDscNode csak az első 20 csomópontot adta vissza.</span><span class="sxs-lookup"><span data-stu-id="773db-2262">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="773db-2263">Most már az összes csomópontot visszaadja</span><span class="sxs-lookup"><span data-stu-id="773db-2263">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="773db-2264">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="773db-2264">Az.Cdn</span></span>
* <span data-ttu-id="773db-2265">Új Powershell-parancsmagok hozzáadva az Egyéni tartományi Https engedélyezése/letiltása szolgáltatáshoz, a régiek elavultak</span><span class="sxs-lookup"><span data-stu-id="773db-2265">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="773db-2266">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-2266">Az.Compute</span></span>
* <span data-ttu-id="773db-2267">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="773db-2267">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="773db-2268">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="773db-2268">Az.DataFactory</span></span>
* <span data-ttu-id="773db-2269">Az ADF .Net SDK verziója 3.0.1-re frissült</span><span class="sxs-lookup"><span data-stu-id="773db-2269">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="773db-2270">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="773db-2270">Az.LogicApp</span></span>
* <span data-ttu-id="773db-2271">Ki lett javítva a hiba, amely miatt a ListWorkflows csak az eredmények első oldalát kérte le</span><span class="sxs-lookup"><span data-stu-id="773db-2271">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="773db-2272">Az.Network</span><span class="sxs-lookup"><span data-stu-id="773db-2272">Az.Network</span></span>
* <span data-ttu-id="773db-2273">Helyettesítő karakterek támogatásának hozzáadása a Network-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="773db-2273">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="773db-2274">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="773db-2274">Az.RecoveryServices</span></span>
* <span data-ttu-id="773db-2275">Azure-beli virtuális gépen futtatott SQL Server támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="773db-2275">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="773db-2276">SDK-frissítés</span><span class="sxs-lookup"><span data-stu-id="773db-2276">SDK Update</span></span>
* <span data-ttu-id="773db-2277">VMappContainer ellenőrzés eltávolítva a Get-ProtectableItem parancsmagból</span><span class="sxs-lookup"><span data-stu-id="773db-2277">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="773db-2278">Name és ServerName paraméterek hozzáadva a Get-ProtectableItem parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="773db-2278">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="773db-2279">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-2279">Az.Resources</span></span>
* <span data-ttu-id="773db-2280">`-TemplateObject` paraméter hozzáadva az üzembe helyező parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="773db-2280">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="773db-2281">További információ: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="773db-2281">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="773db-2282">Ki lett javítva a hiba, amely akkor jelentkezett, amikor a(z) `Get-AzResource` eredménye át lett irányítva a következőbe: `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="773db-2282">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="773db-2283">További információ: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="773db-2283">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="773db-2284">Ki lett javítva a JSON-adattípus módosításával kapcsolatos probléma, amely a(z) `Set-AzResource` futtatásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="773db-2284">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="773db-2285">További információ: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="773db-2285">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="773db-2286">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-2286">Az.Sql</span></span>
* <span data-ttu-id="773db-2287">Az AuditingEndpointsCommunicator frissítése.</span><span class="sxs-lookup"><span data-stu-id="773db-2287">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="773db-2288">Ki lett javítva az új diagnosztikai beállítások létrehozásakor jelentkező ritka eset viselkedése.</span><span class="sxs-lookup"><span data-stu-id="773db-2288">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="773db-2289">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="773db-2289">Az.Storage</span></span>
* <span data-ttu-id="773db-2290">A BlockBlobStorage altípus támogatása a Storage-fiók létrehozásakor      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="773db-2290">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="773db-2291">1.4.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="773db-2291">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="773db-2292">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="773db-2292">Az.AnalysisServices</span></span>
* <span data-ttu-id="773db-2293">Az AddAzureASAccount parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="773db-2293">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="773db-2294">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="773db-2294">Az.Automation</span></span>
* <span data-ttu-id="773db-2295">Az Import-AzAutomationDscNodeConfiguration súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="773db-2295">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="773db-2296">A konfigurációnév-ellenőrzés hozzáadva az Import-AzAutomationDscConfiguration parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="773db-2296">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="773db-2297">Továbbfejlesztett hibakezelés az Import-AzAutomationDscConfiguration parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="773db-2297">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="773db-2298">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="773db-2298">Az.CognitiveServices</span></span>
* <span data-ttu-id="773db-2299">A CustomSubdomainName új választható paraméterként hozzáadva a New-AzCognitiveServicesAccount parancsmaghoz, amellyel altartomány adható meg az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="773db-2299">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="773db-2300">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-2300">Az.Compute</span></span>
* <span data-ttu-id="773db-2301">Kijavítva az azonosító paraméterkészleteivel kapcsolatos probléma</span><span class="sxs-lookup"><span data-stu-id="773db-2301">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="773db-2302">Frissült a Get-AzVMExtension parancsmag, hogy az összes telepített bővítményt listázza, ha a Name paraméter nincs megadva</span><span class="sxs-lookup"><span data-stu-id="773db-2302">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="773db-2303">A Tag és a ResourceId paraméterek hozzáadva az Update-AzImage parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="773db-2303">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="773db-2304">A Get-AzVmssVM példányazonosító nélkül, az InstanceView használatával példánynézetben listázni tudja a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="773db-2304">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="773db-2305">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="773db-2305">Az.DataLakeStore</span></span>
* <span data-ttu-id="773db-2306">Parancsmagok hozzáadása a törölt ADL-elemek enumerálásához és visszaállításához</span><span class="sxs-lookup"><span data-stu-id="773db-2306">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="773db-2307">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="773db-2307">Az.EventHub</span></span>
* <span data-ttu-id="773db-2308">Új SkipEmptyArchives logikai tulajdonság hozzáadva az üres archívumok kihagyásához az Eventhub CaptureDescription osztályában</span><span class="sxs-lookup"><span data-stu-id="773db-2308">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="773db-2309">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="773db-2309">Az.KeyVault</span></span>
* <span data-ttu-id="773db-2310">A Set-AzKeyVaultSecret címkézésének kijavítása</span><span class="sxs-lookup"><span data-stu-id="773db-2310">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="773db-2311">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="773db-2311">Az.LogicApp</span></span>
* <span data-ttu-id="773db-2312">Hozzáadva az integrációs fiókok alapszintű termékváltozatában</span><span class="sxs-lookup"><span data-stu-id="773db-2312">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="773db-2313">Hozzáadva az XSLT 2.0-ban, az XSLT 3.0-ban és a Liquid leképezéstípusok esetén</span><span class="sxs-lookup"><span data-stu-id="773db-2313">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="773db-2314">Új parancsmagok az integrációs fiók szerelvényeihez</span><span class="sxs-lookup"><span data-stu-id="773db-2314">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="773db-2315">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="773db-2315">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="773db-2316">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="773db-2316">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="773db-2317">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="773db-2317">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="773db-2318">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="773db-2318">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="773db-2319">Új parancsmagok az integrációs fiók kötegkonfigurációjához</span><span class="sxs-lookup"><span data-stu-id="773db-2319">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="773db-2320">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="773db-2320">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="773db-2321">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="773db-2321">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="773db-2322">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="773db-2322">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="773db-2323">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="773db-2323">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="773db-2324">A Logic Apps SDK frissítése a 4.1.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="773db-2324">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="773db-2325">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="773db-2325">Az.Monitor</span></span>
* <span data-ttu-id="773db-2326">A Get-AzMetric súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="773db-2326">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="773db-2327">Az.Network</span><span class="sxs-lookup"><span data-stu-id="773db-2327">Az.Network</span></span>
* <span data-ttu-id="773db-2328">Az Add-AzApplicationGatewayCustomError súgójában lévő példa frissítése</span><span class="sxs-lookup"><span data-stu-id="773db-2328">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="773db-2329">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="773db-2329">Az.OperationalInsights</span></span>
* <span data-ttu-id="773db-2330">Kibővített támogatás a New és a Get ApplicationInsights adatforráshoz.</span><span class="sxs-lookup"><span data-stu-id="773db-2330">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="773db-2331">Új „ApplicationInsights” altípus hozzáadva az adott munkaterület Get specific és Get all Application Insights-adatforrásainak támogatásához.</span><span class="sxs-lookup"><span data-stu-id="773db-2331">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="773db-2332">A New-AzOperationalInsightsApplicationInsightsDataSource parancsmag hozzáadva adatforrás létrehozásához a következő Application Insights-erőforrásparaméterekkel: subscriptionId, resourceGroupName és name.</span><span class="sxs-lookup"><span data-stu-id="773db-2332">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="773db-2333">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-2333">Az.Resources</span></span>
* <span data-ttu-id="773db-2334">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="773db-2334">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="773db-2335">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="773db-2335">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="773db-2336">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="773db-2336">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="773db-2337">Ki lett javítva a KeyCredentials ismételt létrehozását megakadályozó hiba</span><span class="sxs-lookup"><span data-stu-id="773db-2337">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="773db-2338">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-2338">Az.Sql</span></span>
* <span data-ttu-id="773db-2339">Rugalmas SQL DB-skálázási szint támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-2339">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="773db-2340">Ki lett javítva az a hiba, hogy a visszaállítási kérésben szereplő szükségtelen tulajdonságok megadása miatt a visszaállítás esetenként meghiúsult</span><span class="sxs-lookup"><span data-stu-id="773db-2340">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="773db-2341">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="773db-2341">Az.Websites</span></span>
* <span data-ttu-id="773db-2342">A Get-AzWebAppSlotMetrics példájának javítása</span><span class="sxs-lookup"><span data-stu-id="773db-2342">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="773db-2343">1.3.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="773db-2343">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="773db-2344">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="773db-2344">Az.Accounts</span></span>
* <span data-ttu-id="773db-2345">Frissítés a ClientRuntime legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="773db-2345">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="773db-2346">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="773db-2346">Az.AnalysisServices</span></span>
<span data-ttu-id="773db-2347">Az Az.AnalysisServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="773db-2347">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="773db-2348">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-2348">Az.Compute</span></span>
* <span data-ttu-id="773db-2349">AEM-bővítmény: Mostantól az UltraSSD, valamint a P60, P70 és P80 lemezek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="773db-2349">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="773db-2350">A Set-AzVMBootDiagnostics súgóleírása frissült.</span><span class="sxs-lookup"><span data-stu-id="773db-2350">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="773db-2351">Az Update-AzImage súgóleírása és példája frissült.</span><span class="sxs-lookup"><span data-stu-id="773db-2351">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="773db-2352">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="773db-2352">Az.RecoveryServices</span></span>
<span data-ttu-id="773db-2353">Az Az.RecoveryServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="773db-2353">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="773db-2354">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-2354">Az.Resources</span></span>
* <span data-ttu-id="773db-2355">Az erőforráscsoportok címkézése ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="773db-2355">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="773db-2356">További információ: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="773db-2356">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="773db-2357">Ki lett javítva az a hiba, amikor a `Get-AzureRmRoleAssignment` nem vette figyelembe az -ErrorAction paramétert.</span><span class="sxs-lookup"><span data-stu-id="773db-2357">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="773db-2358">További információ: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="773db-2358">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="773db-2359">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-2359">Az.Sql</span></span>
* <span data-ttu-id="773db-2360">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-2360">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="773db-2361">Ki lett javítva az a hiba, amikor az Azure-fiókba való bejelentkezés hiánya nullref kivételt eredményezett az SQL-parancsmagok végrehajtásakor.</span><span class="sxs-lookup"><span data-stu-id="773db-2361">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="773db-2362">A nullref kivétel ki lett javítva a Get-AzSqlCapabilityben.</span><span class="sxs-lookup"><span data-stu-id="773db-2362">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="773db-2363">1.2.1 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="773db-2363">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="773db-2364">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="773db-2364">Az.Accounts</span></span>
* <span data-ttu-id="773db-2365">A hitelesítés megfelelő verziójával rendelkező kiadás</span><span class="sxs-lookup"><span data-stu-id="773db-2365">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="773db-2366">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="773db-2366">Az.AnalysisServices</span></span>
* <span data-ttu-id="773db-2367">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="773db-2367">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="773db-2368">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="773db-2368">Az.RecoveryServices</span></span>
* <span data-ttu-id="773db-2369">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="773db-2369">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="773db-2370">1.2.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="773db-2370">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="773db-2371">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="773db-2371">Az.Accounts</span></span>
* <span data-ttu-id="773db-2372">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="773db-2372">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="773db-2373">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="773db-2373">Update incorrect online help URLs</span></span>
* <span data-ttu-id="773db-2374">Az Uninstall-AzureRm figyelmeztető üzenete hozzáadva a PS Core-ban</span><span class="sxs-lookup"><span data-stu-id="773db-2374">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="773db-2375">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="773db-2375">Az.Aks</span></span>
* <span data-ttu-id="773db-2376">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="773db-2376">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="773db-2377">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="773db-2377">Az.Automation</span></span>
* <span data-ttu-id="773db-2378">Mostantól támogatottak a Python 2-runbookok.</span><span class="sxs-lookup"><span data-stu-id="773db-2378">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="773db-2379">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="773db-2379">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="773db-2380">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="773db-2380">Az.Cdn</span></span>
* <span data-ttu-id="773db-2381">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="773db-2381">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="773db-2382">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-2382">Az.Compute</span></span>
* <span data-ttu-id="773db-2383">Az Invoke-AzVMReimage parancsmag hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="773db-2383">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="773db-2384">A TempDisk paraméter hozzá lett adva a Set-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="773db-2384">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="773db-2385">A New-AzVM figyelmeztető üzenete ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="773db-2385">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="773db-2386">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="773db-2386">Az.ContainerRegistry</span></span>
* <span data-ttu-id="773db-2387">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="773db-2387">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="773db-2388">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="773db-2388">Az.DataFactory</span></span>
* <span data-ttu-id="773db-2389">Az ADF .Net SDK verziója 3.0.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="773db-2389">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="773db-2390">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="773db-2390">Az.DataLakeStore</span></span>
* <span data-ttu-id="773db-2391">Ki lett javítva az ADLS-végponttal kapcsolatos probléma az MSI használatakor.</span><span class="sxs-lookup"><span data-stu-id="773db-2391">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="773db-2392">További információ: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="773db-2392">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="773db-2393">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="773db-2393">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="773db-2394">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="773db-2394">Az.IotHub</span></span>
* <span data-ttu-id="773db-2395">Az Encoding formátum hozzá lett adva az Add-IotHubRoutingEndpoint parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="773db-2395">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="773db-2396">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="773db-2396">Az.KeyVault</span></span>
* <span data-ttu-id="773db-2397">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="773db-2397">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="773db-2398">Az.Network</span><span class="sxs-lookup"><span data-stu-id="773db-2398">Az.Network</span></span>
* <span data-ttu-id="773db-2399">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="773db-2399">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="773db-2400">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-2400">Az.Resources</span></span>
* <span data-ttu-id="773db-2401">A helytelen példák ki lettek javítva a New-AzADAppCredential és a New-AzADSpCredential referenciadokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="773db-2401">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="773db-2402">Ki lett javítva az a hiba, amikor a -TemplateFile paraméter nem lett feloldva az erőforráscsoportokat üzembe helyező parancsmagok végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="773db-2402">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="773db-2403">Az.Resources: A New-AzureRmPolicyDefinition -Mode alapértelmezett értékének dokumentációja ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="773db-2403">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="773db-2404">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="773db-2404">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="773db-2405">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="773db-2405">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="773db-2406">Ki lett javítva a „PSResourceGroupDeployment” objektum formázásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="773db-2406">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="773db-2407">További információ: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="773db-2407">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="773db-2408">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="773db-2408">Az.ServiceFabric</span></span>
* <span data-ttu-id="773db-2409">Visszaállítás a VMSS-modell tanúsítványának hozzáadásakor bekövetkező kivétel-visszaadás esetén; javított hiba: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="773db-2409">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="773db-2410">Bizonyos hibaüzenetek ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="773db-2410">Fix some error messages.</span></span>
* <span data-ttu-id="773db-2411">Ki lett javítva az alapértelmezett ARM-sablonnal való fürtlétrehozás a New-AzServiceFabriCluster esetében, amely nem működött az Az-ba történő migrálással.</span><span class="sxs-lookup"><span data-stu-id="773db-2411">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="773db-2412">Ki lett javítva a fürt-/alkalmazástanúsítvány létrehozása, így mostantól csak a fürtnek megfelelő virtuálisgép-méretezési csoportokhoz (Virtual Machine Scale Sets) lesznek hozzáadva, a fürtazonosító bővítményben való ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="773db-2412">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="773db-2413">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="773db-2413">Az.SignalR</span></span>
* <span data-ttu-id="773db-2414">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="773db-2414">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="773db-2415">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-2415">Az.Sql</span></span>
* <span data-ttu-id="773db-2416">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="773db-2416">Update incorrect online help URLs</span></span>
* <span data-ttu-id="773db-2417">A LicenseType paraméter paraméterleírása frissítve lett a lehetséges értékekkel.</span><span class="sxs-lookup"><span data-stu-id="773db-2417">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="773db-2418">Ki lett javítva az a hiba, amikor egy felügyelt példány identitásának frissítése nem működött, ha az volt az egyetlen frissített tulajdonság.</span><span class="sxs-lookup"><span data-stu-id="773db-2418">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="773db-2419">Egyéni rendezések támogatása a felügyelt példányokon</span><span class="sxs-lookup"><span data-stu-id="773db-2419">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="773db-2420">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="773db-2420">Az.Storage</span></span>
* <span data-ttu-id="773db-2421">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="773db-2421">Update incorrect online help URLs</span></span>
* <span data-ttu-id="773db-2422">Részletes hibaüzenet megjelenítése klasszikus naplózás/metrika get/set műveletei esetében a prémium szintű Storage-fiókon, mivel a prémium szintű Storage-fiók nem támogatja a klasszikus naplózást/metrikát.</span><span class="sxs-lookup"><span data-stu-id="773db-2422">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="773db-2423">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="773db-2423">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="773db-2424">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="773db-2424">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="773db-2425">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="773db-2425">Az.TrafficManager</span></span>
* <span data-ttu-id="773db-2426">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="773db-2426">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="773db-2427">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="773db-2427">Az.Websites</span></span>
* <span data-ttu-id="773db-2428">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="773db-2428">Update incorrect online help URLs</span></span>
* <span data-ttu-id="773db-2429">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól a megfelelő erőforráscsoportba és helyre tölti fel a tanúsítványt, ha az alkalmazás ASE-n üzemel.</span><span class="sxs-lookup"><span data-stu-id="773db-2429">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="773db-2430">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól nem írja felül a címkéket SSL-tanúsítvány alkalmazáshoz való kötésekor.</span><span class="sxs-lookup"><span data-stu-id="773db-2430">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="773db-2431">1.1.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="773db-2431">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="773db-2432">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="773db-2432">Az.Accounts</span></span>
* <span data-ttu-id="773db-2433">A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz</span><span class="sxs-lookup"><span data-stu-id="773db-2433">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="773db-2434">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-2434">Az.Compute</span></span>
* <span data-ttu-id="773db-2435">A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni</span><span class="sxs-lookup"><span data-stu-id="773db-2435">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="773db-2436">Frissült az azonosító leírása a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="773db-2436">Updated the description of ID in help files</span></span>
* <span data-ttu-id="773db-2437">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="773db-2437">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="773db-2438">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="773db-2438">Az.DataLakeStore</span></span>
* <span data-ttu-id="773db-2439">A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.</span><span class="sxs-lookup"><span data-stu-id="773db-2439">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="773db-2440">A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva</span><span class="sxs-lookup"><span data-stu-id="773db-2440">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="773db-2441">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="773db-2441">Az.EventGrid</span></span>
* <span data-ttu-id="773db-2442">Frissítve a 2019-01-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="773db-2442">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="773db-2443">A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához</span><span class="sxs-lookup"><span data-stu-id="773db-2443">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="773db-2444">New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="773db-2444">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="773db-2445">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="773db-2445">Event Time-To-Live,</span></span>
        - <span data-ttu-id="773db-2446">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="773db-2446">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="773db-2447">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="773db-2447">Dead letter endpoint.</span></span>
    - <span data-ttu-id="773db-2448">Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="773db-2448">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="773db-2449">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="773db-2449">Event Time-To-Live,</span></span>
        - <span data-ttu-id="773db-2450">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="773db-2450">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="773db-2451">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="773db-2451">Dead letter endpoint.</span></span>
* <span data-ttu-id="773db-2452">Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.</span><span class="sxs-lookup"><span data-stu-id="773db-2452">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="773db-2453">Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.</span><span class="sxs-lookup"><span data-stu-id="773db-2453">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="773db-2454">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="773db-2454">Az.IotHub</span></span>
* <span data-ttu-id="773db-2455">Frissítve az IoT Hub SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="773db-2455">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="773db-2456">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="773db-2456">Az.LogicApp</span></span>
* <span data-ttu-id="773db-2457">A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel</span><span class="sxs-lookup"><span data-stu-id="773db-2457">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="773db-2458">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-2458">Az.Resources</span></span>
* <span data-ttu-id="773db-2459">Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="773db-2459">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="773db-2460">További információ: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="773db-2460">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="773db-2461">Ki lett javítva a -Custom paraméter kezelése a New/Set-AzPolicyDefinition parancsban</span><span class="sxs-lookup"><span data-stu-id="773db-2461">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="773db-2462">Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="773db-2462">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="773db-2463">A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében</span><span class="sxs-lookup"><span data-stu-id="773db-2463">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="773db-2464">További információ: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="773db-2464">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="773db-2465">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="773db-2465">Az.SignalR</span></span>
* <span data-ttu-id="773db-2466">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="773db-2466">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="773db-2467">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-2467">Az.Sql</span></span>
* <span data-ttu-id="773db-2468">A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.</span><span class="sxs-lookup"><span data-stu-id="773db-2468">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="773db-2469">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="773db-2469">Az.Storage</span></span>
* <span data-ttu-id="773db-2470">A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva</span><span class="sxs-lookup"><span data-stu-id="773db-2470">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="773db-2471">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="773db-2471">New-AzStorageContext</span></span>
* <span data-ttu-id="773db-2472">A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz</span><span class="sxs-lookup"><span data-stu-id="773db-2472">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="773db-2473">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="773db-2473">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="773db-2474">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="773db-2474">Az.Websites</span></span>
* <span data-ttu-id="773db-2475">Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban</span><span class="sxs-lookup"><span data-stu-id="773db-2475">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="773db-2476">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="773db-2476">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="773db-2477">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="773db-2477">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="773db-2478">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="773db-2478">General</span></span>

- <span data-ttu-id="773db-2479">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="773db-2479">General Availability of Az Module</span></span>
- <span data-ttu-id="773db-2480">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="773db-2480">Online help for each module</span></span>
- <span data-ttu-id="773db-2481">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="773db-2481">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="773db-2482">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="773db-2482">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="773db-2483">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="773db-2483">Az.Accounts</span></span>
- <span data-ttu-id="773db-2484">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="773db-2484">Changed from Az.Profile</span></span>
- <span data-ttu-id="773db-2485">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="773db-2485">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="773db-2486">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="773db-2486">Az.ApiManagement</span></span>
- <span data-ttu-id="773db-2487">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="773db-2487">Fixes for #7002</span></span>
- <span data-ttu-id="773db-2488">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="773db-2488">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="773db-2489">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="773db-2489">Az.Batch</span></span>
- <span data-ttu-id="773db-2490">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="773db-2490">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="773db-2491">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="773db-2491">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="773db-2492">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="773db-2492">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="773db-2493">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="773db-2493">Az.Billing</span></span>
- <span data-ttu-id="773db-2494">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="773db-2494">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="773db-2495">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="773db-2495">Az.CognitivServices</span></span>
- <span data-ttu-id="773db-2496">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="773db-2496">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="773db-2497">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="773db-2497">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="773db-2498">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="773db-2498">Az.ContainerInstance</span></span>
- <span data-ttu-id="773db-2499">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="773db-2499">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="773db-2500">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="773db-2500">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="773db-2501">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="773db-2501">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="773db-2502">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="773db-2502">Az.DataLakeStore</span></span>
- <span data-ttu-id="773db-2503">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="773db-2503">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="773db-2504">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="773db-2504">Az.Monitor</span></span>
- <span data-ttu-id="773db-2505">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="773db-2505">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="773db-2506">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="773db-2506">Az.KeyVault</span></span>
- <span data-ttu-id="773db-2507">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="773db-2507">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="773db-2508">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="773db-2508">Az.MachineLearning</span></span>
- <span data-ttu-id="773db-2509">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="773db-2509">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="773db-2510">Az.Media</span><span class="sxs-lookup"><span data-stu-id="773db-2510">Az.Media</span></span>
- <span data-ttu-id="773db-2511">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="773db-2511">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="773db-2512">Az.Network</span><span class="sxs-lookup"><span data-stu-id="773db-2512">Az.Network</span></span>
<span data-ttu-id="773db-2513">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="773db-2513">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="773db-2514">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="773db-2514">New cmdlets added:</span></span>
        - <span data-ttu-id="773db-2515">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="773db-2515">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="773db-2516">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="773db-2516">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="773db-2517">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="773db-2517">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="773db-2518">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="773db-2518">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="773db-2519">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="773db-2519">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="773db-2520">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="773db-2520">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="773db-2521">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="773db-2521">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="773db-2522">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="773db-2522">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="773db-2523">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="773db-2523">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="773db-2524">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="773db-2524">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="773db-2525">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="773db-2525">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="773db-2526">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="773db-2526">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="773db-2527">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="773db-2527">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="773db-2528">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="773db-2528">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="773db-2529">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="773db-2529">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="773db-2530">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="773db-2530">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="773db-2531">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="773db-2531">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="773db-2532">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="773db-2532">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="773db-2533">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="773db-2533">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="773db-2534">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="773db-2534">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="773db-2535">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="773db-2535">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="773db-2536">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="773db-2536">Az.OperationalInsights</span></span>
- <span data-ttu-id="773db-2537">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="773db-2537">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="773db-2538">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="773db-2538">Az.Profile</span></span>
- <span data-ttu-id="773db-2539">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="773db-2539">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="773db-2540">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="773db-2540">Az.RecoveryServices</span></span>
- <span data-ttu-id="773db-2541">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="773db-2541">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="773db-2542">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-2542">Az.Resources</span></span>
- <span data-ttu-id="773db-2543">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="773db-2543">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="773db-2544">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="773db-2544">Az.ServiceFabric</span></span>
- <span data-ttu-id="773db-2545">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="773db-2545">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="773db-2546">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="773db-2546">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="773db-2547">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="773db-2547">Az.SIgnalR</span></span>
- <span data-ttu-id="773db-2548">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="773db-2548">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="773db-2549">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-2549">Az.Sql</span></span>
- <span data-ttu-id="773db-2550">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="773db-2550">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="773db-2551">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="773db-2551">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="773db-2552">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="773db-2552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="773db-2553">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="773db-2553">Az.Storage</span></span>
- <span data-ttu-id="773db-2554">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="773db-2554">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="773db-2555">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="773db-2555">Az.Websites</span></span>
- <span data-ttu-id="773db-2556">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="773db-2556">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="773db-2557">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="773db-2557">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="773db-2558">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="773db-2558">General</span></span>

* <span data-ttu-id="773db-2559">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="773db-2559">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="773db-2560">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-2560">Az.Compute</span></span>

* <span data-ttu-id="773db-2561">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="773db-2561">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="773db-2562">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="773db-2562">Az.DataLakeStore</span></span>

* <span data-ttu-id="773db-2563">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="773db-2563">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="773db-2564">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="773db-2564">Az.FrontDoor</span></span>

* <span data-ttu-id="773db-2565">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="773db-2565">Fixed some broken links</span></span>
    - <span data-ttu-id="773db-2566">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="773db-2566">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="773db-2567">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="773db-2567">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="773db-2568">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="773db-2568">Az.RecoveryServices</span></span>

* <span data-ttu-id="773db-2569">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="773db-2569">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="773db-2570">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="773db-2570">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="773db-2571">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-2571">Az.Resources</span></span>

* <span data-ttu-id="773db-2572">[https://github.com/Azure/azure-powershell/issues/7679](https://github.com/Azure/azure-powershell/issues/7679 ) javítása</span><span class="sxs-lookup"><span data-stu-id="773db-2572">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="773db-2573">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="773db-2573">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="773db-2574">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-2574">Az.Sql</span></span>

* <span data-ttu-id="773db-2575">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="773db-2575">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="773db-2576">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="773db-2576">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="773db-2577">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="773db-2577">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="773db-2578">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="773db-2578">Az.Storage</span></span>

* <span data-ttu-id="773db-2579">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="773db-2579">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="773db-2580">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="773db-2580">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="773db-2581">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="773db-2581">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="773db-2582">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="773db-2582">Support Static Website configuration</span></span>
    - <span data-ttu-id="773db-2583">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="773db-2583">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="773db-2584">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="773db-2584">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="773db-2585">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="773db-2585">Az.Websites</span></span>

* <span data-ttu-id="773db-2586">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="773db-2586">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="773db-2587">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="773db-2587">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="773db-2588">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="773db-2588">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="773db-2589">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="773db-2589">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="773db-2590">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="773db-2590">Az.ApiManagement</span></span>
* <span data-ttu-id="773db-2591">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="773db-2591">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="773db-2592">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="773db-2592">Az.Automation</span></span>
* <span data-ttu-id="773db-2593">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="773db-2593">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="773db-2594">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="773db-2594">Added Update Management cmdlets</span></span>
* <span data-ttu-id="773db-2595">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="773db-2595">Added Source Control cmdlets</span></span>
* <span data-ttu-id="773db-2596">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="773db-2596">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="773db-2597">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="773db-2597">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="773db-2598">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-2598">Az.Compute</span></span>
* <span data-ttu-id="773db-2599">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="773db-2599">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="773db-2600">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="773db-2600">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="773db-2601">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="773db-2601">Az.ContainerInstance</span></span>
* <span data-ttu-id="773db-2602">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="773db-2602">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="773db-2603">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="773db-2603">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="773db-2604">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="773db-2604">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="773db-2605">Az.Network</span><span class="sxs-lookup"><span data-stu-id="773db-2605">Az.Network</span></span>
* <span data-ttu-id="773db-2606">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="773db-2606">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="773db-2607">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="773db-2607">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="773db-2608">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="773db-2608">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="773db-2609">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="773db-2609">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="773db-2610">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="773db-2610">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="773db-2611">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="773db-2611">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="773db-2612">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="773db-2612">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="773db-2613">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="773db-2613">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="773db-2614">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="773db-2614">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="773db-2615">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="773db-2615">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="773db-2616">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="773db-2616">Az.Relay</span></span>
* <span data-ttu-id="773db-2617">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="773db-2617">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="773db-2618">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-2618">Az.Resources</span></span>
* <span data-ttu-id="773db-2619">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="773db-2619">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="773db-2620">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="773db-2620">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="773db-2621">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="773db-2621">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="773db-2622">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="773db-2622">Az.ServiceFabric</span></span>
* <span data-ttu-id="773db-2623">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="773db-2623">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="773db-2624">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-2624">Az.Sql</span></span>
* <span data-ttu-id="773db-2625">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="773db-2625">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="773db-2626">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="773db-2626">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="773db-2627">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="773db-2627">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="773db-2628">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="773db-2628">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="773db-2629">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="773db-2629">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="773db-2630">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="773db-2630">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="773db-2631">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="773db-2631">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="773db-2632">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="773db-2632">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="773db-2633">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="773db-2633">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="773db-2634">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="773db-2634">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="773db-2635">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="773db-2635">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="773db-2636">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="773db-2636">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="773db-2637">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="773db-2637">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="773db-2638">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="773db-2638">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="773db-2639">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="773db-2639">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="773db-2640">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="773db-2640">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="773db-2641">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="773db-2641">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="773db-2642">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="773db-2642">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="773db-2643">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="773db-2643">General</span></span>
* <span data-ttu-id="773db-2644">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="773db-2644">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="773db-2645">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="773db-2645">Az.Profile</span></span>
* <span data-ttu-id="773db-2646">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="773db-2646">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="773db-2647">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="773db-2647">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="773db-2648">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="773db-2648">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="773db-2649">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="773db-2649">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="773db-2650">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="773db-2650">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="773db-2651">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="773db-2651">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="773db-2652">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="773db-2652">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="773db-2653">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="773db-2653">Az.CognitiveServices</span></span>
* <span data-ttu-id="773db-2654">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="773db-2654">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="773db-2655">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-2655">Az.Compute</span></span>
* <span data-ttu-id="773db-2656">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="773db-2656">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="773db-2657">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="773db-2657">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="773db-2658">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="773db-2658">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="773db-2659">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="773db-2659">Az.DataLakeStore</span></span>
* <span data-ttu-id="773db-2660">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="773db-2660">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="773db-2661">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="773db-2661">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="773db-2662">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="773db-2662">Az.Insights</span></span>
* <span data-ttu-id="773db-2663">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="773db-2663">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="773db-2664">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="773db-2664">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="773db-2665">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="773db-2665">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="773db-2666">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="773db-2666">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="773db-2667">Az.Network</span><span class="sxs-lookup"><span data-stu-id="773db-2667">Az.Network</span></span>
* <span data-ttu-id="773db-2668">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="773db-2668">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="773db-2669">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="773db-2669">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="773db-2670">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="773db-2670">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="773db-2671">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="773db-2671">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="773db-2672">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="773db-2672">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="773db-2673">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="773db-2673">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="773db-2674">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="773db-2674">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="773db-2675">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="773db-2675">Az.PolicyInsights</span></span>
* <span data-ttu-id="773db-2676">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-2676">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="773db-2677">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-2677">Az.Resources</span></span>
* <span data-ttu-id="773db-2678">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402 ) javítása</span><span class="sxs-lookup"><span data-stu-id="773db-2678">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="773db-2679">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="773db-2679">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="773db-2680">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="773db-2680">Az.ServiceBus</span></span>
* <span data-ttu-id="773db-2681">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="773db-2681">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="773db-2682">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="773db-2682">Az.ServiceFabric</span></span>
* <span data-ttu-id="773db-2683">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="773db-2683">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="773db-2684">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="773db-2684">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="773db-2685">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="773db-2685">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="773db-2686">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="773db-2686">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="773db-2687">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="773db-2687">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="773db-2688">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="773db-2688">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="773db-2689">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="773db-2689">Az.Profile</span></span>
* <span data-ttu-id="773db-2690">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="773db-2690">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="773db-2691">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="773db-2691">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="773db-2692">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-2692">Az.Compute</span></span>
* <span data-ttu-id="773db-2693">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="773db-2693">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="773db-2694">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="773db-2694">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="773db-2695">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="773db-2695">Az.DataLakeStore</span></span>
* <span data-ttu-id="773db-2696">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="773db-2696">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="773db-2697">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="773db-2697">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="773db-2698">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="773db-2698">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="773db-2699">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="773db-2699">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="773db-2700">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="773db-2700">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="773db-2701">Az.Network</span><span class="sxs-lookup"><span data-stu-id="773db-2701">Az.Network</span></span>
* <span data-ttu-id="773db-2702">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="773db-2702">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="773db-2703">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="773db-2703">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="773db-2704">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-2704">Az.Resources</span></span>
* <span data-ttu-id="773db-2705">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="773db-2705">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="773db-2706">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="773db-2706">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="773db-2707">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="773db-2707">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="773db-2708">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="773db-2708">Azure.Storage</span></span>
* <span data-ttu-id="773db-2709">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="773db-2709">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="773db-2710">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="773db-2710">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="773db-2711">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="773db-2711">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="773db-2712">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="773db-2712">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="773db-2713">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="773db-2713">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="773db-2714">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="773db-2714">Az.CognitiveServices</span></span>
* <span data-ttu-id="773db-2715">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="773db-2715">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="773db-2716">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="773db-2716">Az.Compute</span></span>
* <span data-ttu-id="773db-2717">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="773db-2717">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="773db-2718">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="773db-2718">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="773db-2719">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="773db-2719">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="773db-2720">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="773db-2720">Az.DataFactoryV2</span></span>
* <span data-ttu-id="773db-2721">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="773db-2721">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="773db-2722">Az.Network</span><span class="sxs-lookup"><span data-stu-id="773db-2722">Az.Network</span></span>
* <span data-ttu-id="773db-2723">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="773db-2723">Added NetworkProfile functionality.</span></span> <span data-ttu-id="773db-2724">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="773db-2724">new cmdlets added</span></span>
    - <span data-ttu-id="773db-2725">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="773db-2725">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="773db-2726">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="773db-2726">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="773db-2727">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="773db-2727">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="773db-2728">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="773db-2728">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="773db-2729">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="773db-2729">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="773db-2730">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="773db-2730">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="773db-2731">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="773db-2731">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="773db-2732">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="773db-2732">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="773db-2733">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="773db-2733">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="773db-2734">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="773db-2734">Az.RedisCache</span></span>
* <span data-ttu-id="773db-2735">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="773db-2735">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="773db-2736">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="773db-2736">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="773db-2737">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="773db-2737">Az.Resources</span></span>
* <span data-ttu-id="773db-2738">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="773db-2738">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="773db-2739">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="773db-2739">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="773db-2740">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="773db-2740">Az.Sql</span></span>
* <span data-ttu-id="773db-2741">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="773db-2741">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="773db-2742">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="773db-2742">Az.Websites</span></span>
* <span data-ttu-id="773db-2743">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="773db-2743">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="773db-2744">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="773db-2744">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="773db-2745">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="773db-2745">0.2.0 - September 2018</span></span>
 <span data-ttu-id="773db-2746">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="773db-2746">Initial Release</span></span>
