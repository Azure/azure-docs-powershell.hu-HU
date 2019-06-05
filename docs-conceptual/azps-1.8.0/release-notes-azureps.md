---
ms.openlocfilehash: 10d8d50131b3c55ae19c5142c42cb47f37c68c92
ms.sourcegitcommit: 6171bab74aec6785938cad54d584f425ddbb850e
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/21/2019
ms.locfileid: "65971903"
---
## <a name="180---april-2019"></a><span data-ttu-id="d7ceb-101">1.8.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="d7ceb-101">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d7ceb-102">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="d7ceb-102">Highlights since the last major release</span></span>
* <span data-ttu-id="d7ceb-103">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="d7ceb-103">General availability of `Az` module</span></span>
* <span data-ttu-id="d7ceb-104">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="d7ceb-104">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d7ceb-105">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="d7ceb-105">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d7ceb-106">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="d7ceb-106">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d7ceb-107">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="d7ceb-107">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d7ceb-108">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="d7ceb-108">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d7ceb-109">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="d7ceb-109">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d7ceb-110">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d7ceb-110">Az.Accounts</span></span>
* <span data-ttu-id="d7ceb-111">Eltávolítás-AzureRm megfelelően törölni a Mac modulok frissítése</span><span class="sxs-lookup"><span data-stu-id="d7ceb-111">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d7ceb-112">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d7ceb-112">Az.Batch</span></span>
* <span data-ttu-id="d7ceb-113">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-113">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d7ceb-114">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d7ceb-114">Az.Cdn</span></span>
* <span data-ttu-id="d7ceb-115">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-115">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d7ceb-116">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d7ceb-116">Az.CognitiveServices</span></span>
* <span data-ttu-id="d7ceb-117">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-117">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d7ceb-118">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d7ceb-118">Az.Compute</span></span>
* <span data-ttu-id="d7ceb-119">Az AEM telepítési kapcsolatos problémák megoldásához, ha a lemezek erőforrás-azonosítók kisbetűs resourcegroups volt az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="d7ceb-119">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="d7ceb-120">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-120">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d7ceb-121">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d7ceb-121">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d7ceb-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d7ceb-122">Az.DataFactory</span></span>
* <span data-ttu-id="d7ceb-123">Adjon hozzá SsisProperties, ha a NodeCount felügyelt integrációs modul nem null értékű.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-123">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d7ceb-124">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d7ceb-124">Az.DataLakeStore</span></span>
* <span data-ttu-id="d7ceb-125">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-125">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d7ceb-126">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d7ceb-126">Az.EventGrid</span></span>
* <span data-ttu-id="d7ceb-127">A Súgó szöveg jelzi, hogy erőforrásokat kell létrehozni a create/update eseményt előfizetés parancsmagok használata előtt végpont frissítése.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-127">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d7ceb-128">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d7ceb-128">Az.EventHub</span></span>
* <span data-ttu-id="d7ceb-129">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="d7ceb-129">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="d7ceb-130">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d7ceb-130">Az.HDInsight</span></span>
* <span data-ttu-id="d7ceb-131">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-131">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d7ceb-132">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d7ceb-132">Az.IotHub</span></span>
* <span data-ttu-id="d7ceb-133">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-133">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d7ceb-134">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d7ceb-134">Az.KeyVault</span></span>
* <span data-ttu-id="d7ceb-135">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d7ceb-136">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d7ceb-136">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="d7ceb-137">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="d7ceb-137">Az.MachineLearning</span></span>
* <span data-ttu-id="d7ceb-138">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-138">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="d7ceb-139">Az.Media</span><span class="sxs-lookup"><span data-stu-id="d7ceb-139">Az.Media</span></span>
* <span data-ttu-id="d7ceb-140">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d7ceb-141">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d7ceb-141">Az.Monitor</span></span>
  * <span data-ttu-id="d7ceb-142">Riasztási szabály (nem klasszikus) GenV2 mérőszám-alapú új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d7ceb-142">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="d7ceb-143">Új AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="d7ceb-143">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="d7ceb-144">Új AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="d7ceb-144">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="d7ceb-145">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d7ceb-145">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="d7ceb-146">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d7ceb-146">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="d7ceb-147">Adjon hozzá AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d7ceb-147">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="d7ceb-148">Frissített verzió 0.22.0-preview figyelő SDK</span><span class="sxs-lookup"><span data-stu-id="d7ceb-148">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d7ceb-149">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d7ceb-149">Az.Network</span></span>
* <span data-ttu-id="d7ceb-150">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-150">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d7ceb-151">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d7ceb-151">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="d7ceb-152">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="d7ceb-152">Az.NotificationHubs</span></span>
* <span data-ttu-id="d7ceb-153">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-153">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d7ceb-154">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d7ceb-154">Az.OperationalInsights</span></span>
* <span data-ttu-id="d7ceb-155">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-155">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="d7ceb-156">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="d7ceb-156">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="d7ceb-157">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-157">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d7ceb-158">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d7ceb-158">Az.RecoveryServices</span></span>
* <span data-ttu-id="d7ceb-159">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d7ceb-160">Frissített táblázatos formában az SQL azure-beli virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="d7ceb-160">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="d7ceb-161">A hozzáadott alternatív módszert AzureFileShare hely beolvasása</span><span class="sxs-lookup"><span data-stu-id="d7ceb-161">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="d7ceb-162">Frissített ScheduleRunDays SchedulePolicy objektumban időzóna szerint</span><span class="sxs-lookup"><span data-stu-id="d7ceb-162">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d7ceb-163">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d7ceb-163">Az.RedisCache</span></span>
* <span data-ttu-id="d7ceb-164">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-164">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d7ceb-165">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d7ceb-165">Az.Resources</span></span>
* <span data-ttu-id="d7ceb-166">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d7ceb-166">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="d7ceb-167">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d7ceb-167">Az.Sql</span></span>
* <span data-ttu-id="d7ceb-168">Cserélje le a függőségi figyelő SDK közös kód</span><span class="sxs-lookup"><span data-stu-id="d7ceb-168">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="d7ceb-169">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-169">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d7ceb-170">Továbbfejlesztett folyamat, amely több oszlop osztályozási.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-170">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="d7ceb-171">Termékváltozat tulajdonságok (termékváltozat neve, családi, kapacitás) válasz a Get-AzSqlServerServiceObjective és formátum táblaként alapértelmezés szerint tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-171">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="d7ceb-172">Lehetővé teszi a Get-AzSqlServerServiceObjective anélkül, hogy a régióban egy már létező kiszolgáló hely alapján.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-172">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="d7ceb-173">Hozzon létre felügyelt példányt az időzóna-paraméter támogatása.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-173">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="d7ceb-174">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d7ceb-174">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d7ceb-175">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d7ceb-175">Az.Websites</span></span>
* <span data-ttu-id="d7ceb-176">a Set-AzWebApp és a Set-AzWebAppSlot távolítja el a címkék a végrehajtási javítások</span><span class="sxs-lookup"><span data-stu-id="d7ceb-176">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="d7ceb-177">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-177">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d7ceb-178">A webhelyek SDK frissítése.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-178">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="d7ceb-179">A AdminSiteName tulajdonság PSAppServicePlan eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-179">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="d7ceb-180">1.7.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="d7ceb-180">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d7ceb-181">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="d7ceb-181">Highlights since the last major release</span></span>
* <span data-ttu-id="d7ceb-182">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="d7ceb-182">General availability of `Az` module</span></span>
* <span data-ttu-id="d7ceb-183">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="d7ceb-183">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d7ceb-184">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="d7ceb-184">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d7ceb-185">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="d7ceb-185">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d7ceb-186">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="d7ceb-186">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d7ceb-187">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="d7ceb-187">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d7ceb-188">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="d7ceb-188">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d7ceb-189">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d7ceb-189">Az.Accounts</span></span>
* <span data-ttu-id="d7ceb-190">Frissített Add-AzEnvironment és Set-AzEnvironment parancsmag az AzureAnalysisServicesEndpointResourceId paraméter elfogadásához</span><span class="sxs-lookup"><span data-stu-id="d7ceb-190">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d7ceb-191">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d7ceb-191">Az.AnalysisServices</span></span>
* <span data-ttu-id="d7ceb-192">ServiceClient használata DataPlane-parancsmagokban és az eredeti hitelesítési logika eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d7ceb-192">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="d7ceb-193">Az Add-AzureASAccount burkolóként való megadása a Connect-AzAccount számára a kompatibilitástörő változás elkerüléséhez</span><span class="sxs-lookup"><span data-stu-id="d7ceb-193">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d7ceb-194">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d7ceb-194">Az.Automation</span></span>
* <span data-ttu-id="d7ceb-195">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag belefoglalásokat érintő hibája.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-195">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="d7ceb-196">Az IncludedKbNumber és az IncludedPackageNameMask paraméter mostantól működőképes.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-196">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="d7ceb-197">Hibajavítás az Azure Automation frissítéskezelési dinamikus csoportja esetében</span><span class="sxs-lookup"><span data-stu-id="d7ceb-197">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d7ceb-198">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d7ceb-198">Az.Compute</span></span>
* <span data-ttu-id="d7ceb-199">HyperVGeneration paraméter hozzáadása a New-AzDiskConfig és a New-AzSnapshotConfig parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="d7ceb-199">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="d7ceb-200">Virtuális gépek más bérlők katalógus-rendszerképével való létrehozásának engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-200">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="d7ceb-201">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d7ceb-201">Az.ContainerInstance</span></span>
* <span data-ttu-id="d7ceb-202">Ki lett javítva a New-AzContainerGroup üres záró argumentumot hozzáadó -Command paraméterével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="d7ceb-202">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d7ceb-203">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d7ceb-203">Az.DataFactory</span></span>
* <span data-ttu-id="d7ceb-204">Az ADF .Net SDK verziója 3.0.2-re frissült.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-204">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="d7ceb-205">A Set-AzDataFactoryV2 parancsmag a RepoConfiguration beállításaihoz tartozó kiegészítő paraméterekkel lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-205">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d7ceb-206">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d7ceb-206">Az.Resources</span></span>
* <span data-ttu-id="d7ceb-207">Továbbfejlesztett szolgáltatókezelés a Get-AzResource esetében, -ResourceId vagy -ResourceGroupName, -Name és -ResourceType paraméterek megadásakor</span><span class="sxs-lookup"><span data-stu-id="d7ceb-207">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="d7ceb-208">Továbbfejlesztett hibakezelés a Test-AzDeployment és a Test-AzResourceGroupDeployment esetében</span><span class="sxs-lookup"><span data-stu-id="d7ceb-208">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="d7ceb-209">A hibákat nem a telepítés ellenőrzése során kezeli, hanem a parancs kimenetébe foglalja bele</span><span class="sxs-lookup"><span data-stu-id="d7ceb-209">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="d7ceb-210">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="d7ceb-210">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="d7ceb-211">-IgnoreDynamicParameters kapcsolóparaméter hozzáadása telepítési parancsmagokhoz a rendszer által feltett kérdések szkriptekben és feladatokban való mellőzéséhez</span><span class="sxs-lookup"><span data-stu-id="d7ceb-211">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="d7ceb-212">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="d7ceb-212">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="d7ceb-213">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d7ceb-213">Az.Sql</span></span>
* <span data-ttu-id="d7ceb-214">Adatbázisadat-besorolás támogatása.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-214">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d7ceb-215">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d7ceb-215">Az.Storage</span></span>
* <span data-ttu-id="d7ceb-216">Részletes hibaüzenet megjelenítése Storage-környezet -UseConnectedAccount paraméterrel történő létrehozásakor az Azure-fiókba való bejelentkezés nélkül</span><span class="sxs-lookup"><span data-stu-id="d7ceb-216">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="d7ceb-217">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d7ceb-217">New-AzStorageContext</span></span>
* <span data-ttu-id="d7ceb-218">Adott Storage-fiók Blob service-tulajdonságai kezelésének támogatása Management plane API-val</span><span class="sxs-lookup"><span data-stu-id="d7ceb-218">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="d7ceb-219">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d7ceb-219">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="d7ceb-220">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d7ceb-220">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="d7ceb-221">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d7ceb-221">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="d7ceb-222">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d7ceb-222">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="d7ceb-223">Az -AsJob támogatása blobok és fájlok feltöltéséhez, valamint parancsmagok letöltéséhez</span><span class="sxs-lookup"><span data-stu-id="d7ceb-223">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="d7ceb-224">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d7ceb-224">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="d7ceb-225">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d7ceb-225">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="d7ceb-226">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d7ceb-226">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="d7ceb-227">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d7ceb-227">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="d7ceb-228">1.6.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="d7ceb-228">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d7ceb-229">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="d7ceb-229">Highlights since the last major release</span></span>
* <span data-ttu-id="d7ceb-230">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="d7ceb-230">General availability of `Az` module</span></span>
* <span data-ttu-id="d7ceb-231">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="d7ceb-231">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d7ceb-232">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="d7ceb-232">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d7ceb-233">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="d7ceb-233">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d7ceb-234">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="d7ceb-234">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d7ceb-235">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="d7ceb-235">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d7ceb-236">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="d7ceb-236">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d7ceb-237">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d7ceb-237">Az.Automation</span></span>
* <span data-ttu-id="d7ceb-238">Az Azure Automation frissítéskezelése módosult, hogy támogassa az alábbi új funkciókat:</span><span class="sxs-lookup"><span data-stu-id="d7ceb-238">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="d7ceb-239">Dinamikus csoportosítás</span><span class="sxs-lookup"><span data-stu-id="d7ceb-239">Dynamic grouping</span></span>
    * <span data-ttu-id="d7ceb-240">Előzetesen és utólagosan futtatandó szkriptek</span><span class="sxs-lookup"><span data-stu-id="d7ceb-240">Pre-Post script</span></span>
    * <span data-ttu-id="d7ceb-241">Újraindítási beállítás</span><span class="sxs-lookup"><span data-stu-id="d7ceb-241">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d7ceb-242">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d7ceb-242">Az.Compute</span></span>
* <span data-ttu-id="d7ceb-243">Ki lett javítva az elérési útvonal feloldásával kapcsolatos hiba a Get-AzVmBootDiagnosticsData esetében</span><span class="sxs-lookup"><span data-stu-id="d7ceb-243">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="d7ceb-244">A Compute ügyfélkódtár frissült a 25.0.0 verzióra</span><span class="sxs-lookup"><span data-stu-id="d7ceb-244">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d7ceb-245">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d7ceb-245">Az.KeyVault</span></span>
* <span data-ttu-id="d7ceb-246">Helyettesítő karakterek támogatásának hozzáadása a KeyVault-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="d7ceb-246">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d7ceb-247">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d7ceb-247">Az.Network</span></span>
* <span data-ttu-id="d7ceb-248">Az Intelligens veszélyforrás-felderítés támogatásának hozzáadása az Azure Firewallhoz</span><span class="sxs-lookup"><span data-stu-id="d7ceb-248">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="d7ceb-249">Az Application Gateway-tűzfalszabályzat legfelső szintű erőforrása és egyéni szabályok hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d7ceb-249">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d7ceb-250">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d7ceb-250">Az.RecoveryServices</span></span>
* <span data-ttu-id="d7ceb-251">A SnapshotRetentionInDays hozzáadása az Azure-beli virtuális gépek szabályzatához az azonnali RP támogatása érdekében</span><span class="sxs-lookup"><span data-stu-id="d7ceb-251">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="d7ceb-252">Folyamat támogatásának hozzáadása a regisztrációtörlési tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="d7ceb-252">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="d7ceb-253">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d7ceb-253">Az.Resources</span></span>
* <span data-ttu-id="d7ceb-254">Helyettesítő karakterek támogatásának hozzáadása a Get-AzResource és Get-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="d7ceb-254">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="d7ceb-255">Az ARM általános hívása esetén használt hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="d7ceb-255">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="d7ceb-256">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d7ceb-256">Az.Sql</span></span>
* <span data-ttu-id="d7ceb-257">A Fenyegetésészlelés parancsmagjainak paramétere (ExcludeDetectionType) a DetectionType helyett string[] lett, hogy a jövőben is használható legyen az új DetectionType-ok hozzáadásakor, valamint az automatikus kitöltés támogatása érdekében.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-257">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d7ceb-258">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d7ceb-258">Az.Storage</span></span>
* <span data-ttu-id="d7ceb-259">Tárfiók felügyeleti szabályzata lekérésének/beállításának/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="d7ceb-259">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="d7ceb-260">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d7ceb-260">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d7ceb-261">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d7ceb-261">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d7ceb-262">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d7ceb-262">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d7ceb-263">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="d7ceb-263">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="d7ceb-264">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="d7ceb-264">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="d7ceb-265">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="d7ceb-265">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d7ceb-266">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d7ceb-266">Az.Websites</span></span>
* <span data-ttu-id="d7ceb-267">Ki lett javítva az ARM-sablon azon hibája, amely miatt meghiúsul az összes tárolóhely a New-AzWebApp - IncludeSourceWebAppSlots használatával történő klónozása</span><span class="sxs-lookup"><span data-stu-id="d7ceb-267">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="d7ceb-268">1.5.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="d7ceb-268">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d7ceb-269">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d7ceb-269">Az.Accounts</span></span>
* <span data-ttu-id="d7ceb-270">A Register-AzModule parancs hozzáadása az AutoRest által létrehozott parancsmagok támogatásához</span><span class="sxs-lookup"><span data-stu-id="d7ceb-270">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="d7ceb-271">A Connect-AzAccount példáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="d7ceb-271">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d7ceb-272">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d7ceb-272">Az.Automation</span></span>
* <span data-ttu-id="d7ceb-273">A bizonyos havi ütemezések lekérésekor jelentkező hiba kijavítva számos Azure Automation-parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="d7ceb-273">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="d7ceb-274">Ki lett javítva a hiba, amely miatt a Get-AzAutomationDscNode csak az első 20 csomópontot adta vissza.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-274">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="d7ceb-275">Most már az összes csomópontot visszaadja</span><span class="sxs-lookup"><span data-stu-id="d7ceb-275">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d7ceb-276">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d7ceb-276">Az.Cdn</span></span>
* <span data-ttu-id="d7ceb-277">Új Powershell-parancsmagok hozzáadva az Egyéni tartományi Https engedélyezése/letiltása szolgáltatáshoz, a régiek elavultak</span><span class="sxs-lookup"><span data-stu-id="d7ceb-277">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d7ceb-278">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d7ceb-278">Az.Compute</span></span>
* <span data-ttu-id="d7ceb-279">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="d7ceb-279">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d7ceb-280">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d7ceb-280">Az.DataFactory</span></span>
* <span data-ttu-id="d7ceb-281">Az ADF .Net SDK verziója 3.0.1-re frissült</span><span class="sxs-lookup"><span data-stu-id="d7ceb-281">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d7ceb-282">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d7ceb-282">Az.LogicApp</span></span>
* <span data-ttu-id="d7ceb-283">Ki lett javítva a hiba, amely miatt a ListWorkflows csak az eredmények első oldalát kérte le</span><span class="sxs-lookup"><span data-stu-id="d7ceb-283">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d7ceb-284">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d7ceb-284">Az.Network</span></span>
* <span data-ttu-id="d7ceb-285">Helyettesítő karakterek támogatásának hozzáadása a Network-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="d7ceb-285">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d7ceb-286">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d7ceb-286">Az.RecoveryServices</span></span>
* <span data-ttu-id="d7ceb-287">Azure-beli virtuális gépen futtatott SQL Server támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="d7ceb-287">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="d7ceb-288">SDK-frissítés</span><span class="sxs-lookup"><span data-stu-id="d7ceb-288">SDK Update</span></span>
* <span data-ttu-id="d7ceb-289">VMappContainer ellenőrzés eltávolítva a Get-ProtectableItem parancsmagból</span><span class="sxs-lookup"><span data-stu-id="d7ceb-289">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="d7ceb-290">Name és ServerName paraméterek hozzáadva a Get-ProtectableItem parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d7ceb-290">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="d7ceb-291">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d7ceb-291">Az.Resources</span></span>
* <span data-ttu-id="d7ceb-292">`-TemplateObject` paraméter hozzáadva az üzembe helyező parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="d7ceb-292">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="d7ceb-293">További információ: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="d7ceb-293">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="d7ceb-294">Ki lett javítva a hiba, amely akkor jelentkezett, amikor a(z) `Get-AzResource` eredménye át lett irányítva a következőbe: `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="d7ceb-294">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="d7ceb-295">További információ: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="d7ceb-295">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="d7ceb-296">Ki lett javítva a JSON-adattípus módosításával kapcsolatos probléma, amely a(z) `Set-AzResource` futtatásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="d7ceb-296">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="d7ceb-297">További információ: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="d7ceb-297">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="d7ceb-298">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d7ceb-298">Az.Sql</span></span>
* <span data-ttu-id="d7ceb-299">Az AuditingEndpointsCommunicator frissítése.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-299">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="d7ceb-300">Ki lett javítva az új diagnosztikai beállítások létrehozásakor jelentkező ritka eset viselkedése.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-300">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d7ceb-301">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d7ceb-301">Az.Storage</span></span>
* <span data-ttu-id="d7ceb-302">A BlockBlobStorage altípus támogatása a Storage-fiók létrehozásakor      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d7ceb-302">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="d7ceb-303">1.4.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="d7ceb-303">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="d7ceb-304">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d7ceb-304">Az.AnalysisServices</span></span>
* <span data-ttu-id="d7ceb-305">Az AddAzureASAccount parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="d7ceb-305">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d7ceb-306">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d7ceb-306">Az.Automation</span></span>
* <span data-ttu-id="d7ceb-307">Az Import-AzAutomationDscNodeConfiguration súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="d7ceb-307">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="d7ceb-308">A konfigurációnév-ellenőrzés hozzáadva az Import-AzAutomationDscConfiguration parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d7ceb-308">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="d7ceb-309">Továbbfejlesztett hibakezelés az Import-AzAutomationDscConfiguration parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="d7ceb-309">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d7ceb-310">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d7ceb-310">Az.CognitiveServices</span></span>
* <span data-ttu-id="d7ceb-311">A CustomSubdomainName új választható paraméterként hozzáadva a New-AzCognitiveServicesAccount parancsmaghoz, amellyel altartomány adható meg az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-311">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d7ceb-312">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d7ceb-312">Az.Compute</span></span>
* <span data-ttu-id="d7ceb-313">Kijavítva az azonosító paraméterkészleteivel kapcsolatos probléma</span><span class="sxs-lookup"><span data-stu-id="d7ceb-313">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="d7ceb-314">Frissült a Get-AzVMExtension parancsmag, hogy az összes telepített bővítményt listázza, ha a Name paraméter nincs megadva</span><span class="sxs-lookup"><span data-stu-id="d7ceb-314">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="d7ceb-315">A Tag és a ResourceId paraméterek hozzáadva az Update-AzImage parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d7ceb-315">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="d7ceb-316">A Get-AzVmssVM példányazonosító nélkül, az InstanceView használatával példánynézetben listázni tudja a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-316">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d7ceb-317">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d7ceb-317">Az.DataLakeStore</span></span>
* <span data-ttu-id="d7ceb-318">Parancsmagok hozzáadása a törölt ADL-elemek enumerálásához és visszaállításához</span><span class="sxs-lookup"><span data-stu-id="d7ceb-318">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d7ceb-319">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d7ceb-319">Az.EventHub</span></span>
* <span data-ttu-id="d7ceb-320">Új SkipEmptyArchives logikai tulajdonság hozzáadva az üres archívumok kihagyásához az Eventhub CaptureDescription osztályában</span><span class="sxs-lookup"><span data-stu-id="d7ceb-320">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="d7ceb-321">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d7ceb-321">Az.KeyVault</span></span>
* <span data-ttu-id="d7ceb-322">A Set-AzKeyVaultSecret címkézésének kijavítása</span><span class="sxs-lookup"><span data-stu-id="d7ceb-322">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d7ceb-323">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d7ceb-323">Az.LogicApp</span></span>
* <span data-ttu-id="d7ceb-324">Hozzáadva az integrációs fiókok alapszintű termékváltozatában</span><span class="sxs-lookup"><span data-stu-id="d7ceb-324">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="d7ceb-325">Hozzáadva az XSLT 2.0-ban, az XSLT 3.0-ban és a Liquid leképezéstípusok esetén</span><span class="sxs-lookup"><span data-stu-id="d7ceb-325">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="d7ceb-326">Új parancsmagok az integrációs fiók szerelvényeihez</span><span class="sxs-lookup"><span data-stu-id="d7ceb-326">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="d7ceb-327">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d7ceb-327">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d7ceb-328">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d7ceb-328">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d7ceb-329">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d7ceb-329">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d7ceb-330">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d7ceb-330">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="d7ceb-331">Új parancsmagok az integrációs fiók kötegkonfigurációjához</span><span class="sxs-lookup"><span data-stu-id="d7ceb-331">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="d7ceb-332">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d7ceb-332">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d7ceb-333">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d7ceb-333">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d7ceb-334">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d7ceb-334">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d7ceb-335">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d7ceb-335">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="d7ceb-336">A Logic Apps SDK frissítése a 4.1.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="d7ceb-336">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d7ceb-337">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d7ceb-337">Az.Monitor</span></span>
* <span data-ttu-id="d7ceb-338">A Get-AzMetric súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="d7ceb-338">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d7ceb-339">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d7ceb-339">Az.Network</span></span>
* <span data-ttu-id="d7ceb-340">Az Add-AzApplicationGatewayCustomError súgójában lévő példa frissítése</span><span class="sxs-lookup"><span data-stu-id="d7ceb-340">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d7ceb-341">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d7ceb-341">Az.OperationalInsights</span></span>
* <span data-ttu-id="d7ceb-342">Kibővített támogatás a New és a Get ApplicationInsights adatforráshoz.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-342">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="d7ceb-343">Új „ApplicationInsights” altípus hozzáadva az adott munkaterület Get specific és Get all Application Insights-adatforrásainak támogatásához.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-343">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="d7ceb-344">A New-AzOperationalInsightsApplicationInsightsDataSource parancsmag hozzáadva adatforrás létrehozásához a következő Application Insights-erőforrásparaméterekkel: subscriptionId, resourceGroupName és name.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-344">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="d7ceb-345">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d7ceb-345">Az.Resources</span></span>
* <span data-ttu-id="d7ceb-346">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="d7ceb-346">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="d7ceb-347">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="d7ceb-347">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="d7ceb-348">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="d7ceb-348">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="d7ceb-349">Ki lett javítva a KeyCredentials ismételt létrehozását megakadályozó hiba</span><span class="sxs-lookup"><span data-stu-id="d7ceb-349">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="d7ceb-350">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d7ceb-350">Az.Sql</span></span>
* <span data-ttu-id="d7ceb-351">Rugalmas SQL DB-skálázási szint támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d7ceb-351">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="d7ceb-352">Ki lett javítva az a hiba, hogy a visszaállítási kérésben szereplő szükségtelen tulajdonságok megadása miatt a visszaállítás esetenként meghiúsult</span><span class="sxs-lookup"><span data-stu-id="d7ceb-352">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d7ceb-353">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d7ceb-353">Az.Websites</span></span>
* <span data-ttu-id="d7ceb-354">A Get-AzWebAppSlotMetrics példájának javítása</span><span class="sxs-lookup"><span data-stu-id="d7ceb-354">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="d7ceb-355">1.3.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="d7ceb-355">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d7ceb-356">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d7ceb-356">Az.Accounts</span></span>
* <span data-ttu-id="d7ceb-357">Frissítés a ClientRuntime legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="d7ceb-357">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d7ceb-358">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d7ceb-358">Az.AnalysisServices</span></span>
<span data-ttu-id="d7ceb-359">Az Az.AnalysisServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-359">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d7ceb-360">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d7ceb-360">Az.Compute</span></span>
* <span data-ttu-id="d7ceb-361">AEM-bővítmény: Mostantól az UltraSSD, valamint a P60, P70 és P80 lemezek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-361">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="d7ceb-362">A Set-AzVMBootDiagnostics súgóleírása frissült.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-362">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="d7ceb-363">Az Update-AzImage súgóleírása és példája frissült.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-363">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d7ceb-364">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d7ceb-364">Az.RecoveryServices</span></span>
<span data-ttu-id="d7ceb-365">Az Az.RecoveryServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-365">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d7ceb-366">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d7ceb-366">Az.Resources</span></span>
* <span data-ttu-id="d7ceb-367">Az erőforráscsoportok címkézése ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-367">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="d7ceb-368">További információ: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="d7ceb-368">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="d7ceb-369">Ki lett javítva az a hiba, amikor a `Get-AzureRmRoleAssignment` nem vette figyelembe az -ErrorAction paramétert.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-369">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="d7ceb-370">További információ: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="d7ceb-370">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="d7ceb-371">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d7ceb-371">Az.Sql</span></span>
* <span data-ttu-id="d7ceb-372">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d7ceb-372">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="d7ceb-373">Ki lett javítva az a hiba, amikor az Azure-fiókba való bejelentkezés hiánya nullref kivételt eredményezett az SQL-parancsmagok végrehajtásakor.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-373">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="d7ceb-374">A nullref kivétel ki lett javítva a Get-AzSqlCapabilityben.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-374">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="d7ceb-375">1.2.1 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="d7ceb-375">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d7ceb-376">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d7ceb-376">Az.Accounts</span></span>
* <span data-ttu-id="d7ceb-377">A hitelesítés megfelelő verziójával rendelkező kiadás</span><span class="sxs-lookup"><span data-stu-id="d7ceb-377">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d7ceb-378">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d7ceb-378">Az.AnalysisServices</span></span>
* <span data-ttu-id="d7ceb-379">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="d7ceb-379">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d7ceb-380">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d7ceb-380">Az.RecoveryServices</span></span>
* <span data-ttu-id="d7ceb-381">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="d7ceb-381">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="d7ceb-382">1.2.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="d7ceb-382">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d7ceb-383">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d7ceb-383">Az.Accounts</span></span>
* <span data-ttu-id="d7ceb-384">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="d7ceb-384">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d7ceb-385">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-385">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d7ceb-386">Az Uninstall-AzureRm figyelmeztető üzenete hozzáadva a PS Core-ban</span><span class="sxs-lookup"><span data-stu-id="d7ceb-386">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="d7ceb-387">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d7ceb-387">Az.Aks</span></span>
* <span data-ttu-id="d7ceb-388">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-388">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d7ceb-389">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d7ceb-389">Az.Automation</span></span>
* <span data-ttu-id="d7ceb-390">Mostantól támogatottak a Python 2-runbookok.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-390">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="d7ceb-391">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-391">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d7ceb-392">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d7ceb-392">Az.Cdn</span></span>
* <span data-ttu-id="d7ceb-393">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-393">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d7ceb-394">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d7ceb-394">Az.Compute</span></span>
* <span data-ttu-id="d7ceb-395">Az Invoke-AzVMReimage parancsmag hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-395">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="d7ceb-396">A TempDisk paraméter hozzá lett adva a Set-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-396">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="d7ceb-397">A New-AzVM figyelmeztető üzenete ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-397">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="d7ceb-398">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d7ceb-398">Az.ContainerRegistry</span></span>
* <span data-ttu-id="d7ceb-399">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-399">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d7ceb-400">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d7ceb-400">Az.DataFactory</span></span>
* <span data-ttu-id="d7ceb-401">Az ADF .Net SDK verziója 3.0.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-401">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d7ceb-402">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d7ceb-402">Az.DataLakeStore</span></span>
* <span data-ttu-id="d7ceb-403">Ki lett javítva az ADLS-végponttal kapcsolatos probléma az MSI használatakor.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-403">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="d7ceb-404">További információ: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="d7ceb-404">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="d7ceb-405">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-405">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d7ceb-406">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d7ceb-406">Az.IotHub</span></span>
* <span data-ttu-id="d7ceb-407">Az Encoding formátum hozzá lett adva az Add-IotHubRoutingEndpoint parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-407">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d7ceb-408">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d7ceb-408">Az.KeyVault</span></span>
* <span data-ttu-id="d7ceb-409">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-409">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d7ceb-410">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d7ceb-410">Az.Network</span></span>
* <span data-ttu-id="d7ceb-411">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-411">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="d7ceb-412">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d7ceb-412">Az.Resources</span></span>
* <span data-ttu-id="d7ceb-413">A helytelen példák ki lettek javítva a New-AzADAppCredential és a New-AzADSpCredential referenciadokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-413">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="d7ceb-414">Ki lett javítva az a hiba, amikor a -TemplateFile paraméter nem lett feloldva az erőforráscsoportokat üzembe helyező parancsmagok végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-414">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="d7ceb-415">Az.Resources: A New-AzureRmPolicyDefinition -Mode alapértelmezett értékének dokumentációja ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-415">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="d7ceb-416">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="d7ceb-416">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="d7ceb-417">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="d7ceb-417">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="d7ceb-418">Ki lett javítva a „PSResourceGroupDeployment” objektum formázásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-418">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="d7ceb-419">További információ: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="d7ceb-419">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d7ceb-420">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d7ceb-420">Az.ServiceFabric</span></span>
* <span data-ttu-id="d7ceb-421">Visszaállítás a VMSS-modell tanúsítványának hozzáadásakor bekövetkező kivétel-visszaadás esetén; javított hiba: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-421">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="d7ceb-422">Bizonyos hibaüzenetek ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-422">Fix some error messages.</span></span>
* <span data-ttu-id="d7ceb-423">Ki lett javítva az alapértelmezett ARM-sablonnal való fürtlétrehozás a New-AzServiceFabriCluster esetében, amely nem működött az Az-ba történő migrálással.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-423">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="d7ceb-424">Ki lett javítva a fürt-/alkalmazástanúsítvány létrehozása, így mostantól csak a fürtnek megfelelő virtuálisgép-méretezési csoportokhoz (Virtual Machine Scale Sets) lesznek hozzáadva, a fürtazonosító bővítményben való ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-424">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d7ceb-425">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d7ceb-425">Az.SignalR</span></span>
* <span data-ttu-id="d7ceb-426">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-426">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="d7ceb-427">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d7ceb-427">Az.Sql</span></span>
* <span data-ttu-id="d7ceb-428">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-428">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d7ceb-429">A LicenseType paraméter paraméterleírása frissítve lett a lehetséges értékekkel.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-429">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="d7ceb-430">Ki lett javítva az a hiba, amikor egy felügyelt példány identitásának frissítése nem működött, ha az volt az egyetlen frissített tulajdonság.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-430">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="d7ceb-431">Egyéni rendezések támogatása a felügyelt példányokon</span><span class="sxs-lookup"><span data-stu-id="d7ceb-431">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d7ceb-432">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d7ceb-432">Az.Storage</span></span>
* <span data-ttu-id="d7ceb-433">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-433">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d7ceb-434">Részletes hibaüzenet megjelenítése klasszikus naplózás/metrika get/set műveletei esetében a prémium szintű Storage-fiókon, mivel a prémium szintű Storage-fiók nem támogatja a klasszikus naplózást/metrikát.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-434">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="d7ceb-435">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="d7ceb-435">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="d7ceb-436">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="d7ceb-436">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="d7ceb-437">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="d7ceb-437">Az.TrafficManager</span></span>
* <span data-ttu-id="d7ceb-438">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-438">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d7ceb-439">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d7ceb-439">Az.Websites</span></span>
* <span data-ttu-id="d7ceb-440">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-440">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d7ceb-441">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól a megfelelő erőforráscsoportba és helyre tölti fel a tanúsítványt, ha az alkalmazás ASE-n üzemel.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-441">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="d7ceb-442">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól nem írja felül a címkéket SSL-tanúsítvány alkalmazáshoz való kötésekor.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-442">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="d7ceb-443">1.1.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="d7ceb-443">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d7ceb-444">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d7ceb-444">Az.Accounts</span></span>
* <span data-ttu-id="d7ceb-445">A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz</span><span class="sxs-lookup"><span data-stu-id="d7ceb-445">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d7ceb-446">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d7ceb-446">Az.Compute</span></span>
* <span data-ttu-id="d7ceb-447">A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni</span><span class="sxs-lookup"><span data-stu-id="d7ceb-447">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="d7ceb-448">Frissült az azonosító leírása a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="d7ceb-448">Updated the description of ID in help files</span></span>
* <span data-ttu-id="d7ceb-449">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="d7ceb-449">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d7ceb-450">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d7ceb-450">Az.DataLakeStore</span></span>
* <span data-ttu-id="d7ceb-451">A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-451">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="d7ceb-452">A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva</span><span class="sxs-lookup"><span data-stu-id="d7ceb-452">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d7ceb-453">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d7ceb-453">Az.EventGrid</span></span>
* <span data-ttu-id="d7ceb-454">Frissítve a 2019-01-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-454">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="d7ceb-455">A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához</span><span class="sxs-lookup"><span data-stu-id="d7ceb-455">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="d7ceb-456">New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="d7ceb-456">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="d7ceb-457">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="d7ceb-457">Event Time-To-Live,</span></span>
        - <span data-ttu-id="d7ceb-458">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="d7ceb-458">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="d7ceb-459">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-459">Dead letter endpoint.</span></span>
    - <span data-ttu-id="d7ceb-460">Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="d7ceb-460">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="d7ceb-461">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="d7ceb-461">Event Time-To-Live,</span></span>
        - <span data-ttu-id="d7ceb-462">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="d7ceb-462">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="d7ceb-463">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-463">Dead letter endpoint.</span></span>
* <span data-ttu-id="d7ceb-464">Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-464">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="d7ceb-465">Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-465">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d7ceb-466">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d7ceb-466">Az.IotHub</span></span>
* <span data-ttu-id="d7ceb-467">Frissítve az IoT Hub SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="d7ceb-467">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d7ceb-468">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d7ceb-468">Az.LogicApp</span></span>
* <span data-ttu-id="d7ceb-469">A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel</span><span class="sxs-lookup"><span data-stu-id="d7ceb-469">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="d7ceb-470">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d7ceb-470">Az.Resources</span></span>
* <span data-ttu-id="d7ceb-471">Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="d7ceb-471">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="d7ceb-472">További információ: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="d7ceb-472">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="d7ceb-473">Ki lett javítva a -Custom paraméter kezelése a New/Set-AzPolicyDefinition parancsban</span><span class="sxs-lookup"><span data-stu-id="d7ceb-473">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="d7ceb-474">Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="d7ceb-474">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="d7ceb-475">A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében</span><span class="sxs-lookup"><span data-stu-id="d7ceb-475">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="d7ceb-476">További információ: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="d7ceb-476">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d7ceb-477">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d7ceb-477">Az.SignalR</span></span>
* <span data-ttu-id="d7ceb-478">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="d7ceb-478">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="d7ceb-479">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d7ceb-479">Az.Sql</span></span>
* <span data-ttu-id="d7ceb-480">A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-480">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d7ceb-481">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d7ceb-481">Az.Storage</span></span>
* <span data-ttu-id="d7ceb-482">A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva</span><span class="sxs-lookup"><span data-stu-id="d7ceb-482">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="d7ceb-483">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d7ceb-483">New-AzStorageContext</span></span>
* <span data-ttu-id="d7ceb-484">A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz</span><span class="sxs-lookup"><span data-stu-id="d7ceb-484">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="d7ceb-485">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="d7ceb-485">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d7ceb-486">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d7ceb-486">Az.Websites</span></span>
* <span data-ttu-id="d7ceb-487">Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban</span><span class="sxs-lookup"><span data-stu-id="d7ceb-487">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="d7ceb-488">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="d7ceb-488">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="d7ceb-489">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="d7ceb-489">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="d7ceb-490">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="d7ceb-490">General</span></span>

- <span data-ttu-id="d7ceb-491">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="d7ceb-491">General Availability of Az Module</span></span>
- <span data-ttu-id="d7ceb-492">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="d7ceb-492">Online help for each module</span></span>
- <span data-ttu-id="d7ceb-493">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="d7ceb-493">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="d7ceb-494">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d7ceb-494">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="d7ceb-495">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d7ceb-495">Az.Accounts</span></span>
- <span data-ttu-id="d7ceb-496">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="d7ceb-496">Changed from Az.Profile</span></span>
- <span data-ttu-id="d7ceb-497">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="d7ceb-497">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="d7ceb-498">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d7ceb-498">Az.ApiManagement</span></span>
- <span data-ttu-id="d7ceb-499">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="d7ceb-499">Fixes for #7002</span></span>
- <span data-ttu-id="d7ceb-500">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d7ceb-500">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="d7ceb-501">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d7ceb-501">Az.Batch</span></span>
- <span data-ttu-id="d7ceb-502">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-502">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="d7ceb-503">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-503">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="d7ceb-504">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d7ceb-504">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="d7ceb-505">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="d7ceb-505">Az.Billing</span></span>
- <span data-ttu-id="d7ceb-506">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-506">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="d7ceb-507">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="d7ceb-507">Az.CognitivServices</span></span>
- <span data-ttu-id="d7ceb-508">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-508">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="d7ceb-509">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-509">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="d7ceb-510">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d7ceb-510">Az.ContainerInstance</span></span>
- <span data-ttu-id="d7ceb-511">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="d7ceb-511">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="d7ceb-512">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="d7ceb-512">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="d7ceb-513">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d7ceb-513">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="d7ceb-514">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d7ceb-514">Az.DataLakeStore</span></span>
- <span data-ttu-id="d7ceb-515">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d7ceb-515">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="d7ceb-516">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d7ceb-516">Az.Monitor</span></span>
- <span data-ttu-id="d7ceb-517">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d7ceb-517">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="d7ceb-518">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d7ceb-518">Az.KeyVault</span></span>
- <span data-ttu-id="d7ceb-519">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-519">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="d7ceb-520">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="d7ceb-520">Az.MachineLearning</span></span>
- <span data-ttu-id="d7ceb-521">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="d7ceb-521">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="d7ceb-522">Az.Media</span><span class="sxs-lookup"><span data-stu-id="d7ceb-522">Az.Media</span></span>
- <span data-ttu-id="d7ceb-523">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="d7ceb-523">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="d7ceb-524">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d7ceb-524">Az.Network</span></span>
<span data-ttu-id="d7ceb-525">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-525">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="d7ceb-526">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="d7ceb-526">New cmdlets added:</span></span>
        - <span data-ttu-id="d7ceb-527">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d7ceb-527">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d7ceb-528">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d7ceb-528">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d7ceb-529">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d7ceb-529">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d7ceb-530">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d7ceb-530">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d7ceb-531">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d7ceb-531">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d7ceb-532">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="d7ceb-532">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="d7ceb-533">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d7ceb-533">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="d7ceb-534">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d7ceb-534">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="d7ceb-535">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d7ceb-535">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="d7ceb-536">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d7ceb-536">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="d7ceb-537">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d7ceb-537">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="d7ceb-538">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d7ceb-538">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="d7ceb-539">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d7ceb-539">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="d7ceb-540">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d7ceb-540">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="d7ceb-541">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-541">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="d7ceb-542">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d7ceb-542">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="d7ceb-543">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d7ceb-543">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="d7ceb-544">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d7ceb-544">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="d7ceb-545">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d7ceb-545">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="d7ceb-546">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="d7ceb-546">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="d7ceb-547">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d7ceb-547">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="d7ceb-548">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d7ceb-548">Az.OperationalInsights</span></span>
- <span data-ttu-id="d7ceb-549">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d7ceb-549">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="d7ceb-550">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d7ceb-550">Az.Profile</span></span>
- <span data-ttu-id="d7ceb-551">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d7ceb-551">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="d7ceb-552">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d7ceb-552">Az.RecoveryServices</span></span>
- <span data-ttu-id="d7ceb-553">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d7ceb-553">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="d7ceb-554">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d7ceb-554">Az.Resources</span></span>
- <span data-ttu-id="d7ceb-555">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d7ceb-555">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="d7ceb-556">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d7ceb-556">Az.ServiceFabric</span></span>
- <span data-ttu-id="d7ceb-557">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="d7ceb-557">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="d7ceb-558">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d7ceb-558">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="d7ceb-559">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="d7ceb-559">Az.SIgnalR</span></span>
- <span data-ttu-id="d7ceb-560">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="d7ceb-560">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="d7ceb-561">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d7ceb-561">Az.Sql</span></span>
- <span data-ttu-id="d7ceb-562">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="d7ceb-562">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="d7ceb-563">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="d7ceb-563">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="d7ceb-564">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d7ceb-564">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="d7ceb-565">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d7ceb-565">Az.Storage</span></span>
- <span data-ttu-id="d7ceb-566">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d7ceb-566">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="d7ceb-567">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d7ceb-567">Az.Websites</span></span>
- <span data-ttu-id="d7ceb-568">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d7ceb-568">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="d7ceb-569">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="d7ceb-569">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="d7ceb-570">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="d7ceb-570">General</span></span>

* <span data-ttu-id="d7ceb-571">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="d7ceb-571">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="d7ceb-572">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d7ceb-572">Az.Compute</span></span>

* <span data-ttu-id="d7ceb-573">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-573">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="d7ceb-574">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d7ceb-574">Az.DataLakeStore</span></span>

* <span data-ttu-id="d7ceb-575">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="d7ceb-575">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="d7ceb-576">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d7ceb-576">Az.FrontDoor</span></span>

* <span data-ttu-id="d7ceb-577">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="d7ceb-577">Fixed some broken links</span></span>
    - <span data-ttu-id="d7ceb-578">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-578">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="d7ceb-579">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-579">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="d7ceb-580">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d7ceb-580">Az.RecoveryServices</span></span>

* <span data-ttu-id="d7ceb-581">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-581">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="d7ceb-582">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-582">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="d7ceb-583">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d7ceb-583">Az.Resources</span></span>

* <span data-ttu-id="d7ceb-584">https://github.com/Azure/azure-powershell/issues/7679 javítása</span><span class="sxs-lookup"><span data-stu-id="d7ceb-584">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="d7ceb-585">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-585">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="d7ceb-586">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d7ceb-586">Az.Sql</span></span>

* <span data-ttu-id="d7ceb-587">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="d7ceb-587">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="d7ceb-588">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="d7ceb-588">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="d7ceb-589">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-589">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="d7ceb-590">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d7ceb-590">Az.Storage</span></span>

* <span data-ttu-id="d7ceb-591">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d7ceb-591">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="d7ceb-592">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-592">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="d7ceb-593">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d7ceb-593">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="d7ceb-594">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="d7ceb-594">Support Static Website configuration</span></span>
    - <span data-ttu-id="d7ceb-595">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d7ceb-595">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="d7ceb-596">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d7ceb-596">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="d7ceb-597">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d7ceb-597">Az.Websites</span></span>

* <span data-ttu-id="d7ceb-598">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d7ceb-598">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="d7ceb-599">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-599">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="d7ceb-600">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-600">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="d7ceb-601">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="d7ceb-601">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="d7ceb-602">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d7ceb-602">Az.ApiManagement</span></span>
* <span data-ttu-id="d7ceb-603">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-603">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="d7ceb-604">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d7ceb-604">Az.Automation</span></span>
* <span data-ttu-id="d7ceb-605">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-605">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="d7ceb-606">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-606">Added Update Management cmdlets</span></span>
* <span data-ttu-id="d7ceb-607">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-607">Added Source Control cmdlets</span></span>
* <span data-ttu-id="d7ceb-608">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-608">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="d7ceb-609">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-609">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="d7ceb-610">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d7ceb-610">Az.Compute</span></span>
* <span data-ttu-id="d7ceb-611">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-611">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="d7ceb-612">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-612">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="d7ceb-613">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d7ceb-613">Az.ContainerInstance</span></span>
* <span data-ttu-id="d7ceb-614">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-614">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="d7ceb-615">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="d7ceb-615">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="d7ceb-616">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-616">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="d7ceb-617">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d7ceb-617">Az.Network</span></span>
* <span data-ttu-id="d7ceb-618">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-618">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="d7ceb-619">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-619">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="d7ceb-620">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-620">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="d7ceb-621">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-621">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="d7ceb-622">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="d7ceb-622">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="d7ceb-623">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-623">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="d7ceb-624">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-624">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="d7ceb-625">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="d7ceb-625">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="d7ceb-626">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-626">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="d7ceb-627">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-627">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="d7ceb-628">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="d7ceb-628">Az.Relay</span></span>
* <span data-ttu-id="d7ceb-629">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-629">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="d7ceb-630">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d7ceb-630">Az.Resources</span></span>
* <span data-ttu-id="d7ceb-631">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-631">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="d7ceb-632">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-632">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="d7ceb-633">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-633">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="d7ceb-634">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d7ceb-634">Az.ServiceFabric</span></span>
* <span data-ttu-id="d7ceb-635">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-635">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="d7ceb-636">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d7ceb-636">Az.Sql</span></span>
* <span data-ttu-id="d7ceb-637">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-637">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="d7ceb-638">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d7ceb-638">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d7ceb-639">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d7ceb-639">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d7ceb-640">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d7ceb-640">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d7ceb-641">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d7ceb-641">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d7ceb-642">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d7ceb-642">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d7ceb-643">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d7ceb-643">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d7ceb-644">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d7ceb-644">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d7ceb-645">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d7ceb-645">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="d7ceb-646">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-646">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="d7ceb-647">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-647">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="d7ceb-648">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-648">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="d7ceb-649">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-649">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="d7ceb-650">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-650">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="d7ceb-651">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-651">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="d7ceb-652">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-652">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="d7ceb-653">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-653">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="d7ceb-654">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="d7ceb-654">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="d7ceb-655">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="d7ceb-655">General</span></span>
* <span data-ttu-id="d7ceb-656">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-656">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="d7ceb-657">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d7ceb-657">Az.Profile</span></span>
* <span data-ttu-id="d7ceb-658">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-658">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="d7ceb-659">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="d7ceb-659">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="d7ceb-660">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="d7ceb-660">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="d7ceb-661">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="d7ceb-661">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="d7ceb-662">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="d7ceb-662">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="d7ceb-663">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="d7ceb-663">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="d7ceb-664">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="d7ceb-664">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="d7ceb-665">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d7ceb-665">Az.CognitiveServices</span></span>
* <span data-ttu-id="d7ceb-666">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-666">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d7ceb-667">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d7ceb-667">Az.Compute</span></span>
* <span data-ttu-id="d7ceb-668">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="d7ceb-668">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="d7ceb-669">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="d7ceb-669">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="d7ceb-670">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-670">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d7ceb-671">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d7ceb-671">Az.DataLakeStore</span></span>
* <span data-ttu-id="d7ceb-672">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-672">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="d7ceb-673">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-673">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="d7ceb-674">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="d7ceb-674">Az.Insights</span></span>
* <span data-ttu-id="d7ceb-675">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="d7ceb-675">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="d7ceb-676">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="d7ceb-676">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="d7ceb-677">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="d7ceb-677">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="d7ceb-678">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="d7ceb-678">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d7ceb-679">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d7ceb-679">Az.Network</span></span>
* <span data-ttu-id="d7ceb-680">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="d7ceb-680">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="d7ceb-681">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="d7ceb-681">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="d7ceb-682">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="d7ceb-682">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="d7ceb-683">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d7ceb-683">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="d7ceb-684">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="d7ceb-684">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="d7ceb-685">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="d7ceb-685">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="d7ceb-686">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d7ceb-686">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d7ceb-687">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d7ceb-687">Az.PolicyInsights</span></span>
* <span data-ttu-id="d7ceb-688">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d7ceb-688">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="d7ceb-689">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d7ceb-689">Az.Resources</span></span>
* <span data-ttu-id="d7ceb-690">https://github.com/Azure/azure-powershell/issues/7402 javítása</span><span class="sxs-lookup"><span data-stu-id="d7ceb-690">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="d7ceb-691">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="d7ceb-691">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d7ceb-692">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d7ceb-692">Az.ServiceBus</span></span>
* <span data-ttu-id="d7ceb-693">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-693">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d7ceb-694">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d7ceb-694">Az.ServiceFabric</span></span>
* <span data-ttu-id="d7ceb-695">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-695">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="d7ceb-696">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="d7ceb-696">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="d7ceb-697">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="d7ceb-697">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="d7ceb-698">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="d7ceb-698">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="d7ceb-699">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-699">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="d7ceb-700">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="d7ceb-700">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="d7ceb-701">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d7ceb-701">Az.Profile</span></span>
* <span data-ttu-id="d7ceb-702">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-702">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="d7ceb-703">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-703">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d7ceb-704">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d7ceb-704">Az.Compute</span></span>
* <span data-ttu-id="d7ceb-705">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-705">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="d7ceb-706">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-706">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d7ceb-707">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d7ceb-707">Az.DataLakeStore</span></span>
* <span data-ttu-id="d7ceb-708">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="d7ceb-708">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="d7ceb-709">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-709">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="d7ceb-710">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-710">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="d7ceb-711">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-711">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="d7ceb-712">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-712">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d7ceb-713">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d7ceb-713">Az.Network</span></span>
* <span data-ttu-id="d7ceb-714">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-714">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="d7ceb-715">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-715">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d7ceb-716">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d7ceb-716">Az.Resources</span></span>
* <span data-ttu-id="d7ceb-717">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="d7ceb-717">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="d7ceb-718">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-718">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="d7ceb-719">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="d7ceb-719">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="d7ceb-720">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="d7ceb-720">Azure.Storage</span></span>
* <span data-ttu-id="d7ceb-721">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="d7ceb-721">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="d7ceb-722">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d7ceb-722">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="d7ceb-723">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d7ceb-723">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="d7ceb-724">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-724">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="d7ceb-725">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="d7ceb-725">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="d7ceb-726">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d7ceb-726">Az.CognitiveServices</span></span>
* <span data-ttu-id="d7ceb-727">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-727">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d7ceb-728">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d7ceb-728">Az.Compute</span></span>
* <span data-ttu-id="d7ceb-729">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-729">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="d7ceb-730">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-730">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="d7ceb-731">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="d7ceb-731">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="d7ceb-732">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="d7ceb-732">Az.DataFactoryV2</span></span>
* <span data-ttu-id="d7ceb-733">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-733">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d7ceb-734">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d7ceb-734">Az.Network</span></span>
* <span data-ttu-id="d7ceb-735">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-735">Added NetworkProfile functionality.</span></span> <span data-ttu-id="d7ceb-736">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d7ceb-736">new cmdlets added</span></span>
    - <span data-ttu-id="d7ceb-737">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d7ceb-737">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="d7ceb-738">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d7ceb-738">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="d7ceb-739">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d7ceb-739">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="d7ceb-740">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d7ceb-740">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="d7ceb-741">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="d7ceb-741">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="d7ceb-742">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="d7ceb-742">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="d7ceb-743">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="d7ceb-743">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="d7ceb-744">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="d7ceb-744">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="d7ceb-745">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="d7ceb-745">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d7ceb-746">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d7ceb-746">Az.RedisCache</span></span>
* <span data-ttu-id="d7ceb-747">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-747">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="d7ceb-748">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="d7ceb-748">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="d7ceb-749">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d7ceb-749">Az.Resources</span></span>
* <span data-ttu-id="d7ceb-750">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d7ceb-750">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="d7ceb-751">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="d7ceb-751">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="d7ceb-752">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d7ceb-752">Az.Sql</span></span>
* <span data-ttu-id="d7ceb-753">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="d7ceb-753">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d7ceb-754">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d7ceb-754">Az.Websites</span></span>
* <span data-ttu-id="d7ceb-755">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="d7ceb-755">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="d7ceb-756">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="d7ceb-756">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="d7ceb-757">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="d7ceb-757">0.2.0 - September 2018</span></span>
 <span data-ttu-id="d7ceb-758">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="d7ceb-758">Initial Release</span></span>