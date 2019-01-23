---
ms.openlocfilehash: 179d22fa065944695e4769f2698e3cabc7666b04
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/16/2019
ms.locfileid: "54342019"
---
## <a name="110---january-2019"></a><span data-ttu-id="6bd2b-101">1.1.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="6bd2b-101">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6bd2b-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6bd2b-102">Az.Accounts</span></span>
* <span data-ttu-id="6bd2b-103">A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz</span><span class="sxs-lookup"><span data-stu-id="6bd2b-103">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6bd2b-104">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6bd2b-104">Az.Compute</span></span>
* <span data-ttu-id="6bd2b-105">A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni</span><span class="sxs-lookup"><span data-stu-id="6bd2b-105">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="6bd2b-106">Frissült az azonosító leírása a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="6bd2b-106">Updated the description of ID in help files</span></span>
* <span data-ttu-id="6bd2b-107">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="6bd2b-107">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6bd2b-108">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6bd2b-108">Az.DataLakeStore</span></span>
* <span data-ttu-id="6bd2b-109">A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-109">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="6bd2b-110">A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva</span><span class="sxs-lookup"><span data-stu-id="6bd2b-110">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6bd2b-111">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6bd2b-111">Az.EventGrid</span></span>
* <span data-ttu-id="6bd2b-112">Frissítve a 2019-01-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-112">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="6bd2b-113">A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához</span><span class="sxs-lookup"><span data-stu-id="6bd2b-113">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="6bd2b-114">New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="6bd2b-114">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="6bd2b-115">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="6bd2b-115">Event Time-To-Live,</span></span>
        - <span data-ttu-id="6bd2b-116">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="6bd2b-116">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="6bd2b-117">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-117">Dead letter endpoint.</span></span>
    - <span data-ttu-id="6bd2b-118">Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="6bd2b-118">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="6bd2b-119">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="6bd2b-119">Event Time-To-Live,</span></span>
        - <span data-ttu-id="6bd2b-120">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="6bd2b-120">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="6bd2b-121">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-121">Dead letter endpoint.</span></span>
* <span data-ttu-id="6bd2b-122">Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-122">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="6bd2b-123">Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-123">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6bd2b-124">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6bd2b-124">Az.IotHub</span></span>
* <span data-ttu-id="6bd2b-125">Frissítve az IoT Hub SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="6bd2b-125">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6bd2b-126">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6bd2b-126">Az.LogicApp</span></span>
* <span data-ttu-id="6bd2b-127">A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel</span><span class="sxs-lookup"><span data-stu-id="6bd2b-127">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="6bd2b-128">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6bd2b-128">Az.Resources</span></span>
* <span data-ttu-id="6bd2b-129">Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="6bd2b-129">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="6bd2b-130">További információ: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="6bd2b-130">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="6bd2b-131">Ki lett javítva a -Custom paraméter kezelés a New/Set-AzPolicyDefinition parancsban</span><span class="sxs-lookup"><span data-stu-id="6bd2b-131">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="6bd2b-132">Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="6bd2b-132">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="6bd2b-133">A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében</span><span class="sxs-lookup"><span data-stu-id="6bd2b-133">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="6bd2b-134">További információ: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="6bd2b-134">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6bd2b-135">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6bd2b-135">Az.SignalR</span></span>
* <span data-ttu-id="6bd2b-136">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="6bd2b-136">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="6bd2b-137">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6bd2b-137">Az.Sql</span></span>
* <span data-ttu-id="6bd2b-138">A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-138">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6bd2b-139">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6bd2b-139">Az.Storage</span></span>
* <span data-ttu-id="6bd2b-140">A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva</span><span class="sxs-lookup"><span data-stu-id="6bd2b-140">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="6bd2b-141">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6bd2b-141">New-AzStorageContext</span></span>
* <span data-ttu-id="6bd2b-142">A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz</span><span class="sxs-lookup"><span data-stu-id="6bd2b-142">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="6bd2b-143">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="6bd2b-143">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6bd2b-144">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6bd2b-144">Az.Websites</span></span>
* <span data-ttu-id="6bd2b-145">Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban</span><span class="sxs-lookup"><span data-stu-id="6bd2b-145">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="6bd2b-146">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="6bd2b-146">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="6bd2b-147">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="6bd2b-147">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="6bd2b-148">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="6bd2b-148">General</span></span>

- <span data-ttu-id="6bd2b-149">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="6bd2b-149">General Availability of Az Module</span></span>
- <span data-ttu-id="6bd2b-150">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="6bd2b-150">Online help for each module</span></span>
- <span data-ttu-id="6bd2b-151">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="6bd2b-151">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="6bd2b-152">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="6bd2b-152">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="6bd2b-153">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6bd2b-153">Az.Accounts</span></span>
- <span data-ttu-id="6bd2b-154">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="6bd2b-154">Changed from Az.Profile</span></span>
- <span data-ttu-id="6bd2b-155">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="6bd2b-155">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="6bd2b-156">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6bd2b-156">Az.ApiManagement</span></span>
- <span data-ttu-id="6bd2b-157">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="6bd2b-157">Fixes for #7002</span></span>
- <span data-ttu-id="6bd2b-158">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="6bd2b-158">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="6bd2b-159">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6bd2b-159">Az.Batch</span></span>
- <span data-ttu-id="6bd2b-160">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-160">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="6bd2b-161">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-161">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="6bd2b-162">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="6bd2b-162">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="6bd2b-163">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="6bd2b-163">Az.Billing</span></span>
- <span data-ttu-id="6bd2b-164">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-164">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="6bd2b-165">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="6bd2b-165">Az.CognitivServices</span></span>
- <span data-ttu-id="6bd2b-166">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-166">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="6bd2b-167">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-167">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="6bd2b-168">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6bd2b-168">Az.ContainerInstance</span></span>
- <span data-ttu-id="6bd2b-169">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="6bd2b-169">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="6bd2b-170">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="6bd2b-170">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="6bd2b-171">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="6bd2b-171">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="6bd2b-172">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6bd2b-172">Az.DataLakeStore</span></span>
- <span data-ttu-id="6bd2b-173">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="6bd2b-173">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="6bd2b-174">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6bd2b-174">Az.Monitor</span></span>
- <span data-ttu-id="6bd2b-175">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="6bd2b-175">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="6bd2b-176">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6bd2b-176">Az.KeyVault</span></span>
- <span data-ttu-id="6bd2b-177">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-177">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="6bd2b-178">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6bd2b-178">Az.MachineLearning</span></span>
- <span data-ttu-id="6bd2b-179">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="6bd2b-179">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="6bd2b-180">Az.Media</span><span class="sxs-lookup"><span data-stu-id="6bd2b-180">Az.Media</span></span>
- <span data-ttu-id="6bd2b-181">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="6bd2b-181">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="6bd2b-182">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6bd2b-182">Az.Network</span></span>
<span data-ttu-id="6bd2b-183">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-183">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="6bd2b-184">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="6bd2b-184">New cmdlets added:</span></span>
        - <span data-ttu-id="6bd2b-185">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6bd2b-185">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6bd2b-186">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6bd2b-186">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6bd2b-187">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6bd2b-187">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6bd2b-188">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6bd2b-188">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6bd2b-189">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6bd2b-189">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6bd2b-190">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="6bd2b-190">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="6bd2b-191">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="6bd2b-191">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="6bd2b-192">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="6bd2b-192">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="6bd2b-193">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="6bd2b-193">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="6bd2b-194">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6bd2b-194">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="6bd2b-195">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6bd2b-195">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="6bd2b-196">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6bd2b-196">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="6bd2b-197">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6bd2b-197">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="6bd2b-198">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6bd2b-198">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="6bd2b-199">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-199">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="6bd2b-200">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="6bd2b-200">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="6bd2b-201">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6bd2b-201">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="6bd2b-202">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6bd2b-202">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="6bd2b-203">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6bd2b-203">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="6bd2b-204">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="6bd2b-204">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="6bd2b-205">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="6bd2b-205">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="6bd2b-206">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6bd2b-206">Az.OperationalInsights</span></span>
- <span data-ttu-id="6bd2b-207">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="6bd2b-207">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="6bd2b-208">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6bd2b-208">Az.Profile</span></span>
- <span data-ttu-id="6bd2b-209">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6bd2b-209">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="6bd2b-210">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6bd2b-210">Az.RecoveryServices</span></span>
- <span data-ttu-id="6bd2b-211">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="6bd2b-211">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="6bd2b-212">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6bd2b-212">Az.Resources</span></span>
- <span data-ttu-id="6bd2b-213">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="6bd2b-213">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="6bd2b-214">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6bd2b-214">Az.ServiceFabric</span></span>
- <span data-ttu-id="6bd2b-215">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="6bd2b-215">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="6bd2b-216">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="6bd2b-216">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="6bd2b-217">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="6bd2b-217">Az.SIgnalR</span></span>
- <span data-ttu-id="6bd2b-218">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="6bd2b-218">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="6bd2b-219">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6bd2b-219">Az.Sql</span></span>
- <span data-ttu-id="6bd2b-220">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="6bd2b-220">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="6bd2b-221">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="6bd2b-221">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="6bd2b-222">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="6bd2b-222">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="6bd2b-223">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6bd2b-223">Az.Storage</span></span>
- <span data-ttu-id="6bd2b-224">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="6bd2b-224">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="6bd2b-225">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6bd2b-225">Az.Websites</span></span>
- <span data-ttu-id="6bd2b-226">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="6bd2b-226">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="6bd2b-227">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="6bd2b-227">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="6bd2b-228">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="6bd2b-228">General</span></span>

* <span data-ttu-id="6bd2b-229">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="6bd2b-229">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="6bd2b-230">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6bd2b-230">Az.Compute</span></span>

* <span data-ttu-id="6bd2b-231">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-231">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="6bd2b-232">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6bd2b-232">Az.DataLakeStore</span></span>

* <span data-ttu-id="6bd2b-233">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="6bd2b-233">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="6bd2b-234">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6bd2b-234">Az.FrontDoor</span></span>

* <span data-ttu-id="6bd2b-235">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="6bd2b-235">Fixed some broken links</span></span>
    - <span data-ttu-id="6bd2b-236">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-236">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="6bd2b-237">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-237">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="6bd2b-238">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6bd2b-238">Az.RecoveryServices</span></span>

* <span data-ttu-id="6bd2b-239">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-239">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="6bd2b-240">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-240">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="6bd2b-241">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6bd2b-241">Az.Resources</span></span>

* <span data-ttu-id="6bd2b-242"> https://github.com/Azure/azure-powershell/issues/7679 javítása</span><span class="sxs-lookup"><span data-stu-id="6bd2b-242">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="6bd2b-243">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-243">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="6bd2b-244">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6bd2b-244">Az.Sql</span></span>

* <span data-ttu-id="6bd2b-245">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="6bd2b-245">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="6bd2b-246">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="6bd2b-246">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="6bd2b-247">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-247">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="6bd2b-248">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6bd2b-248">Az.Storage</span></span>

* <span data-ttu-id="6bd2b-249">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="6bd2b-249">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="6bd2b-250">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-250">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="6bd2b-251">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="6bd2b-251">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="6bd2b-252">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="6bd2b-252">Support Static Website configuration</span></span>
    - <span data-ttu-id="6bd2b-253">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6bd2b-253">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="6bd2b-254">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6bd2b-254">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="6bd2b-255">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6bd2b-255">Az.Websites</span></span>

* <span data-ttu-id="6bd2b-256">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6bd2b-256">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="6bd2b-257">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-257">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="6bd2b-258">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-258">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="6bd2b-259">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="6bd2b-259">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="6bd2b-260">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6bd2b-260">Az.ApiManagement</span></span>
* <span data-ttu-id="6bd2b-261">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-261">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="6bd2b-262">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6bd2b-262">Az.Automation</span></span>
* <span data-ttu-id="6bd2b-263">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-263">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="6bd2b-264">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-264">Added Update Management cmdlets</span></span>
* <span data-ttu-id="6bd2b-265">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-265">Added Source Control cmdlets</span></span>
* <span data-ttu-id="6bd2b-266">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-266">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="6bd2b-267">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-267">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="6bd2b-268">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6bd2b-268">Az.Compute</span></span>
* <span data-ttu-id="6bd2b-269">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-269">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="6bd2b-270">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-270">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="6bd2b-271">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6bd2b-271">Az.ContainerInstance</span></span>
* <span data-ttu-id="6bd2b-272">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-272">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="6bd2b-273">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="6bd2b-273">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="6bd2b-274">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-274">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="6bd2b-275">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6bd2b-275">Az.Network</span></span>
* <span data-ttu-id="6bd2b-276">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-276">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="6bd2b-277">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-277">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="6bd2b-278">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-278">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="6bd2b-279">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-279">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="6bd2b-280">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6bd2b-280">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6bd2b-281">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-281">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="6bd2b-282">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-282">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="6bd2b-283">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="6bd2b-283">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="6bd2b-284">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-284">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="6bd2b-285">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-285">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="6bd2b-286">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="6bd2b-286">Az.Relay</span></span>
* <span data-ttu-id="6bd2b-287">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-287">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="6bd2b-288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6bd2b-288">Az.Resources</span></span>
* <span data-ttu-id="6bd2b-289">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-289">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="6bd2b-290">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-290">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="6bd2b-291">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-291">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="6bd2b-292">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6bd2b-292">Az.ServiceFabric</span></span>
* <span data-ttu-id="6bd2b-293">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-293">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="6bd2b-294">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6bd2b-294">Az.Sql</span></span>
* <span data-ttu-id="6bd2b-295">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-295">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="6bd2b-296">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6bd2b-296">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6bd2b-297">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6bd2b-297">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6bd2b-298">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6bd2b-298">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6bd2b-299">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6bd2b-299">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6bd2b-300">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6bd2b-300">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6bd2b-301">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6bd2b-301">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6bd2b-302">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6bd2b-302">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6bd2b-303">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6bd2b-303">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="6bd2b-304">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-304">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="6bd2b-305">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-305">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="6bd2b-306">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-306">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="6bd2b-307">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-307">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="6bd2b-308">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-308">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="6bd2b-309">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-309">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="6bd2b-310">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-310">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="6bd2b-311">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-311">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="6bd2b-312">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="6bd2b-312">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6bd2b-313">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="6bd2b-313">General</span></span>
* <span data-ttu-id="6bd2b-314">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-314">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="6bd2b-315">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6bd2b-315">Az.Profile</span></span>
* <span data-ttu-id="6bd2b-316">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-316">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="6bd2b-317">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="6bd2b-317">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="6bd2b-318">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="6bd2b-318">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="6bd2b-319">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="6bd2b-319">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="6bd2b-320">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="6bd2b-320">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="6bd2b-321">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="6bd2b-321">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="6bd2b-322">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="6bd2b-322">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="6bd2b-323">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6bd2b-323">Az.CognitiveServices</span></span>
* <span data-ttu-id="6bd2b-324">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-324">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6bd2b-325">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6bd2b-325">Az.Compute</span></span>
* <span data-ttu-id="6bd2b-326">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="6bd2b-326">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="6bd2b-327">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="6bd2b-327">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="6bd2b-328">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-328">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6bd2b-329">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6bd2b-329">Az.DataLakeStore</span></span>
* <span data-ttu-id="6bd2b-330">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-330">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="6bd2b-331">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-331">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="6bd2b-332">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="6bd2b-332">Az.Insights</span></span>
* <span data-ttu-id="6bd2b-333">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="6bd2b-333">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="6bd2b-334">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="6bd2b-334">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="6bd2b-335">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="6bd2b-335">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="6bd2b-336">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="6bd2b-336">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6bd2b-337">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6bd2b-337">Az.Network</span></span>
* <span data-ttu-id="6bd2b-338">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="6bd2b-338">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="6bd2b-339">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="6bd2b-339">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="6bd2b-340">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="6bd2b-340">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="6bd2b-341">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6bd2b-341">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="6bd2b-342">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="6bd2b-342">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="6bd2b-343">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="6bd2b-343">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="6bd2b-344">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6bd2b-344">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6bd2b-345">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6bd2b-345">Az.PolicyInsights</span></span>
* <span data-ttu-id="6bd2b-346">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="6bd2b-346">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="6bd2b-347">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6bd2b-347">Az.Resources</span></span>
* <span data-ttu-id="6bd2b-348"> https://github.com/Azure/azure-powershell/issues/7402 javítása</span><span class="sxs-lookup"><span data-stu-id="6bd2b-348">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="6bd2b-349">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="6bd2b-349">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6bd2b-350">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6bd2b-350">Az.ServiceBus</span></span>
* <span data-ttu-id="6bd2b-351">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-351">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6bd2b-352">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6bd2b-352">Az.ServiceFabric</span></span>
* <span data-ttu-id="6bd2b-353">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-353">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="6bd2b-354">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="6bd2b-354">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="6bd2b-355">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="6bd2b-355">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="6bd2b-356">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="6bd2b-356">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="6bd2b-357">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-357">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="6bd2b-358">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="6bd2b-358">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="6bd2b-359">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6bd2b-359">Az.Profile</span></span>
* <span data-ttu-id="6bd2b-360">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-360">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="6bd2b-361">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-361">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6bd2b-362">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6bd2b-362">Az.Compute</span></span>
* <span data-ttu-id="6bd2b-363">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-363">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="6bd2b-364">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-364">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6bd2b-365">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6bd2b-365">Az.DataLakeStore</span></span>
* <span data-ttu-id="6bd2b-366">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="6bd2b-366">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="6bd2b-367">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-367">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="6bd2b-368">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-368">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="6bd2b-369">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-369">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="6bd2b-370">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-370">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6bd2b-371">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6bd2b-371">Az.Network</span></span>
* <span data-ttu-id="6bd2b-372">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-372">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="6bd2b-373">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-373">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6bd2b-374">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6bd2b-374">Az.Resources</span></span>
* <span data-ttu-id="6bd2b-375">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="6bd2b-375">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="6bd2b-376">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-376">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="6bd2b-377">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="6bd2b-377">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="6bd2b-378">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6bd2b-378">Azure.Storage</span></span>
* <span data-ttu-id="6bd2b-379">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="6bd2b-379">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="6bd2b-380">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6bd2b-380">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="6bd2b-381">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="6bd2b-381">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="6bd2b-382">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-382">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="6bd2b-383">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="6bd2b-383">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="6bd2b-384">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6bd2b-384">Az.CognitiveServices</span></span>
* <span data-ttu-id="6bd2b-385">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-385">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6bd2b-386">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6bd2b-386">Az.Compute</span></span>
* <span data-ttu-id="6bd2b-387">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-387">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="6bd2b-388">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-388">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="6bd2b-389">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="6bd2b-389">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="6bd2b-390">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6bd2b-390">Az.DataFactoryV2</span></span>
* <span data-ttu-id="6bd2b-391">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-391">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6bd2b-392">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6bd2b-392">Az.Network</span></span>
* <span data-ttu-id="6bd2b-393">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-393">Added NetworkProfile functionality.</span></span> <span data-ttu-id="6bd2b-394">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="6bd2b-394">new cmdlets added</span></span>
    - <span data-ttu-id="6bd2b-395">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6bd2b-395">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="6bd2b-396">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6bd2b-396">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="6bd2b-397">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6bd2b-397">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="6bd2b-398">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6bd2b-398">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="6bd2b-399">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="6bd2b-399">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="6bd2b-400">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="6bd2b-400">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="6bd2b-401">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="6bd2b-401">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="6bd2b-402">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="6bd2b-402">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="6bd2b-403">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="6bd2b-403">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6bd2b-404">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6bd2b-404">Az.RedisCache</span></span>
* <span data-ttu-id="6bd2b-405">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-405">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="6bd2b-406">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="6bd2b-406">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="6bd2b-407">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6bd2b-407">Az.Resources</span></span>
* <span data-ttu-id="6bd2b-408">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="6bd2b-408">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="6bd2b-409">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="6bd2b-409">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="6bd2b-410">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6bd2b-410">Az.Sql</span></span>
* <span data-ttu-id="6bd2b-411">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="6bd2b-411">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6bd2b-412">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6bd2b-412">Az.Websites</span></span>
* <span data-ttu-id="6bd2b-413">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="6bd2b-413">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="6bd2b-414">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="6bd2b-414">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="6bd2b-415">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="6bd2b-415">0.2.0 - September 2018</span></span>
 <span data-ttu-id="6bd2b-416">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="6bd2b-416">Initial Release</span></span>