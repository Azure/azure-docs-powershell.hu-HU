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
ms.openlocfilehash: 8a7b184ed06eb078956229fa67d02840014e3aaf
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/08/2018
ms.locfileid: "51275520"
---
# <a name="release-notes"></a><span data-ttu-id="a7456-103">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="a7456-103">Release notes</span></span>

<span data-ttu-id="a7456-104">Az alábbiakban az Azure PowerShell jelen kiadásában végrehajtott módosítások listája olvasható.</span><span class="sxs-lookup"><span data-stu-id="a7456-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6120---november-2018"></a><span data-ttu-id="a7456-105">6.12.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="a7456-105">6.12.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a7456-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a7456-106">AzureRM.Profile</span></span>
* <span data-ttu-id="a7456-107">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="a7456-107">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="a7456-108">A TenantId paraméter a Connect-AzureRmAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="a7456-108">Rename param TenantId in cmdlet Connect-AzureRmAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="a7456-109">Frissítve lett a TenantId leírása a Connect-AzureRmAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a7456-109">Updated TenantId description for Connect-AzureRmAccount</span></span>
* <span data-ttu-id="a7456-110">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="a7456-110">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="a7456-111">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="a7456-111">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="a7456-112">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="a7456-112">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="a7456-113">Javítva lett az a probléma, amely miatt a „Disconnect-AzureRmAccount” jelenik meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="a7456-113">Fix issue where 'Disconnect-AzureRmAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a><span data-ttu-id="a7456-114">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="a7456-114">AzureRM.Automation</span></span>
* <span data-ttu-id="a7456-115">A parancsmag DLL-fájlja át lett nevezve a következőre: Microsoft.Azure.Commands.Automation.dll</span><span class="sxs-lookup"><span data-stu-id="a7456-115">Renamed cmdlet DLL filename to Microsoft.Azure.Commands.Automation.dll</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="a7456-116">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a7456-116">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="a7456-117">Hozzá lett adva a Get-AzureRmCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="a7456-117">Add Get-AzureRmCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a7456-118">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a7456-118">AzureRM.Compute</span></span>
* <span data-ttu-id="a7456-119">Hozzá lett adva az Add-AzureRmVmssVMDataDisk és a Remove-AzureRmVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="a7456-119">Add Add-AzureRmVmssVMDataDisk and Remove-AzureRmVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="a7456-120">A Get-AzureRmVMImage megjeleníti a következőt: AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="a7456-120">Get-AzureRmVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="a7456-121">Javítva lett az a probléma, amely miatt a SetAzureRmVMChefExtension -BootstrapOptions és -JsonAttribute beállítások értékei nem json formátumban lettek beállítva.</span><span class="sxs-lookup"><span data-stu-id="a7456-121">Fixed SetAzureRmVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a7456-122">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a7456-122">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a7456-123">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="a7456-123">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="a7456-124">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="a7456-124">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="a7456-125">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="a7456-125">AzureRM.Insights</span></span>
* <span data-ttu-id="a7456-126">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="a7456-126">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="a7456-127">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="a7456-127">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="a7456-128">Javítva lett a 7513-as hiba [Insights] A Set-AzureRmDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="a7456-128">Fixed issue #7513 [Insights] Set-AzureRMDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="a7456-129">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="a7456-129">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a7456-130">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a7456-130">AzureRM.Network</span></span>
* <span data-ttu-id="a7456-131">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="a7456-131">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="a7456-132">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="a7456-132">Get-AzureRmExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="a7456-133">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="a7456-133">Get-AzureRmExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="a7456-134">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a7456-134">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="a7456-135">Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="a7456-135">Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="a7456-136">Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="a7456-136">Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="a7456-137">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a7456-137">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="a7456-138">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a7456-138">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="a7456-139">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7456-139">Added policy remediation cmdlets</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="a7456-140">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a7456-140">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a7456-141">Hozzá lett adva az Azure-fájlmegosztások támogatása a Recovery Servicesben.</span><span class="sxs-lookup"><span data-stu-id="a7456-141">Added support for azure file shares in recovery services.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a7456-142">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a7456-142">AzureRM.Resources</span></span>
* <span data-ttu-id="a7456-143">https://github.com/Azure/azure-powershell/issues/7402 javítása</span><span class="sxs-lookup"><span data-stu-id="a7456-143">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="a7456-144">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzureRmResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="a7456-144">Allow listing resources using the '-ResourceId' parameter for 'Get-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a7456-145">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a7456-145">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a7456-146">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="a7456-146">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="a7456-147">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a7456-147">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="a7456-148">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="a7456-148">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="a7456-149">Javítva lett az Add-AzureRmServiceFabricClusterCertificate parancsmag</span><span class="sxs-lookup"><span data-stu-id="a7456-149">Fix 'Add-AzureRmServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="a7456-150">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="a7456-150">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="a7456-151">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="a7456-151">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="a7456-152">Javítva lett az Update-AzureRmServiceFabricDurability parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="a7456-152">Fix 'Update-AzureRmServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="6110---october-2018"></a><span data-ttu-id="a7456-153">6.11.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="a7456-153">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a7456-154">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a7456-154">AzureRM.Profile</span></span>
* <span data-ttu-id="a7456-155">Ki lett javítva a Get-AzureRmSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="a7456-155">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="a7456-156">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="a7456-156">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="a7456-157">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="a7456-157">AzureRM.Backup</span></span>
* <span data-ttu-id="a7456-158">Elavult Azure Backup-parancsmagok.</span><span class="sxs-lookup"><span data-stu-id="a7456-158">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a7456-159">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a7456-159">AzureRM.Compute</span></span>
* <span data-ttu-id="a7456-160">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a New-AzureRmVm parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="a7456-160">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="a7456-161">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="a7456-161">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a7456-162">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a7456-162">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a7456-163">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="a7456-163">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="a7456-164">Get-AzureRmDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="a7456-164">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="a7456-165">Add-AzureRmDataLakeStoreVirtualNetworkRule: A virtuális hálózati szabályt hozzáadja a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="a7456-165">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a7456-166">Set-AzureRmDataLakeStoreVirtualNetworkRule: Módosítja a kiválasztott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="a7456-166">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a7456-167">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="a7456-167">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a7456-168">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a7456-168">AzureRM.Network</span></span>
* <span data-ttu-id="a7456-169">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="a7456-169">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="a7456-170">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="a7456-170">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a7456-171">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a7456-171">AzureRM.Resources</span></span>
* <span data-ttu-id="a7456-172">Egy értelmezhető kivétel forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat eseteket, amelyekben a Get-AzureRMRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="a7456-172">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="a7456-173">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="a7456-173">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="a7456-174">6.10.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="a7456-174">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="a7456-175">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a7456-175">Azure.Storage</span></span>
* <span data-ttu-id="a7456-176">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="a7456-176">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="a7456-177">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a7456-177">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="a7456-178">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a7456-178">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="a7456-179">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a7456-179">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="a7456-180">A Get-AzureRmCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="a7456-180">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a7456-181">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a7456-181">AzureRM.Compute</span></span>
* <span data-ttu-id="a7456-182">Ki lett javítva a Get-AzureRmVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon</span><span class="sxs-lookup"><span data-stu-id="a7456-182">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="a7456-183">A SimpleParameterSet egy példája hozzá lett adva a New-AzureRmVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="a7456-183">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="a7456-184">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="a7456-184">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="a7456-185">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a7456-185">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="a7456-186">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="a7456-186">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a7456-187">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a7456-187">AzureRM.Network</span></span>
* <span data-ttu-id="a7456-188">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="a7456-188">Added NetworkProfile functionality.</span></span> <span data-ttu-id="a7456-189">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7456-189">new cmdlets added</span></span>
    - <span data-ttu-id="a7456-190">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a7456-190">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="a7456-191">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a7456-191">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="a7456-192">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a7456-192">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="a7456-193">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a7456-193">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="a7456-194">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="a7456-194">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="a7456-195">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="a7456-195">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="a7456-196">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="a7456-196">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="a7456-197">Hozzá lett adva a New-AzureRmVirtualNetworkTap, a Get-AzureRmVirtualNetworkTap, a Set-AzureRmVirtualNetworkTap és a Remove-AzureRmVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="a7456-197">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="a7456-198">Hozzá lett adva a Set-AzureRmNEtworkInterfaceTapConfig, a Get-AzureRmNEtworkInterfaceTapConfig és a Remove-AzureRmNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="a7456-198">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="a7456-199">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a7456-199">AzureRM.RedisCache</span></span>
* <span data-ttu-id="a7456-200">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="a7456-200">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="a7456-201">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="a7456-201">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a7456-202">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a7456-202">AzureRM.Resources</span></span>
* <span data-ttu-id="a7456-203">A hiányzó -Mode paraméter hozzá lett adva a Set-AzureRmPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a7456-203">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="a7456-204">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzureRmProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="a7456-204">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a7456-205">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a7456-205">AzureRM.Sql</span></span>
* <span data-ttu-id="a7456-206">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="a7456-206">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="a7456-207">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="a7456-207">AzureRM.Storage</span></span>
* <span data-ttu-id="a7456-208">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="a7456-208">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="a7456-209">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="a7456-209">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a7456-210">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a7456-210">AzureRM.Websites</span></span>
* <span data-ttu-id="a7456-211">Új Get-AzureRMWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhook URL-címét</span><span class="sxs-lookup"><span data-stu-id="a7456-211">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="a7456-212">Új New-AzureRMWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="a7456-212">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="a7456-213">6.9.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="a7456-213">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a7456-214">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="a7456-214">General</span></span>
* <span data-ttu-id="a7456-215">Az AzureRM.SignalR hozzáadva az AzureRM összesített modulhoz</span><span class="sxs-lookup"><span data-stu-id="a7456-215">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="a7456-216">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a7456-216">AzureRM.Profile</span></span>
* <span data-ttu-id="a7456-217">Kisebb módosítások a tárolók általános kódjában</span><span class="sxs-lookup"><span data-stu-id="a7456-217">Minor changes to the storage common code</span></span>
* <span data-ttu-id="a7456-218">Teljes paramétertípusokkal frissült súgófájlok</span><span class="sxs-lookup"><span data-stu-id="a7456-218">Updated help files to include full parameter types.</span></span>
* <span data-ttu-id="a7456-219">A -ServicePrincipal módosítása nem kötelezőre a ServicePrincipalCertificateWithSubscriptionId paraméterkészletben</span><span class="sxs-lookup"><span data-stu-id="a7456-219">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="a7456-220">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a7456-220">Azure.Storage</span></span>
* <span data-ttu-id="a7456-221">Storage-környezet létrehozásának támogatása OAuth használatával.</span><span class="sxs-lookup"><span data-stu-id="a7456-221">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="a7456-222">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="a7456-222">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="a7456-223">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="a7456-223">AzureRM.Cdn</span></span>
* <span data-ttu-id="a7456-224">Standard_Microsoft hozzáadva a CDN-díjszabási termékváltozatban.</span><span class="sxs-lookup"><span data-stu-id="a7456-224">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="a7456-225">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a7456-225">AzureRM.Compute</span></span>
* <span data-ttu-id="a7456-226">A Key Vault és a Storage függőségeinek áthelyezése az általános függőségekhez</span><span class="sxs-lookup"><span data-stu-id="a7456-226">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="a7456-227">További virtuálisgép-méretek támogatása hozzáadva az AEM-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="a7456-227">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="a7456-228">A PublicIPPrefix paraméter hozzáadva a New-AzureRmVmssIpConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a7456-228">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="a7456-229">A ResourceId paraméter hozzáadva az Invoke-AzureRmVMRunCommand parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a7456-229">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="a7456-230">Az Invoke-AzureRmVmssVMRunCommand parancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7456-230">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="a7456-231">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="a7456-231">AzureRM.Dns</span></span>
* <span data-ttu-id="a7456-232">Aliasrekord támogatása hozzáadva DNS-rekord létrehozása során</span><span class="sxs-lookup"><span data-stu-id="a7456-232">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="a7456-233">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="a7456-233">AzureRM.Insights</span></span>
* <span data-ttu-id="a7456-234">A 6833-as és a 7102-es hiba kijavítva (Diagnosztikai beállítások területe)</span><span class="sxs-lookup"><span data-stu-id="a7456-234">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="a7456-235">Az alapértelmezett név, például a „service” hibái a diagnosztikai beállítások megadása és listázása/lekérése során</span><span class="sxs-lookup"><span data-stu-id="a7456-235">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="a7456-236">Diagnosztikai beállítások kategóriákkal történő létrehozásának hibái</span><span class="sxs-lookup"><span data-stu-id="a7456-236">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="a7456-237">Elavulási üzenetek hozzáadva a metrikák időfelbontási szintjeinek paramétereihez</span><span class="sxs-lookup"><span data-stu-id="a7456-237">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="a7456-238">Az időfelbontási szintek paramétereit még elfogadja a rendszer (ez nem egy kompatibilitástörő változás), viszont figyelmen kívül hagyja a háttérrendszerben, mivel csak a PT1M érvényes</span><span class="sxs-lookup"><span data-stu-id="a7456-238">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a7456-239">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a7456-239">AzureRM.Network</span></span>
* <span data-ttu-id="a7456-240">A LoadBalancer parancsmagokat érintő változások</span><span class="sxs-lookup"><span data-stu-id="a7456-240">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="a7456-241">LoadBalancerInboundNatPoolConfig: az IdleTimeoutInMinutes, az EnableFloatingIp és az EnableTcpReset paraméterek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7456-241">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="a7456-242">LoadBalancerInboundNatRuleConfig: az EnableTcpReset paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7456-242">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="a7456-243">LoadBalancerRuleConfig: az EnableTcpReset paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7456-243">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="a7456-244">LoadBalancerProbeConfig: a Protocol paraméterhez tartozó „Https” érték támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7456-244">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="a7456-245">Új parancsok hozzáadva a LoadBalancer új, OutboundRule nevű alerőforrásához</span><span class="sxs-lookup"><span data-stu-id="a7456-245">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="a7456-246">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a7456-246">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="a7456-247">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a7456-247">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="a7456-248">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a7456-248">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="a7456-249">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a7456-249">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="a7456-250">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a7456-250">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="a7456-251">Új HostedWorkloads tulajdonság hozzáadva a PSNetworkInterface-hez</span><span class="sxs-lookup"><span data-stu-id="a7456-251">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="a7456-252">Új parancsmagok hozzáadva a következő szolgáltatáshoz: Azure Firewall ARM-en keresztül</span><span class="sxs-lookup"><span data-stu-id="a7456-252">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="a7456-253">Get-AzureRmFirewall hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7456-253">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="a7456-254">Set-AzureRmFirewall hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7456-254">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="a7456-255">New-AzureRmFirewall hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7456-255">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="a7456-256">Remove-AzureRmFirewall hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7456-256">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="a7456-257">New-AzureRmFirewallApplicationRuleCollection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7456-257">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="a7456-258">New-AzureRmFirewallApplicationRule hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7456-258">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="a7456-259">New-AzureRmFirewallNatRuleCollection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7456-259">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="a7456-260">New-AzureRmFirewallNatRule hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7456-260">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="a7456-261">New-AzureRmFirewallNetworkRuleCollection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7456-261">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="a7456-262">New-AzureRmFirewallNetworkRule hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7456-262">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="a7456-263">Támogatás hozzáadva a megbízható főtanúsítványokhoz és az automatikus skálázás konfigurálásához az Application Gatewayben</span><span class="sxs-lookup"><span data-stu-id="a7456-263">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="a7456-264">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="a7456-264">New Cmdlets added:</span></span>
      - <span data-ttu-id="a7456-265">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a7456-265">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="a7456-266">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a7456-266">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="a7456-267">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a7456-267">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="a7456-268">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a7456-268">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="a7456-269">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a7456-269">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="a7456-270">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7456-270">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="a7456-271">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7456-271">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="a7456-272">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7456-272">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="a7456-273">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7456-273">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="a7456-274">Parancsmagok frissítve a -TrustedRootCertificate nevű, nem kötelező paraméterrel</span><span class="sxs-lookup"><span data-stu-id="a7456-274">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="a7456-275">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a7456-275">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="a7456-276">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a7456-276">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="a7456-277">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a7456-277">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="a7456-278">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a7456-278">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="a7456-279">Parancsmagok frissítve az -AutoscaleConfiguration nevű, nem kötelező paraméterrel</span><span class="sxs-lookup"><span data-stu-id="a7456-279">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="a7456-280">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a7456-280">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="a7456-281">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a7456-281">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="a7456-282">A Get-AzureInterfaceEndpoint parancsmag hozzáadva a felhasználói felület végpontjához</span><span class="sxs-lookup"><span data-stu-id="a7456-282">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="a7456-283">Támogatás hozzáadva több címelőtaghoz egy alhálózaton belül</span><span class="sxs-lookup"><span data-stu-id="a7456-283">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="a7456-284">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="a7456-284">Updated cmdlets:</span></span>
  - <span data-ttu-id="a7456-285">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a7456-285">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="a7456-286">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a7456-286">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="a7456-287">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a7456-287">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="a7456-288">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a7456-288">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="a7456-289">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a7456-289">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="a7456-290">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a7456-290">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="a7456-291">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a7456-291">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="a7456-292">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a7456-292">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="a7456-293">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7456-293">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="a7456-294">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7456-294">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="a7456-295">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7456-295">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="a7456-296">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a7456-296">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="a7456-297">New-AzureRmNetworkInterfaceIpConfig - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a7456-297">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="a7456-298">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="a7456-298">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="a7456-299">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="a7456-299">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="a7456-300">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a7456-300">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="a7456-301">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a7456-301">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="a7456-302">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a7456-302">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="a7456-303">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a7456-303">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="a7456-304">Alhálózat-delegálási parancsmagok hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="a7456-304">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="a7456-305">New-AzureRmDelegation: Létrehoz egy új delegálást, amelyet hozzá lehet adni egy alhálózathoz</span><span class="sxs-lookup"><span data-stu-id="a7456-305">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="a7456-306">Remove-AzureRmDelegation: Felvesz egy alhálózatot, és eltávolítja a megadott delegálási nevet az adott alhálózatból</span><span class="sxs-lookup"><span data-stu-id="a7456-306">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="a7456-307">Add-AzureRmDelegation: Felvesz egy alhálózatot, és eltávolítja a megadott szolgáltatásnevet az adott alhálózatból</span><span class="sxs-lookup"><span data-stu-id="a7456-307">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="a7456-308">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="a7456-308">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="a7456-309">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="a7456-309">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="a7456-310">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="a7456-310">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="a7456-311">A felügyelt lemezek támogatása</span><span class="sxs-lookup"><span data-stu-id="a7456-311">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="a7456-312">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a7456-312">AzureRM.RedisCache</span></span>
* <span data-ttu-id="a7456-313">Insights-függőség frissítve</span><span class="sxs-lookup"><span data-stu-id="a7456-313">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a7456-314">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a7456-314">AzureRM.Resources</span></span>
* <span data-ttu-id="a7456-315">A New-AzureRmResourceGroupDeployment frissítve az új RollbackAction paraméterrel</span><span class="sxs-lookup"><span data-stu-id="a7456-315">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="a7456-316">Az OnErrorDeployment támogatása az új paraméterrel</span><span class="sxs-lookup"><span data-stu-id="a7456-316">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="a7456-317">A felügyelt identitás támogatása a szabályzat-hozzárendeléseknél</span><span class="sxs-lookup"><span data-stu-id="a7456-317">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="a7456-318">Az alapértelmezett értékekkel rendelkező paraméterek már nem szükségesek a szabályzatok a New-AzureRmPolicyAssignmenttel történő hozzárendelésekor</span><span class="sxs-lookup"><span data-stu-id="a7456-318">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="a7456-319">Az új Get-AzureRmPolicyAlias parancsmag hozzáadva a szabályzataliasok lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="a7456-319">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a7456-320">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a7456-320">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a7456-321">A 7161-es hiba kijavítva</span><span class="sxs-lookup"><span data-stu-id="a7456-321">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="a7456-322">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="a7456-322">AzureRM.SignalR</span></span>
* <span data-ttu-id="a7456-323">Termékváltozatnevek frissítve Free_F1-re és Standard_S1-re</span><span class="sxs-lookup"><span data-stu-id="a7456-323">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="a7456-324">Verzió mező hozzáadva a PSSignalRResource objektumhoz, és kapcsolati sztring hozzáadva a PSSignalRKeys objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="a7456-324">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="a7456-325">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="a7456-325">AzureRM.Storage</span></span>
* <span data-ttu-id="a7456-326">Módosíthatatlansági szabályzat támogatva az AzureRM.Storage-ban</span><span class="sxs-lookup"><span data-stu-id="a7456-326">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="a7456-327">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a7456-327">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="a7456-328">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a7456-328">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="a7456-329">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a7456-329">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="a7456-330">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a7456-330">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="a7456-331">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a7456-331">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="a7456-332">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="a7456-332">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="a7456-333">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="a7456-333">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="a7456-334">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a7456-334">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="a7456-335">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a7456-335">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="a7456-336">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a7456-336">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="a7456-337">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a7456-337">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a7456-338">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a7456-338">AzureRM.Websites</span></span>
* <span data-ttu-id="a7456-339">Két új parancsmag hozzáadva: Get-AzureRmDeletedWebApp és Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="a7456-339">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="a7456-340">A New-AzureRmAppServicePlan -HyperV kapcsoló hozzáadva App Service-csomag létrehozásához Windows-tárolóval</span><span class="sxs-lookup"><span data-stu-id="a7456-340">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="a7456-341">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot – Új paraméterek (–ContainerRegistryUser sztring -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) hozzáadva Windows-tárolóalkalmazás létrehozásához és felügyeletéhez</span><span class="sxs-lookup"><span data-stu-id="a7456-341">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="a7456-342">6.8.1 – 2018. augusztus</span><span class="sxs-lookup"><span data-stu-id="a7456-342">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a7456-343">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="a7456-343">General</span></span>
* <span data-ttu-id="a7456-344">Ki lett javítva az alapértelmezett erőforráscsoportok beállításának hiányával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="a7456-344">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="a7456-345">Frissített közös futtatókörnyezeti szerelvények</span><span class="sxs-lookup"><span data-stu-id="a7456-345">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="a7456-346">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a7456-346">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="a7456-347">Ki lett javítva az alapértelmezett erőforráscsoportok beállításának hiányával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="a7456-347">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="a7456-348">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="a7456-348">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="a7456-349">Az Import-AzureRmApiManagementApi és az \*-AzureRmApiManagementCertificate parancsmagok már tudják kezelni a relatív elérési utakat</span><span class="sxs-lookup"><span data-stu-id="a7456-349">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="a7456-350">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="a7456-350">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="a7456-351">A CertificateInformation egy beállítható tulajdonság, amely a Set-AzureRmApiManagement parancsmag megfelelő működését biztosítja.</span><span class="sxs-lookup"><span data-stu-id="a7456-351">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="a7456-352">Javítva a nuget 4.0.4-es előzetes verziójára való frissítéssel</span><span class="sxs-lookup"><span data-stu-id="a7456-352">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="a7456-353">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="a7456-353">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="a7456-354">A termékben való név szerinti kereséshez tartozó Odata-szűrő kijavítva</span><span class="sxs-lookup"><span data-stu-id="a7456-354">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="a7456-355">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="a7456-355">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="a7456-356">Az API-ban való név szerinti kereséshez tartozó Odata-szűrő kijavítva</span><span class="sxs-lookup"><span data-stu-id="a7456-356">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="a7456-357">Az AzureMonitor támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7456-357">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="a7456-358">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a7456-358">AzureRM.Compute</span></span>
* <span data-ttu-id="a7456-359">Ki lett javítva a hibakimenetből hiányzó céllal kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="a7456-359">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="a7456-360">Ki lett javítva a felügyelt lemezekkel rendelkező virtuális gépek tárfióktípusával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="a7456-360">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="a7456-361">Ki lett javítva az alapértelmezett erőforráscsoportok beállításának hiányával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="a7456-361">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="a7456-362">Ki lettek javítva az AEM Extension-parancsmagok az egyéb környezetekben (pl. Azure China)</span><span class="sxs-lookup"><span data-stu-id="a7456-362">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a7456-363">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a7456-363">AzureRM.Network</span></span>
* <span data-ttu-id="a7456-364">A parancsmagkimenetek alapértelmezett ábrázolása táblanézetre módosítva</span><span class="sxs-lookup"><span data-stu-id="a7456-364">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="a7456-365">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a7456-365">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="a7456-366">Ki lett javítva az a hiba, amely az Update-AzureRmPowerBIEmbeddedCapacity kapcsán jelentkezett a felfüggesztett kapacitás méretezésére tett kísérlet során</span><span class="sxs-lookup"><span data-stu-id="a7456-366">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="a7456-367">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a7456-367">AzureRM.Resources</span></span>
* <span data-ttu-id="a7456-368">Ki lett javítva a felügyelt alkalmazások Marketplace-ről való létrehozásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="a7456-368">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a7456-369">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a7456-369">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a7456-370">Hibák kijavítva:</span><span class="sxs-lookup"><span data-stu-id="a7456-370">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a7456-371">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a7456-371">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a7456-372">A MultiValue útválasztási módszer támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7456-372">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="a7456-373">Új paraméter A MultiValue-útválasztáshoz: MaxReturn</span><span class="sxs-lookup"><span data-stu-id="a7456-373">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="a7456-374">Az alhálózati útválasztási módszer támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7456-374">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="a7456-375">IP-címtartományok (alhálózatok) támogatása a végpontokon</span><span class="sxs-lookup"><span data-stu-id="a7456-375">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="a7456-376">Egyéni fejlécek profilokban való támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7456-376">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="a7456-377">Várt állapotkód-tartományok profilokban való támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7456-377">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="a7456-378">Egyéni fejlécek végpontokon való támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7456-378">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="a7456-379">6.8.0 – 2018. augusztus</span><span class="sxs-lookup"><span data-stu-id="a7456-379">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a7456-380">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="a7456-380">General</span></span>
* <span data-ttu-id="a7456-381">Ki lett javítva az alapértelmezett erőforráscsoportok beállításának hiányával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="a7456-381">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="a7456-382">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a7456-382">AzureRM.Profile</span></span>
* <span data-ttu-id="a7456-383">Lejárati tulajdonság hozzáadva a Connect-AzureRmAccount során visszaadott jogkivonatokhoz</span><span class="sxs-lookup"><span data-stu-id="a7456-383">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a7456-384">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a7456-384">AzureRM.Compute</span></span>
* <span data-ttu-id="a7456-385">Ki lett javítva a hibakimenetből hiányzó céllal kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="a7456-385">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="a7456-386">Ki lett javítva a felügyelt lemezekkel rendelkező virtuális gépek tárfióktípusával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="a7456-386">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="a7456-387">Ki lettek javítva az AEM Extension-parancsmagok az egyéb környezetekben (pl. Azure China)</span><span class="sxs-lookup"><span data-stu-id="a7456-387">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="a7456-388">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="a7456-388">AzureRM.IotHub</span></span>
* <span data-ttu-id="a7456-389">Ki lettek javítva a New-AzureRmIotHubExportDevices és a New-AzureRmIotHubImportDevices példái</span><span class="sxs-lookup"><span data-stu-id="a7456-389">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a7456-390">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a7456-390">AzureRM.Network</span></span>
* <span data-ttu-id="a7456-391">Az alapértelmezett modellek ábrázolása módosítva táblázatos nézetre</span><span class="sxs-lookup"><span data-stu-id="a7456-391">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="a7456-392">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a7456-392">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="a7456-393">Ki lett javítva az a hiba, amely az Update-AzureRmPowerBIEmbeddedCapacity kapcsán jelentkezett a felfüggesztett kapacitás méretezésére tett kísérlet során</span><span class="sxs-lookup"><span data-stu-id="a7456-393">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a7456-394">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a7456-394">AzureRM.Resources</span></span>
* <span data-ttu-id="a7456-395">Ki lett javítva a felügyelt alkalmazások MarketPlace-ről való létrehozásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="a7456-395">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a7456-396">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a7456-396">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a7456-397">Problémák megoldása</span><span class="sxs-lookup"><span data-stu-id="a7456-397">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a7456-398">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a7456-398">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a7456-399">A MultiValue útválasztási módszer támogatása</span><span class="sxs-lookup"><span data-stu-id="a7456-399">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="a7456-400">Új paraméter A MultiValue-útválasztáshoz: MaxReturn</span><span class="sxs-lookup"><span data-stu-id="a7456-400">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="a7456-401">A Subnet útválasztási módszer támogatása</span><span class="sxs-lookup"><span data-stu-id="a7456-401">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="a7456-402">IP-címtartományok (alhálózatok) támogatása a végpontokon</span><span class="sxs-lookup"><span data-stu-id="a7456-402">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="a7456-403">Egyéni fejlécek támogatása a profilokban</span><span class="sxs-lookup"><span data-stu-id="a7456-403">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="a7456-404">Várt állapotkód-tartományok támogatása a profilokban</span><span class="sxs-lookup"><span data-stu-id="a7456-404">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="a7456-405">Egyéni fejlécek támogatása a végpontokon</span><span class="sxs-lookup"><span data-stu-id="a7456-405">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a7456-406">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a7456-406">AzureRM.Websites</span></span>
* <span data-ttu-id="a7456-407">Ki lett javítva az alapértelmezett erőforráscsoportok helytelen beállításával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="a7456-407">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="a7456-408">6.7.0 – 2018. augusztus</span><span class="sxs-lookup"><span data-stu-id="a7456-408">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a7456-409">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a7456-409">AzureRM.Profile</span></span>
* <span data-ttu-id="a7456-410">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-410">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="a7456-411">A környezetek ütközésének elkerülése érdekében a felhasználói azonosító hozzá lett adva az alapértelmezett környezetnévhez</span><span class="sxs-lookup"><span data-stu-id="a7456-411">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="a7456-412">A Clear-AzureRmContext környezetek kiválasztásával kapcsolatos hibáinak javítása #6398</span><span class="sxs-lookup"><span data-stu-id="a7456-412">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="a7456-413">A bérlői tartomány a -TenantId paraméternek történő átadásának engedélyezése a Connect-AzureRmAccount esetén</span><span class="sxs-lookup"><span data-stu-id="a7456-413">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="a7456-414">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a7456-414">Azure.Storage</span></span>
* <span data-ttu-id="a7456-415">Az 5 TB-os korlátozás feloldása Azure-fájlmegosztási kvóta esetén</span><span class="sxs-lookup"><span data-stu-id="a7456-415">Remove the 5TB limitation for Azure File Share quota</span></span>
* <span data-ttu-id="a7456-416">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="a7456-416">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="a7456-417">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a7456-417">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="a7456-418">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-418">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="a7456-419">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a7456-419">Azure.AnalysisServices</span></span>
* <span data-ttu-id="a7456-420">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-420">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="a7456-421">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a7456-421">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="a7456-422">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-422">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="a7456-423">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="a7456-423">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="a7456-424">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-424">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="a7456-425">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="a7456-425">AzureRM.Automation</span></span>
* <span data-ttu-id="a7456-426">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-426">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="a7456-427">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="a7456-427">AzureRM.Backup</span></span>
* <span data-ttu-id="a7456-428">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-428">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="a7456-429">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="a7456-429">AzureRM.Batch</span></span>
* <span data-ttu-id="a7456-430">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-430">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="a7456-431">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="a7456-431">AzureRM.Billing</span></span>
* <span data-ttu-id="a7456-432">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-432">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="a7456-433">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="a7456-433">AzureRM.Cdn</span></span>
* <span data-ttu-id="a7456-434">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-434">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="a7456-435">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a7456-435">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="a7456-436">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-436">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a7456-437">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a7456-437">AzureRM.Compute</span></span>
* <span data-ttu-id="a7456-438">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-438">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="a7456-439">Az EvictionPolicy paraméter hozzá lett adva a New-AzureRmVmssConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a7456-439">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="a7456-440">Az alapértelmezett hely használata a New-AzureRmVm DiskFileParameterSet paraméterében, ha nincs megadva hely.</span><span class="sxs-lookup"><span data-stu-id="a7456-440">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="a7456-441">A paraméter leírásának javítása a Save-AzureRmVMImage esetén</span><span class="sxs-lookup"><span data-stu-id="a7456-441">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="a7456-442">A Get-AzureRmVMDiskEncryptionStatus parancsmag javítása bizonyos egyetlen menetes helyzetekben</span><span class="sxs-lookup"><span data-stu-id="a7456-442">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="a7456-443">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="a7456-443">AzureRM.Consumption</span></span>
* <span data-ttu-id="a7456-444">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-444">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="a7456-445">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a7456-445">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="a7456-446">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-446">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="a7456-447">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a7456-447">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="a7456-448">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-448">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="a7456-449">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="a7456-449">AzureRM.DataFactories</span></span>
* <span data-ttu-id="a7456-450">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-450">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="a7456-451">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a7456-451">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="a7456-452">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-452">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="a7456-453">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="a7456-453">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="a7456-454">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-454">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a7456-455">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a7456-455">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a7456-456">A hibakeresés javítása olyan esetekben, amikor a DebugPreference a PowerShell-parancssorból van beállítva</span><span class="sxs-lookup"><span data-stu-id="a7456-456">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="a7456-457">Példa frissítve a Set-AzureRmDataLakeStoreItemAcl esetén</span><span class="sxs-lookup"><span data-stu-id="a7456-457">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="a7456-458">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-458">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="a7456-459">Példa frissítve a Set-AzureRmDataLakeStoreItemAclEntry esetén</span><span class="sxs-lookup"><span data-stu-id="a7456-459">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="a7456-460">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="a7456-460">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="a7456-461">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-461">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="a7456-462">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="a7456-462">AzureRM.Dns</span></span>
* <span data-ttu-id="a7456-463">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-463">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="a7456-464">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a7456-464">AzureRM.EventGrid</span></span>
* <span data-ttu-id="a7456-465">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-465">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="a7456-466">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="a7456-466">AzureRM.EventHub</span></span>
* <span data-ttu-id="a7456-467">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-467">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="a7456-468">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a7456-468">AzureRM.HDInsight</span></span>
* <span data-ttu-id="a7456-469">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-469">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="a7456-470">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="a7456-470">AzureRM.Insights</span></span>
* <span data-ttu-id="a7456-471">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-471">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="a7456-472">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="a7456-472">AzureRM.IotHub</span></span>
* <span data-ttu-id="a7456-473">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-473">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a7456-474">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a7456-474">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a7456-475">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-475">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="a7456-476">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a7456-476">AzureRM.LogicApp</span></span>
* <span data-ttu-id="a7456-477">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-477">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="a7456-478">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a7456-478">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="a7456-479">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-479">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="a7456-480">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="a7456-480">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="a7456-481">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-481">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="a7456-482">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a7456-482">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="a7456-483">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="a7456-484">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="a7456-484">AzureRM.Media</span></span>
* <span data-ttu-id="a7456-485">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a7456-486">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a7456-486">AzureRM.Network</span></span>
* <span data-ttu-id="a7456-487">Példa hozzáadva a Set-AzureRmLocalNetworkGateway esetén</span><span class="sxs-lookup"><span data-stu-id="a7456-487">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="a7456-488">Példák és leírások hozzáadva az Add-AzureRmVirtualNetworkGatewayIpConfig, a Get-AzureRmVirtualNetworkGatewayConnectionSharedKey és a New-AzureRmVirtualNetworkGatewayConnection esetén</span><span class="sxs-lookup"><span data-stu-id="a7456-488">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="a7456-489">Példák hozzáadva a Remove-AzureRmVirtualNetworkGatewayIpConfig és a Reset-AzureRmVirtualNetworkGateway esetén</span><span class="sxs-lookup"><span data-stu-id="a7456-489">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="a7456-490">Példa hozzáadva a Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey esetén</span><span class="sxs-lookup"><span data-stu-id="a7456-490">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="a7456-491">Példa hozzáadva a Set-AzureRmVirtualNetworkGatewayConnectionSharedKey esetén</span><span class="sxs-lookup"><span data-stu-id="a7456-491">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="a7456-492">Példa hozzáadva a Set-AzureRmVirtualNetworkGatewayConnection esetén</span><span class="sxs-lookup"><span data-stu-id="a7456-492">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="a7456-493">Parancsmagok a legfrissebb kódgenerálóval történő újragenerálása az ApplicationSecurityGroup, a RouteTable és a Usage esetén</span><span class="sxs-lookup"><span data-stu-id="a7456-493">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="a7456-494">Hibaüzenet pontosítva a Get-AzureRmVirtualNetworkSubnetConfig esetén egy nem létező alhálózat lekérésére tett kísérletkor</span><span class="sxs-lookup"><span data-stu-id="a7456-494">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="a7456-495">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="a7456-495">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="a7456-496">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-496">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="a7456-497">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a7456-497">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="a7456-498">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-498">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="a7456-499">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a7456-499">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="a7456-500">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-500">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="a7456-501">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a7456-501">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="a7456-502">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-502">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="a7456-503">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a7456-503">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="a7456-504">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-504">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="a7456-505">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a7456-505">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a7456-506">Szabályzatszűrő hozzáadva a Get-AzureRmRecoveryServicesBackItem parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="a7456-506">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="a7456-507">A parancs visszaadja azon biztonsági mentési elemek listáját, amelyek az adott szabályzatazonosító védelme alá tartoznak.</span><span class="sxs-lookup"><span data-stu-id="a7456-507">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="a7456-508">A Microsoft.Azure.Management.RecoveryServices.Backup frissítve a 3.0.0-preview verzióra.</span><span class="sxs-lookup"><span data-stu-id="a7456-508">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="a7456-509">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-509">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="a7456-510">A TargetResourceGroupName paraméter hozzá lett adva a Restore-AzureRmRecoveryServicesBackupItem parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="a7456-510">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="a7456-511">A Managed Diskek visszaállítására kijelölt erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="a7456-511">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="a7456-512">Managed Diskkel rendelkező virtuális gépek biztonsági másolataira érvényes.</span><span class="sxs-lookup"><span data-stu-id="a7456-512">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="a7456-513">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="a7456-513">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="a7456-514">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-514">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="a7456-515">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a7456-515">AzureRM.RedisCache</span></span>
* <span data-ttu-id="a7456-516">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-516">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="a7456-517">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="a7456-517">AzureRM.Relay</span></span>
* <span data-ttu-id="a7456-518">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-518">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a7456-519">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a7456-519">AzureRM.Resources</span></span>
* <span data-ttu-id="a7456-520">A sablonlapú üzembe helyezés támogatása előfizetési hatókörben.</span><span class="sxs-lookup"><span data-stu-id="a7456-520">Support template deployment at subscription scope.</span></span> <span data-ttu-id="a7456-521">Hozzáadott új parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="a7456-521">Add new Cmdlets:</span></span>
    - <span data-ttu-id="a7456-522">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a7456-522">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="a7456-523">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a7456-523">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="a7456-524">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a7456-524">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="a7456-525">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a7456-525">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="a7456-526">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a7456-526">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="a7456-527">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="a7456-527">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="a7456-528">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="a7456-528">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="a7456-529">Egy hiba javítása, amely során hibaüzenet jelenik meg, ha a Set-AzureRmResource felé egy környezetet továbbítanak</span><span class="sxs-lookup"><span data-stu-id="a7456-529">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="a7456-530">Példa javítva a New-AzureRmResourceGroupDeployment esetén</span><span class="sxs-lookup"><span data-stu-id="a7456-530">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="a7456-531">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-531">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="a7456-532">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="a7456-532">AzureRM.Scheduler</span></span>
* <span data-ttu-id="a7456-533">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-533">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a7456-534">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a7456-534">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a7456-535">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-535">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="a7456-536">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a7456-536">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="a7456-537">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-537">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a7456-538">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a7456-538">AzureRM.Sql</span></span>
* <span data-ttu-id="a7456-539">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-539">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="a7456-540">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="a7456-540">AzureRM.Storage</span></span>
* <span data-ttu-id="a7456-541">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-541">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="a7456-542">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="a7456-542">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="a7456-543">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-543">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="a7456-544">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="a7456-544">AzureRM.Tags</span></span>
* <span data-ttu-id="a7456-545">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-545">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a7456-546">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a7456-546">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a7456-547">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-547">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="a7456-548">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="a7456-548">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="a7456-549">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-549">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a7456-550">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a7456-550">AzureRM.Websites</span></span>
* <span data-ttu-id="a7456-551">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7456-551">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="a7456-552">6.6.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="a7456-552">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a7456-553">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="a7456-553">General</span></span>
* <span data-ttu-id="a7456-554">Frissültek a súgófájlok, hogy minden paramétertípust és a helyes kimeneti/bemeneti típusokat tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="a7456-554">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="a7456-555">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a7456-555">AzureRM.Profile</span></span>
* <span data-ttu-id="a7456-556">Frissült a Common.Strategy kódtár, így ellenőrizni lehet, hogy az erőforrás jelenlegi konfigurációja kompatibilis-e a célerőforrással.</span><span class="sxs-lookup"><span data-stu-id="a7456-556">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="a7456-557">A Common.Storage új ps1xml-típusokkal egészült ki</span><span class="sxs-lookup"><span data-stu-id="a7456-557">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="a7456-558">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a7456-558">Azure.Storage</span></span>
* <span data-ttu-id="a7456-559">A Storage-környezet DefaultProfile használatával történő lekérésének támogatása</span><span class="sxs-lookup"><span data-stu-id="a7456-559">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="a7456-560">A Ps1XmlAttribute hozzá lett adva a parancsmagok kimeneti típusainak tulajdonságaihoz.</span><span class="sxs-lookup"><span data-stu-id="a7456-560">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="a7456-561">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a7456-561">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="a7456-562">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="a7456-562">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="a7456-563">Javítottuk az Automapper hibáját, amely a PsApiManagementApi ApiContractra történő fordítása során jelentkezett</span><span class="sxs-lookup"><span data-stu-id="a7456-563">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="a7456-564">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="a7456-564">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="a7456-565">Javítottuk a File.Save hibáját, hogy a kódolási típus ne terhelje túl</span><span class="sxs-lookup"><span data-stu-id="a7456-565">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="a7456-566">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="a7456-566">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="a7456-567">Frissült a 4.0.3-as Nuget-verzióra, amely felszámolta az apiId mintában jelentkező kivételeit</span><span class="sxs-lookup"><span data-stu-id="a7456-567">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a7456-568">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a7456-568">AzureRM.Compute</span></span>
* <span data-ttu-id="a7456-569">Javítottuk a hibát, amely miatt meghiúsult a virtuális gépek létrehozása a DiskFileParameterSet elemmel a New-AzureRmVm parancsmagban, mert átneveződött a PremiumLRS tárfiók típusa.</span><span class="sxs-lookup"><span data-stu-id="a7456-569">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="a7456-570">Javítottuk az Invoke-AzureRmVMRunCommand parancsmagot</span><span class="sxs-lookup"><span data-stu-id="a7456-570">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="a7456-571">Frissült a Get-AzureRmAvailabilitySet, hogy lehetővé váljon egy előfizetés összes rendelkezésre állási csoportjának listázása.</span><span class="sxs-lookup"><span data-stu-id="a7456-571">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="a7456-572">(A ResouceGroupName paraméter mostantól opcionális.)</span><span class="sxs-lookup"><span data-stu-id="a7456-572">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="a7456-573">Frissült a SimpleParameterSet a New-AzureRmVm parancsmagban, hogy engedélyezni lehessen a gyorsított hálózatot az arra alkalmas virtuális gépeken.</span><span class="sxs-lookup"><span data-stu-id="a7456-573">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="a7456-574">Frissült a New-AzureRmVmss egyszerű paraméterkészlet, hogy ne jöjjön létre vmss, ha egy felhasználó által megadott LB már létezik.</span><span class="sxs-lookup"><span data-stu-id="a7456-574">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="a7456-575">Frissült a New-AzureRmDisk példája</span><span class="sxs-lookup"><span data-stu-id="a7456-575">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="a7456-576">Hozzá lett adva egy, a New-AzureRmVM-re vonatkozó példa</span><span class="sxs-lookup"><span data-stu-id="a7456-576">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="a7456-577">Frissült a Set-AzureRmVMOSDisk leírása</span><span class="sxs-lookup"><span data-stu-id="a7456-577">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="a7456-578">Megfelelő helyesírással és előtaggal frissült a Set-AzureRmVMBginfoExtension 1. példája.</span><span class="sxs-lookup"><span data-stu-id="a7456-578">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="a7456-579">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a7456-579">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="a7456-580">Az ADF.Net SDK verziója 1.1.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="a7456-580">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="a7456-581">Támogatást kaptak az adat-előállítók között megosztott helyi integrációs modulok.</span><span class="sxs-lookup"><span data-stu-id="a7456-581">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="a7456-582">Hozzá lett adva a -SharedIntegrationRuntimeResourceId paraméter a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="a7456-582">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="a7456-583">Hozzá lett adva a -LinkedDataFactoryName paraméter a Remove-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="a7456-583">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a7456-584">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a7456-584">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a7456-585">A DataPlane SDK (Microsoft.Azure.DataLake.Store) verziója 1.1.9-re frissült</span><span class="sxs-lookup"><span data-stu-id="a7456-585">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="a7456-586">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="a7456-586">AzureRM.EventHub</span></span>
* <span data-ttu-id="a7456-587">Frissült az InputObject és a ResourceId átirányítása az eltávolítási parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="a7456-587">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="a7456-588">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="a7456-588">AzureRM.Insights</span></span>
* <span data-ttu-id="a7456-589">Javítottuk az OutputType formázását a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="a7456-589">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="a7456-590">A Microsoft.Azure.Management.Monitor SDK 0.19.1-es előzetes verziója elérhetővé vált</span><span class="sxs-lookup"><span data-stu-id="a7456-590">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a7456-591">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a7456-591">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a7456-592">Javítottuk a Set-AzureRmKeyVaultAccessPolicy átirányítási hibáját</span><span class="sxs-lookup"><span data-stu-id="a7456-592">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a7456-593">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a7456-593">AzureRM.Network</span></span>
* <span data-ttu-id="a7456-594">Új példák lettek hozzáadva a LoadBalancerInboundNatPoolConfig parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="a7456-594">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a7456-595">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a7456-595">AzureRM.Resources</span></span>
* <span data-ttu-id="a7456-596">Javítottuk a hibát, amely akkor jelentkezett, amikor a címke neve és értéke is meg lett adva a Get-AzureRmResource-hoz</span><span class="sxs-lookup"><span data-stu-id="a7456-596">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="a7456-597">Javítottuk a Set-AzureRmResource átirányítási forgatókönyvét</span><span class="sxs-lookup"><span data-stu-id="a7456-597">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a7456-598">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a7456-598">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a7456-599">Frissült az InputObject és a ResourceId átirányítása az eltávolítási parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="a7456-599">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="a7456-600">Kijavítottunk néhány hibát</span><span class="sxs-lookup"><span data-stu-id="a7456-600">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="a7456-601">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a7456-601">AzureRM.Sql</span></span>
* <span data-ttu-id="a7456-602">A következő parancsmagokkal támogatást biztosítottunk a kiszolgáló komplex veszélyforrások elleni védelméhez:</span><span class="sxs-lookup"><span data-stu-id="a7456-602">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="a7456-603">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a7456-603">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="a7456-604">A következő parancsmagokkal támogatást biztosítottunk a sebezhetőségi felméréshez:</span><span class="sxs-lookup"><span data-stu-id="a7456-604">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="a7456-605">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="a7456-605">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="a7456-606">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="a7456-606">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="a7456-607">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="a7456-607">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="a7456-608">Javítottuk a Remove-AzureRmSqlServerFirewallRule példáját</span><span class="sxs-lookup"><span data-stu-id="a7456-608">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="a7456-609">Javítottuk a dátum és idő helytelen kezelését a Get-AzureSqlSyncGroupLog USA-n kívüli kulturális környezeteiben</span><span class="sxs-lookup"><span data-stu-id="a7456-609">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="a7456-610">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="a7456-610">AzureRM.Storage</span></span>
* <span data-ttu-id="a7456-611">A Ps1XmlAttribute hozzá lett adva a parancsmagok kimeneti típusainak tulajdonságaihoz</span><span class="sxs-lookup"><span data-stu-id="a7456-611">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="a7456-612">A StorageAccount parancsmag kimenete táblanézetben is megjeleníthetővé vált</span><span class="sxs-lookup"><span data-stu-id="a7456-612">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="a7456-613">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a7456-613">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="a7456-614">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a7456-614">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="a7456-615">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a7456-615">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="a7456-616">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="a7456-616">AzureRM.Tags</span></span>
* <span data-ttu-id="a7456-617">El lett távolítva egy helytelen állítás a Tag parancsmag súgójából</span><span class="sxs-lookup"><span data-stu-id="a7456-617">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="a7456-618">6.5.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="a7456-618">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a7456-619">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a7456-619">AzureRM.Profile</span></span>
* <span data-ttu-id="a7456-620">A Get-AzureRmContextAutosaveSetting súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="a7456-620">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="a7456-621">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a7456-621">Azure.Storage</span></span>
* <span data-ttu-id="a7456-622">Blob vagy fájl feltöltésének támogatása csak írási SAS-jogkivonattal</span><span class="sxs-lookup"><span data-stu-id="a7456-622">Support Upload Blob or File with write only Sas token</span></span>
* <span data-ttu-id="a7456-623">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a7456-623">Set-AzureStorageBlobContent</span></span>
* <span data-ttu-id="a7456-624">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a7456-624">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="a7456-625">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a7456-625">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="a7456-626">A kötelező ResourceGroupName tulajdonság hozzáadása az AS-hez.</span><span class="sxs-lookup"><span data-stu-id="a7456-626">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="a7456-627">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="a7456-627">AzureRM.Automation</span></span>
* <span data-ttu-id="a7456-628">A súgó frissítése és a New-AzureRMAutomationSchedule példájának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="a7456-628">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a7456-629">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a7456-629">AzureRM.Compute</span></span>
* <span data-ttu-id="a7456-630">A -Tag paraméter hozzáadása a következőhöz: Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a7456-630">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="a7456-631">Az Add-AzureRmVmssExtension példájának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="a7456-631">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="a7456-632">A Remove-AzureRmVmssExtension példáinak hozzáadása</span><span class="sxs-lookup"><span data-stu-id="a7456-632">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="a7456-633">A Set-AzureRmVMAccessExtension súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="a7456-633">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="a7456-634">A New-AzureRmVmss SimpleParameterSet készletének frissítése, hogy a SinglePlacementGroup alapértelmezés szerint false (hamis) legyen, és a SinglePlacementGroup kapcsolóparaméter hozzáadása, amellyel a felhasználó egyetlen elhelyezési csoportban hozhatja létre a VMSS-t.</span><span class="sxs-lookup"><span data-stu-id="a7456-634">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="a7456-635">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="a7456-635">AzureRM.EventHub</span></span>
* <span data-ttu-id="a7456-636">A csak olvasási PendingReplicationOperationsCount tulajdonság hozzáadása a PSEventHubDRConfigurationAttributes osztályhoz, amely megadja a függőben lévő replikációs műveletek számát a replikáció során</span><span class="sxs-lookup"><span data-stu-id="a7456-636">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a7456-637">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a7456-637">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a7456-638">A Set-AzureRmKeyVaultAccessPolicy hibaüzenetének frissítése</span><span class="sxs-lookup"><span data-stu-id="a7456-638">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="a7456-639">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a7456-639">AzureRM.LogicApp</span></span>
* <span data-ttu-id="a7456-640">„A paraméterkészlet nem oldható fel” hiba kijavítása a következőben: New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a7456-640">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a7456-641">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a7456-641">AzureRM.Network</span></span>
* <span data-ttu-id="a7456-642">Társviszony-létesítés engedélyezése több bérlőben lévő virtuális hálózatok között a következőhöz: Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="a7456-642">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="a7456-643">Az alábbi parancsmagok frissítése az Application Gatewayhez</span><span class="sxs-lookup"><span data-stu-id="a7456-643">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="a7456-644">New-AzureRmApplicationGateway: Hozzáadott EnableFIPS jelző és zónatámogatás</span><span class="sxs-lookup"><span data-stu-id="a7456-644">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="a7456-645">New-AzureRmApplicationGatewaySku: Hozzáadott új Standard_v2 és WAF_v2 SKU-k</span><span class="sxs-lookup"><span data-stu-id="a7456-645">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="a7456-646">Set-AzureRmApplicationGatewaySku: Hozzáadott új Standard_v2 és WAF_v2 SKU-k</span><span class="sxs-lookup"><span data-stu-id="a7456-646">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="a7456-647">A legújabb generátorverzióval újból létrehozott RouteTable parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a7456-647">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="a7456-648">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="a7456-648">AzureRM.Relay</span></span>
* <span data-ttu-id="a7456-649">Frissített Markdown-fájlok, a példában lévő paraméternév-hiba javítása</span><span class="sxs-lookup"><span data-stu-id="a7456-649">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a7456-650">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a7456-650">AzureRM.Resources</span></span>
* <span data-ttu-id="a7456-651">A Roleassignment és a roledefinition parancsmagok frissítése:</span><span class="sxs-lookup"><span data-stu-id="a7456-651">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="a7456-652">A felesleges roledefinition hívások eltávolítása a lapozás részeként.</span><span class="sxs-lookup"><span data-stu-id="a7456-652">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="a7456-653">A Get-AzureRmRoleAssignment parancsmag javítása</span><span class="sxs-lookup"><span data-stu-id="a7456-653">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="a7456-654">Az -ExpandPrincipalGroups parancsparaméter működésének javítása</span><span class="sxs-lookup"><span data-stu-id="a7456-654">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="a7456-655">A Get-AzureRmResource hibájának kijavítása, ahol a -ResourceType paraméter különbséget tett a kis- és nagybetűk között</span><span class="sxs-lookup"><span data-stu-id="a7456-655">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a7456-656">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a7456-656">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a7456-657">A top és skip paraméter hozzáadása a listázási parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="a7456-657">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="a7456-658">Standard – Prémium NameSpace migrálási parancsmagok hozzáadása:</span><span class="sxs-lookup"><span data-stu-id="a7456-658">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="a7456-659">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a7456-659">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="a7456-660">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a7456-660">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="a7456-661">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a7456-661">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="a7456-662">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a7456-662">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="a7456-663">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a7456-663">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="a7456-664">A csak olvasási PendingReplicationOperationsCount tulajdonság hozzáadása a PSServiceBusDRConfigurationAttributes osztályhoz, amely megadja a függőben lévő replikációs műveletek számát a replikáció során</span><span class="sxs-lookup"><span data-stu-id="a7456-664">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="a7456-665">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a7456-665">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="a7456-666">A New-AzureRmServiceFabricCluster példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="a7456-666">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a7456-667">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a7456-667">AzureRM.Sql</span></span>
* <span data-ttu-id="a7456-668">Új parancsmagok hozzáadása a Management.Sql elemhez, amelyekkel az ügyfelek TDE-tanúsítványt adhatnak az SQL Server-példányhoz vagy egy felügyelt példányhoz</span><span class="sxs-lookup"><span data-stu-id="a7456-668">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="a7456-669">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="a7456-669">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="a7456-670">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="a7456-670">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a7456-671">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a7456-671">AzureRM.Websites</span></span>
* <span data-ttu-id="a7456-672">A `Set-AzureRmWebApp -AssignIdentity` és `Set-AzureRmWebAppSlot -AssignIdentity` a false (hamis) érték esetén mostantól eltávolítja az Identitás tulajdonságot a hely object.Removing „előzetes verzió” címkéjéből is.</span><span class="sxs-lookup"><span data-stu-id="a7456-672">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="a7456-673">A `Get-AzureRmWebAppMetrics` és a `Get-AzureRmAppServicePlanMetrics` példa frissítése</span><span class="sxs-lookup"><span data-stu-id="a7456-673">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="a7456-674">A `Set-AzureRmWebApp -PhpVersion` támogatja az off értéket érvényes PHP-verzióként</span><span class="sxs-lookup"><span data-stu-id="a7456-674">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="a7456-675">6.4.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="a7456-675">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a7456-676">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="a7456-676">General</span></span>
* <span data-ttu-id="a7456-677">Az OutputType attribútum formázása javítva a legtöbb modul súgófájljaiban</span><span class="sxs-lookup"><span data-stu-id="a7456-677">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="a7456-678">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a7456-678">AzureRM.Profile</span></span>
* <span data-ttu-id="a7456-679">A Ps1Xml attribútum hozzáadva az alapszintű kimenettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="a7456-679">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a7456-680">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a7456-680">AzureRM.Compute</span></span>
* <span data-ttu-id="a7456-681">A VMSS IP-címke funkciója</span><span class="sxs-lookup"><span data-stu-id="a7456-681">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="a7456-682">A „New-AzureRmVmssIpTagConfig” parancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7456-682">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="a7456-683">Az IpTag paraméter hozzáadva a New-AzureRmVmssIpConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a7456-683">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="a7456-684">A VMSS automatikus operációsrendszer-visszaállítási funkciója</span><span class="sxs-lookup"><span data-stu-id="a7456-684">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="a7456-685">A DisableAutoRollback-paraméterek hozzáadva a New-AzureRmVmssConfig és az Update-AzureRmVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a7456-685">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="a7456-686">A VMSS operációsrendszer-frissítési előzmények funkciója</span><span class="sxs-lookup"><span data-stu-id="a7456-686">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="a7456-687">Az OSUpgradeHistory kapcsolóparaméter hozzáadva a Get-AzureRmVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a7456-687">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="a7456-688">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="a7456-688">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="a7456-689">Katalógushozzáférés-vezérlési listák támogatása hozzáadva az alábbi parancsokhoz:</span><span class="sxs-lookup"><span data-stu-id="a7456-689">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="a7456-690">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a7456-690">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="a7456-691">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a7456-691">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="a7456-692">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a7456-692">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a7456-693">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a7456-693">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a7456-694">Megszakítás támogatása és az előrehaladás nyomon követése hozzáadva a Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry és Set-AzureRmDataLakeStoreItemAcl parancshoz</span><span class="sxs-lookup"><span data-stu-id="a7456-694">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="a7456-695">Megszakítás támogatása hozzáadva az Export-AzureRmDataLakeStoreChildItemProperties parancshoz</span><span class="sxs-lookup"><span data-stu-id="a7456-695">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="a7456-696">A rekurzív műveleteket végző parancsmagok hibakeresési üzeneteinek kiürítése javítva</span><span class="sxs-lookup"><span data-stu-id="a7456-696">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="a7456-697">A DataLake-parancsmagok tesztelési helye javítva</span><span class="sxs-lookup"><span data-stu-id="a7456-697">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="a7456-698">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="a7456-698">AzureRM.EventHub</span></span>
* <span data-ttu-id="a7456-699">Opcionális MaxCount paraméter hozzáadva a Get-AzureRmEventHub és a Get-AzureRmEventHubConsumerGroup listaműveleti parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a7456-699">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="a7456-700">Ki lett javítva egy probléma a New-AzureRmEventHub parancsmagban, ahol legalább egy paramétert meg kellett adni az új EventHub létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="a7456-700">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="a7456-701">Az alapértelmezett paraméterkészlet rendelkezésre áll.</span><span class="sxs-lookup"><span data-stu-id="a7456-701">Provided Default Parameter set.</span></span>
* <span data-ttu-id="a7456-702">-KeyValue opcionális paraméter hozzáadva a New-AzureRmEventHubKey parancsmaghoz, amellyel a felhasználó megadhatja a KeyValue paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="a7456-702">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a7456-703">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a7456-703">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a7456-704">Ki lett javítva az a probléma, hogy a Get-AzureRmKeyVault -Tag paramétere az összes erőforrást visszaadta</span><span class="sxs-lookup"><span data-stu-id="a7456-704">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a7456-705">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a7456-705">AzureRM.Network</span></span>
* <span data-ttu-id="a7456-706">Új termékváltozatok közzététele a zónaredundáns VirtualNetworkGatewayshez</span><span class="sxs-lookup"><span data-stu-id="a7456-706">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="a7456-707">Új parancsok hozzáadva a következő funkcióhoz: ExpressRoute-partner API-k az ARM-en keresztül</span><span class="sxs-lookup"><span data-stu-id="a7456-707">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="a7456-708">Get-AzureRmExpressRouteCrossConnection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7456-708">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="a7456-709">Set-AzureRmExpressRouteCrossConnection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7456-709">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="a7456-710">Add-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7456-710">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="a7456-711">Get-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7456-711">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="a7456-712">Remove-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7456-712">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="a7456-713">Get-AzureRMExpressRouteCrossConnectionArpTable hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7456-713">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="a7456-714">Get-AzureRMExpressRouteCrossConnectionRouteTable hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7456-714">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="a7456-715">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7456-715">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="a7456-716">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a7456-716">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a7456-717">Get-AzureRmRecoveryServicesBackupStatus parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="a7456-717">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="a7456-718">Ez a parancsmag egy virtuális gép azonosítójának használatával ellenőrzi, hogy a virtuális gépet védi-e tároló az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="a7456-718">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="a7456-719">Ha van ilyen tároló, a parancsmag megjeleníti annak részleteit.</span><span class="sxs-lookup"><span data-stu-id="a7456-719">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a7456-720">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a7456-720">AzureRM.Resources</span></span>
* <span data-ttu-id="a7456-721">Frissültek a Get-AzureRmPolicyAssignment-parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="a7456-721">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="a7456-722">-Scope-értékek listázásának támogatása hozzáadva a felügyeleti csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="a7456-722">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="a7456-723">-Scope-értékekkel történő egyedi hozzárendelések lekérésének támogatása hozzáadva a felügyeleti csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="a7456-723">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="a7456-724">-Effective és -All kapcsoló hozzáadva a vezérlő paraméterhez</span><span class="sxs-lookup"><span data-stu-id="a7456-724">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="a7456-725">Frissültek a Get/New/Remove/Set-AzureRmPolicyDefinition-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a7456-725">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="a7456-726">-ManagementGroupName paraméter hozzáadva a műveletek adott felügyeleti csoporton történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="a7456-726">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="a7456-727">-SubscriptionId paraméter hozzáadva a műveletek adott előfizetésen történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="a7456-727">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="a7456-728">Frissültek a Get/New/Remove/Set-AzureRmPolicySetDefinition-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a7456-728">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="a7456-729">-ManagementGroupName paraméter hozzáadva a műveletek adott felügyeleti csoporton történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="a7456-729">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="a7456-730">-SubscriptionId paraméter hozzáadva a műveletek adott előfizetésen történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="a7456-730">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="a7456-731">KeyVault titkoskulcs-referencia paraméterekben történő használatának támogatása hozzáadva a TemplateParameterObject használatakor a New-AzureRmResourceGroupDeployment parancsmagban</span><span class="sxs-lookup"><span data-stu-id="a7456-731">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="a7456-732">Ki lett javítva egy probléma, amelynek során a rendszer nem vette figyelembe a New-AzureRmADAppCredential parancsmag -EndDate paraméterét</span><span class="sxs-lookup"><span data-stu-id="a7456-732">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="a7456-733">Ki lett javítva egy probléma, amelynek során az Add-AzureRmADGroupMember parancsmag nem megfelelő URL-címet használt a kérések elvégzéséhez</span><span class="sxs-lookup"><span data-stu-id="a7456-733">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="a7456-734">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a7456-734">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a7456-735">A -KeyValue opcionális paraméter hozzáadva a New-AzureRmServiceBusKey parancsmaghoz, amellyel a felhasználó megadhatja a KeyValue paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="a7456-735">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a7456-736">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a7456-736">AzureRM.Sql</span></span>
* <span data-ttu-id="a7456-737">Tisztázva lettek az SQLDW felhasználó által meghatározott visszaállítási pontjai a New-AzureRmSqlDatabaseRestorePoint súgójában</span><span class="sxs-lookup"><span data-stu-id="a7456-737">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="a7456-738">Frissült a -ComputeGeneration paraméter dokumentációja több parancsmagban</span><span class="sxs-lookup"><span data-stu-id="a7456-738">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="a7456-739">6.3.0 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="a7456-739">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a7456-740">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a7456-740">AzureRM.Profile</span></span>
* <span data-ttu-id="a7456-741">Az Enable-AzureRmContextAutoSave hibaüzenetei frissültek</span><span class="sxs-lookup"><span data-stu-id="a7456-741">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="a7456-742">Egy környezet jön létre minden előfizetéshez, amelyben a Connect-AzureRmAccount korábbi környezet nélkül fut</span><span class="sxs-lookup"><span data-stu-id="a7456-742">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="a7456-743">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a7456-743">Azure.Storage</span></span>
* <span data-ttu-id="a7456-744">További információk lettek hozzáadva a súgófájlokhoz a -Permissions paraméterrel kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="a7456-744">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a7456-745">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a7456-745">AzureRM.Compute</span></span>
* <span data-ttu-id="a7456-746">A Get-AzureRmVmDiskEncryptionStatus kijavít egy hibát, amely az adatlemezekkel nem rendelkező virtuális gépeken jelentkezik</span><span class="sxs-lookup"><span data-stu-id="a7456-746">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="a7456-747">A Compute ügyfélkódtár-verziója frissült, a következő parancsmagok javítása érdekében</span><span class="sxs-lookup"><span data-stu-id="a7456-747">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="a7456-748">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="a7456-748">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="a7456-749">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="a7456-749">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="a7456-750">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="a7456-750">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="a7456-751">A következő parancsmagok ki lettek javítva, így helyesen jelenítik meg a műveletazonosítót és a művelet állapotát:</span><span class="sxs-lookup"><span data-stu-id="a7456-751">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="a7456-752">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a7456-752">Start-AzureRmVM</span></span>
    - <span data-ttu-id="a7456-753">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a7456-753">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="a7456-754">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a7456-754">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="a7456-755">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a7456-755">Set-AzureRmVM</span></span>
    - <span data-ttu-id="a7456-756">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a7456-756">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="a7456-757">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a7456-757">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="a7456-758">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="a7456-758">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="a7456-759">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="a7456-759">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="a7456-760">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a7456-760">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="a7456-761">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a7456-761">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="a7456-762">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a7456-762">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="a7456-763">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a7456-763">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="a7456-764">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="a7456-764">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="a7456-765">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="a7456-765">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="a7456-766">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="a7456-766">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="a7456-767">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="a7456-767">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="a7456-768">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="a7456-768">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="a7456-769">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="a7456-769">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="a7456-770">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a7456-770">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="a7456-771">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a7456-771">AzureRM.EventGrid</span></span>
* <span data-ttu-id="a7456-772">A ValidateNotNullOrEmpty érvényesítési feltételei az Update-AzureRmEventGridSubscription parancsmagban található SubjectBeginsWith/SubjectEndsWith esetében el lettek távolítva, így ha szükséges, ezek a paraméterek üres sztringre módosíthatók.</span><span class="sxs-lookup"><span data-stu-id="a7456-772">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a7456-773">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a7456-773">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a7456-774">Ki lett javítva egy probléma, amelynek során a parancs nem adott vissza címkét a Get-AzureRmKeyVault -Tag futtatásakor</span><span class="sxs-lookup"><span data-stu-id="a7456-774">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="a7456-775">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a7456-775">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="a7456-776">A Policy Insights-parancsmagok nyilvános kiadása</span><span class="sxs-lookup"><span data-stu-id="a7456-776">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="a7456-777">A 2018.04.04. dátumú API-verziót használják</span><span class="sxs-lookup"><span data-stu-id="a7456-777">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="a7456-778">A PolicyDefinitionReferenceId hozzá lett adva a Get-AzureRmPolicyStateSummary eredményeihez</span><span class="sxs-lookup"><span data-stu-id="a7456-778">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="a7456-779">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a7456-779">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a7456-780">A -Vault paraméter hozzá lett adva a RecoveryServices.Backup-parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="a7456-780">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="a7456-781">Ha át van adva, felülbírálja a Set-AzureRmRecoveryServicesContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a7456-781">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a7456-782">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a7456-782">AzureRM.Sql</span></span>
* <span data-ttu-id="a7456-783">A Get-AzureRmSqlDatabaseExpanded súgófájljában lévő példa frissült</span><span class="sxs-lookup"><span data-stu-id="a7456-783">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a7456-784">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a7456-784">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a7456-785">Az Add-AzureRmTrafficManagerEndpointConfig súgófájlja frissült</span><span class="sxs-lookup"><span data-stu-id="a7456-785">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a7456-786">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a7456-786">AzureRM.Websites</span></span>
* <span data-ttu-id="a7456-787">Frissült a Set-AzureRmWebApp, így az AppSettings nem lesz felülírva az -AssignIdentity használatakor</span><span class="sxs-lookup"><span data-stu-id="a7456-787">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="a7456-788">Frissült a New-AzureRmWebAppSlot, így figyelembe veszi az AppServicePlan paramétert választható paraméterként</span><span class="sxs-lookup"><span data-stu-id="a7456-788">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="a7456-789">6.2.1 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="a7456-789">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="a7456-790">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a7456-790">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="a7456-791">Frissült a PSWorkspace modell, így lehetővé teszi, hogy a hálózat a típust paraméterként használja</span><span class="sxs-lookup"><span data-stu-id="a7456-791">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="a7456-792">6.2.0 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="a7456-792">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a7456-793">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a7456-793">AzureRM.Profile</span></span>
* <span data-ttu-id="a7456-794">Kijavítottuk a problémát, amely miatt a Newtonsoft.Json 10.0.3-as verziója nem töltődött be a modul importálása során</span><span class="sxs-lookup"><span data-stu-id="a7456-794">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a7456-795">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a7456-795">AzureRM.Compute</span></span>
* <span data-ttu-id="a7456-796">VMSS VM frissítési funkciója</span><span class="sxs-lookup"><span data-stu-id="a7456-796">VMSS VM Update feature</span></span>
    - <span data-ttu-id="a7456-797">Hozzá lett adva az Update-AzureRmVmssVM és a New-AzureRmVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="a7456-797">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="a7456-798">A VirtualMachineScaleSetVM paraméter hozzá lett adva az Add-AzureRmVMDataDisk parancsmaghoz, hogy adatlemezt lehessen hozzáadni a VMSS VM-hez</span><span class="sxs-lookup"><span data-stu-id="a7456-798">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="a7456-799">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a7456-799">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="a7456-800">Az ADF .Net SDK frissült a 0.8.0-s előzetes verzióra, amely az alábbi változásokat tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="a7456-800">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="a7456-801">Hozzá lett adva a gyári adattár konfigurálási művelete</span><span class="sxs-lookup"><span data-stu-id="a7456-801">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="a7456-802">Frissült a QuickBooks társított szolgáltatás a consumerKey és a consumerSecret tulajdonság elérhetővé tételéhez</span><span class="sxs-lookup"><span data-stu-id="a7456-802">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="a7456-803">Több modelltípus is frissült, a SecretBase-től az objektumig</span><span class="sxs-lookup"><span data-stu-id="a7456-803">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="a7456-804">A rendszer blobesemény-indítókkal bővült</span><span class="sxs-lookup"><span data-stu-id="a7456-804">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="a7456-805">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a7456-805">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a7456-806">A dokumentáció kimeneti példával bővült</span><span class="sxs-lookup"><span data-stu-id="a7456-806">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="a7456-807">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a7456-807">AzureRM.Network</span></span>
* <span data-ttu-id="a7456-808">Engedélyezve lettek a Traffic Analytics-paraméterek a Network Watcher-parancsmagokon</span><span class="sxs-lookup"><span data-stu-id="a7456-808">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a7456-809">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a7456-809">AzureRM.Resources</span></span>
* <span data-ttu-id="a7456-810">Kijavítottuk a „PSResource” objektum(ok) Get-AzureRmResource által visszaadott „Properties” tulajdonságával kapcsolatos hibát</span><span class="sxs-lookup"><span data-stu-id="a7456-810">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="a7456-811">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="a7456-811">AzureRM.Scheduler</span></span>
* <span data-ttu-id="a7456-812">Kijavítottuk a hibát, amely miatt a ServiceBusQueueJob frissítése nem állított be új hitelesítési adatokat</span><span class="sxs-lookup"><span data-stu-id="a7456-812">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="a7456-813">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a7456-813">AzureRM.Sql</span></span>
* <span data-ttu-id="a7456-814">A következő parancsmagok az opcionális LicenseType paraméterrel frissültek</span><span class="sxs-lookup"><span data-stu-id="a7456-814">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="a7456-815">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a7456-815">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="a7456-816">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a7456-816">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="a7456-817">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="a7456-817">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="a7456-818">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a7456-818">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="a7456-819">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a7456-819">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a7456-820">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a7456-820">AzureRM.Websites</span></span>
* <span data-ttu-id="a7456-821">Frissült a New-AzureRMWebApp, hogy képes legyen a stratégia könyvtárból származó bevett algoritmusok használatára.</span><span class="sxs-lookup"><span data-stu-id="a7456-821">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="a7456-822">6.1.0 – 2018. május</span><span class="sxs-lookup"><span data-stu-id="a7456-822">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a7456-823">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a7456-823">AzureRM.Profile</span></span>
* <span data-ttu-id="a7456-824">Ki lett javítva az a hiba, amelyben a „Clear-AzureRmContext” futtatása egy üres környezetet tartott meg az előző alapértelmezett környezet nevével, így a felhasználó nem tudott létrehozni új környezetet a régi néven</span><span class="sxs-lookup"><span data-stu-id="a7456-824">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="a7456-825">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a7456-825">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="a7456-826">Az átjárók társítási/társításmegszüntetési műveleteinek engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="a7456-826">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="a7456-827">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a7456-827">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="a7456-828">Az ApiVersion, ApiRelease és ApiRevision paraméterek mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="a7456-828">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="a7456-829">A Service Fabric háttérrendszer mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="a7456-829">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="a7456-830">Az Application Insights naplózó mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="a7456-830">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="a7456-831">Az „Alapszintű” termékváltozat érvényes termékváltozatként való elismerése mostantól támogatott az API Management szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="a7456-831">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="a7456-832">A privát hitelesítésszolgáltató által kiállított tanúsítványok fő- vagy hitelesítésszolgáltatói tanúsítványként való telepítése mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="a7456-832">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="a7456-833">Az egyéni SSL-tanúsítványok KeyVault- és többproxys gazdaneveken keresztüli fogadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="a7456-833">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="a7456-834">Az MSI-identitások mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="a7456-834">Added support for MSI identity</span></span>
* <span data-ttu-id="a7456-835">A házirendek URL-kapcsolaton keresztüli fogadása mostantól támogatott MEGJEGYZÉS: A következő parancsmagok elavulttá válnak a jövőbeli kiadásokban</span><span class="sxs-lookup"><span data-stu-id="a7456-835">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="a7456-836">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="a7456-836">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="a7456-837">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7456-837">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="a7456-838">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="a7456-838">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="a7456-839">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="a7456-839">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="a7456-840">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="a7456-840">AzureRM.Batch</span></span>
* <span data-ttu-id="a7456-841">Új Get-AzureBatchPoolNodeCounts parancsmag kiadása</span><span class="sxs-lookup"><span data-stu-id="a7456-841">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="a7456-842">Új Start-AzureBatchComputeNodeServiceLogUpload parancsmag kiadása</span><span class="sxs-lookup"><span data-stu-id="a7456-842">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="a7456-843">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="a7456-843">AzureRM.Consumption</span></span>
* <span data-ttu-id="a7456-844">A Get-AzureRmConsumptionUsageDetail parancsmag kiegészítése új Expand, ResourceGroup, InstanceName, InstanceId, Tags és Top paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="a7456-844">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a7456-845">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a7456-845">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a7456-846">Az Export-AzureRmDataLakeStoreChildItemProperties példájának kijavítása</span><span class="sxs-lookup"><span data-stu-id="a7456-846">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="a7456-847">A Set-AzureRmDataLakeStoreItemAclEntry Recurse esetében fellépő null paraméter kivétel kijavítása</span><span class="sxs-lookup"><span data-stu-id="a7456-847">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="a7456-848">A Set-AzureRmDataLakeStoreItemAclEntry, a Set-AzureRmDataLakeStoreItemAcl és a Remove-AzureRmDataLakeStoreItemAclEntry súgófájljainak javítása</span><span class="sxs-lookup"><span data-stu-id="a7456-848">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="a7456-849">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a7456-849">AzureRM.Network</span></span>
* <span data-ttu-id="a7456-850">A hálózati SDK-verzió felléptetése a 18.0.0-s előzetes verzióról a 19.0.0-s előzetes verzióra</span><span class="sxs-lookup"><span data-stu-id="a7456-850">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="a7456-851">Új parancsmag hozzáadva a protokollkonfigurációk létrehozásához</span><span class="sxs-lookup"><span data-stu-id="a7456-851">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="a7456-852">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7456-852">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="a7456-853">Új parancsmag hozzáadva az új kapcsolatcsoportok hozzáadásához a meglévő ExpressRoute-kapcsolatcsoportokhoz.</span><span class="sxs-lookup"><span data-stu-id="a7456-853">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="a7456-854">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a7456-854">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="a7456-855">Új parancsmag hozzáadva a kapcsolatcsoportok eltávolításához a meglévő ExpressRoute-kapcsolatcsoportokból.</span><span class="sxs-lookup"><span data-stu-id="a7456-855">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="a7456-856">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a7456-856">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="a7456-857">Új parancsmag hozzáadva a kapcsolatcsoportok lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="a7456-857">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="a7456-858">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a7456-858">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="a7456-859">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a7456-859">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="a7456-860">A kiszolgálói hitelesítés létrehozott tanúsítványokkal való használata (5998. sz. hiba) ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="a7456-860">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a7456-861">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a7456-861">AzureRM.Sql</span></span>
* <span data-ttu-id="a7456-862">A frissített naplózási parancsmagok lehetővé teszik az AuditAction és AuditActionGroup paraméterek eltávolítását</span><span class="sxs-lookup"><span data-stu-id="a7456-862">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="a7456-863">A Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy hibája ki lett javítva, amikor az új rugalmas adatmegőrzési szabályzatok megadásakor a parancs a következő hibát adta vissza: „A hosszútávú adatmegőrzési szabályzat megadása Azure Recovery Services-tárolókkal és szabályzatokkal már nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="a7456-863">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="a7456-864">Adja le a kérést az új rugalmas adatmegőrzési szabályzattal”.</span><span class="sxs-lookup"><span data-stu-id="a7456-864">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="a7456-865">Az összes Azure SQL Database/ElasticPool létrehozással/frissítéssel kapcsolatos parancsmag frissítve lett az új Database API használatára, amely támogatja a termékváltozat tulajdonságot a méretezéssel és szintekkel kapcsolatos tulajdonságok esetében.</span><span class="sxs-lookup"><span data-stu-id="a7456-865">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="a7456-866">A frissített parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="a7456-866">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="a7456-867">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a7456-867">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="a7456-868">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a7456-868">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="a7456-869">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="a7456-869">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="a7456-870">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a7456-870">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="a7456-871">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a7456-871">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a7456-872">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a7456-872">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a7456-873">A Get-AzureRmTrafficManagerProfile paramétereinek frissítésével a -ResourceGroupName paraméter megadása mostantól kötelező a -Name paraméter használata esetén.</span><span class="sxs-lookup"><span data-stu-id="a7456-873">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
