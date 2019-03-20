---
ms.openlocfilehash: 9915ff37e59a73c1d226a216213fd9016b55d3d4
ms.sourcegitcommit: 447276d46ffeeb37f0c07a570536665e36c5ddb8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/14/2019
ms.locfileid: "57882480"
---
## <a name="150---march-2019"></a><span data-ttu-id="15c59-101">1.5.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="15c59-101">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="15c59-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="15c59-102">Az.Accounts</span></span>
* <span data-ttu-id="15c59-103">A Register-AzModule parancs hozzáadása az AutoRest által létrehozott parancsmagok támogatásához</span><span class="sxs-lookup"><span data-stu-id="15c59-103">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="15c59-104">A Connect-AzAccount példáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="15c59-104">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="15c59-105">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="15c59-105">Az.Automation</span></span>
* <span data-ttu-id="15c59-106">A bizonyos havi ütemezések lekérésekor jelentkező hiba kijavítva számos Azure Automation-parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="15c59-106">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="15c59-107">Ki lett javítva a hiba, amely miatt a Get-AzAutomationDscNode csak az első 20 csomópontot adta vissza.</span><span class="sxs-lookup"><span data-stu-id="15c59-107">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="15c59-108">Most már az összes csomópontot visszaadja</span><span class="sxs-lookup"><span data-stu-id="15c59-108">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="15c59-109">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="15c59-109">Az.Cdn</span></span>
* <span data-ttu-id="15c59-110">Új Powershell-parancsmagok hozzáadva az Egyéni tartományi Https engedélyezése/letiltása szolgáltatáshoz, a régiek elavultak</span><span class="sxs-lookup"><span data-stu-id="15c59-110">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="15c59-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="15c59-111">Az.Compute</span></span>
* <span data-ttu-id="15c59-112">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="15c59-112">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="15c59-113">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="15c59-113">Az.DataFactory</span></span>
* <span data-ttu-id="15c59-114">Az ADF .Net SDK verziója 3.0.1-re frissült</span><span class="sxs-lookup"><span data-stu-id="15c59-114">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="15c59-115">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="15c59-115">Az.LogicApp</span></span>
* <span data-ttu-id="15c59-116">Ki lett javítva a hiba, amely miatt a ListWorkflows csak az eredmények első oldalát kérte le</span><span class="sxs-lookup"><span data-stu-id="15c59-116">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="15c59-117">Az.Network</span><span class="sxs-lookup"><span data-stu-id="15c59-117">Az.Network</span></span>
* <span data-ttu-id="15c59-118">Helyettesítő karakterek támogatásának hozzáadása a Network-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="15c59-118">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="15c59-119">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="15c59-119">Az.RecoveryServices</span></span>
* <span data-ttu-id="15c59-120">Azure-beli virtuális gépen futtatott SQL Server támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="15c59-120">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="15c59-121">SDK-frissítés</span><span class="sxs-lookup"><span data-stu-id="15c59-121">SDK Update</span></span>
* <span data-ttu-id="15c59-122">VMappContainer ellenőrzés eltávolítva a Get-ProtectableItem parancsmagból</span><span class="sxs-lookup"><span data-stu-id="15c59-122">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="15c59-123">Name és ServerName paraméterek hozzáadva a Get-ProtectableItem parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="15c59-123">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="15c59-124">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="15c59-124">Az.Resources</span></span>
* <span data-ttu-id="15c59-125">`-TemplateObject` paraméter hozzáadva az üzembe helyező parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="15c59-125">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="15c59-126">További információ: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="15c59-126">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="15c59-127">Ki lett javítva a hiba, amely akkor jelentkezett, amikor a(z) `Get-AzResource` eredménye át lett irányítva a következőbe: `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="15c59-127">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="15c59-128">További információ: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="15c59-128">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="15c59-129">Ki lett javítva a JSON-adattípus módosításával kapcsolatos probléma, amely a(z) `Set-AzResource` futtatásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="15c59-129">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="15c59-130">További információ: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="15c59-130">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="15c59-131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="15c59-131">Az.Sql</span></span>
* <span data-ttu-id="15c59-132">Az AuditingEndpointsCommunicator frissítése.</span><span class="sxs-lookup"><span data-stu-id="15c59-132">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="15c59-133">Ki lett javítva az új diagnosztikai beállítások létrehozásakor jelentkező ritka eset viselkedése.</span><span class="sxs-lookup"><span data-stu-id="15c59-133">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="15c59-134">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="15c59-134">Az.Storage</span></span>
* <span data-ttu-id="15c59-135">A BlockBlobStorage altípus támogatása a Storage-fiók létrehozásakor      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="15c59-135">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="15c59-136">1.4.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="15c59-136">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="15c59-137">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="15c59-137">Az.AnalysisServices</span></span>
* <span data-ttu-id="15c59-138">Az AddAzureASAccount parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="15c59-138">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="15c59-139">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="15c59-139">Az.Automation</span></span>
* <span data-ttu-id="15c59-140">Az Import-AzAutomationDscNodeConfiguration súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="15c59-140">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="15c59-141">A konfigurációnév-ellenőrzés hozzáadva az Import-AzAutomationDscConfiguration parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="15c59-141">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="15c59-142">Továbbfejlesztett hibakezelés az Import-AzAutomationDscConfiguration parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="15c59-142">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="15c59-143">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="15c59-143">Az.CognitiveServices</span></span>
* <span data-ttu-id="15c59-144">A CustomSubdomainName új választható paraméterként hozzáadva a New-AzCognitiveServicesAccount parancsmaghoz, amellyel altartomány adható meg az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="15c59-144">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="15c59-145">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="15c59-145">Az.Compute</span></span>
* <span data-ttu-id="15c59-146">Kijavítva az azonosító paraméterkészleteivel kapcsolatos probléma</span><span class="sxs-lookup"><span data-stu-id="15c59-146">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="15c59-147">Frissült a Get-AzVMExtension parancsmag, hogy az összes telepített bővítményt listázza, ha a Name paraméter nincs megadva</span><span class="sxs-lookup"><span data-stu-id="15c59-147">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="15c59-148">A Tag és a ResourceId paraméterek hozzáadva az Update-AzImage parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="15c59-148">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="15c59-149">A Get-AzVmssVM példányazonosító nélkül, az InstanceView használatával példánynézetben listázni tudja a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="15c59-149">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="15c59-150">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="15c59-150">Az.DataLakeStore</span></span>
* <span data-ttu-id="15c59-151">Parancsmagok hozzáadása a törölt ADL-elemek enumerálásához és visszaállításához</span><span class="sxs-lookup"><span data-stu-id="15c59-151">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="15c59-152">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="15c59-152">Az.EventHub</span></span>
* <span data-ttu-id="15c59-153">Új SkipEmptyArchives logikai tulajdonság hozzáadva az üres archívumok kihagyásához az Eventhub CaptureDescription osztályában</span><span class="sxs-lookup"><span data-stu-id="15c59-153">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="15c59-154">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="15c59-154">Az.KeyVault</span></span>
* <span data-ttu-id="15c59-155">A Set-AzKeyVaultSecret címkézésének kijavítása</span><span class="sxs-lookup"><span data-stu-id="15c59-155">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="15c59-156">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="15c59-156">Az.LogicApp</span></span>
* <span data-ttu-id="15c59-157">Hozzáadva az integrációs fiókok alapszintű termékváltozatában</span><span class="sxs-lookup"><span data-stu-id="15c59-157">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="15c59-158">Hozzáadva az XSLT 2.0-ban, az XSLT 3.0-ban és a Liquid leképezéstípusok esetén</span><span class="sxs-lookup"><span data-stu-id="15c59-158">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="15c59-159">Új parancsmagok az integrációs fiók szerelvényeihez</span><span class="sxs-lookup"><span data-stu-id="15c59-159">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="15c59-160">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="15c59-160">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="15c59-161">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="15c59-161">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="15c59-162">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="15c59-162">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="15c59-163">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="15c59-163">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="15c59-164">Új parancsmagok az integrációs fiók kötegkonfigurációjához</span><span class="sxs-lookup"><span data-stu-id="15c59-164">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="15c59-165">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="15c59-165">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="15c59-166">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="15c59-166">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="15c59-167">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="15c59-167">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="15c59-168">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="15c59-168">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="15c59-169">A Logic Apps SDK frissítése a 4.1.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="15c59-169">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="15c59-170">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="15c59-170">Az.Monitor</span></span>
* <span data-ttu-id="15c59-171">A Get-AzMetric súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="15c59-171">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="15c59-172">Az.Network</span><span class="sxs-lookup"><span data-stu-id="15c59-172">Az.Network</span></span>
* <span data-ttu-id="15c59-173">Az Add-AzApplicationGatewayCustomError súgójában lévő példa frissítése</span><span class="sxs-lookup"><span data-stu-id="15c59-173">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="15c59-174">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="15c59-174">Az.OperationalInsights</span></span>
* <span data-ttu-id="15c59-175">Kibővített támogatás a New és a Get ApplicationInsights adatforráshoz.</span><span class="sxs-lookup"><span data-stu-id="15c59-175">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="15c59-176">Új „ApplicationInsights” altípus hozzáadva az adott munkaterület Get specific és Get all Application Insights-adatforrásainak támogatásához.</span><span class="sxs-lookup"><span data-stu-id="15c59-176">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="15c59-177">A New-AzOperationalInsightsApplicationInsightsDataSource parancsmag hozzáadva adatforrás létrehozásához a következő Application Insights-erőforrásparaméterekkel: subscriptionId, resourceGroupName és name.</span><span class="sxs-lookup"><span data-stu-id="15c59-177">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="15c59-178">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="15c59-178">Az.Resources</span></span>
* <span data-ttu-id="15c59-179">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="15c59-179">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="15c59-180">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="15c59-180">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="15c59-181">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="15c59-181">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="15c59-182">Ki lett javítva a KeyCredentials ismételt létrehozását megakadályozó hiba</span><span class="sxs-lookup"><span data-stu-id="15c59-182">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="15c59-183">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="15c59-183">Az.Sql</span></span>
* <span data-ttu-id="15c59-184">Rugalmas SQL DB-skálázási szint támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="15c59-184">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="15c59-185">Ki lett javítva az a hiba, hogy a visszaállítási kérésben szereplő szükségtelen tulajdonságok megadása miatt a visszaállítás esetenként meghiúsult</span><span class="sxs-lookup"><span data-stu-id="15c59-185">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="15c59-186">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="15c59-186">Az.Websites</span></span>
* <span data-ttu-id="15c59-187">A Get-AzWebAppSlotMetrics példájának javítása</span><span class="sxs-lookup"><span data-stu-id="15c59-187">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="15c59-188">1.3.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="15c59-188">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="15c59-189">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="15c59-189">Az.Accounts</span></span>
* <span data-ttu-id="15c59-190">Frissítés a ClientRuntime legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="15c59-190">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="15c59-191">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="15c59-191">Az.AnalysisServices</span></span>
<span data-ttu-id="15c59-192">Az Az.AnalysisServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="15c59-192">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="15c59-193">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="15c59-193">Az.Compute</span></span>
* <span data-ttu-id="15c59-194">AEM-bővítmény: Mostantól az UltraSSD, valamint a P60, P70 és P80 lemezek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="15c59-194">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="15c59-195">A Set-AzVMBootDiagnostics súgóleírása frissült.</span><span class="sxs-lookup"><span data-stu-id="15c59-195">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="15c59-196">Az Update-AzImage súgóleírása és példája frissült.</span><span class="sxs-lookup"><span data-stu-id="15c59-196">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="15c59-197">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="15c59-197">Az.RecoveryServices</span></span>
<span data-ttu-id="15c59-198">Az Az.RecoveryServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="15c59-198">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="15c59-199">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="15c59-199">Az.Resources</span></span>
* <span data-ttu-id="15c59-200">Az erőforráscsoportok címkézése ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="15c59-200">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="15c59-201">További információ: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="15c59-201">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="15c59-202">Ki lett javítva az a hiba, amikor a `Get-AzureRmRoleAssignment` nem vette figyelembe az -ErrorAction paramétert.</span><span class="sxs-lookup"><span data-stu-id="15c59-202">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="15c59-203">További információ: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="15c59-203">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="15c59-204">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="15c59-204">Az.Sql</span></span>
* <span data-ttu-id="15c59-205">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hozzáadva</span><span class="sxs-lookup"><span data-stu-id="15c59-205">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="15c59-206">Ki lett javítva az a hiba, amikor az Azure-fiókba való bejelentkezés hiánya nullref kivételt eredményezett az SQL-parancsmagok végrehajtásakor.</span><span class="sxs-lookup"><span data-stu-id="15c59-206">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="15c59-207">A nullref kivétel ki lett javítva a Get-AzSqlCapabilityben.</span><span class="sxs-lookup"><span data-stu-id="15c59-207">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="15c59-208">1.2.1 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="15c59-208">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="15c59-209">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="15c59-209">Az.Accounts</span></span>
* <span data-ttu-id="15c59-210">A hitelesítés megfelelő verziójával rendelkező kiadás</span><span class="sxs-lookup"><span data-stu-id="15c59-210">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="15c59-211">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="15c59-211">Az.AnalysisServices</span></span>
* <span data-ttu-id="15c59-212">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="15c59-212">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="15c59-213">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="15c59-213">Az.RecoveryServices</span></span>
* <span data-ttu-id="15c59-214">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="15c59-214">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="15c59-215">1.2.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="15c59-215">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="15c59-216">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="15c59-216">Az.Accounts</span></span>
* <span data-ttu-id="15c59-217">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="15c59-217">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="15c59-218">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="15c59-218">Update incorrect online help URLs</span></span>
* <span data-ttu-id="15c59-219">Az Uninstall-AzureRm figyelmeztető üzenete hozzáadva a PS Core-ban</span><span class="sxs-lookup"><span data-stu-id="15c59-219">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="15c59-220">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="15c59-220">Az.Aks</span></span>
* <span data-ttu-id="15c59-221">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="15c59-221">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="15c59-222">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="15c59-222">Az.Automation</span></span>
* <span data-ttu-id="15c59-223">Mostantól támogatottak a Python 2-runbookok.</span><span class="sxs-lookup"><span data-stu-id="15c59-223">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="15c59-224">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="15c59-224">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="15c59-225">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="15c59-225">Az.Cdn</span></span>
* <span data-ttu-id="15c59-226">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="15c59-226">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="15c59-227">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="15c59-227">Az.Compute</span></span>
* <span data-ttu-id="15c59-228">Az Invoke-AzVMReimage parancsmag hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="15c59-228">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="15c59-229">A TempDisk paraméter hozzá lett adva a Set-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="15c59-229">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="15c59-230">A New-AzVM figyelmeztető üzenete ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="15c59-230">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="15c59-231">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="15c59-231">Az.ContainerRegistry</span></span>
* <span data-ttu-id="15c59-232">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="15c59-232">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="15c59-233">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="15c59-233">Az.DataFactory</span></span>
* <span data-ttu-id="15c59-234">Az ADF .Net SDK verziója 3.0.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="15c59-234">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="15c59-235">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="15c59-235">Az.DataLakeStore</span></span>
* <span data-ttu-id="15c59-236">Ki lett javítva az ADLS-végponttal kapcsolatos probléma az MSI használatakor.</span><span class="sxs-lookup"><span data-stu-id="15c59-236">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="15c59-237">További információ: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="15c59-237">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="15c59-238">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="15c59-238">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="15c59-239">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="15c59-239">Az.IotHub</span></span>
* <span data-ttu-id="15c59-240">Az Encoding formátum hozzá lett adva az Add-IotHubRoutingEndpoint parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="15c59-240">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="15c59-241">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="15c59-241">Az.KeyVault</span></span>
* <span data-ttu-id="15c59-242">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="15c59-242">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="15c59-243">Az.Network</span><span class="sxs-lookup"><span data-stu-id="15c59-243">Az.Network</span></span>
* <span data-ttu-id="15c59-244">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="15c59-244">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="15c59-245">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="15c59-245">Az.Resources</span></span>
* <span data-ttu-id="15c59-246">A helytelen példák ki lettek javítva a New-AzADAppCredential és a New-AzADSpCredential referenciadokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="15c59-246">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="15c59-247">Ki lett javítva az a hiba, amikor a -TemplateFile paraméter nem lett feloldva az erőforráscsoportokat üzembe helyező parancsmagok végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="15c59-247">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="15c59-248">Az.Resources: A New-AzureRmPolicyDefinition -Mode alapértelmezett értékének dokumentációja ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="15c59-248">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="15c59-249">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="15c59-249">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="15c59-250">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="15c59-250">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="15c59-251">Ki lett javítva a „PSResourceGroupDeployment” objektum formázásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="15c59-251">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="15c59-252">További információ: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="15c59-252">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="15c59-253">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="15c59-253">Az.ServiceFabric</span></span>
* <span data-ttu-id="15c59-254">Visszaállítás a VMSS-modell tanúsítványának hozzáadásakor bekövetkező kivétel-visszaadás esetén; javított hiba: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="15c59-254">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="15c59-255">Bizonyos hibaüzenetek ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="15c59-255">Fix some error messages.</span></span>
* <span data-ttu-id="15c59-256">Ki lett javítva az alapértelmezett ARM-sablonnal való fürtlétrehozás a New-AzServiceFabriCluster esetében, amely nem működött az Az-ba történő migrálással.</span><span class="sxs-lookup"><span data-stu-id="15c59-256">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="15c59-257">Ki lett javítva a fürt-/alkalmazástanúsítvány létrehozása, így mostantól csak a fürtnek megfelelő virtuálisgép-méretezési csoportokhoz (Virtual Machine Scale Sets) lesznek hozzáadva, a fürtazonosító bővítményben való ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="15c59-257">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="15c59-258">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="15c59-258">Az.SignalR</span></span>
* <span data-ttu-id="15c59-259">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="15c59-259">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="15c59-260">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="15c59-260">Az.Sql</span></span>
* <span data-ttu-id="15c59-261">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="15c59-261">Update incorrect online help URLs</span></span>
* <span data-ttu-id="15c59-262">A LicenseType paraméter paraméterleírása frissítve lett a lehetséges értékekkel.</span><span class="sxs-lookup"><span data-stu-id="15c59-262">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="15c59-263">Ki lett javítva az a hiba, amikor egy felügyelt példány identitásának frissítése nem működött, ha az volt az egyetlen frissített tulajdonság.</span><span class="sxs-lookup"><span data-stu-id="15c59-263">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="15c59-264">Egyéni rendezések támogatása a felügyelt példányokon</span><span class="sxs-lookup"><span data-stu-id="15c59-264">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="15c59-265">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="15c59-265">Az.Storage</span></span>
* <span data-ttu-id="15c59-266">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="15c59-266">Update incorrect online help URLs</span></span>
* <span data-ttu-id="15c59-267">Részletes hibaüzenet megjelenítése klasszikus naplózás/metrika get/set műveletei esetében a prémium szintű Storage-fiókon, mivel a prémium szintű Storage-fiók nem támogatja a klasszikus naplózást/metrikát.</span><span class="sxs-lookup"><span data-stu-id="15c59-267">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="15c59-268">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="15c59-268">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="15c59-269">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="15c59-269">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="15c59-270">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="15c59-270">Az.TrafficManager</span></span>
* <span data-ttu-id="15c59-271">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="15c59-271">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="15c59-272">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="15c59-272">Az.Websites</span></span>
* <span data-ttu-id="15c59-273">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="15c59-273">Update incorrect online help URLs</span></span>
* <span data-ttu-id="15c59-274">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól a megfelelő erőforráscsoportba és helyre tölti fel a tanúsítványt, ha az alkalmazás ASE-n üzemel.</span><span class="sxs-lookup"><span data-stu-id="15c59-274">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="15c59-275">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól nem írja felül a címkéket SSL-tanúsítvány alkalmazáshoz való kötésekor.</span><span class="sxs-lookup"><span data-stu-id="15c59-275">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="15c59-276">1.1.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="15c59-276">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="15c59-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="15c59-277">Az.Accounts</span></span>
* <span data-ttu-id="15c59-278">A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz</span><span class="sxs-lookup"><span data-stu-id="15c59-278">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="15c59-279">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="15c59-279">Az.Compute</span></span>
* <span data-ttu-id="15c59-280">A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni</span><span class="sxs-lookup"><span data-stu-id="15c59-280">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="15c59-281">Frissült az azonosító leírása a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="15c59-281">Updated the description of ID in help files</span></span>
* <span data-ttu-id="15c59-282">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="15c59-282">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="15c59-283">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="15c59-283">Az.DataLakeStore</span></span>
* <span data-ttu-id="15c59-284">A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.</span><span class="sxs-lookup"><span data-stu-id="15c59-284">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="15c59-285">A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva</span><span class="sxs-lookup"><span data-stu-id="15c59-285">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="15c59-286">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="15c59-286">Az.EventGrid</span></span>
* <span data-ttu-id="15c59-287">Frissítve a 2019-01-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="15c59-287">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="15c59-288">A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához</span><span class="sxs-lookup"><span data-stu-id="15c59-288">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="15c59-289">New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="15c59-289">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="15c59-290">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="15c59-290">Event Time-To-Live,</span></span>
        - <span data-ttu-id="15c59-291">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="15c59-291">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="15c59-292">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="15c59-292">Dead letter endpoint.</span></span>
    - <span data-ttu-id="15c59-293">Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="15c59-293">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="15c59-294">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="15c59-294">Event Time-To-Live,</span></span>
        - <span data-ttu-id="15c59-295">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="15c59-295">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="15c59-296">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="15c59-296">Dead letter endpoint.</span></span>
* <span data-ttu-id="15c59-297">Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.</span><span class="sxs-lookup"><span data-stu-id="15c59-297">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="15c59-298">Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.</span><span class="sxs-lookup"><span data-stu-id="15c59-298">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="15c59-299">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="15c59-299">Az.IotHub</span></span>
* <span data-ttu-id="15c59-300">Frissítve az IoT Hub SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="15c59-300">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="15c59-301">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="15c59-301">Az.LogicApp</span></span>
* <span data-ttu-id="15c59-302">A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel</span><span class="sxs-lookup"><span data-stu-id="15c59-302">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="15c59-303">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="15c59-303">Az.Resources</span></span>
* <span data-ttu-id="15c59-304">Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="15c59-304">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="15c59-305">További információ: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="15c59-305">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="15c59-306">Ki lett javítva a -Custom paraméter kezelése a New/Set-AzPolicyDefinition parancsban</span><span class="sxs-lookup"><span data-stu-id="15c59-306">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="15c59-307">Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="15c59-307">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="15c59-308">A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében</span><span class="sxs-lookup"><span data-stu-id="15c59-308">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="15c59-309">További információ: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="15c59-309">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="15c59-310">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="15c59-310">Az.SignalR</span></span>
* <span data-ttu-id="15c59-311">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="15c59-311">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="15c59-312">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="15c59-312">Az.Sql</span></span>
* <span data-ttu-id="15c59-313">A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.</span><span class="sxs-lookup"><span data-stu-id="15c59-313">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="15c59-314">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="15c59-314">Az.Storage</span></span>
* <span data-ttu-id="15c59-315">A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva</span><span class="sxs-lookup"><span data-stu-id="15c59-315">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="15c59-316">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="15c59-316">New-AzStorageContext</span></span>
* <span data-ttu-id="15c59-317">A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz</span><span class="sxs-lookup"><span data-stu-id="15c59-317">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="15c59-318">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="15c59-318">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="15c59-319">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="15c59-319">Az.Websites</span></span>
* <span data-ttu-id="15c59-320">Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban</span><span class="sxs-lookup"><span data-stu-id="15c59-320">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="15c59-321">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="15c59-321">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="15c59-322">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="15c59-322">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="15c59-323">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="15c59-323">General</span></span>

- <span data-ttu-id="15c59-324">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="15c59-324">General Availability of Az Module</span></span>
- <span data-ttu-id="15c59-325">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="15c59-325">Online help for each module</span></span>
- <span data-ttu-id="15c59-326">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="15c59-326">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="15c59-327">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="15c59-327">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="15c59-328">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="15c59-328">Az.Accounts</span></span>
- <span data-ttu-id="15c59-329">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="15c59-329">Changed from Az.Profile</span></span>
- <span data-ttu-id="15c59-330">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="15c59-330">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="15c59-331">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="15c59-331">Az.ApiManagement</span></span>
- <span data-ttu-id="15c59-332">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="15c59-332">Fixes for #7002</span></span>
- <span data-ttu-id="15c59-333">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="15c59-333">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="15c59-334">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="15c59-334">Az.Batch</span></span>
- <span data-ttu-id="15c59-335">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="15c59-335">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="15c59-336">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="15c59-336">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="15c59-337">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="15c59-337">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="15c59-338">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="15c59-338">Az.Billing</span></span>
- <span data-ttu-id="15c59-339">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="15c59-339">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="15c59-340">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="15c59-340">Az.CognitivServices</span></span>
- <span data-ttu-id="15c59-341">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="15c59-341">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="15c59-342">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="15c59-342">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="15c59-343">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="15c59-343">Az.ContainerInstance</span></span>
- <span data-ttu-id="15c59-344">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="15c59-344">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="15c59-345">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="15c59-345">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="15c59-346">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="15c59-346">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="15c59-347">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="15c59-347">Az.DataLakeStore</span></span>
- <span data-ttu-id="15c59-348">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="15c59-348">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="15c59-349">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="15c59-349">Az.Monitor</span></span>
- <span data-ttu-id="15c59-350">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="15c59-350">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="15c59-351">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="15c59-351">Az.KeyVault</span></span>
- <span data-ttu-id="15c59-352">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="15c59-352">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="15c59-353">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="15c59-353">Az.MachineLearning</span></span>
- <span data-ttu-id="15c59-354">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="15c59-354">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="15c59-355">Az.Media</span><span class="sxs-lookup"><span data-stu-id="15c59-355">Az.Media</span></span>
- <span data-ttu-id="15c59-356">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="15c59-356">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="15c59-357">Az.Network</span><span class="sxs-lookup"><span data-stu-id="15c59-357">Az.Network</span></span>
<span data-ttu-id="15c59-358">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="15c59-358">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="15c59-359">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="15c59-359">New cmdlets added:</span></span>
        - <span data-ttu-id="15c59-360">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="15c59-360">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="15c59-361">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="15c59-361">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="15c59-362">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="15c59-362">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="15c59-363">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="15c59-363">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="15c59-364">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="15c59-364">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="15c59-365">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="15c59-365">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="15c59-366">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="15c59-366">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="15c59-367">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="15c59-367">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="15c59-368">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="15c59-368">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="15c59-369">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="15c59-369">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="15c59-370">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="15c59-370">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="15c59-371">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="15c59-371">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="15c59-372">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="15c59-372">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="15c59-373">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="15c59-373">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="15c59-374">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="15c59-374">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="15c59-375">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="15c59-375">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="15c59-376">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="15c59-376">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="15c59-377">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="15c59-377">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="15c59-378">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="15c59-378">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="15c59-379">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="15c59-379">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="15c59-380">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="15c59-380">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="15c59-381">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="15c59-381">Az.OperationalInsights</span></span>
- <span data-ttu-id="15c59-382">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="15c59-382">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="15c59-383">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="15c59-383">Az.Profile</span></span>
- <span data-ttu-id="15c59-384">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="15c59-384">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="15c59-385">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="15c59-385">Az.RecoveryServices</span></span>
- <span data-ttu-id="15c59-386">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="15c59-386">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="15c59-387">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="15c59-387">Az.Resources</span></span>
- <span data-ttu-id="15c59-388">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="15c59-388">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="15c59-389">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="15c59-389">Az.ServiceFabric</span></span>
- <span data-ttu-id="15c59-390">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="15c59-390">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="15c59-391">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="15c59-391">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="15c59-392">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="15c59-392">Az.SIgnalR</span></span>
- <span data-ttu-id="15c59-393">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="15c59-393">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="15c59-394">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="15c59-394">Az.Sql</span></span>
- <span data-ttu-id="15c59-395">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="15c59-395">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="15c59-396">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="15c59-396">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="15c59-397">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="15c59-397">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="15c59-398">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="15c59-398">Az.Storage</span></span>
- <span data-ttu-id="15c59-399">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="15c59-399">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="15c59-400">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="15c59-400">Az.Websites</span></span>
- <span data-ttu-id="15c59-401">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="15c59-401">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="15c59-402">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="15c59-402">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="15c59-403">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="15c59-403">General</span></span>

* <span data-ttu-id="15c59-404">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="15c59-404">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="15c59-405">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="15c59-405">Az.Compute</span></span>

* <span data-ttu-id="15c59-406">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="15c59-406">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="15c59-407">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="15c59-407">Az.DataLakeStore</span></span>

* <span data-ttu-id="15c59-408">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="15c59-408">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="15c59-409">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="15c59-409">Az.FrontDoor</span></span>

* <span data-ttu-id="15c59-410">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="15c59-410">Fixed some broken links</span></span>
    - <span data-ttu-id="15c59-411">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="15c59-411">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="15c59-412">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="15c59-412">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="15c59-413">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="15c59-413">Az.RecoveryServices</span></span>

* <span data-ttu-id="15c59-414">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="15c59-414">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="15c59-415">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="15c59-415">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="15c59-416">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="15c59-416">Az.Resources</span></span>

* <span data-ttu-id="15c59-417"> https://github.com/Azure/azure-powershell/issues/7679 javítása</span><span class="sxs-lookup"><span data-stu-id="15c59-417">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="15c59-418">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="15c59-418">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="15c59-419">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="15c59-419">Az.Sql</span></span>

* <span data-ttu-id="15c59-420">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="15c59-420">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="15c59-421">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="15c59-421">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="15c59-422">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="15c59-422">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="15c59-423">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="15c59-423">Az.Storage</span></span>

* <span data-ttu-id="15c59-424">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="15c59-424">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="15c59-425">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="15c59-425">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="15c59-426">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="15c59-426">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="15c59-427">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="15c59-427">Support Static Website configuration</span></span>
    - <span data-ttu-id="15c59-428">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="15c59-428">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="15c59-429">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="15c59-429">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="15c59-430">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="15c59-430">Az.Websites</span></span>

* <span data-ttu-id="15c59-431">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="15c59-431">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="15c59-432">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="15c59-432">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="15c59-433">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="15c59-433">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="15c59-434">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="15c59-434">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="15c59-435">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="15c59-435">Az.ApiManagement</span></span>
* <span data-ttu-id="15c59-436">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="15c59-436">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="15c59-437">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="15c59-437">Az.Automation</span></span>
* <span data-ttu-id="15c59-438">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="15c59-438">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="15c59-439">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="15c59-439">Added Update Management cmdlets</span></span>
* <span data-ttu-id="15c59-440">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="15c59-440">Added Source Control cmdlets</span></span>
* <span data-ttu-id="15c59-441">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="15c59-441">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="15c59-442">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="15c59-442">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="15c59-443">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="15c59-443">Az.Compute</span></span>
* <span data-ttu-id="15c59-444">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="15c59-444">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="15c59-445">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="15c59-445">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="15c59-446">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="15c59-446">Az.ContainerInstance</span></span>
* <span data-ttu-id="15c59-447">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="15c59-447">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="15c59-448">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="15c59-448">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="15c59-449">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="15c59-449">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="15c59-450">Az.Network</span><span class="sxs-lookup"><span data-stu-id="15c59-450">Az.Network</span></span>
* <span data-ttu-id="15c59-451">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="15c59-451">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="15c59-452">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="15c59-452">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="15c59-453">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="15c59-453">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="15c59-454">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="15c59-454">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="15c59-455">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="15c59-455">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="15c59-456">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="15c59-456">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="15c59-457">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="15c59-457">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="15c59-458">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="15c59-458">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="15c59-459">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="15c59-459">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="15c59-460">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="15c59-460">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="15c59-461">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="15c59-461">Az.Relay</span></span>
* <span data-ttu-id="15c59-462">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="15c59-462">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="15c59-463">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="15c59-463">Az.Resources</span></span>
* <span data-ttu-id="15c59-464">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="15c59-464">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="15c59-465">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="15c59-465">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="15c59-466">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="15c59-466">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="15c59-467">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="15c59-467">Az.ServiceFabric</span></span>
* <span data-ttu-id="15c59-468">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="15c59-468">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="15c59-469">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="15c59-469">Az.Sql</span></span>
* <span data-ttu-id="15c59-470">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="15c59-470">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="15c59-471">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="15c59-471">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="15c59-472">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="15c59-472">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="15c59-473">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="15c59-473">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="15c59-474">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="15c59-474">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="15c59-475">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="15c59-475">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="15c59-476">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="15c59-476">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="15c59-477">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="15c59-477">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="15c59-478">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="15c59-478">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="15c59-479">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="15c59-479">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="15c59-480">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="15c59-480">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="15c59-481">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="15c59-481">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="15c59-482">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="15c59-482">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="15c59-483">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="15c59-483">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="15c59-484">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="15c59-484">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="15c59-485">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="15c59-485">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="15c59-486">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="15c59-486">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="15c59-487">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="15c59-487">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="15c59-488">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="15c59-488">General</span></span>
* <span data-ttu-id="15c59-489">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="15c59-489">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="15c59-490">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="15c59-490">Az.Profile</span></span>
* <span data-ttu-id="15c59-491">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="15c59-491">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="15c59-492">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="15c59-492">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="15c59-493">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="15c59-493">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="15c59-494">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="15c59-494">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="15c59-495">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="15c59-495">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="15c59-496">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="15c59-496">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="15c59-497">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="15c59-497">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="15c59-498">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="15c59-498">Az.CognitiveServices</span></span>
* <span data-ttu-id="15c59-499">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="15c59-499">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="15c59-500">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="15c59-500">Az.Compute</span></span>
* <span data-ttu-id="15c59-501">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="15c59-501">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="15c59-502">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="15c59-502">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="15c59-503">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="15c59-503">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="15c59-504">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="15c59-504">Az.DataLakeStore</span></span>
* <span data-ttu-id="15c59-505">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="15c59-505">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="15c59-506">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="15c59-506">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="15c59-507">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="15c59-507">Az.Insights</span></span>
* <span data-ttu-id="15c59-508">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="15c59-508">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="15c59-509">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="15c59-509">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="15c59-510">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="15c59-510">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="15c59-511">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="15c59-511">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="15c59-512">Az.Network</span><span class="sxs-lookup"><span data-stu-id="15c59-512">Az.Network</span></span>
* <span data-ttu-id="15c59-513">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="15c59-513">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="15c59-514">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="15c59-514">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="15c59-515">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="15c59-515">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="15c59-516">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="15c59-516">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="15c59-517">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="15c59-517">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="15c59-518">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="15c59-518">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="15c59-519">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="15c59-519">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="15c59-520">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="15c59-520">Az.PolicyInsights</span></span>
* <span data-ttu-id="15c59-521">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="15c59-521">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="15c59-522">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="15c59-522">Az.Resources</span></span>
* <span data-ttu-id="15c59-523"> https://github.com/Azure/azure-powershell/issues/7402 javítása</span><span class="sxs-lookup"><span data-stu-id="15c59-523">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="15c59-524">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="15c59-524">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="15c59-525">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="15c59-525">Az.ServiceBus</span></span>
* <span data-ttu-id="15c59-526">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="15c59-526">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="15c59-527">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="15c59-527">Az.ServiceFabric</span></span>
* <span data-ttu-id="15c59-528">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="15c59-528">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="15c59-529">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="15c59-529">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="15c59-530">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="15c59-530">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="15c59-531">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="15c59-531">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="15c59-532">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="15c59-532">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="15c59-533">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="15c59-533">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="15c59-534">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="15c59-534">Az.Profile</span></span>
* <span data-ttu-id="15c59-535">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="15c59-535">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="15c59-536">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="15c59-536">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="15c59-537">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="15c59-537">Az.Compute</span></span>
* <span data-ttu-id="15c59-538">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="15c59-538">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="15c59-539">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="15c59-539">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="15c59-540">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="15c59-540">Az.DataLakeStore</span></span>
* <span data-ttu-id="15c59-541">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="15c59-541">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="15c59-542">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="15c59-542">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="15c59-543">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="15c59-543">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="15c59-544">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="15c59-544">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="15c59-545">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="15c59-545">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="15c59-546">Az.Network</span><span class="sxs-lookup"><span data-stu-id="15c59-546">Az.Network</span></span>
* <span data-ttu-id="15c59-547">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="15c59-547">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="15c59-548">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="15c59-548">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="15c59-549">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="15c59-549">Az.Resources</span></span>
* <span data-ttu-id="15c59-550">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="15c59-550">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="15c59-551">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="15c59-551">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="15c59-552">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="15c59-552">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="15c59-553">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="15c59-553">Azure.Storage</span></span>
* <span data-ttu-id="15c59-554">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="15c59-554">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="15c59-555">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="15c59-555">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="15c59-556">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="15c59-556">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="15c59-557">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="15c59-557">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="15c59-558">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="15c59-558">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="15c59-559">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="15c59-559">Az.CognitiveServices</span></span>
* <span data-ttu-id="15c59-560">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="15c59-560">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="15c59-561">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="15c59-561">Az.Compute</span></span>
* <span data-ttu-id="15c59-562">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="15c59-562">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="15c59-563">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="15c59-563">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="15c59-564">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="15c59-564">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="15c59-565">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="15c59-565">Az.DataFactoryV2</span></span>
* <span data-ttu-id="15c59-566">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="15c59-566">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="15c59-567">Az.Network</span><span class="sxs-lookup"><span data-stu-id="15c59-567">Az.Network</span></span>
* <span data-ttu-id="15c59-568">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="15c59-568">Added NetworkProfile functionality.</span></span> <span data-ttu-id="15c59-569">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="15c59-569">new cmdlets added</span></span>
    - <span data-ttu-id="15c59-570">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="15c59-570">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="15c59-571">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="15c59-571">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="15c59-572">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="15c59-572">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="15c59-573">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="15c59-573">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="15c59-574">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="15c59-574">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="15c59-575">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="15c59-575">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="15c59-576">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="15c59-576">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="15c59-577">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="15c59-577">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="15c59-578">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="15c59-578">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="15c59-579">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="15c59-579">Az.RedisCache</span></span>
* <span data-ttu-id="15c59-580">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="15c59-580">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="15c59-581">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="15c59-581">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="15c59-582">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="15c59-582">Az.Resources</span></span>
* <span data-ttu-id="15c59-583">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="15c59-583">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="15c59-584">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="15c59-584">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="15c59-585">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="15c59-585">Az.Sql</span></span>
* <span data-ttu-id="15c59-586">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="15c59-586">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="15c59-587">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="15c59-587">Az.Websites</span></span>
* <span data-ttu-id="15c59-588">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="15c59-588">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="15c59-589">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="15c59-589">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="15c59-590">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="15c59-590">0.2.0 - September 2018</span></span>
 <span data-ttu-id="15c59-591">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="15c59-591">Initial Release</span></span>