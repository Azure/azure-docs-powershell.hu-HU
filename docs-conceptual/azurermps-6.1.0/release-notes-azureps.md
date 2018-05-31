---
title: Az Azure PowerShell változásnaplója | Microsoft Docs
description: Az alábbiakban az Azure PowerShell legutóbbi kiadásában végrehajtott módosítások előzményei olvashatók.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 0b7902155c47f2e6355e9147c203867288caab81
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/23/2018
ms.locfileid: "34461895"
---
# <a name="release-notes"></a><span data-ttu-id="f9ebf-103">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="f9ebf-103">Release notes</span></span>

<span data-ttu-id="f9ebf-104">Az alábbiakban az Azure PowerShell jelen kiadásában végrehajtott módosítások listája olvasható.</span><span class="sxs-lookup"><span data-stu-id="f9ebf-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="610---may-2018"></a><span data-ttu-id="f9ebf-105">6.1.0 – 2018. május</span><span class="sxs-lookup"><span data-stu-id="f9ebf-105">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="f9ebf-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f9ebf-106">AzureRM.Profile</span></span>
* <span data-ttu-id="f9ebf-107">Ki lett javítva az a hiba, amelyben a „Clear-AzureRmContext” futtatása egy üres környezetet tartott meg az előző alapértelmezett környezet nevével, így a felhasználó nem tudott létrehozni új környezetet a régi néven</span><span class="sxs-lookup"><span data-stu-id="f9ebf-107">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="f9ebf-108">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f9ebf-108">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="f9ebf-109">Az átjárók társítási/társításmegszüntetési műveleteinek engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="f9ebf-109">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="f9ebf-110">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f9ebf-110">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="f9ebf-111">Az ApiVersion, ApiRelease és ApiRevision paraméterek mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="f9ebf-111">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="f9ebf-112">A Service Fabric háttérrendszer mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="f9ebf-112">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="f9ebf-113">Az Application Insights naplózó mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="f9ebf-113">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="f9ebf-114">Az „Alapszintű” termékváltozat érvényes termékváltozatként való elismerése mostantól támogatott az API Management szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="f9ebf-114">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="f9ebf-115">A privát hitelesítésszolgáltató által kiállított tanúsítványok fő- vagy hitelesítésszolgáltatói tanúsítványként való telepítése mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="f9ebf-115">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="f9ebf-116">Az egyéni SSL-tanúsítványok KeyVault- és többproxys gazdaneveken keresztüli fogadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="f9ebf-116">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="f9ebf-117">Az MSI-identitások mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="f9ebf-117">Added support for MSI identity</span></span>
* <span data-ttu-id="f9ebf-118">A házirendek URL-kapcsolaton keresztüli fogadása mostantól támogatott MEGJEGYZÉS: A következő parancsmagok elavulttá válnak a jövőbeli kiadásokban</span><span class="sxs-lookup"><span data-stu-id="f9ebf-118">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="f9ebf-119">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="f9ebf-119">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="f9ebf-120">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9ebf-120">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="f9ebf-121">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="f9ebf-121">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="f9ebf-122">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="f9ebf-122">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="f9ebf-123">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="f9ebf-123">AzureRM.Batch</span></span>
* <span data-ttu-id="f9ebf-124">Új Get-AzureBatchPoolNodeCounts parancsmag kiadása</span><span class="sxs-lookup"><span data-stu-id="f9ebf-124">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="f9ebf-125">Új Start-AzureBatchComputeNodeServiceLogUpload parancsmag kiadása</span><span class="sxs-lookup"><span data-stu-id="f9ebf-125">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="f9ebf-126">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="f9ebf-126">AzureRM.Consumption</span></span>
* <span data-ttu-id="f9ebf-127">A Get-AzureRmConsumptionUsageDetail parancsmag kiegészítése új Expand, ResourceGroup, InstanceName, InstanceId, Tags és Top paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="f9ebf-127">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="f9ebf-128">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f9ebf-128">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="f9ebf-129">Az Export-AzureRmDataLakeStoreChildItemProperties példájának kijavítása</span><span class="sxs-lookup"><span data-stu-id="f9ebf-129">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="f9ebf-130">A Set-AzureRmDataLakeStoreItemAclEntry Recurse esetében fellépő null paraméter kivétel kijavítása</span><span class="sxs-lookup"><span data-stu-id="f9ebf-130">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="f9ebf-131">A Set-AzureRmDataLakeStoreItemAclEntry, a Set-AzureRmDataLakeStoreItemAcl és a Remove-AzureRmDataLakeStoreItemAclEntry súgófájljainak javítása</span><span class="sxs-lookup"><span data-stu-id="f9ebf-131">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="f9ebf-132">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f9ebf-132">AzureRM.Network</span></span>
* <span data-ttu-id="f9ebf-133">A hálózati SDK-verzió felléptetése a 18.0.0-s előzetes verzióról a 19.0.0-s előzetes verzióra</span><span class="sxs-lookup"><span data-stu-id="f9ebf-133">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="f9ebf-134">Új parancsmag hozzáadva a protokollkonfigurációk létrehozásához</span><span class="sxs-lookup"><span data-stu-id="f9ebf-134">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="f9ebf-135">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9ebf-135">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="f9ebf-136">Új parancsmag hozzáadva az új kapcsolatcsoportok hozzáadásához a meglévő ExpressRoute-kapcsolatcsoportokhoz.</span><span class="sxs-lookup"><span data-stu-id="f9ebf-136">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="f9ebf-137">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f9ebf-137">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="f9ebf-138">Új parancsmag hozzáadva a kapcsolatcsoportok eltávolításához a meglévő ExpressRoute-kapcsolatcsoportokból.</span><span class="sxs-lookup"><span data-stu-id="f9ebf-138">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="f9ebf-139">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f9ebf-139">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="f9ebf-140">Új parancsmag hozzáadva a kapcsolatcsoportok lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="f9ebf-140">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="f9ebf-141">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f9ebf-141">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="f9ebf-142">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f9ebf-142">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="f9ebf-143">A kiszolgálói hitelesítés létrehozott tanúsítványokkal való használata (5998. sz. hiba) ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="f9ebf-143">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="f9ebf-144">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f9ebf-144">AzureRM.Sql</span></span>
* <span data-ttu-id="f9ebf-145">A frissített naplózási parancsmagok lehetővé teszik az AuditAction és AuditActionGroup paraméterek eltávolítását</span><span class="sxs-lookup"><span data-stu-id="f9ebf-145">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="f9ebf-146">A Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy hibája ki lett javítva, amikor az új rugalmas adatmegőrzési szabályzatok megadásakor a parancs a következő hibát adta vissza: „A hosszútávú adatmegőrzési szabályzat megadása Azure Recovery Services-tárolókkal és szabályzatokkal már nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="f9ebf-146">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="f9ebf-147">Adja le a kérést az új rugalmas adatmegőrzési szabályzattal”.</span><span class="sxs-lookup"><span data-stu-id="f9ebf-147">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="f9ebf-148">Az összes Azure SQL Database/ElasticPool létrehozással/frissítéssel kapcsolatos parancsmag frissítve lett az új Database API használatára, amely támogatja a termékváltozat tulajdonságot a méretezéssel és szintekkel kapcsolatos tulajdonságok esetében.</span><span class="sxs-lookup"><span data-stu-id="f9ebf-148">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="f9ebf-149">A frissített parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="f9ebf-149">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="f9ebf-150">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f9ebf-150">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="f9ebf-151">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f9ebf-151">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="f9ebf-152">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="f9ebf-152">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="f9ebf-153">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f9ebf-153">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="f9ebf-154">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f9ebf-154">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="f9ebf-155">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f9ebf-155">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="f9ebf-156">A Get-AzureRmTrafficManagerProfile paramétereinek frissítésével a -ResourceGroupName paraméter megadása mostantól kötelező a -Name paraméter használata esetén.</span><span class="sxs-lookup"><span data-stu-id="f9ebf-156">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>