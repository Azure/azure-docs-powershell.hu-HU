---
title: Az Azure PowerShell változásnaplója | Microsoft Docs
description: Az alábbiakban az Azure PowerShell legutóbbi kiadásában végrehajtott módosítások előzményei olvashatók.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.openlocfilehash: eec8b5960f787fa9ca1130b4f8b49c9d896aa99e
ms.sourcegitcommit: 1f699b72bf544d92459da9d888cc0091f9415b65
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/06/2018
ms.locfileid: "50971975"
---
# <a name="release-notes"></a><span data-ttu-id="a86f8-103">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="a86f8-103">Release notes</span></span>

<span data-ttu-id="a86f8-104">Az alábbiakban az Azure PowerShell jelen kiadásában végrehajtott módosítások listája olvasható.</span><span class="sxs-lookup"><span data-stu-id="a86f8-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6110---october-2018"></a><span data-ttu-id="a86f8-105">6.11.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="a86f8-105">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a86f8-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a86f8-106">AzureRM.Profile</span></span>
* <span data-ttu-id="a86f8-107">Ki lett javítva a Get-AzureRmSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="a86f8-107">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="a86f8-108">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="a86f8-108">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="a86f8-109">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="a86f8-109">AzureRM.Backup</span></span>
* <span data-ttu-id="a86f8-110">Elavult Azure Backup-parancsmagok.</span><span class="sxs-lookup"><span data-stu-id="a86f8-110">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a86f8-111">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a86f8-111">AzureRM.Compute</span></span>
* <span data-ttu-id="a86f8-112">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a New-AzureRmVm parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="a86f8-112">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="a86f8-113">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="a86f8-113">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a86f8-114">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a86f8-114">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a86f8-115">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="a86f8-115">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="a86f8-116">Get-AzureRmDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="a86f8-116">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="a86f8-117">Add-AzureRmDataLakeStoreVirtualNetworkRule: A virtuális hálózati szabályt hozzáadja a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="a86f8-117">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a86f8-118">Set-AzureRmDataLakeStoreVirtualNetworkRule: Módosítja a kiválasztott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="a86f8-118">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a86f8-119">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="a86f8-119">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a86f8-120">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a86f8-120">AzureRM.Network</span></span>
* <span data-ttu-id="a86f8-121">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="a86f8-121">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="a86f8-122">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="a86f8-122">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a86f8-123">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a86f8-123">AzureRM.Resources</span></span>
* <span data-ttu-id="a86f8-124">Egy értelmezhető kivétel forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat eseteket, amelyekben a Get-AzureRMRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="a86f8-124">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="a86f8-125">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="a86f8-125">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="a86f8-126">6.10.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="a86f8-126">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="a86f8-127">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a86f8-127">Azure.Storage</span></span>
* <span data-ttu-id="a86f8-128">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="a86f8-128">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="a86f8-129">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a86f8-129">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="a86f8-130">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a86f8-130">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="a86f8-131">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a86f8-131">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="a86f8-132">A Get-AzureRmCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="a86f8-132">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a86f8-133">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a86f8-133">AzureRM.Compute</span></span>
* <span data-ttu-id="a86f8-134">Ki lett javítva a Get-AzureRmVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon</span><span class="sxs-lookup"><span data-stu-id="a86f8-134">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="a86f8-135">A SimpleParameterSet egy példája hozzá lett adva a New-AzureRmVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="a86f8-135">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="a86f8-136">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="a86f8-136">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="a86f8-137">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a86f8-137">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="a86f8-138">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="a86f8-138">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a86f8-139">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a86f8-139">AzureRM.Network</span></span>
* <span data-ttu-id="a86f8-140">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="a86f8-140">Added NetworkProfile functionality.</span></span> <span data-ttu-id="a86f8-141">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a86f8-141">new cmdlets added</span></span>
    - <span data-ttu-id="a86f8-142">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a86f8-142">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="a86f8-143">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a86f8-143">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="a86f8-144">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a86f8-144">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="a86f8-145">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a86f8-145">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="a86f8-146">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="a86f8-146">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="a86f8-147">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="a86f8-147">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="a86f8-148">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="a86f8-148">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="a86f8-149">Hozzá lett adva a New-AzureRmVirtualNetworkTap, a Get-AzureRmVirtualNetworkTap, a Set-AzureRmVirtualNetworkTap és a Remove-AzureRmVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="a86f8-149">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="a86f8-150">Hozzá lett adva a Set-AzureRmNEtworkInterfaceTapConfig, a Get-AzureRmNEtworkInterfaceTapConfig és a Remove-AzureRmNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="a86f8-150">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="a86f8-151">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a86f8-151">AzureRM.RedisCache</span></span>
* <span data-ttu-id="a86f8-152">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="a86f8-152">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="a86f8-153">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="a86f8-153">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a86f8-154">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a86f8-154">AzureRM.Resources</span></span>
* <span data-ttu-id="a86f8-155">A hiányzó -Mode paraméter hozzá lett adva a Set-AzureRmPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a86f8-155">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="a86f8-156">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzureRmProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="a86f8-156">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a86f8-157">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a86f8-157">AzureRM.Sql</span></span>
* <span data-ttu-id="a86f8-158">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="a86f8-158">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="a86f8-159">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="a86f8-159">AzureRM.Storage</span></span>
* <span data-ttu-id="a86f8-160">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="a86f8-160">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="a86f8-161">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="a86f8-161">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a86f8-162">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a86f8-162">AzureRM.Websites</span></span>
* <span data-ttu-id="a86f8-163">Új Get-AzureRMWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhook URL-címét</span><span class="sxs-lookup"><span data-stu-id="a86f8-163">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="a86f8-164">Új New-AzureRMWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="a86f8-164">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="a86f8-165">6.9.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="a86f8-165">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a86f8-166">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="a86f8-166">General</span></span>
* <span data-ttu-id="a86f8-167">Az AzureRM.SignalR hozzáadva az AzureRM összesített modulhoz</span><span class="sxs-lookup"><span data-stu-id="a86f8-167">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="a86f8-168">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a86f8-168">AzureRM.Profile</span></span>
* <span data-ttu-id="a86f8-169">Kisebb módosítások a tárolók általános kódjában</span><span class="sxs-lookup"><span data-stu-id="a86f8-169">Minor changes to the storage common code</span></span>
* <span data-ttu-id="a86f8-170">Teljes paramétertípusokkal frissült súgófájlok</span><span class="sxs-lookup"><span data-stu-id="a86f8-170">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="a86f8-171">A -ServicePrincipal módosítása nem kötelezőre a ServicePrincipalCertificateWithSubscriptionId paraméterkészletben</span><span class="sxs-lookup"><span data-stu-id="a86f8-171">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="a86f8-172">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a86f8-172">Azure.Storage</span></span>
* <span data-ttu-id="a86f8-173">Storage-környezet létrehozásának támogatása OAuth használatával.</span><span class="sxs-lookup"><span data-stu-id="a86f8-173">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="a86f8-174">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="a86f8-174">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="a86f8-175">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="a86f8-175">AzureRM.Cdn</span></span>
* <span data-ttu-id="a86f8-176">Standard_Microsoft hozzáadva a CDN-díjszabási termékváltozatban.</span><span class="sxs-lookup"><span data-stu-id="a86f8-176">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="a86f8-177">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a86f8-177">AzureRM.Compute</span></span>
* <span data-ttu-id="a86f8-178">A Key Vault és a Storage függőségeinek áthelyezése az általános függőségekhez</span><span class="sxs-lookup"><span data-stu-id="a86f8-178">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="a86f8-179">További virtuálisgép-méretek támogatása hozzáadva az AEM-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="a86f8-179">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="a86f8-180">A PublicIPPrefix paraméter hozzáadva a New-AzureRmVmssIpConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a86f8-180">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="a86f8-181">A ResourceId paraméter hozzáadva az Invoke-AzureRmVMRunCommand parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a86f8-181">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="a86f8-182">Az Invoke-AzureRmVmssVMRunCommand parancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a86f8-182">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="a86f8-183">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="a86f8-183">AzureRM.Dns</span></span>
* <span data-ttu-id="a86f8-184">Aliasrekord támogatása hozzáadva DNS-rekord létrehozása során</span><span class="sxs-lookup"><span data-stu-id="a86f8-184">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="a86f8-185">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="a86f8-185">AzureRM.Insights</span></span>
* <span data-ttu-id="a86f8-186">A 6833-as és a 7102-es hiba kijavítva (Diagnosztikai beállítások területe)</span><span class="sxs-lookup"><span data-stu-id="a86f8-186">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="a86f8-187">Az alapértelmezett név, például a „service” hibái a diagnosztikai beállítások megadása és listázása/lekérése során</span><span class="sxs-lookup"><span data-stu-id="a86f8-187">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="a86f8-188">Diagnosztikai beállítások kategóriákkal történő létrehozásának hibái</span><span class="sxs-lookup"><span data-stu-id="a86f8-188">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="a86f8-189">Elavulási üzenetek hozzáadva a metrikák időfelbontási szintjeinek paramétereihez</span><span class="sxs-lookup"><span data-stu-id="a86f8-189">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="a86f8-190">Az időfelbontási szintek paramétereit még elfogadja a rendszer (ez nem egy kompatibilitástörő változás), viszont figyelmen kívül hagyja a háttérrendszerben, mivel csak a PT1M érvényes</span><span class="sxs-lookup"><span data-stu-id="a86f8-190">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a86f8-191">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a86f8-191">AzureRM.Network</span></span>
* <span data-ttu-id="a86f8-192">A LoadBalancer parancsmagokat érintő változások</span><span class="sxs-lookup"><span data-stu-id="a86f8-192">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="a86f8-193">LoadBalancerInboundNatPoolConfig: az IdleTimeoutInMinutes, az EnableFloatingIp és az EnableTcpReset paraméterek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a86f8-193">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="a86f8-194">LoadBalancerInboundNatRuleConfig: az EnableTcpReset paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a86f8-194">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="a86f8-195">LoadBalancerRuleConfig: az EnableTcpReset paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a86f8-195">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="a86f8-196">LoadBalancerProbeConfig: a Protocol paraméterhez tartozó „Https” érték támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a86f8-196">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="a86f8-197">Új parancsok hozzáadva a LoadBalancer új, OutboundRule nevű alerőforrásához</span><span class="sxs-lookup"><span data-stu-id="a86f8-197">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="a86f8-198">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a86f8-198">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="a86f8-199">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a86f8-199">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="a86f8-200">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a86f8-200">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="a86f8-201">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a86f8-201">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="a86f8-202">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a86f8-202">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="a86f8-203">Új HostedWorkloads tulajdonság hozzáadva a PSNetworkInterface-hez</span><span class="sxs-lookup"><span data-stu-id="a86f8-203">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="a86f8-204">Új parancsmagok hozzáadva a következő szolgáltatáshoz: Azure Firewall ARM-en keresztül</span><span class="sxs-lookup"><span data-stu-id="a86f8-204">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="a86f8-205">Get-AzureRmFirewall hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a86f8-205">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="a86f8-206">Set-AzureRmFirewall hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a86f8-206">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="a86f8-207">New-AzureRmFirewall hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a86f8-207">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="a86f8-208">Remove-AzureRmFirewall hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a86f8-208">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="a86f8-209">New-AzureRmFirewallApplicationRuleCollection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a86f8-209">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="a86f8-210">New-AzureRmFirewallApplicationRule hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a86f8-210">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="a86f8-211">New-AzureRmFirewallNatRuleCollection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a86f8-211">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="a86f8-212">New-AzureRmFirewallNatRule hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a86f8-212">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="a86f8-213">New-AzureRmFirewallNetworkRuleCollection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a86f8-213">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="a86f8-214">New-AzureRmFirewallNetworkRule hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a86f8-214">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="a86f8-215">Támogatás hozzáadva a megbízható főtanúsítványokhoz és az automatikus skálázás konfigurálásához az Application Gatewayben</span><span class="sxs-lookup"><span data-stu-id="a86f8-215">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="a86f8-216">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="a86f8-216">New Cmdlets added:</span></span>
      - <span data-ttu-id="a86f8-217">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a86f8-217">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="a86f8-218">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a86f8-218">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="a86f8-219">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a86f8-219">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="a86f8-220">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a86f8-220">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="a86f8-221">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a86f8-221">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="a86f8-222">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a86f8-222">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="a86f8-223">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a86f8-223">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="a86f8-224">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a86f8-224">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="a86f8-225">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a86f8-225">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="a86f8-226">Parancsmagok frissítve a -TrustedRootCertificate nevű, nem kötelező paraméterrel</span><span class="sxs-lookup"><span data-stu-id="a86f8-226">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="a86f8-227">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a86f8-227">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="a86f8-228">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a86f8-228">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="a86f8-229">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a86f8-229">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="a86f8-230">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a86f8-230">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="a86f8-231">Parancsmagok frissítve az -AutoscaleConfiguration nevű, nem kötelező paraméterrel</span><span class="sxs-lookup"><span data-stu-id="a86f8-231">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="a86f8-232">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a86f8-232">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="a86f8-233">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a86f8-233">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="a86f8-234">A Get-AzureInterfaceEndpoint parancsmag hozzáadva a felhasználói felület végpontjához</span><span class="sxs-lookup"><span data-stu-id="a86f8-234">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="a86f8-235">Támogatás hozzáadva több címelőtaghoz egy alhálózaton belül</span><span class="sxs-lookup"><span data-stu-id="a86f8-235">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="a86f8-236">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="a86f8-236">Updated cmdlets:</span></span>
  - <span data-ttu-id="a86f8-237">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a86f8-237">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="a86f8-238">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a86f8-238">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="a86f8-239">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a86f8-239">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="a86f8-240">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a86f8-240">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="a86f8-241">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a86f8-241">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="a86f8-242">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a86f8-242">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="a86f8-243">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a86f8-243">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="a86f8-244">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a86f8-244">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="a86f8-245">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a86f8-245">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="a86f8-246">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a86f8-246">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="a86f8-247">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a86f8-247">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="a86f8-248">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a86f8-248">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="a86f8-249">New-AzureRmNetworkInterfaceIpConfig - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a86f8-249">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="a86f8-250">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="a86f8-250">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="a86f8-251">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="a86f8-251">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="a86f8-252">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a86f8-252">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="a86f8-253">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a86f8-253">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="a86f8-254">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a86f8-254">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="a86f8-255">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a86f8-255">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="a86f8-256">Alhálózat-delegálási parancsmagok hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="a86f8-256">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="a86f8-257">New-AzureRmDelegation: Létrehoz egy új delegálást, amelyet hozzá lehet adni egy alhálózathoz</span><span class="sxs-lookup"><span data-stu-id="a86f8-257">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="a86f8-258">Remove-AzureRmDelegation: Felvesz egy alhálózatot, és eltávolítja a megadott delegálási nevet az adott alhálózatból</span><span class="sxs-lookup"><span data-stu-id="a86f8-258">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="a86f8-259">Add-AzureRmDelegation: Felvesz egy alhálózatot, és eltávolítja a megadott szolgáltatásnevet az adott alhálózatból</span><span class="sxs-lookup"><span data-stu-id="a86f8-259">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="a86f8-260">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="a86f8-260">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="a86f8-261">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="a86f8-261">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="a86f8-262">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="a86f8-262">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="a86f8-263">A felügyelt lemezek támogatása</span><span class="sxs-lookup"><span data-stu-id="a86f8-263">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="a86f8-264">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a86f8-264">AzureRM.RedisCache</span></span>
* <span data-ttu-id="a86f8-265">Insights-függőség frissítve</span><span class="sxs-lookup"><span data-stu-id="a86f8-265">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a86f8-266">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a86f8-266">AzureRM.Resources</span></span>
* <span data-ttu-id="a86f8-267">A New-AzureRmResourceGroupDeployment frissítve az új RollbackAction paraméterrel</span><span class="sxs-lookup"><span data-stu-id="a86f8-267">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="a86f8-268">Az OnErrorDeployment támogatása az új paraméterrel</span><span class="sxs-lookup"><span data-stu-id="a86f8-268">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="a86f8-269">A felügyelt identitás támogatása a szabályzat-hozzárendeléseknél</span><span class="sxs-lookup"><span data-stu-id="a86f8-269">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="a86f8-270">Az alapértelmezett értékekkel rendelkező paraméterek már nem szükségesek a szabályzatok a New-AzureRmPolicyAssignmenttel történő hozzárendelésekor</span><span class="sxs-lookup"><span data-stu-id="a86f8-270">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="a86f8-271">Az új Get-AzureRmPolicyAlias parancsmag hozzáadva a szabályzataliasok lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="a86f8-271">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a86f8-272">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a86f8-272">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a86f8-273">A 7161-es hiba kijavítva</span><span class="sxs-lookup"><span data-stu-id="a86f8-273">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="a86f8-274">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="a86f8-274">AzureRM.SignalR</span></span>
* <span data-ttu-id="a86f8-275">Termékváltozatnevek frissítve Free_F1-re és Standard_S1-re</span><span class="sxs-lookup"><span data-stu-id="a86f8-275">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="a86f8-276">Verzió mező hozzáadva a PSSignalRResource objektumhoz, és kapcsolati sztring hozzáadva a PSSignalRKeys objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="a86f8-276">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="a86f8-277">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="a86f8-277">AzureRM.Storage</span></span>
* <span data-ttu-id="a86f8-278">Módosíthatatlansági szabályzat támogatva az AzureRM.Storage-ban</span><span class="sxs-lookup"><span data-stu-id="a86f8-278">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="a86f8-279">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a86f8-279">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="a86f8-280">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a86f8-280">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="a86f8-281">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a86f8-281">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="a86f8-282">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a86f8-282">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="a86f8-283">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a86f8-283">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="a86f8-284">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="a86f8-284">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="a86f8-285">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="a86f8-285">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="a86f8-286">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a86f8-286">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="a86f8-287">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a86f8-287">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="a86f8-288">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a86f8-288">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="a86f8-289">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a86f8-289">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a86f8-290">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a86f8-290">AzureRM.Websites</span></span>
* <span data-ttu-id="a86f8-291">Két új parancsmag hozzáadva: Get-AzureRmDeletedWebApp és Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="a86f8-291">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="a86f8-292">A New-AzureRmAppServicePlan -HyperV kapcsoló hozzáadva App Service-csomag létrehozásához Windows-tárolóval</span><span class="sxs-lookup"><span data-stu-id="a86f8-292">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="a86f8-293">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot – Új paraméterek (–ContainerRegistryUser sztring -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) hozzáadva Windows-tárolóalkalmazás létrehozásához és felügyeletéhez</span><span class="sxs-lookup"><span data-stu-id="a86f8-293">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="a86f8-294">6.8.1 – 2018. augusztus</span><span class="sxs-lookup"><span data-stu-id="a86f8-294">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a86f8-295">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="a86f8-295">General</span></span>
* <span data-ttu-id="a86f8-296">Ki lett javítva az alapértelmezett erőforráscsoportok beállításának hiányával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="a86f8-296">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="a86f8-297">Frissített közös futtatókörnyezeti szerelvények</span><span class="sxs-lookup"><span data-stu-id="a86f8-297">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="a86f8-298">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a86f8-298">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="a86f8-299">Ki lett javítva az alapértelmezett erőforráscsoportok beállításának hiányával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="a86f8-299">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="a86f8-300">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="a86f8-300">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="a86f8-301">Az Import-AzureRmApiManagementApi és az \*-AzureRmApiManagementCertificate parancsmagok már tudják kezelni a relatív elérési utakat</span><span class="sxs-lookup"><span data-stu-id="a86f8-301">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="a86f8-302">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="a86f8-302">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="a86f8-303">A CertificateInformation egy beállítható tulajdonság, amely a Set-AzureRmApiManagement parancsmag megfelelő működését biztosítja.</span><span class="sxs-lookup"><span data-stu-id="a86f8-303">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="a86f8-304">Javítva a nuget 4.0.4-es előzetes verziójára való frissítéssel</span><span class="sxs-lookup"><span data-stu-id="a86f8-304">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="a86f8-305">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="a86f8-305">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="a86f8-306">A termékben való név szerinti kereséshez tartozó Odata-szűrő kijavítva</span><span class="sxs-lookup"><span data-stu-id="a86f8-306">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="a86f8-307">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="a86f8-307">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="a86f8-308">Az API-ban való név szerinti kereséshez tartozó Odata-szűrő kijavítva</span><span class="sxs-lookup"><span data-stu-id="a86f8-308">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="a86f8-309">Az AzureMonitor támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a86f8-309">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="a86f8-310">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a86f8-310">AzureRM.Compute</span></span>
* <span data-ttu-id="a86f8-311">Ki lett javítva a hibakimenetből hiányzó céllal kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="a86f8-311">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="a86f8-312">Ki lett javítva a felügyelt lemezekkel rendelkező virtuális gépek tárfióktípusával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="a86f8-312">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="a86f8-313">Ki lett javítva az alapértelmezett erőforráscsoportok beállításának hiányával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="a86f8-313">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="a86f8-314">Ki lettek javítva az AEM Extension-parancsmagok az egyéb környezetekben (pl. Azure China)</span><span class="sxs-lookup"><span data-stu-id="a86f8-314">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a86f8-315">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a86f8-315">AzureRM.Network</span></span>
* <span data-ttu-id="a86f8-316">A parancsmagkimenetek alapértelmezett ábrázolása táblanézetre módosítva</span><span class="sxs-lookup"><span data-stu-id="a86f8-316">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="a86f8-317">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a86f8-317">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="a86f8-318">Ki lett javítva az a hiba, amely az Update-AzureRmPowerBIEmbeddedCapacity kapcsán jelentkezett a felfüggesztett kapacitás méretezésére tett kísérlet során</span><span class="sxs-lookup"><span data-stu-id="a86f8-318">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="a86f8-319">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a86f8-319">AzureRM.Resources</span></span>
* <span data-ttu-id="a86f8-320">Ki lett javítva a felügyelt alkalmazások Marketplace-ről való létrehozásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="a86f8-320">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a86f8-321">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a86f8-321">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a86f8-322">Hibák kijavítva:</span><span class="sxs-lookup"><span data-stu-id="a86f8-322">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a86f8-323">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a86f8-323">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a86f8-324">A MultiValue útválasztási módszer támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a86f8-324">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="a86f8-325">Új paraméter A MultiValue-útválasztáshoz: MaxReturn</span><span class="sxs-lookup"><span data-stu-id="a86f8-325">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="a86f8-326">Az alhálózati útválasztási módszer támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a86f8-326">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="a86f8-327">IP-címtartományok (alhálózatok) támogatása a végpontokon</span><span class="sxs-lookup"><span data-stu-id="a86f8-327">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="a86f8-328">Egyéni fejlécek profilokban való támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a86f8-328">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="a86f8-329">Várt állapotkód-tartományok profilokban való támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a86f8-329">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="a86f8-330">Egyéni fejlécek végpontokon való támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a86f8-330">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="a86f8-331">6.8.0 – 2018. augusztus</span><span class="sxs-lookup"><span data-stu-id="a86f8-331">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a86f8-332">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="a86f8-332">General</span></span>
* <span data-ttu-id="a86f8-333">Ki lett javítva az alapértelmezett erőforráscsoportok beállításának hiányával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="a86f8-333">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="a86f8-334">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a86f8-334">AzureRM.Profile</span></span>
* <span data-ttu-id="a86f8-335">Lejárati tulajdonság hozzáadva a Connect-AzureRmAccount során visszaadott jogkivonatokhoz</span><span class="sxs-lookup"><span data-stu-id="a86f8-335">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a86f8-336">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a86f8-336">AzureRM.Compute</span></span>
* <span data-ttu-id="a86f8-337">Ki lett javítva a hibakimenetből hiányzó céllal kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="a86f8-337">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="a86f8-338">Ki lett javítva a felügyelt lemezekkel rendelkező virtuális gépek tárfióktípusával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="a86f8-338">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="a86f8-339">Ki lettek javítva az AEM Extension-parancsmagok az egyéb környezetekben (pl. Azure China)</span><span class="sxs-lookup"><span data-stu-id="a86f8-339">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="a86f8-340">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="a86f8-340">AzureRM.IotHub</span></span>
* <span data-ttu-id="a86f8-341">Ki lettek javítva a New-AzureRmIotHubExportDevices és a New-AzureRmIotHubImportDevices példái</span><span class="sxs-lookup"><span data-stu-id="a86f8-341">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a86f8-342">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a86f8-342">AzureRM.Network</span></span>
* <span data-ttu-id="a86f8-343">Az alapértelmezett modellek ábrázolása módosítva táblázatos nézetre</span><span class="sxs-lookup"><span data-stu-id="a86f8-343">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="a86f8-344">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a86f8-344">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="a86f8-345">Ki lett javítva az a hiba, amely az Update-AzureRmPowerBIEmbeddedCapacity kapcsán jelentkezett a felfüggesztett kapacitás méretezésére tett kísérlet során</span><span class="sxs-lookup"><span data-stu-id="a86f8-345">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a86f8-346">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a86f8-346">AzureRM.Resources</span></span>
* <span data-ttu-id="a86f8-347">Ki lett javítva a felügyelt alkalmazások MarketPlace-ről való létrehozásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="a86f8-347">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a86f8-348">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a86f8-348">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a86f8-349">Problémák megoldása</span><span class="sxs-lookup"><span data-stu-id="a86f8-349">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a86f8-350">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a86f8-350">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a86f8-351">A MultiValue útválasztási módszer támogatása</span><span class="sxs-lookup"><span data-stu-id="a86f8-351">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="a86f8-352">Új paraméter A MultiValue-útválasztáshoz: MaxReturn</span><span class="sxs-lookup"><span data-stu-id="a86f8-352">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="a86f8-353">A Subnet útválasztási módszer támogatása</span><span class="sxs-lookup"><span data-stu-id="a86f8-353">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="a86f8-354">IP-címtartományok (alhálózatok) támogatása a végpontokon</span><span class="sxs-lookup"><span data-stu-id="a86f8-354">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="a86f8-355">Egyéni fejlécek támogatása a profilokban</span><span class="sxs-lookup"><span data-stu-id="a86f8-355">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="a86f8-356">Várt állapotkód-tartományok támogatása a profilokban</span><span class="sxs-lookup"><span data-stu-id="a86f8-356">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="a86f8-357">Egyéni fejlécek támogatása a végpontokon</span><span class="sxs-lookup"><span data-stu-id="a86f8-357">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a86f8-358">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a86f8-358">AzureRM.Websites</span></span>
* <span data-ttu-id="a86f8-359">Ki lett javítva az alapértelmezett erőforráscsoportok helytelen beállításával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="a86f8-359">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="a86f8-360">6.7.0 – 2018. augusztus</span><span class="sxs-lookup"><span data-stu-id="a86f8-360">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a86f8-361">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a86f8-361">AzureRM.Profile</span></span>
* <span data-ttu-id="a86f8-362">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-362">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="a86f8-363">A környezetek ütközésének elkerülése érdekében a felhasználói azonosító hozzá lett adva az alapértelmezett környezetnévhez</span><span class="sxs-lookup"><span data-stu-id="a86f8-363">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="a86f8-364">A Clear-AzureRmContext környezetek kiválasztásával kapcsolatos hibáinak javítása #6398</span><span class="sxs-lookup"><span data-stu-id="a86f8-364">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="a86f8-365">A bérlői tartomány a -TenantId paraméternek történő átadásának engedélyezése a Connect-AzureRmAccount esetén</span><span class="sxs-lookup"><span data-stu-id="a86f8-365">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="a86f8-366">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a86f8-366">Azure.Storage</span></span>
* <span data-ttu-id="a86f8-367">Az 5 TB-os korlátozás feloldása Azure-fájlmegosztási kvóta esetén</span><span class="sxs-lookup"><span data-stu-id="a86f8-367">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="a86f8-368">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="a86f8-368">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="a86f8-369">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a86f8-369">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="a86f8-370">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-370">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="a86f8-371">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a86f8-371">Azure.AnalysisServices</span></span>
* <span data-ttu-id="a86f8-372">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-372">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="a86f8-373">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a86f8-373">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="a86f8-374">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-374">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="a86f8-375">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="a86f8-375">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="a86f8-376">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-376">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="a86f8-377">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="a86f8-377">AzureRM.Automation</span></span>
* <span data-ttu-id="a86f8-378">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-378">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="a86f8-379">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="a86f8-379">AzureRM.Backup</span></span>
* <span data-ttu-id="a86f8-380">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-380">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="a86f8-381">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="a86f8-381">AzureRM.Batch</span></span>
* <span data-ttu-id="a86f8-382">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-382">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="a86f8-383">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="a86f8-383">AzureRM.Billing</span></span>
* <span data-ttu-id="a86f8-384">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-384">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="a86f8-385">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="a86f8-385">AzureRM.Cdn</span></span>
* <span data-ttu-id="a86f8-386">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-386">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="a86f8-387">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a86f8-387">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="a86f8-388">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-388">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a86f8-389">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a86f8-389">AzureRM.Compute</span></span>
* <span data-ttu-id="a86f8-390">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-390">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="a86f8-391">Az EvictionPolicy paraméter hozzá lett adva a New-AzureRmVmssConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a86f8-391">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="a86f8-392">Az alapértelmezett hely használata a New-AzureRmVm DiskFileParameterSet paraméterében, ha nincs megadva hely.</span><span class="sxs-lookup"><span data-stu-id="a86f8-392">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="a86f8-393">A paraméter leírásának javítása a Save-AzureRmVMImage esetén</span><span class="sxs-lookup"><span data-stu-id="a86f8-393">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="a86f8-394">A Get-AzureRmVMDiskEncryptionStatus parancsmag javítása bizonyos egyetlen menetes helyzetekben</span><span class="sxs-lookup"><span data-stu-id="a86f8-394">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="a86f8-395">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="a86f8-395">AzureRM.Consumption</span></span>
* <span data-ttu-id="a86f8-396">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="a86f8-397">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a86f8-397">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="a86f8-398">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-398">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="a86f8-399">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a86f8-399">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="a86f8-400">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-400">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="a86f8-401">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="a86f8-401">AzureRM.DataFactories</span></span>
* <span data-ttu-id="a86f8-402">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-402">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="a86f8-403">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a86f8-403">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="a86f8-404">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-404">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="a86f8-405">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="a86f8-405">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="a86f8-406">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a86f8-407">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a86f8-407">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a86f8-408">A hibakeresés javítása olyan esetekben, amikor a DebugPreference a PowerShell-parancssorból van beállítva</span><span class="sxs-lookup"><span data-stu-id="a86f8-408">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="a86f8-409">Példa frissítve a Set-AzureRmDataLakeStoreItemAcl esetén</span><span class="sxs-lookup"><span data-stu-id="a86f8-409">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="a86f8-410">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-410">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="a86f8-411">Példa frissítve a Set-AzureRmDataLakeStoreItemAclEntry esetén</span><span class="sxs-lookup"><span data-stu-id="a86f8-411">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="a86f8-412">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="a86f8-412">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="a86f8-413">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-413">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="a86f8-414">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="a86f8-414">AzureRM.Dns</span></span>
* <span data-ttu-id="a86f8-415">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-415">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="a86f8-416">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a86f8-416">AzureRM.EventGrid</span></span>
* <span data-ttu-id="a86f8-417">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-417">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="a86f8-418">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="a86f8-418">AzureRM.EventHub</span></span>
* <span data-ttu-id="a86f8-419">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-419">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="a86f8-420">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a86f8-420">AzureRM.HDInsight</span></span>
* <span data-ttu-id="a86f8-421">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-421">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="a86f8-422">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="a86f8-422">AzureRM.Insights</span></span>
* <span data-ttu-id="a86f8-423">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-423">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="a86f8-424">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="a86f8-424">AzureRM.IotHub</span></span>
* <span data-ttu-id="a86f8-425">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-425">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a86f8-426">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a86f8-426">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a86f8-427">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="a86f8-428">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a86f8-428">AzureRM.LogicApp</span></span>
* <span data-ttu-id="a86f8-429">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="a86f8-430">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a86f8-430">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="a86f8-431">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="a86f8-432">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="a86f8-432">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="a86f8-433">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="a86f8-434">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a86f8-434">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="a86f8-435">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="a86f8-436">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="a86f8-436">AzureRM.Media</span></span>
* <span data-ttu-id="a86f8-437">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-437">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a86f8-438">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a86f8-438">AzureRM.Network</span></span>
* <span data-ttu-id="a86f8-439">Példa hozzáadva a Set-AzureRmLocalNetworkGateway esetén</span><span class="sxs-lookup"><span data-stu-id="a86f8-439">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="a86f8-440">Példák és leírások hozzáadva az Add-AzureRmVirtualNetworkGatewayIpConfig, a Get-AzureRmVirtualNetworkGatewayConnectionSharedKey és a New-AzureRmVirtualNetworkGatewayConnection esetén</span><span class="sxs-lookup"><span data-stu-id="a86f8-440">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="a86f8-441">Példák hozzáadva a Remove-AzureRmVirtualNetworkGatewayIpConfig és a Reset-AzureRmVirtualNetworkGateway esetén</span><span class="sxs-lookup"><span data-stu-id="a86f8-441">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="a86f8-442">Példa hozzáadva a Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey esetén</span><span class="sxs-lookup"><span data-stu-id="a86f8-442">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="a86f8-443">Példa hozzáadva a Set-AzureRmVirtualNetworkGatewayConnectionSharedKey esetén</span><span class="sxs-lookup"><span data-stu-id="a86f8-443">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="a86f8-444">Példa hozzáadva a Set-AzureRmVirtualNetworkGatewayConnection esetén</span><span class="sxs-lookup"><span data-stu-id="a86f8-444">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="a86f8-445">Parancsmagok a legfrissebb kódgenerálóval történő újragenerálása az ApplicationSecurityGroup, a RouteTable és a Usage esetén</span><span class="sxs-lookup"><span data-stu-id="a86f8-445">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="a86f8-446">Hibaüzenet pontosítva a Get-AzureRmVirtualNetworkSubnetConfig esetén egy nem létező alhálózat lekérésére tett kísérletkor</span><span class="sxs-lookup"><span data-stu-id="a86f8-446">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="a86f8-447">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="a86f8-447">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="a86f8-448">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-448">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="a86f8-449">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a86f8-449">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="a86f8-450">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-450">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="a86f8-451">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a86f8-451">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="a86f8-452">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-452">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="a86f8-453">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a86f8-453">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="a86f8-454">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-454">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="a86f8-455">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a86f8-455">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="a86f8-456">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-456">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="a86f8-457">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a86f8-457">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a86f8-458">Szabályzatszűrő hozzáadva a Get-AzureRmRecoveryServicesBackItem parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="a86f8-458">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="a86f8-459">A parancs visszaadja azon biztonsági mentési elemek listáját, amelyek az adott szabályzatazonosító védelme alá tartoznak.</span><span class="sxs-lookup"><span data-stu-id="a86f8-459">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="a86f8-460">A Microsoft.Azure.Management.RecoveryServices.Backup frissítve a 3.0.0-preview verzióra.</span><span class="sxs-lookup"><span data-stu-id="a86f8-460">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="a86f8-461">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-461">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="a86f8-462">A TargetResourceGroupName paraméter hozzá lett adva a Restore-AzureRmRecoveryServicesBackupItem parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="a86f8-462">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="a86f8-463">A Managed Diskek visszaállítására kijelölt erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="a86f8-463">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="a86f8-464">Managed Diskkel rendelkező virtuális gépek biztonsági másolataira érvényes.</span><span class="sxs-lookup"><span data-stu-id="a86f8-464">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="a86f8-465">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="a86f8-465">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="a86f8-466">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-466">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="a86f8-467">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a86f8-467">AzureRM.RedisCache</span></span>
* <span data-ttu-id="a86f8-468">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-468">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="a86f8-469">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="a86f8-469">AzureRM.Relay</span></span>
* <span data-ttu-id="a86f8-470">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-470">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a86f8-471">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a86f8-471">AzureRM.Resources</span></span>
* <span data-ttu-id="a86f8-472">A sablonlapú üzembe helyezés támogatása előfizetési hatókörben.</span><span class="sxs-lookup"><span data-stu-id="a86f8-472">Support template deployment at subscription scope.</span></span> <span data-ttu-id="a86f8-473">Hozzáadott új parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="a86f8-473">Add new Cmdlets:</span></span>
    - <span data-ttu-id="a86f8-474">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a86f8-474">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="a86f8-475">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a86f8-475">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="a86f8-476">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a86f8-476">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="a86f8-477">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a86f8-477">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="a86f8-478">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a86f8-478">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="a86f8-479">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="a86f8-479">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="a86f8-480">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="a86f8-480">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="a86f8-481">Egy hiba javítása, amely során hibaüzenet jelenik meg, ha a Set-AzureRmResource felé egy környezetet továbbítanak</span><span class="sxs-lookup"><span data-stu-id="a86f8-481">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="a86f8-482">Példa javítva a New-AzureRmResourceGroupDeployment esetén</span><span class="sxs-lookup"><span data-stu-id="a86f8-482">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="a86f8-483">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="a86f8-484">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="a86f8-484">AzureRM.Scheduler</span></span>
* <span data-ttu-id="a86f8-485">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a86f8-486">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a86f8-486">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a86f8-487">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-487">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="a86f8-488">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a86f8-488">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="a86f8-489">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-489">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a86f8-490">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a86f8-490">AzureRM.Sql</span></span>
* <span data-ttu-id="a86f8-491">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-491">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="a86f8-492">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="a86f8-492">AzureRM.Storage</span></span>
* <span data-ttu-id="a86f8-493">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-493">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="a86f8-494">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="a86f8-494">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="a86f8-495">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-495">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="a86f8-496">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="a86f8-496">AzureRM.Tags</span></span>
* <span data-ttu-id="a86f8-497">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-497">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a86f8-498">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a86f8-498">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a86f8-499">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-499">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="a86f8-500">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="a86f8-500">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="a86f8-501">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-501">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a86f8-502">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a86f8-502">AzureRM.Websites</span></span>
* <span data-ttu-id="a86f8-503">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-503">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="a86f8-504">6.6.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="a86f8-504">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a86f8-505">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="a86f8-505">General</span></span>
* <span data-ttu-id="a86f8-506">Frissültek a súgófájlok, hogy minden paramétertípust és a helyes kimeneti/bemeneti típusokat tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="a86f8-506">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="a86f8-507">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a86f8-507">AzureRM.Profile</span></span>
* <span data-ttu-id="a86f8-508">Frissült a Common.Strategy kódtár, így ellenőrizni lehet, hogy az erőforrás jelenlegi konfigurációja kompatibilis-e a célerőforrással.</span><span class="sxs-lookup"><span data-stu-id="a86f8-508">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="a86f8-509">A Common.Storage új ps1xml-típusokkal egészült ki</span><span class="sxs-lookup"><span data-stu-id="a86f8-509">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="a86f8-510">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a86f8-510">Azure.Storage</span></span>
* <span data-ttu-id="a86f8-511">A Storage-környezet DefaultProfile használatával történő lekérésének támogatása</span><span class="sxs-lookup"><span data-stu-id="a86f8-511">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="a86f8-512">A Ps1XmlAttribute hozzá lett adva a parancsmagok kimeneti típusainak tulajdonságaihoz.</span><span class="sxs-lookup"><span data-stu-id="a86f8-512">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="a86f8-513">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a86f8-513">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="a86f8-514">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="a86f8-514">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="a86f8-515">Javítottuk az Automapper hibáját, amely a PsApiManagementApi ApiContractra történő fordítása során jelentkezett</span><span class="sxs-lookup"><span data-stu-id="a86f8-515">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="a86f8-516">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="a86f8-516">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="a86f8-517">Javítottuk a File.Save hibáját, hogy a kódolási típus ne terhelje túl</span><span class="sxs-lookup"><span data-stu-id="a86f8-517">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="a86f8-518">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="a86f8-518">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="a86f8-519">Frissült a 4.0.3-as Nuget-verzióra, amely felszámolta az apiId mintában jelentkező kivételeit</span><span class="sxs-lookup"><span data-stu-id="a86f8-519">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a86f8-520">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a86f8-520">AzureRM.Compute</span></span>
* <span data-ttu-id="a86f8-521">Javítottuk a hibát, amely miatt meghiúsult a virtuális gépek létrehozása a DiskFileParameterSet elemmel a New-AzureRmVm parancsmagban, mert átneveződött a PremiumLRS tárfiók típusa.</span><span class="sxs-lookup"><span data-stu-id="a86f8-521">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="a86f8-522">Javítottuk az Invoke-AzureRmVMRunCommand parancsmagot</span><span class="sxs-lookup"><span data-stu-id="a86f8-522">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="a86f8-523">Frissült a Get-AzureRmAvailabilitySet, hogy lehetővé váljon egy előfizetés összes rendelkezésre állási csoportjának listázása.</span><span class="sxs-lookup"><span data-stu-id="a86f8-523">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="a86f8-524">(A ResouceGroupName paraméter mostantól opcionális.)</span><span class="sxs-lookup"><span data-stu-id="a86f8-524">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="a86f8-525">Frissült a SimpleParameterSet a New-AzureRmVm parancsmagban, hogy engedélyezni lehessen a gyorsított hálózatot az arra alkalmas virtuális gépeken.</span><span class="sxs-lookup"><span data-stu-id="a86f8-525">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="a86f8-526">Frissült a New-AzureRmVmss egyszerű paraméterkészlet, hogy ne jöjjön létre vmss, ha egy felhasználó által megadott LB már létezik.</span><span class="sxs-lookup"><span data-stu-id="a86f8-526">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="a86f8-527">Frissült a New-AzureRmDisk példája</span><span class="sxs-lookup"><span data-stu-id="a86f8-527">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="a86f8-528">Hozzá lett adva egy, a New-AzureRmVM-re vonatkozó példa</span><span class="sxs-lookup"><span data-stu-id="a86f8-528">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="a86f8-529">Frissült a Set-AzureRmVMOSDisk leírása</span><span class="sxs-lookup"><span data-stu-id="a86f8-529">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="a86f8-530">Megfelelő helyesírással és előtaggal frissült a Set-AzureRmVMBginfoExtension 1. példája.</span><span class="sxs-lookup"><span data-stu-id="a86f8-530">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="a86f8-531">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a86f8-531">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="a86f8-532">Az ADF.Net SDK verziója 1.1.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="a86f8-532">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="a86f8-533">Támogatást kaptak az adat-előállítók között megosztott helyi integrációs modulok.</span><span class="sxs-lookup"><span data-stu-id="a86f8-533">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="a86f8-534">Hozzá lett adva a -SharedIntegrationRuntimeResourceId paraméter a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="a86f8-534">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="a86f8-535">Hozzá lett adva a -LinkedDataFactoryName paraméter a Remove-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="a86f8-535">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a86f8-536">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a86f8-536">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a86f8-537">A DataPlane SDK (Microsoft.Azure.DataLake.Store) verziója 1.1.9-re frissült</span><span class="sxs-lookup"><span data-stu-id="a86f8-537">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="a86f8-538">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="a86f8-538">AzureRM.EventHub</span></span>
* <span data-ttu-id="a86f8-539">Frissült az InputObject és a ResourceId átirányítása az eltávolítási parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="a86f8-539">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="a86f8-540">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="a86f8-540">AzureRM.Insights</span></span>
* <span data-ttu-id="a86f8-541">Javítottuk az OutputType formázását a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="a86f8-541">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="a86f8-542">A Microsoft.Azure.Management.Monitor SDK 0.19.1-es előzetes verziója elérhetővé vált</span><span class="sxs-lookup"><span data-stu-id="a86f8-542">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a86f8-543">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a86f8-543">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a86f8-544">Javítottuk a Set-AzureRmKeyVaultAccessPolicy átirányítási hibáját</span><span class="sxs-lookup"><span data-stu-id="a86f8-544">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a86f8-545">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a86f8-545">AzureRM.Network</span></span>
* <span data-ttu-id="a86f8-546">Új példák lettek hozzáadva a LoadBalancerInboundNatPoolConfig parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="a86f8-546">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a86f8-547">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a86f8-547">AzureRM.Resources</span></span>
* <span data-ttu-id="a86f8-548">Javítottuk a hibát, amely akkor jelentkezett, amikor a címke neve és értéke is meg lett adva a Get-AzureRmResource-hoz</span><span class="sxs-lookup"><span data-stu-id="a86f8-548">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="a86f8-549">Javítottuk a Set-AzureRmResource átirányítási forgatókönyvét</span><span class="sxs-lookup"><span data-stu-id="a86f8-549">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a86f8-550">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a86f8-550">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a86f8-551">Frissült az InputObject és a ResourceId átirányítása az eltávolítási parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="a86f8-551">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="a86f8-552">Kijavítottunk néhány hibát</span><span class="sxs-lookup"><span data-stu-id="a86f8-552">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="a86f8-553">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a86f8-553">AzureRM.Sql</span></span>
* <span data-ttu-id="a86f8-554">A következő parancsmagokkal támogatást biztosítottunk a kiszolgáló komplex veszélyforrások elleni védelméhez:</span><span class="sxs-lookup"><span data-stu-id="a86f8-554">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="a86f8-555">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a86f8-555">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="a86f8-556">A következő parancsmagokkal támogatást biztosítottunk a sebezhetőségi felméréshez:</span><span class="sxs-lookup"><span data-stu-id="a86f8-556">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="a86f8-557">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="a86f8-557">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="a86f8-558">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="a86f8-558">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="a86f8-559">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="a86f8-559">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="a86f8-560">Javítottuk a Remove-AzureRmSqlServerFirewallRule példáját</span><span class="sxs-lookup"><span data-stu-id="a86f8-560">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="a86f8-561">Javítottuk a dátum és idő helytelen kezelését a Get-AzureSqlSyncGroupLog USA-n kívüli kulturális környezeteiben</span><span class="sxs-lookup"><span data-stu-id="a86f8-561">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="a86f8-562">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="a86f8-562">AzureRM.Storage</span></span>
* <span data-ttu-id="a86f8-563">A Ps1XmlAttribute hozzá lett adva a parancsmagok kimeneti típusainak tulajdonságaihoz</span><span class="sxs-lookup"><span data-stu-id="a86f8-563">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="a86f8-564">A StorageAccount parancsmag kimenete táblanézetben is megjeleníthetővé vált</span><span class="sxs-lookup"><span data-stu-id="a86f8-564">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="a86f8-565">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a86f8-565">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="a86f8-566">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a86f8-566">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="a86f8-567">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a86f8-567">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="a86f8-568">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="a86f8-568">AzureRM.Tags</span></span>
* <span data-ttu-id="a86f8-569">El lett távolítva egy helytelen állítás a Tag parancsmag súgójából</span><span class="sxs-lookup"><span data-stu-id="a86f8-569">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="a86f8-570">6.5.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="a86f8-570">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a86f8-571">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a86f8-571">AzureRM.Profile</span></span>
* <span data-ttu-id="a86f8-572">A Get-AzureRmContextAutosaveSetting súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="a86f8-572">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="a86f8-573">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a86f8-573">Azure.Storage</span></span>
* <span data-ttu-id="a86f8-574">Blob vagy fájl feltöltésének támogatása csak írási SAS-jogkivonattal</span><span class="sxs-lookup"><span data-stu-id="a86f8-574">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="a86f8-575">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a86f8-575">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="a86f8-576">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a86f8-576">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="a86f8-577">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a86f8-577">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="a86f8-578">A kötelező ResourceGroupName tulajdonság hozzáadása az AS-hez.</span><span class="sxs-lookup"><span data-stu-id="a86f8-578">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="a86f8-579">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="a86f8-579">AzureRM.Automation</span></span>
* <span data-ttu-id="a86f8-580">A súgó frissítése és a New-AzureRMAutomationSchedule példájának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="a86f8-580">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a86f8-581">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a86f8-581">AzureRM.Compute</span></span>
* <span data-ttu-id="a86f8-582">A -Tag paraméter hozzáadása a következőhöz: Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a86f8-582">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="a86f8-583">Az Add-AzureRmVmssExtension példájának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="a86f8-583">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="a86f8-584">A Remove-AzureRmVmssExtension példáinak hozzáadása</span><span class="sxs-lookup"><span data-stu-id="a86f8-584">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="a86f8-585">A Set-AzureRmVMAccessExtension súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="a86f8-585">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="a86f8-586">A New-AzureRmVmss SimpleParameterSet készletének frissítése, hogy a SinglePlacementGroup alapértelmezés szerint false (hamis) legyen, és a SinglePlacementGroup kapcsolóparaméter hozzáadása, amellyel a felhasználó egyetlen elhelyezési csoportban hozhatja létre a VMSS-t.</span><span class="sxs-lookup"><span data-stu-id="a86f8-586">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="a86f8-587">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="a86f8-587">AzureRM.EventHub</span></span>
* <span data-ttu-id="a86f8-588">A csak olvasási PendingReplicationOperationsCount tulajdonság hozzáadása a PSEventHubDRConfigurationAttributes osztályhoz, amely megadja a függőben lévő replikációs műveletek számát a replikáció során</span><span class="sxs-lookup"><span data-stu-id="a86f8-588">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a86f8-589">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a86f8-589">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a86f8-590">A Set-AzureRmKeyVaultAccessPolicy hibaüzenetének frissítése</span><span class="sxs-lookup"><span data-stu-id="a86f8-590">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="a86f8-591">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a86f8-591">AzureRM.LogicApp</span></span>
* <span data-ttu-id="a86f8-592">„A paraméterkészlet nem oldható fel” hiba kijavítása a következőben: New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a86f8-592">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a86f8-593">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a86f8-593">AzureRM.Network</span></span>
* <span data-ttu-id="a86f8-594">Társviszony-létesítés engedélyezése több bérlőben lévő virtuális hálózatok között a következőhöz: Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="a86f8-594">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="a86f8-595">Az alábbi parancsmagok frissítése az Application Gatewayhez</span><span class="sxs-lookup"><span data-stu-id="a86f8-595">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="a86f8-596">New-AzureRmApplicationGateway: Hozzáadott EnableFIPS jelző és zónatámogatás</span><span class="sxs-lookup"><span data-stu-id="a86f8-596">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="a86f8-597">New-AzureRmApplicationGatewaySku: Hozzáadott új Standard_v2 és WAF_v2 SKU-k</span><span class="sxs-lookup"><span data-stu-id="a86f8-597">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="a86f8-598">Set-AzureRmApplicationGatewaySku: Hozzáadott új Standard_v2 és WAF_v2 SKU-k</span><span class="sxs-lookup"><span data-stu-id="a86f8-598">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="a86f8-599">A legújabb generátorverzióval újból létrehozott RouteTable parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a86f8-599">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="a86f8-600">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="a86f8-600">AzureRM.Relay</span></span>
* <span data-ttu-id="a86f8-601">Frissített Markdown-fájlok, a példában lévő paraméternév-hiba javítása</span><span class="sxs-lookup"><span data-stu-id="a86f8-601">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a86f8-602">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a86f8-602">AzureRM.Resources</span></span>
* <span data-ttu-id="a86f8-603">A Roleassignment és a roledefinition parancsmagok frissítése:</span><span class="sxs-lookup"><span data-stu-id="a86f8-603">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="a86f8-604">A felesleges roledefinition hívások eltávolítása a lapozás részeként.</span><span class="sxs-lookup"><span data-stu-id="a86f8-604">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="a86f8-605">A Get-AzureRmRoleAssignment parancsmag javítása</span><span class="sxs-lookup"><span data-stu-id="a86f8-605">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="a86f8-606">Az -ExpandPrincipalGroups parancsparaméter működésének javítása</span><span class="sxs-lookup"><span data-stu-id="a86f8-606">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="a86f8-607">A Get-AzureRmResource hibájának kijavítása, ahol a -ResourceType paraméter különbséget tett a kis- és nagybetűk között</span><span class="sxs-lookup"><span data-stu-id="a86f8-607">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a86f8-608">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a86f8-608">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a86f8-609">A top és skip paraméter hozzáadása a listázási parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="a86f8-609">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="a86f8-610">Standard – Prémium NameSpace migrálási parancsmagok hozzáadása:</span><span class="sxs-lookup"><span data-stu-id="a86f8-610">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="a86f8-611">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a86f8-611">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="a86f8-612">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a86f8-612">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="a86f8-613">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a86f8-613">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="a86f8-614">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a86f8-614">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="a86f8-615">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a86f8-615">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="a86f8-616">A csak olvasási PendingReplicationOperationsCount tulajdonság hozzáadása a PSServiceBusDRConfigurationAttributes osztályhoz, amely megadja a függőben lévő replikációs műveletek számát a replikáció során</span><span class="sxs-lookup"><span data-stu-id="a86f8-616">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="a86f8-617">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a86f8-617">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="a86f8-618">A New-AzureRmServiceFabricCluster példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="a86f8-618">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a86f8-619">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a86f8-619">AzureRM.Sql</span></span>
* <span data-ttu-id="a86f8-620">Új parancsmagok hozzáadása a Management.Sql elemhez, amelyekkel az ügyfelek TDE-tanúsítványt adhatnak az SQL Server-példányhoz vagy egy felügyelt példányhoz</span><span class="sxs-lookup"><span data-stu-id="a86f8-620">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="a86f8-621">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="a86f8-621">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="a86f8-622">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="a86f8-622">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a86f8-623">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a86f8-623">AzureRM.Websites</span></span>
* <span data-ttu-id="a86f8-624">A `Set-AzureRmWebApp -AssignIdentity` és `Set-AzureRmWebAppSlot -AssignIdentity` a false (hamis) érték esetén mostantól eltávolítja az Identitás tulajdonságot a hely object.Removing „előzetes verzió” címkéjéből is.</span><span class="sxs-lookup"><span data-stu-id="a86f8-624">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="a86f8-625">A `Get-AzureRmWebAppMetrics` és a `Get-AzureRmAppServicePlanMetrics` példa frissítése</span><span class="sxs-lookup"><span data-stu-id="a86f8-625">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="a86f8-626">A `Set-AzureRmWebApp -PhpVersion` támogatja az off értéket érvényes PHP-verzióként</span><span class="sxs-lookup"><span data-stu-id="a86f8-626">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="a86f8-627">6.4.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="a86f8-627">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a86f8-628">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="a86f8-628">General</span></span>
* <span data-ttu-id="a86f8-629">Az OutputType attribútum formázása javítva a legtöbb modul súgófájljaiban</span><span class="sxs-lookup"><span data-stu-id="a86f8-629">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="a86f8-630">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a86f8-630">AzureRM.Profile</span></span>
* <span data-ttu-id="a86f8-631">A Ps1Xml attribútum hozzáadva az alapszintű kimenettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="a86f8-631">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a86f8-632">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a86f8-632">AzureRM.Compute</span></span>
* <span data-ttu-id="a86f8-633">A VMSS IP-címke funkciója</span><span class="sxs-lookup"><span data-stu-id="a86f8-633">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="a86f8-634">A „New-AzureRmVmssIpTagConfig” parancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a86f8-634">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="a86f8-635">Az IpTag paraméter hozzáadva a New-AzureRmVmssIpConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a86f8-635">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="a86f8-636">A VMSS automatikus operációsrendszer-visszaállítási funkciója</span><span class="sxs-lookup"><span data-stu-id="a86f8-636">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="a86f8-637">A DisableAutoRollback-paraméterek hozzáadva a New-AzureRmVmssConfig és az Update-AzureRmVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a86f8-637">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="a86f8-638">A VMSS operációsrendszer-frissítési előzmények funkciója</span><span class="sxs-lookup"><span data-stu-id="a86f8-638">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="a86f8-639">Az OSUpgradeHistory kapcsolóparaméter hozzáadva a Get-AzureRmVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a86f8-639">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="a86f8-640">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="a86f8-640">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="a86f8-641">Katalógushozzáférés-vezérlési listák támogatása hozzáadva az alábbi parancsokhoz:</span><span class="sxs-lookup"><span data-stu-id="a86f8-641">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="a86f8-642">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a86f8-642">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="a86f8-643">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a86f8-643">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="a86f8-644">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a86f8-644">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a86f8-645">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a86f8-645">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a86f8-646">Megszakítás támogatása és az előrehaladás nyomon követése hozzáadva a Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry és Set-AzureRmDataLakeStoreItemAcl parancshoz</span><span class="sxs-lookup"><span data-stu-id="a86f8-646">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="a86f8-647">Megszakítás támogatása hozzáadva az Export-AzureRmDataLakeStoreChildItemProperties parancshoz</span><span class="sxs-lookup"><span data-stu-id="a86f8-647">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="a86f8-648">A rekurzív műveleteket végző parancsmagok hibakeresési üzeneteinek kiürítése javítva</span><span class="sxs-lookup"><span data-stu-id="a86f8-648">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="a86f8-649">A DataLake-parancsmagok tesztelési helye javítva</span><span class="sxs-lookup"><span data-stu-id="a86f8-649">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="a86f8-650">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="a86f8-650">AzureRM.EventHub</span></span>
* <span data-ttu-id="a86f8-651">Opcionális MaxCount paraméter hozzáadva a Get-AzureRmEventHub és a Get-AzureRmEventHubConsumerGroup listaműveleti parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a86f8-651">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="a86f8-652">Ki lett javítva egy probléma a New-AzureRmEventHub parancsmagban, ahol legalább egy paramétert meg kellett adni az új EventHub létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="a86f8-652">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="a86f8-653">Az alapértelmezett paraméterkészlet rendelkezésre áll.</span><span class="sxs-lookup"><span data-stu-id="a86f8-653">Provided Default Parameter set.</span></span>
* <span data-ttu-id="a86f8-654">-KeyValue opcionális paraméter hozzáadva a New-AzureRmEventHubKey parancsmaghoz, amellyel a felhasználó megadhatja a KeyValue paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="a86f8-654">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a86f8-655">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a86f8-655">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a86f8-656">Ki lett javítva az a probléma, hogy a Get-AzureRmKeyVault -Tag paramétere az összes erőforrást visszaadta</span><span class="sxs-lookup"><span data-stu-id="a86f8-656">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a86f8-657">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a86f8-657">AzureRM.Network</span></span>
* <span data-ttu-id="a86f8-658">Új termékváltozatok közzététele a zónaredundáns VirtualNetworkGatewayshez</span><span class="sxs-lookup"><span data-stu-id="a86f8-658">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="a86f8-659">Új parancsok hozzáadva a következő funkcióhoz: ExpressRoute-partner API-k az ARM-en keresztül</span><span class="sxs-lookup"><span data-stu-id="a86f8-659">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="a86f8-660">Get-AzureRmExpressRouteCrossConnection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a86f8-660">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="a86f8-661">Set-AzureRmExpressRouteCrossConnection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a86f8-661">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="a86f8-662">Add-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a86f8-662">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="a86f8-663">Get-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a86f8-663">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="a86f8-664">Remove-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a86f8-664">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="a86f8-665">Get-AzureRMExpressRouteCrossConnectionArpTable hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a86f8-665">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="a86f8-666">Get-AzureRMExpressRouteCrossConnectionRouteTable hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a86f8-666">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="a86f8-667">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a86f8-667">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="a86f8-668">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a86f8-668">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a86f8-669">Get-AzureRmRecoveryServicesBackupStatus parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="a86f8-669">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="a86f8-670">Ez a parancsmag egy virtuális gép azonosítójának használatával ellenőrzi, hogy a virtuális gépet védi-e tároló az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="a86f8-670">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="a86f8-671">Ha van ilyen tároló, a parancsmag megjeleníti annak részleteit.</span><span class="sxs-lookup"><span data-stu-id="a86f8-671">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a86f8-672">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a86f8-672">AzureRM.Resources</span></span>
* <span data-ttu-id="a86f8-673">Frissültek a Get-AzureRmPolicyAssignment-parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="a86f8-673">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="a86f8-674">-Scope-értékek listázásának támogatása hozzáadva a felügyeleti csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="a86f8-674">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="a86f8-675">-Scope-értékekkel történő egyedi hozzárendelések lekérésének támogatása hozzáadva a felügyeleti csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="a86f8-675">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="a86f8-676">-Effective és -All kapcsoló hozzáadva a vezérlő paraméterhez</span><span class="sxs-lookup"><span data-stu-id="a86f8-676">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="a86f8-677">Frissültek a Get/New/Remove/Set-AzureRmPolicyDefinition-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a86f8-677">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="a86f8-678">-ManagementGroupName paraméter hozzáadva a műveletek adott felügyeleti csoporton történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="a86f8-678">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="a86f8-679">-SubscriptionId paraméter hozzáadva a műveletek adott előfizetésen történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="a86f8-679">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="a86f8-680">Frissültek a Get/New/Remove/Set-AzureRmPolicySetDefinition-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a86f8-680">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="a86f8-681">-ManagementGroupName paraméter hozzáadva a műveletek adott felügyeleti csoporton történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="a86f8-681">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="a86f8-682">-SubscriptionId paraméter hozzáadva a műveletek adott előfizetésen történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="a86f8-682">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="a86f8-683">KeyVault titkoskulcs-referencia paraméterekben történő használatának támogatása hozzáadva a TemplateParameterObject használatakor a New-AzureRmResourceGroupDeployment parancsmagban</span><span class="sxs-lookup"><span data-stu-id="a86f8-683">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="a86f8-684">Ki lett javítva egy probléma, amelynek során a rendszer nem vette figyelembe a New-AzureRmADAppCredential parancsmag -EndDate paraméterét</span><span class="sxs-lookup"><span data-stu-id="a86f8-684">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="a86f8-685">Ki lett javítva egy probléma, amelynek során az Add-AzureRmADGroupMember parancsmag nem megfelelő URL-címet használt a kérések elvégzéséhez</span><span class="sxs-lookup"><span data-stu-id="a86f8-685">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="a86f8-686">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a86f8-686">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a86f8-687">A -KeyValue opcionális paraméter hozzáadva a New-AzureRmServiceBusKey parancsmaghoz, amellyel a felhasználó megadhatja a KeyValue paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="a86f8-687">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a86f8-688">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a86f8-688">AzureRM.Sql</span></span>
* <span data-ttu-id="a86f8-689">Tisztázva lettek az SQLDW felhasználó által meghatározott visszaállítási pontjai a New-AzureRmSqlDatabaseRestorePoint súgójában</span><span class="sxs-lookup"><span data-stu-id="a86f8-689">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="a86f8-690">Frissült a -ComputeGeneration paraméter dokumentációja több parancsmagban</span><span class="sxs-lookup"><span data-stu-id="a86f8-690">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="a86f8-691">6.3.0 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="a86f8-691">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a86f8-692">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a86f8-692">AzureRM.Profile</span></span>
* <span data-ttu-id="a86f8-693">Az Enable-AzureRmContextAutoSave hibaüzenetei frissültek</span><span class="sxs-lookup"><span data-stu-id="a86f8-693">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="a86f8-694">Egy környezet jön létre minden előfizetéshez, amelyben a Connect-AzureRmAccount korábbi környezet nélkül fut</span><span class="sxs-lookup"><span data-stu-id="a86f8-694">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="a86f8-695">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a86f8-695">Azure.Storage</span></span>
* <span data-ttu-id="a86f8-696">További információk lettek hozzáadva a súgófájlokhoz a -Permissions paraméterrel kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="a86f8-696">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a86f8-697">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a86f8-697">AzureRM.Compute</span></span>
* <span data-ttu-id="a86f8-698">A Get-AzureRmVmDiskEncryptionStatus kijavít egy hibát, amely az adatlemezekkel nem rendelkező virtuális gépeken jelentkezik</span><span class="sxs-lookup"><span data-stu-id="a86f8-698">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="a86f8-699">A Compute ügyfélkódtár-verziója frissült, a következő parancsmagok javítása érdekében</span><span class="sxs-lookup"><span data-stu-id="a86f8-699">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="a86f8-700">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="a86f8-700">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="a86f8-701">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="a86f8-701">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="a86f8-702">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="a86f8-702">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="a86f8-703">A következő parancsmagok ki lettek javítva, így helyesen jelenítik meg a műveletazonosítót és a művelet állapotát:</span><span class="sxs-lookup"><span data-stu-id="a86f8-703">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="a86f8-704">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a86f8-704">Start-AzureRmVM</span></span>
    - <span data-ttu-id="a86f8-705">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a86f8-705">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="a86f8-706">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a86f8-706">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="a86f8-707">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a86f8-707">Set-AzureRmVM</span></span>
    - <span data-ttu-id="a86f8-708">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a86f8-708">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="a86f8-709">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a86f8-709">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="a86f8-710">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="a86f8-710">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="a86f8-711">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="a86f8-711">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="a86f8-712">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a86f8-712">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="a86f8-713">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a86f8-713">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="a86f8-714">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a86f8-714">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="a86f8-715">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a86f8-715">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="a86f8-716">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="a86f8-716">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="a86f8-717">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="a86f8-717">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="a86f8-718">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="a86f8-718">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="a86f8-719">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="a86f8-719">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="a86f8-720">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="a86f8-720">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="a86f8-721">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="a86f8-721">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="a86f8-722">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a86f8-722">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="a86f8-723">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a86f8-723">AzureRM.EventGrid</span></span>
* <span data-ttu-id="a86f8-724">A ValidateNotNullOrEmpty érvényesítési feltételei az Update-AzureRmEventGridSubscription parancsmagban található SubjectBeginsWith/SubjectEndsWith esetében el lettek távolítva, így ha szükséges, ezek a paraméterek üres sztringre módosíthatók.</span><span class="sxs-lookup"><span data-stu-id="a86f8-724">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a86f8-725">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a86f8-725">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a86f8-726">Ki lett javítva egy probléma, amelynek során a parancs nem adott vissza címkét a Get-AzureRmKeyVault -Tag futtatásakor</span><span class="sxs-lookup"><span data-stu-id="a86f8-726">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="a86f8-727">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a86f8-727">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="a86f8-728">A Policy Insights-parancsmagok nyilvános kiadása</span><span class="sxs-lookup"><span data-stu-id="a86f8-728">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="a86f8-729">A 2018.04.04. dátumú API-verziót használják</span><span class="sxs-lookup"><span data-stu-id="a86f8-729">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="a86f8-730">A PolicyDefinitionReferenceId hozzá lett adva a Get-AzureRmPolicyStateSummary eredményeihez</span><span class="sxs-lookup"><span data-stu-id="a86f8-730">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="a86f8-731">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a86f8-731">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a86f8-732">A -Vault paraméter hozzá lett adva a RecoveryServices.Backup-parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="a86f8-732">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="a86f8-733">Ha át van adva, felülbírálja a Set-AzureRmRecoveryServicesContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a86f8-733">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a86f8-734">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a86f8-734">AzureRM.Sql</span></span>
* <span data-ttu-id="a86f8-735">A Get-AzureRmSqlDatabaseExpanded súgófájljában lévő példa frissült</span><span class="sxs-lookup"><span data-stu-id="a86f8-735">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a86f8-736">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a86f8-736">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a86f8-737">Az Add-AzureRmTrafficManagerEndpointConfig súgófájlja frissült</span><span class="sxs-lookup"><span data-stu-id="a86f8-737">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a86f8-738">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a86f8-738">AzureRM.Websites</span></span>
* <span data-ttu-id="a86f8-739">Frissült a Set-AzureRmWebApp, így az AppSettings nem lesz felülírva az -AssignIdentity használatakor</span><span class="sxs-lookup"><span data-stu-id="a86f8-739">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="a86f8-740">Frissült a New-AzureRmWebAppSlot, így figyelembe veszi az AppServicePlan paramétert választható paraméterként</span><span class="sxs-lookup"><span data-stu-id="a86f8-740">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="a86f8-741">6.2.1 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="a86f8-741">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="a86f8-742">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a86f8-742">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="a86f8-743">Frissült a PSWorkspace modell, így lehetővé teszi, hogy a hálózat a típust paraméterként használja</span><span class="sxs-lookup"><span data-stu-id="a86f8-743">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="a86f8-744">6.2.0 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="a86f8-744">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a86f8-745">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a86f8-745">AzureRM.Profile</span></span>
* <span data-ttu-id="a86f8-746">Kijavítottuk a problémát, amely miatt a Newtonsoft.Json 10.0.3-as verziója nem töltődött be a modul importálása során</span><span class="sxs-lookup"><span data-stu-id="a86f8-746">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a86f8-747">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a86f8-747">AzureRM.Compute</span></span>
* <span data-ttu-id="a86f8-748">VMSS VM frissítési funkciója</span><span class="sxs-lookup"><span data-stu-id="a86f8-748">VMSS VM Update feature</span></span>
    - <span data-ttu-id="a86f8-749">Hozzá lett adva az Update-AzureRmVmssVM és a New-AzureRmVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="a86f8-749">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="a86f8-750">A VirtualMachineScaleSetVM paraméter hozzá lett adva az Add-AzureRmVMDataDisk parancsmaghoz, hogy adatlemezt lehessen hozzáadni a VMSS VM-hez</span><span class="sxs-lookup"><span data-stu-id="a86f8-750">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="a86f8-751">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a86f8-751">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="a86f8-752">Az ADF .Net SDK frissült a 0.8.0-s előzetes verzióra, amely az alábbi változásokat tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="a86f8-752">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="a86f8-753">Hozzá lett adva a gyári adattár konfigurálási művelete</span><span class="sxs-lookup"><span data-stu-id="a86f8-753">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="a86f8-754">Frissült a QuickBooks társított szolgáltatás a consumerKey és a consumerSecret tulajdonság elérhetővé tételéhez</span><span class="sxs-lookup"><span data-stu-id="a86f8-754">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="a86f8-755">Több modelltípus is frissült, a SecretBase-től az objektumig</span><span class="sxs-lookup"><span data-stu-id="a86f8-755">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="a86f8-756">A rendszer blobesemény-indítókkal bővült</span><span class="sxs-lookup"><span data-stu-id="a86f8-756">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="a86f8-757">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a86f8-757">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a86f8-758">A dokumentáció kimeneti példával bővült</span><span class="sxs-lookup"><span data-stu-id="a86f8-758">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="a86f8-759">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a86f8-759">AzureRM.Network</span></span>
* <span data-ttu-id="a86f8-760">Engedélyezve lettek a Traffic Analytics-paraméterek a Network Watcher-parancsmagokon</span><span class="sxs-lookup"><span data-stu-id="a86f8-760">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a86f8-761">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a86f8-761">AzureRM.Resources</span></span>
* <span data-ttu-id="a86f8-762">Kijavítottuk a „PSResource” objektum(ok) Get-AzureRmResource által visszaadott „Properties” tulajdonságával kapcsolatos hibát</span><span class="sxs-lookup"><span data-stu-id="a86f8-762">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="a86f8-763">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="a86f8-763">AzureRM.Scheduler</span></span>
* <span data-ttu-id="a86f8-764">Kijavítottuk a hibát, amely miatt a ServiceBusQueueJob frissítése nem állított be új hitelesítési adatokat</span><span class="sxs-lookup"><span data-stu-id="a86f8-764">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="a86f8-765">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a86f8-765">AzureRM.Sql</span></span>
* <span data-ttu-id="a86f8-766">A következő parancsmagok az opcionális LicenseType paraméterrel frissültek</span><span class="sxs-lookup"><span data-stu-id="a86f8-766">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="a86f8-767">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a86f8-767">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="a86f8-768">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a86f8-768">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="a86f8-769">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="a86f8-769">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="a86f8-770">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a86f8-770">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="a86f8-771">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a86f8-771">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a86f8-772">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a86f8-772">AzureRM.Websites</span></span>
* <span data-ttu-id="a86f8-773">Frissült a New-AzureRMWebApp, hogy képes legyen a stratégia könyvtárból származó bevett algoritmusok használatára.</span><span class="sxs-lookup"><span data-stu-id="a86f8-773">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="a86f8-774">6.1.0 – 2018. május</span><span class="sxs-lookup"><span data-stu-id="a86f8-774">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a86f8-775">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a86f8-775">AzureRM.Profile</span></span>
* <span data-ttu-id="a86f8-776">Ki lett javítva az a hiba, amelyben a „Clear-AzureRmContext” futtatása egy üres környezetet tartott meg az előző alapértelmezett környezet nevével, így a felhasználó nem tudott létrehozni új környezetet a régi néven</span><span class="sxs-lookup"><span data-stu-id="a86f8-776">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="a86f8-777">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a86f8-777">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="a86f8-778">Az átjárók társítási/társításmegszüntetési műveleteinek engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="a86f8-778">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="a86f8-779">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a86f8-779">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="a86f8-780">Az ApiVersion, ApiRelease és ApiRevision paraméterek mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="a86f8-780">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="a86f8-781">A Service Fabric háttérrendszer mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="a86f8-781">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="a86f8-782">Az Application Insights naplózó mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="a86f8-782">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="a86f8-783">Az „Alapszintű” termékváltozat érvényes termékváltozatként való elismerése mostantól támogatott az API Management szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="a86f8-783">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="a86f8-784">A privát hitelesítésszolgáltató által kiállított tanúsítványok fő- vagy hitelesítésszolgáltatói tanúsítványként való telepítése mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="a86f8-784">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="a86f8-785">Az egyéni SSL-tanúsítványok KeyVault- és többproxys gazdaneveken keresztüli fogadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="a86f8-785">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="a86f8-786">Az MSI-identitások mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="a86f8-786">Added support for MSI identity</span></span>
* <span data-ttu-id="a86f8-787">A házirendek URL-kapcsolaton keresztüli fogadása mostantól támogatott MEGJEGYZÉS: A következő parancsmagok elavulttá válnak a jövőbeli kiadásokban</span><span class="sxs-lookup"><span data-stu-id="a86f8-787">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="a86f8-788">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="a86f8-788">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="a86f8-789">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="a86f8-789">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="a86f8-790">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="a86f8-790">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="a86f8-791">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="a86f8-791">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="a86f8-792">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="a86f8-792">AzureRM.Batch</span></span>
* <span data-ttu-id="a86f8-793">Új Get-AzureBatchPoolNodeCounts parancsmag kiadása</span><span class="sxs-lookup"><span data-stu-id="a86f8-793">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="a86f8-794">Új Start-AzureBatchComputeNodeServiceLogUpload parancsmag kiadása</span><span class="sxs-lookup"><span data-stu-id="a86f8-794">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="a86f8-795">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="a86f8-795">AzureRM.Consumption</span></span>
* <span data-ttu-id="a86f8-796">A Get-AzureRmConsumptionUsageDetail parancsmag kiegészítése új Expand, ResourceGroup, InstanceName, InstanceId, Tags és Top paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="a86f8-796">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a86f8-797">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a86f8-797">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a86f8-798">Az Export-AzureRmDataLakeStoreChildItemProperties példájának kijavítása</span><span class="sxs-lookup"><span data-stu-id="a86f8-798">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="a86f8-799">A Set-AzureRmDataLakeStoreItemAclEntry Recurse esetében fellépő null paraméter kivétel kijavítása</span><span class="sxs-lookup"><span data-stu-id="a86f8-799">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="a86f8-800">A Set-AzureRmDataLakeStoreItemAclEntry, a Set-AzureRmDataLakeStoreItemAcl és a Remove-AzureRmDataLakeStoreItemAclEntry súgófájljainak javítása</span><span class="sxs-lookup"><span data-stu-id="a86f8-800">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="a86f8-801">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a86f8-801">AzureRM.Network</span></span>
* <span data-ttu-id="a86f8-802">A hálózati SDK-verzió felléptetése a 18.0.0-s előzetes verzióról a 19.0.0-s előzetes verzióra</span><span class="sxs-lookup"><span data-stu-id="a86f8-802">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="a86f8-803">Új parancsmag hozzáadva a protokollkonfigurációk létrehozásához</span><span class="sxs-lookup"><span data-stu-id="a86f8-803">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="a86f8-804">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a86f8-804">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="a86f8-805">Új parancsmag hozzáadva az új kapcsolatcsoportok hozzáadásához a meglévő ExpressRoute-kapcsolatcsoportokhoz.</span><span class="sxs-lookup"><span data-stu-id="a86f8-805">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="a86f8-806">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a86f8-806">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="a86f8-807">Új parancsmag hozzáadva a kapcsolatcsoportok eltávolításához a meglévő ExpressRoute-kapcsolatcsoportokból.</span><span class="sxs-lookup"><span data-stu-id="a86f8-807">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="a86f8-808">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a86f8-808">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="a86f8-809">Új parancsmag hozzáadva a kapcsolatcsoportok lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="a86f8-809">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="a86f8-810">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a86f8-810">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="a86f8-811">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a86f8-811">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="a86f8-812">A kiszolgálói hitelesítés létrehozott tanúsítványokkal való használata (5998. sz. hiba) ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="a86f8-812">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a86f8-813">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a86f8-813">AzureRM.Sql</span></span>
* <span data-ttu-id="a86f8-814">A frissített naplózási parancsmagok lehetővé teszik az AuditAction és AuditActionGroup paraméterek eltávolítását</span><span class="sxs-lookup"><span data-stu-id="a86f8-814">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="a86f8-815">A Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy hibája ki lett javítva, amikor az új rugalmas adatmegőrzési szabályzatok megadásakor a parancs a következő hibát adta vissza: „A hosszútávú adatmegőrzési szabályzat megadása Azure Recovery Services-tárolókkal és szabályzatokkal már nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="a86f8-815">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="a86f8-816">Adja le a kérést az új rugalmas adatmegőrzési szabályzattal”.</span><span class="sxs-lookup"><span data-stu-id="a86f8-816">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="a86f8-817">Az összes Azure SQL Database/ElasticPool létrehozással/frissítéssel kapcsolatos parancsmag frissítve lett az új Database API használatára, amely támogatja a termékváltozat tulajdonságot a méretezéssel és szintekkel kapcsolatos tulajdonságok esetében.</span><span class="sxs-lookup"><span data-stu-id="a86f8-817">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="a86f8-818">A frissített parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="a86f8-818">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="a86f8-819">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a86f8-819">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="a86f8-820">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a86f8-820">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="a86f8-821">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="a86f8-821">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="a86f8-822">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a86f8-822">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="a86f8-823">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a86f8-823">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a86f8-824">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a86f8-824">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a86f8-825">A Get-AzureRmTrafficManagerProfile paramétereinek frissítésével a -ResourceGroupName paraméter megadása mostantól kötelező a -Name paraméter használata esetén.</span><span class="sxs-lookup"><span data-stu-id="a86f8-825">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
