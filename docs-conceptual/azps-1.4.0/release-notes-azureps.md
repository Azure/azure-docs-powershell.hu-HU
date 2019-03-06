## <a name="140---february-2019"></a><span data-ttu-id="c2fb9-101">1.4.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="c2fb9-101">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="c2fb9-102">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c2fb9-102">Az.AnalysisServices</span></span>
* <span data-ttu-id="c2fb9-103">Az AddAzureASAccount parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="c2fb9-103">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c2fb9-104">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c2fb9-104">Az.Automation</span></span>
* <span data-ttu-id="c2fb9-105">Az Import-AzAutomationDscNodeConfiguration súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="c2fb9-105">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="c2fb9-106">A konfigurációnév-ellenőrzés hozzáadva az Import-AzAutomationDscConfiguration parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="c2fb9-106">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="c2fb9-107">Továbbfejlesztett hibakezelés az Import-AzAutomationDscConfiguration parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="c2fb9-107">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c2fb9-108">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c2fb9-108">Az.CognitiveServices</span></span>
* <span data-ttu-id="c2fb9-109">A CustomSubdomainName új választható paraméterként hozzáadva a New-AzCognitiveServicesAccount parancsmaghoz, amellyel altartomány adható meg az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-109">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c2fb9-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c2fb9-110">Az.Compute</span></span>
* <span data-ttu-id="c2fb9-111">Kijavítva az azonosító paraméterkészleteivel kapcsolatos probléma</span><span class="sxs-lookup"><span data-stu-id="c2fb9-111">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="c2fb9-112">Frissült a Get-AzVMExtension parancsmag, hogy az összes telepített bővítményt listázza, ha a Name paraméter nincs megadva</span><span class="sxs-lookup"><span data-stu-id="c2fb9-112">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="c2fb9-113">A Tag és a ResourceId paraméterek hozzáadva az Update-AzImage parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="c2fb9-113">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="c2fb9-114">A Get-AzVmssVM példányazonosító nélkül, az InstanceView használatával példánynézetben listázni tudja a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-114">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c2fb9-115">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c2fb9-115">Az.DataLakeStore</span></span>
* <span data-ttu-id="c2fb9-116">Parancsmagok hozzáadása a törölt ADL-elemek enumerálásához és visszaállításához</span><span class="sxs-lookup"><span data-stu-id="c2fb9-116">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c2fb9-117">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c2fb9-117">Az.EventHub</span></span>
* <span data-ttu-id="c2fb9-118">Új SkipEmptyArchives logikai tulajdonság hozzáadva az üres archívumok kihagyásához az Eventhub CaptureDescription osztályában</span><span class="sxs-lookup"><span data-stu-id="c2fb9-118">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="c2fb9-119">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c2fb9-119">Az.KeyVault</span></span>
* <span data-ttu-id="c2fb9-120">A Set-AzKeyVaultSecret címkézésének kijavítása</span><span class="sxs-lookup"><span data-stu-id="c2fb9-120">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="c2fb9-121">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c2fb9-121">Az.LogicApp</span></span>
* <span data-ttu-id="c2fb9-122">Hozzáadva az integrációs fiókok alapszintű termékváltozatában</span><span class="sxs-lookup"><span data-stu-id="c2fb9-122">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="c2fb9-123">Hozzáadva az XSLT 2.0-ban, az XSLT 3.0-ban és a Liquid leképezéstípusok esetén</span><span class="sxs-lookup"><span data-stu-id="c2fb9-123">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="c2fb9-124">Új parancsmagok az integrációs fiók szerelvényeihez</span><span class="sxs-lookup"><span data-stu-id="c2fb9-124">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="c2fb9-125">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c2fb9-125">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="c2fb9-126">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c2fb9-126">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="c2fb9-127">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c2fb9-127">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="c2fb9-128">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c2fb9-128">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="c2fb9-129">Új parancsmagok az integrációs fiók kötegkonfigurációjához</span><span class="sxs-lookup"><span data-stu-id="c2fb9-129">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="c2fb9-130">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2fb9-130">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="c2fb9-131">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2fb9-131">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="c2fb9-132">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2fb9-132">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="c2fb9-133">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2fb9-133">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="c2fb9-134">A Logic Apps SDK frissítése a 4.1.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="c2fb9-134">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c2fb9-135">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c2fb9-135">Az.Monitor</span></span>
* <span data-ttu-id="c2fb9-136">A Get-AzMetric súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="c2fb9-136">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c2fb9-137">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c2fb9-137">Az.Network</span></span>
* <span data-ttu-id="c2fb9-138">Az Add-AzApplicationGatewayCustomError súgójában lévő példa frissítése</span><span class="sxs-lookup"><span data-stu-id="c2fb9-138">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c2fb9-139">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c2fb9-139">Az.OperationalInsights</span></span>
* <span data-ttu-id="c2fb9-140">Kibővített támogatás a New és a Get ApplicationInsights adatforráshoz.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-140">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="c2fb9-141">Új „ApplicationInsights” altípus hozzáadva az adott munkaterület Get specific és Get all Application Insights-adatforrásainak támogatásához.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-141">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="c2fb9-142">A New-AzOperationalInsightsApplicationInsightsDataSource parancsmag hozzáadva adatforrás létrehozásához a következő Application Insights-erőforrásparaméterekkel: subscriptionId, resourceGroupName és name.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-142">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="c2fb9-143">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c2fb9-143">Az.Resources</span></span>
* <span data-ttu-id="c2fb9-144">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="c2fb9-144">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="c2fb9-145">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="c2fb9-145">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="c2fb9-146">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="c2fb9-146">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="c2fb9-147">Ki lett javítva a KeyCredentials ismételt létrehozását megakadályozó hiba</span><span class="sxs-lookup"><span data-stu-id="c2fb9-147">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="c2fb9-148">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c2fb9-148">Az.Sql</span></span>
* <span data-ttu-id="c2fb9-149">Rugalmas SQL DB-skálázási szint támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="c2fb9-149">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="c2fb9-150">Ki lett javítva az a hiba, hogy a visszaállítási kérésben szereplő szükségtelen tulajdonságok megadása miatt a visszaállítás esetenként meghiúsult</span><span class="sxs-lookup"><span data-stu-id="c2fb9-150">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c2fb9-151">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c2fb9-151">Az.Websites</span></span>
* <span data-ttu-id="c2fb9-152">A Get-AzWebAppSlotMetrics példájának javítása</span><span class="sxs-lookup"><span data-stu-id="c2fb9-152">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="c2fb9-153">1.3.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="c2fb9-153">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c2fb9-154">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c2fb9-154">Az.Accounts</span></span>
* <span data-ttu-id="c2fb9-155">Frissítés a ClientRuntime legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="c2fb9-155">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="c2fb9-156">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c2fb9-156">Az.AnalysisServices</span></span>
<span data-ttu-id="c2fb9-157">Az Az.AnalysisServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-157">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c2fb9-158">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c2fb9-158">Az.Compute</span></span>
* <span data-ttu-id="c2fb9-159">AEM-bővítmény: Mostantól az UltraSSD, valamint a P60, P70 és P80 lemezek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-159">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="c2fb9-160">A Set-AzVMBootDiagnostics súgóleírása frissült.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-160">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="c2fb9-161">Az Update-AzImage súgóleírása és példája frissült.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-161">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c2fb9-162">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c2fb9-162">Az.RecoveryServices</span></span>
<span data-ttu-id="c2fb9-163">Az Az.RecoveryServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-163">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c2fb9-164">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c2fb9-164">Az.Resources</span></span>
* <span data-ttu-id="c2fb9-165">Az erőforráscsoportok címkézése ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-165">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="c2fb9-166">További információ: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="c2fb9-166">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="c2fb9-167">Ki lett javítva az a hiba, amikor a `Get-AzureRmRoleAssignment` nem vette figyelembe az -ErrorAction paramétert.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-167">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="c2fb9-168">További információ: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="c2fb9-168">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="c2fb9-169">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c2fb9-169">Az.Sql</span></span>
* <span data-ttu-id="c2fb9-170">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hozzáadva</span><span class="sxs-lookup"><span data-stu-id="c2fb9-170">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="c2fb9-171">Ki lett javítva az a hiba, amikor az Azure-fiókba való bejelentkezés hiánya nullref kivételt eredményezett az SQL-parancsmagok végrehajtásakor.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-171">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="c2fb9-172">A nullref kivétel ki lett javítva a Get-AzSqlCapabilityben.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-172">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="c2fb9-173">1.2.1 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="c2fb9-173">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c2fb9-174">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c2fb9-174">Az.Accounts</span></span>
* <span data-ttu-id="c2fb9-175">A hitelesítés megfelelő verziójával rendelkező kiadás</span><span class="sxs-lookup"><span data-stu-id="c2fb9-175">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="c2fb9-176">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c2fb9-176">Az.AnalysisServices</span></span>
* <span data-ttu-id="c2fb9-177">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="c2fb9-177">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c2fb9-178">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c2fb9-178">Az.RecoveryServices</span></span>
* <span data-ttu-id="c2fb9-179">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="c2fb9-179">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="c2fb9-180">1.2.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="c2fb9-180">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c2fb9-181">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c2fb9-181">Az.Accounts</span></span>
* <span data-ttu-id="c2fb9-182">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="c2fb9-182">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="c2fb9-183">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-183">Update incorrect online help URLs</span></span>
* <span data-ttu-id="c2fb9-184">Az Uninstall-AzureRm figyelmeztető üzenete hozzáadva a PS Core-ban</span><span class="sxs-lookup"><span data-stu-id="c2fb9-184">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="c2fb9-185">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="c2fb9-185">Az.Aks</span></span>
* <span data-ttu-id="c2fb9-186">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-186">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c2fb9-187">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c2fb9-187">Az.Automation</span></span>
* <span data-ttu-id="c2fb9-188">Mostantól támogatottak a Python 2-runbookok.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-188">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="c2fb9-189">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-189">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="c2fb9-190">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c2fb9-190">Az.Cdn</span></span>
* <span data-ttu-id="c2fb9-191">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-191">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c2fb9-192">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c2fb9-192">Az.Compute</span></span>
* <span data-ttu-id="c2fb9-193">Az Invoke-AzVMReimage parancsmag hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-193">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="c2fb9-194">A TempDisk paraméter hozzá lett adva a Set-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-194">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="c2fb9-195">A New-AzVM figyelmeztető üzenete ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-195">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="c2fb9-196">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c2fb9-196">Az.ContainerRegistry</span></span>
* <span data-ttu-id="c2fb9-197">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-197">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c2fb9-198">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c2fb9-198">Az.DataFactory</span></span>
* <span data-ttu-id="c2fb9-199">Az ADF .Net SDK verziója 3.0.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-199">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c2fb9-200">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c2fb9-200">Az.DataLakeStore</span></span>
* <span data-ttu-id="c2fb9-201">Ki lett javítva az ADLS-végponttal kapcsolatos probléma az MSI használatakor.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-201">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="c2fb9-202">További információ: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="c2fb9-202">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="c2fb9-203">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-203">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c2fb9-204">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c2fb9-204">Az.IotHub</span></span>
* <span data-ttu-id="c2fb9-205">Az Encoding formátum hozzá lett adva az Add-IotHubRoutingEndpoint parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-205">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c2fb9-206">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c2fb9-206">Az.KeyVault</span></span>
* <span data-ttu-id="c2fb9-207">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-207">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c2fb9-208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c2fb9-208">Az.Network</span></span>
* <span data-ttu-id="c2fb9-209">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-209">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="c2fb9-210">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c2fb9-210">Az.Resources</span></span>
* <span data-ttu-id="c2fb9-211">A helytelen példák ki lettek javítva a New-AzADAppCredential és a New-AzADSpCredential referenciadokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-211">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="c2fb9-212">Ki lett javítva az a hiba, amikor a -TemplateFile paraméter nem lett feloldva az erőforráscsoportokat üzembe helyező parancsmagok végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-212">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="c2fb9-213">Az.Resources: A New-AzureRmPolicyDefinition -Mode alapértelmezett értékének dokumentációja ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-213">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="c2fb9-214">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="c2fb9-214">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="c2fb9-215">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="c2fb9-215">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="c2fb9-216">Ki lett javítva a „PSResourceGroupDeployment” objektum formázásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-216">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="c2fb9-217">További információ: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="c2fb9-217">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c2fb9-218">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c2fb9-218">Az.ServiceFabric</span></span>
* <span data-ttu-id="c2fb9-219">Visszaállítás a VMSS-modell tanúsítványának hozzáadásakor bekövetkező kivétel-visszaadás esetén; javított hiba: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-219">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="c2fb9-220">Bizonyos hibaüzenetek ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-220">Fix some error messages.</span></span>
* <span data-ttu-id="c2fb9-221">Ki lett javítva az alapértelmezett ARM-sablonnal való fürtlétrehozás a New-AzServiceFabriCluster esetében, amely nem működött az Az-ba történő migrálással.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-221">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="c2fb9-222">Ki lett javítva a fürt-/alkalmazástanúsítvány létrehozása, így mostantól csak a fürtnek megfelelő virtuálisgép-méretezési csoportokhoz (Virtual Machine Scale Sets) lesznek hozzáadva, a fürtazonosító bővítményben való ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-222">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="c2fb9-223">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="c2fb9-223">Az.SignalR</span></span>
* <span data-ttu-id="c2fb9-224">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-224">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="c2fb9-225">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c2fb9-225">Az.Sql</span></span>
* <span data-ttu-id="c2fb9-226">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-226">Update incorrect online help URLs</span></span>
* <span data-ttu-id="c2fb9-227">A LicenseType paraméter paraméterleírása frissítve lett a lehetséges értékekkel.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-227">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="c2fb9-228">Ki lett javítva az a hiba, amikor egy felügyelt példány identitásának frissítése nem működött, ha az volt az egyetlen frissített tulajdonság.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-228">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="c2fb9-229">Egyéni rendezések támogatása a felügyelt példányokon</span><span class="sxs-lookup"><span data-stu-id="c2fb9-229">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c2fb9-230">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c2fb9-230">Az.Storage</span></span>
* <span data-ttu-id="c2fb9-231">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-231">Update incorrect online help URLs</span></span>
* <span data-ttu-id="c2fb9-232">Részletes hibaüzenet megjelenítése klasszikus naplózás/metrika get/set műveletei esetében a prémium szintű Storage-fiókon, mivel a prémium szintű Storage-fiók nem támogatja a klasszikus naplózást/metrikát.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-232">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="c2fb9-233">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="c2fb9-233">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="c2fb9-234">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="c2fb9-234">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="c2fb9-235">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c2fb9-235">Az.TrafficManager</span></span>
* <span data-ttu-id="c2fb9-236">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-236">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c2fb9-237">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c2fb9-237">Az.Websites</span></span>
* <span data-ttu-id="c2fb9-238">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-238">Update incorrect online help URLs</span></span>
* <span data-ttu-id="c2fb9-239">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól a megfelelő erőforráscsoportba és helyre tölti fel a tanúsítványt, ha az alkalmazás ASE-n üzemel.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-239">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="c2fb9-240">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól nem írja felül a címkéket SSL-tanúsítvány alkalmazáshoz való kötésekor.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-240">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="c2fb9-241">1.1.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="c2fb9-241">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c2fb9-242">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c2fb9-242">Az.Accounts</span></span>
* <span data-ttu-id="c2fb9-243">A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz</span><span class="sxs-lookup"><span data-stu-id="c2fb9-243">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c2fb9-244">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c2fb9-244">Az.Compute</span></span>
* <span data-ttu-id="c2fb9-245">A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni</span><span class="sxs-lookup"><span data-stu-id="c2fb9-245">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="c2fb9-246">Frissült az azonosító leírása a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="c2fb9-246">Updated the description of ID in help files</span></span>
* <span data-ttu-id="c2fb9-247">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="c2fb9-247">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c2fb9-248">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c2fb9-248">Az.DataLakeStore</span></span>
* <span data-ttu-id="c2fb9-249">A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-249">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="c2fb9-250">A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva</span><span class="sxs-lookup"><span data-stu-id="c2fb9-250">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="c2fb9-251">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c2fb9-251">Az.EventGrid</span></span>
* <span data-ttu-id="c2fb9-252">Frissítve a 2019-01-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-252">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="c2fb9-253">A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához</span><span class="sxs-lookup"><span data-stu-id="c2fb9-253">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="c2fb9-254">New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="c2fb9-254">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="c2fb9-255">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="c2fb9-255">Event Time-To-Live,</span></span>
        - <span data-ttu-id="c2fb9-256">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="c2fb9-256">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="c2fb9-257">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-257">Dead letter endpoint.</span></span>
    - <span data-ttu-id="c2fb9-258">Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="c2fb9-258">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="c2fb9-259">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="c2fb9-259">Event Time-To-Live,</span></span>
        - <span data-ttu-id="c2fb9-260">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="c2fb9-260">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="c2fb9-261">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-261">Dead letter endpoint.</span></span>
* <span data-ttu-id="c2fb9-262">Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-262">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="c2fb9-263">Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-263">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c2fb9-264">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c2fb9-264">Az.IotHub</span></span>
* <span data-ttu-id="c2fb9-265">Frissítve az IoT Hub SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="c2fb9-265">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="c2fb9-266">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c2fb9-266">Az.LogicApp</span></span>
* <span data-ttu-id="c2fb9-267">A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel</span><span class="sxs-lookup"><span data-stu-id="c2fb9-267">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="c2fb9-268">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c2fb9-268">Az.Resources</span></span>
* <span data-ttu-id="c2fb9-269">Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="c2fb9-269">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="c2fb9-270">További információ: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="c2fb9-270">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="c2fb9-271">Ki lett javítva a -Custom paraméter kezelés a New/Set-AzPolicyDefinition parancsban</span><span class="sxs-lookup"><span data-stu-id="c2fb9-271">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="c2fb9-272">Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="c2fb9-272">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="c2fb9-273">A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében</span><span class="sxs-lookup"><span data-stu-id="c2fb9-273">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="c2fb9-274">További információ: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="c2fb9-274">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="c2fb9-275">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="c2fb9-275">Az.SignalR</span></span>
* <span data-ttu-id="c2fb9-276">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="c2fb9-276">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="c2fb9-277">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c2fb9-277">Az.Sql</span></span>
* <span data-ttu-id="c2fb9-278">A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-278">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c2fb9-279">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c2fb9-279">Az.Storage</span></span>
* <span data-ttu-id="c2fb9-280">A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva</span><span class="sxs-lookup"><span data-stu-id="c2fb9-280">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="c2fb9-281">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="c2fb9-281">New-AzStorageContext</span></span>
* <span data-ttu-id="c2fb9-282">A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz</span><span class="sxs-lookup"><span data-stu-id="c2fb9-282">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="c2fb9-283">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="c2fb9-283">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c2fb9-284">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c2fb9-284">Az.Websites</span></span>
* <span data-ttu-id="c2fb9-285">Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban</span><span class="sxs-lookup"><span data-stu-id="c2fb9-285">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="c2fb9-286">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="c2fb9-286">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="c2fb9-287">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="c2fb9-287">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="c2fb9-288">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="c2fb9-288">General</span></span>

- <span data-ttu-id="c2fb9-289">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="c2fb9-289">General Availability of Az Module</span></span>
- <span data-ttu-id="c2fb9-290">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="c2fb9-290">Online help for each module</span></span>
- <span data-ttu-id="c2fb9-291">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="c2fb9-291">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="c2fb9-292">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="c2fb9-292">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="c2fb9-293">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c2fb9-293">Az.Accounts</span></span>
- <span data-ttu-id="c2fb9-294">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="c2fb9-294">Changed from Az.Profile</span></span>
- <span data-ttu-id="c2fb9-295">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="c2fb9-295">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="c2fb9-296">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c2fb9-296">Az.ApiManagement</span></span>
- <span data-ttu-id="c2fb9-297">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="c2fb9-297">Fixes for #7002</span></span>
- <span data-ttu-id="c2fb9-298">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="c2fb9-298">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="c2fb9-299">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="c2fb9-299">Az.Batch</span></span>
- <span data-ttu-id="c2fb9-300">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-300">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="c2fb9-301">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-301">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="c2fb9-302">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="c2fb9-302">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="c2fb9-303">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="c2fb9-303">Az.Billing</span></span>
- <span data-ttu-id="c2fb9-304">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-304">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="c2fb9-305">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="c2fb9-305">Az.CognitivServices</span></span>
- <span data-ttu-id="c2fb9-306">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-306">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="c2fb9-307">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-307">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="c2fb9-308">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c2fb9-308">Az.ContainerInstance</span></span>
- <span data-ttu-id="c2fb9-309">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="c2fb9-309">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="c2fb9-310">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="c2fb9-310">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="c2fb9-311">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="c2fb9-311">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="c2fb9-312">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c2fb9-312">Az.DataLakeStore</span></span>
- <span data-ttu-id="c2fb9-313">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="c2fb9-313">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="c2fb9-314">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c2fb9-314">Az.Monitor</span></span>
- <span data-ttu-id="c2fb9-315">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="c2fb9-315">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="c2fb9-316">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c2fb9-316">Az.KeyVault</span></span>
- <span data-ttu-id="c2fb9-317">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-317">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="c2fb9-318">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="c2fb9-318">Az.MachineLearning</span></span>
- <span data-ttu-id="c2fb9-319">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="c2fb9-319">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="c2fb9-320">Az.Media</span><span class="sxs-lookup"><span data-stu-id="c2fb9-320">Az.Media</span></span>
- <span data-ttu-id="c2fb9-321">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="c2fb9-321">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="c2fb9-322">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c2fb9-322">Az.Network</span></span>
<span data-ttu-id="c2fb9-323">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-323">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="c2fb9-324">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="c2fb9-324">New cmdlets added:</span></span>
        - <span data-ttu-id="c2fb9-325">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c2fb9-325">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c2fb9-326">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c2fb9-326">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c2fb9-327">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c2fb9-327">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c2fb9-328">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c2fb9-328">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c2fb9-329">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c2fb9-329">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c2fb9-330">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="c2fb9-330">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="c2fb9-331">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="c2fb9-331">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="c2fb9-332">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2fb9-332">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="c2fb9-333">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="c2fb9-333">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="c2fb9-334">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c2fb9-334">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="c2fb9-335">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c2fb9-335">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="c2fb9-336">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c2fb9-336">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="c2fb9-337">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c2fb9-337">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="c2fb9-338">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c2fb9-338">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="c2fb9-339">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-339">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="c2fb9-340">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="c2fb9-340">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="c2fb9-341">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c2fb9-341">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="c2fb9-342">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c2fb9-342">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="c2fb9-343">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c2fb9-343">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="c2fb9-344">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="c2fb9-344">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="c2fb9-345">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="c2fb9-345">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="c2fb9-346">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c2fb9-346">Az.OperationalInsights</span></span>
- <span data-ttu-id="c2fb9-347">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="c2fb9-347">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="c2fb9-348">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c2fb9-348">Az.Profile</span></span>
- <span data-ttu-id="c2fb9-349">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c2fb9-349">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="c2fb9-350">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c2fb9-350">Az.RecoveryServices</span></span>
- <span data-ttu-id="c2fb9-351">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="c2fb9-351">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="c2fb9-352">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c2fb9-352">Az.Resources</span></span>
- <span data-ttu-id="c2fb9-353">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="c2fb9-353">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="c2fb9-354">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c2fb9-354">Az.ServiceFabric</span></span>
- <span data-ttu-id="c2fb9-355">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="c2fb9-355">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="c2fb9-356">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="c2fb9-356">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="c2fb9-357">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="c2fb9-357">Az.SIgnalR</span></span>
- <span data-ttu-id="c2fb9-358">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="c2fb9-358">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="c2fb9-359">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c2fb9-359">Az.Sql</span></span>
- <span data-ttu-id="c2fb9-360">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="c2fb9-360">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="c2fb9-361">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="c2fb9-361">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="c2fb9-362">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="c2fb9-362">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="c2fb9-363">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c2fb9-363">Az.Storage</span></span>
- <span data-ttu-id="c2fb9-364">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="c2fb9-364">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="c2fb9-365">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c2fb9-365">Az.Websites</span></span>
- <span data-ttu-id="c2fb9-366">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="c2fb9-366">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="c2fb9-367">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="c2fb9-367">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="c2fb9-368">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="c2fb9-368">General</span></span>

* <span data-ttu-id="c2fb9-369">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="c2fb9-369">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="c2fb9-370">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c2fb9-370">Az.Compute</span></span>

* <span data-ttu-id="c2fb9-371">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-371">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="c2fb9-372">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c2fb9-372">Az.DataLakeStore</span></span>

* <span data-ttu-id="c2fb9-373">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="c2fb9-373">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="c2fb9-374">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c2fb9-374">Az.FrontDoor</span></span>

* <span data-ttu-id="c2fb9-375">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="c2fb9-375">Fixed some broken links</span></span>
    - <span data-ttu-id="c2fb9-376">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-376">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="c2fb9-377">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-377">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="c2fb9-378">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c2fb9-378">Az.RecoveryServices</span></span>

* <span data-ttu-id="c2fb9-379">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-379">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="c2fb9-380">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-380">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="c2fb9-381">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c2fb9-381">Az.Resources</span></span>

* <span data-ttu-id="c2fb9-382"> https://github.com/Azure/azure-powershell/issues/7679 javítása</span><span class="sxs-lookup"><span data-stu-id="c2fb9-382">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="c2fb9-383">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-383">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="c2fb9-384">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c2fb9-384">Az.Sql</span></span>

* <span data-ttu-id="c2fb9-385">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="c2fb9-385">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="c2fb9-386">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="c2fb9-386">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="c2fb9-387">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-387">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="c2fb9-388">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c2fb9-388">Az.Storage</span></span>

* <span data-ttu-id="c2fb9-389">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="c2fb9-389">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="c2fb9-390">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-390">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="c2fb9-391">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c2fb9-391">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="c2fb9-392">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="c2fb9-392">Support Static Website configuration</span></span>
    - <span data-ttu-id="c2fb9-393">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="c2fb9-393">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="c2fb9-394">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="c2fb9-394">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="c2fb9-395">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c2fb9-395">Az.Websites</span></span>

* <span data-ttu-id="c2fb9-396">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c2fb9-396">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="c2fb9-397">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-397">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="c2fb9-398">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-398">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="c2fb9-399">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="c2fb9-399">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="c2fb9-400">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c2fb9-400">Az.ApiManagement</span></span>
* <span data-ttu-id="c2fb9-401">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-401">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="c2fb9-402">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c2fb9-402">Az.Automation</span></span>
* <span data-ttu-id="c2fb9-403">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-403">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="c2fb9-404">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-404">Added Update Management cmdlets</span></span>
* <span data-ttu-id="c2fb9-405">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-405">Added Source Control cmdlets</span></span>
* <span data-ttu-id="c2fb9-406">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-406">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="c2fb9-407">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-407">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="c2fb9-408">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c2fb9-408">Az.Compute</span></span>
* <span data-ttu-id="c2fb9-409">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-409">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="c2fb9-410">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-410">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="c2fb9-411">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c2fb9-411">Az.ContainerInstance</span></span>
* <span data-ttu-id="c2fb9-412">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-412">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="c2fb9-413">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="c2fb9-413">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="c2fb9-414">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-414">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="c2fb9-415">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c2fb9-415">Az.Network</span></span>
* <span data-ttu-id="c2fb9-416">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-416">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="c2fb9-417">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-417">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="c2fb9-418">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-418">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="c2fb9-419">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-419">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="c2fb9-420">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c2fb9-420">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c2fb9-421">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-421">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="c2fb9-422">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-422">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="c2fb9-423">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="c2fb9-423">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="c2fb9-424">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-424">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="c2fb9-425">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-425">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="c2fb9-426">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="c2fb9-426">Az.Relay</span></span>
* <span data-ttu-id="c2fb9-427">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-427">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="c2fb9-428">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c2fb9-428">Az.Resources</span></span>
* <span data-ttu-id="c2fb9-429">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-429">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="c2fb9-430">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-430">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="c2fb9-431">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-431">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="c2fb9-432">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c2fb9-432">Az.ServiceFabric</span></span>
* <span data-ttu-id="c2fb9-433">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-433">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="c2fb9-434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c2fb9-434">Az.Sql</span></span>
* <span data-ttu-id="c2fb9-435">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-435">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="c2fb9-436">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c2fb9-436">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c2fb9-437">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c2fb9-437">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c2fb9-438">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c2fb9-438">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c2fb9-439">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c2fb9-439">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c2fb9-440">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c2fb9-440">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="c2fb9-441">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c2fb9-441">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="c2fb9-442">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c2fb9-442">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="c2fb9-443">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c2fb9-443">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="c2fb9-444">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-444">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="c2fb9-445">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-445">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="c2fb9-446">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-446">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="c2fb9-447">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-447">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="c2fb9-448">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-448">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="c2fb9-449">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-449">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="c2fb9-450">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-450">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="c2fb9-451">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-451">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="c2fb9-452">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="c2fb9-452">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c2fb9-453">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="c2fb9-453">General</span></span>
* <span data-ttu-id="c2fb9-454">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-454">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="c2fb9-455">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c2fb9-455">Az.Profile</span></span>
* <span data-ttu-id="c2fb9-456">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-456">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="c2fb9-457">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="c2fb9-457">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="c2fb9-458">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="c2fb9-458">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="c2fb9-459">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="c2fb9-459">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="c2fb9-460">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="c2fb9-460">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="c2fb9-461">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="c2fb9-461">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="c2fb9-462">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="c2fb9-462">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="c2fb9-463">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c2fb9-463">Az.CognitiveServices</span></span>
* <span data-ttu-id="c2fb9-464">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-464">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c2fb9-465">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c2fb9-465">Az.Compute</span></span>
* <span data-ttu-id="c2fb9-466">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="c2fb9-466">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="c2fb9-467">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="c2fb9-467">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="c2fb9-468">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-468">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c2fb9-469">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c2fb9-469">Az.DataLakeStore</span></span>
* <span data-ttu-id="c2fb9-470">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-470">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="c2fb9-471">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-471">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="c2fb9-472">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="c2fb9-472">Az.Insights</span></span>
* <span data-ttu-id="c2fb9-473">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="c2fb9-473">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="c2fb9-474">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="c2fb9-474">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="c2fb9-475">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="c2fb9-475">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="c2fb9-476">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="c2fb9-476">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c2fb9-477">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c2fb9-477">Az.Network</span></span>
* <span data-ttu-id="c2fb9-478">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="c2fb9-478">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="c2fb9-479">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="c2fb9-479">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="c2fb9-480">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="c2fb9-480">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="c2fb9-481">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c2fb9-481">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="c2fb9-482">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="c2fb9-482">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="c2fb9-483">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="c2fb9-483">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="c2fb9-484">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c2fb9-484">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="c2fb9-485">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c2fb9-485">Az.PolicyInsights</span></span>
* <span data-ttu-id="c2fb9-486">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="c2fb9-486">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="c2fb9-487">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c2fb9-487">Az.Resources</span></span>
* <span data-ttu-id="c2fb9-488"> https://github.com/Azure/azure-powershell/issues/7402 javítása</span><span class="sxs-lookup"><span data-stu-id="c2fb9-488">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="c2fb9-489">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="c2fb9-489">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="c2fb9-490">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c2fb9-490">Az.ServiceBus</span></span>
* <span data-ttu-id="c2fb9-491">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-491">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c2fb9-492">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c2fb9-492">Az.ServiceFabric</span></span>
* <span data-ttu-id="c2fb9-493">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-493">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="c2fb9-494">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="c2fb9-494">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="c2fb9-495">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="c2fb9-495">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="c2fb9-496">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="c2fb9-496">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="c2fb9-497">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-497">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="c2fb9-498">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="c2fb9-498">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="c2fb9-499">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c2fb9-499">Az.Profile</span></span>
* <span data-ttu-id="c2fb9-500">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-500">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="c2fb9-501">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-501">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c2fb9-502">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c2fb9-502">Az.Compute</span></span>
* <span data-ttu-id="c2fb9-503">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-503">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="c2fb9-504">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-504">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c2fb9-505">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c2fb9-505">Az.DataLakeStore</span></span>
* <span data-ttu-id="c2fb9-506">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="c2fb9-506">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="c2fb9-507">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-507">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="c2fb9-508">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-508">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="c2fb9-509">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-509">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="c2fb9-510">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-510">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c2fb9-511">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c2fb9-511">Az.Network</span></span>
* <span data-ttu-id="c2fb9-512">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-512">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="c2fb9-513">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-513">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c2fb9-514">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c2fb9-514">Az.Resources</span></span>
* <span data-ttu-id="c2fb9-515">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="c2fb9-515">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="c2fb9-516">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-516">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="c2fb9-517">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="c2fb9-517">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="c2fb9-518">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c2fb9-518">Azure.Storage</span></span>
* <span data-ttu-id="c2fb9-519">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="c2fb9-519">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="c2fb9-520">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="c2fb9-520">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="c2fb9-521">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c2fb9-521">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="c2fb9-522">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-522">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="c2fb9-523">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="c2fb9-523">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="c2fb9-524">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c2fb9-524">Az.CognitiveServices</span></span>
* <span data-ttu-id="c2fb9-525">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-525">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c2fb9-526">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c2fb9-526">Az.Compute</span></span>
* <span data-ttu-id="c2fb9-527">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-527">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="c2fb9-528">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-528">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="c2fb9-529">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="c2fb9-529">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="c2fb9-530">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c2fb9-530">Az.DataFactoryV2</span></span>
* <span data-ttu-id="c2fb9-531">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-531">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c2fb9-532">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c2fb9-532">Az.Network</span></span>
* <span data-ttu-id="c2fb9-533">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-533">Added NetworkProfile functionality.</span></span> <span data-ttu-id="c2fb9-534">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="c2fb9-534">new cmdlets added</span></span>
    - <span data-ttu-id="c2fb9-535">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c2fb9-535">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="c2fb9-536">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c2fb9-536">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="c2fb9-537">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c2fb9-537">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="c2fb9-538">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c2fb9-538">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="c2fb9-539">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="c2fb9-539">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="c2fb9-540">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="c2fb9-540">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="c2fb9-541">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="c2fb9-541">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="c2fb9-542">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="c2fb9-542">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="c2fb9-543">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="c2fb9-543">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="c2fb9-544">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c2fb9-544">Az.RedisCache</span></span>
* <span data-ttu-id="c2fb9-545">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="c2fb9-545">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="c2fb9-546">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="c2fb9-546">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="c2fb9-547">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c2fb9-547">Az.Resources</span></span>
* <span data-ttu-id="c2fb9-548">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="c2fb9-548">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="c2fb9-549">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="c2fb9-549">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="c2fb9-550">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c2fb9-550">Az.Sql</span></span>
* <span data-ttu-id="c2fb9-551">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="c2fb9-551">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c2fb9-552">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c2fb9-552">Az.Websites</span></span>
* <span data-ttu-id="c2fb9-553">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="c2fb9-553">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="c2fb9-554">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="c2fb9-554">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="c2fb9-555">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="c2fb9-555">0.2.0 - September 2018</span></span>
 <span data-ttu-id="c2fb9-556">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="c2fb9-556">Initial Release</span></span>