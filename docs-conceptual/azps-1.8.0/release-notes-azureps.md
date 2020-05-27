---
title: Az Azure PowerShell kibocsátási megjegyzései
description: Megismerheti az Azure PowerShell-modulok legújabb frissítéseit.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/30/2019
ms.openlocfilehash: 287e9e1f066d0768e7f572ca7f5f2ee2b78931d9
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/14/2020
ms.locfileid: "83386969"
---
## <a name="180---april-2019"></a><span data-ttu-id="73100-103">1.8.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="73100-103">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="73100-104">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="73100-104">Highlights since the last major release</span></span>
* <span data-ttu-id="73100-105">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="73100-105">General availability of `Az` module</span></span>
* <span data-ttu-id="73100-106">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="73100-106">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="73100-107">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="73100-107">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="73100-108">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="73100-108">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="73100-109">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="73100-109">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="73100-110">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="73100-110">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="73100-111">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="73100-111">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="73100-112">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73100-112">Az.Accounts</span></span>
* <span data-ttu-id="73100-113">Eltávolítás-AzureRm megfelelően törölni a Mac modulok frissítése</span><span class="sxs-lookup"><span data-stu-id="73100-113">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="73100-114">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="73100-114">Az.Batch</span></span>
* <span data-ttu-id="73100-115">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="73100-115">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="73100-116">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="73100-116">Az.Cdn</span></span>
* <span data-ttu-id="73100-117">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="73100-117">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="73100-118">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="73100-118">Az.CognitiveServices</span></span>
* <span data-ttu-id="73100-119">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="73100-119">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73100-120">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73100-120">Az.Compute</span></span>
* <span data-ttu-id="73100-121">Az AEM telepítési kapcsolatos problémák megoldásához, ha a lemezek erőforrás-azonosítók kisbetűs resourcegroups volt az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="73100-121">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="73100-122">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="73100-122">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="73100-123">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="73100-123">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73100-124">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73100-124">Az.DataFactory</span></span>
* <span data-ttu-id="73100-125">Adjon hozzá SsisProperties, ha a NodeCount felügyelt integrációs modul nem null értékű.</span><span class="sxs-lookup"><span data-stu-id="73100-125">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73100-126">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73100-126">Az.DataLakeStore</span></span>
* <span data-ttu-id="73100-127">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="73100-127">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="73100-128">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="73100-128">Az.EventGrid</span></span>
* <span data-ttu-id="73100-129">A Súgó szöveg jelzi, hogy erőforrásokat kell létrehozni a create/update eseményt előfizetés parancsmagok használata előtt végpont frissítése.</span><span class="sxs-lookup"><span data-stu-id="73100-129">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="73100-130">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="73100-130">Az.EventHub</span></span>
* <span data-ttu-id="73100-131">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="73100-131">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="73100-132">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="73100-132">Az.HDInsight</span></span>
* <span data-ttu-id="73100-133">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="73100-133">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="73100-134">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="73100-134">Az.IotHub</span></span>
* <span data-ttu-id="73100-135">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="73100-135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="73100-136">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73100-136">Az.KeyVault</span></span>
* <span data-ttu-id="73100-137">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="73100-137">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="73100-138">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="73100-138">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="73100-139">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="73100-139">Az.MachineLearning</span></span>
* <span data-ttu-id="73100-140">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="73100-140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="73100-141">Az.Media</span><span class="sxs-lookup"><span data-stu-id="73100-141">Az.Media</span></span>
* <span data-ttu-id="73100-142">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="73100-142">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73100-143">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73100-143">Az.Monitor</span></span>
  * <span data-ttu-id="73100-144">Riasztási szabály (nem klasszikus) GenV2 mérőszám-alapú új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="73100-144">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="73100-145">Új AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="73100-145">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="73100-146">Új AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="73100-146">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="73100-147">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="73100-147">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="73100-148">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="73100-148">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="73100-149">Adjon hozzá AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="73100-149">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="73100-150">Frissített verzió 0.22.0-preview figyelő SDK</span><span class="sxs-lookup"><span data-stu-id="73100-150">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73100-151">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73100-151">Az.Network</span></span>
* <span data-ttu-id="73100-152">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="73100-152">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="73100-153">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="73100-153">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="73100-154">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="73100-154">Az.NotificationHubs</span></span>
* <span data-ttu-id="73100-155">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="73100-155">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="73100-156">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="73100-156">Az.OperationalInsights</span></span>
* <span data-ttu-id="73100-157">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="73100-157">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="73100-158">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="73100-158">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="73100-159">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="73100-159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73100-160">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73100-160">Az.RecoveryServices</span></span>
* <span data-ttu-id="73100-161">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="73100-161">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="73100-162">Frissített táblázatos formában az SQL azure-beli virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="73100-162">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="73100-163">A hozzáadott alternatív módszert AzureFileShare hely beolvasása</span><span class="sxs-lookup"><span data-stu-id="73100-163">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="73100-164">Frissített ScheduleRunDays SchedulePolicy objektumban időzóna szerint</span><span class="sxs-lookup"><span data-stu-id="73100-164">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="73100-165">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="73100-165">Az.RedisCache</span></span>
* <span data-ttu-id="73100-166">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="73100-166">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="73100-167">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73100-167">Az.Resources</span></span>
* <span data-ttu-id="73100-168">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="73100-168">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="73100-169">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73100-169">Az.Sql</span></span>
* <span data-ttu-id="73100-170">Cserélje le a függőségi figyelő SDK közös kód</span><span class="sxs-lookup"><span data-stu-id="73100-170">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="73100-171">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="73100-171">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="73100-172">Továbbfejlesztett folyamat, amely több oszlop osztályozási.</span><span class="sxs-lookup"><span data-stu-id="73100-172">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="73100-173">Termékváltozat tulajdonságok (termékváltozat neve, családi, kapacitás) válasz a Get-AzSqlServerServiceObjective és formátum táblaként alapértelmezés szerint tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="73100-173">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="73100-174">Lehetővé teszi a Get-AzSqlServerServiceObjective anélkül, hogy a régióban egy már létező kiszolgáló hely alapján.</span><span class="sxs-lookup"><span data-stu-id="73100-174">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="73100-175">Hozzon létre felügyelt példányt az időzóna-paraméter támogatása.</span><span class="sxs-lookup"><span data-stu-id="73100-175">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="73100-176">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="73100-176">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73100-177">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73100-177">Az.Websites</span></span>
* <span data-ttu-id="73100-178">a Set-AzWebApp és a Set-AzWebAppSlot távolítja el a címkék a végrehajtási javítások</span><span class="sxs-lookup"><span data-stu-id="73100-178">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="73100-179">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="73100-179">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="73100-180">A webhelyek SDK frissítése.</span><span class="sxs-lookup"><span data-stu-id="73100-180">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="73100-181">A AdminSiteName tulajdonság PSAppServicePlan eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="73100-181">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="73100-182">1.7.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="73100-182">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="73100-183">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="73100-183">Highlights since the last major release</span></span>
* <span data-ttu-id="73100-184">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="73100-184">General availability of `Az` module</span></span>
* <span data-ttu-id="73100-185">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="73100-185">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="73100-186">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="73100-186">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="73100-187">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="73100-187">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="73100-188">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="73100-188">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="73100-189">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="73100-189">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="73100-190">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="73100-190">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="73100-191">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73100-191">Az.Accounts</span></span>
* <span data-ttu-id="73100-192">Frissített Add-AzEnvironment és Set-AzEnvironment parancsmag az AzureAnalysisServicesEndpointResourceId paraméter elfogadásához</span><span class="sxs-lookup"><span data-stu-id="73100-192">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="73100-193">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="73100-193">Az.AnalysisServices</span></span>
* <span data-ttu-id="73100-194">ServiceClient használata DataPlane-parancsmagokban és az eredeti hitelesítési logika eltávolítása</span><span class="sxs-lookup"><span data-stu-id="73100-194">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="73100-195">Az Add-AzureASAccount burkolóként való megadása a Connect-AzAccount számára a kompatibilitástörő változás elkerüléséhez</span><span class="sxs-lookup"><span data-stu-id="73100-195">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="73100-196">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73100-196">Az.Automation</span></span>
* <span data-ttu-id="73100-197">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag belefoglalásokat érintő hibája.</span><span class="sxs-lookup"><span data-stu-id="73100-197">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="73100-198">Az IncludedKbNumber és az IncludedPackageNameMask paraméter mostantól működőképes.</span><span class="sxs-lookup"><span data-stu-id="73100-198">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="73100-199">Hibajavítás az Azure Automation frissítéskezelési dinamikus csoportja esetében</span><span class="sxs-lookup"><span data-stu-id="73100-199">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73100-200">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73100-200">Az.Compute</span></span>
* <span data-ttu-id="73100-201">HyperVGeneration paraméter hozzáadása a New-AzDiskConfig és a New-AzSnapshotConfig parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="73100-201">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="73100-202">Virtuális gépek más bérlők katalógus-rendszerképével való létrehozásának engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="73100-202">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="73100-203">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="73100-203">Az.ContainerInstance</span></span>
* <span data-ttu-id="73100-204">Ki lett javítva a New-AzContainerGroup üres záró argumentumot hozzáadó -Command paraméterével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="73100-204">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73100-205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73100-205">Az.DataFactory</span></span>
* <span data-ttu-id="73100-206">Az ADF .Net SDK verziója 3.0.2-re frissült.</span><span class="sxs-lookup"><span data-stu-id="73100-206">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="73100-207">A Set-AzDataFactoryV2 parancsmag a RepoConfiguration beállításaihoz tartozó kiegészítő paraméterekkel lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="73100-207">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="73100-208">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73100-208">Az.Resources</span></span>
* <span data-ttu-id="73100-209">Továbbfejlesztett szolgáltatókezelés a Get-AzResource esetében, -ResourceId vagy -ResourceGroupName, -Name és -ResourceType paraméterek megadásakor</span><span class="sxs-lookup"><span data-stu-id="73100-209">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="73100-210">Továbbfejlesztett hibakezelés a Test-AzDeployment és a Test-AzResourceGroupDeployment esetében</span><span class="sxs-lookup"><span data-stu-id="73100-210">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="73100-211">A hibákat nem a telepítés ellenőrzése során kezeli, hanem a parancs kimenetébe foglalja bele</span><span class="sxs-lookup"><span data-stu-id="73100-211">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="73100-212">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="73100-212">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="73100-213">-IgnoreDynamicParameters kapcsolóparaméter hozzáadása telepítési parancsmagokhoz a rendszer által feltett kérdések szkriptekben és feladatokban való mellőzéséhez</span><span class="sxs-lookup"><span data-stu-id="73100-213">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="73100-214">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="73100-214">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="73100-215">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73100-215">Az.Sql</span></span>
* <span data-ttu-id="73100-216">Adatbázisadat-besorolás támogatása.</span><span class="sxs-lookup"><span data-stu-id="73100-216">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73100-217">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73100-217">Az.Storage</span></span>
* <span data-ttu-id="73100-218">Részletes hibaüzenet megjelenítése Storage-környezet -UseConnectedAccount paraméterrel történő létrehozásakor az Azure-fiókba való bejelentkezés nélkül</span><span class="sxs-lookup"><span data-stu-id="73100-218">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="73100-219">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="73100-219">New-AzStorageContext</span></span>
* <span data-ttu-id="73100-220">Adott Storage-fiók Blob service-tulajdonságai kezelésének támogatása Management plane API-val</span><span class="sxs-lookup"><span data-stu-id="73100-220">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="73100-221">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="73100-221">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="73100-222">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="73100-222">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="73100-223">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="73100-223">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="73100-224">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="73100-224">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="73100-225">Az -AsJob támogatása blobok és fájlok feltöltéséhez, valamint parancsmagok letöltéséhez</span><span class="sxs-lookup"><span data-stu-id="73100-225">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="73100-226">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="73100-226">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="73100-227">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="73100-227">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="73100-228">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="73100-228">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="73100-229">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="73100-229">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="73100-230">1.6.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="73100-230">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="73100-231">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="73100-231">Highlights since the last major release</span></span>
* <span data-ttu-id="73100-232">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="73100-232">General availability of `Az` module</span></span>
* <span data-ttu-id="73100-233">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="73100-233">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="73100-234">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="73100-234">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="73100-235">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="73100-235">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="73100-236">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="73100-236">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="73100-237">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="73100-237">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="73100-238">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="73100-238">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="73100-239">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73100-239">Az.Automation</span></span>
* <span data-ttu-id="73100-240">Az Azure Automation frissítéskezelése módosult, hogy támogassa az alábbi új funkciókat:</span><span class="sxs-lookup"><span data-stu-id="73100-240">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="73100-241">Dinamikus csoportosítás</span><span class="sxs-lookup"><span data-stu-id="73100-241">Dynamic grouping</span></span>
    * <span data-ttu-id="73100-242">Előzetesen és utólagosan futtatandó szkriptek</span><span class="sxs-lookup"><span data-stu-id="73100-242">Pre-Post script</span></span>
    * <span data-ttu-id="73100-243">Újraindítási beállítás</span><span class="sxs-lookup"><span data-stu-id="73100-243">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73100-244">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73100-244">Az.Compute</span></span>
* <span data-ttu-id="73100-245">Ki lett javítva az elérési útvonal feloldásával kapcsolatos hiba a Get-AzVmBootDiagnosticsData esetében</span><span class="sxs-lookup"><span data-stu-id="73100-245">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="73100-246">A Compute ügyfélkódtár frissült a 25.0.0 verzióra</span><span class="sxs-lookup"><span data-stu-id="73100-246">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="73100-247">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73100-247">Az.KeyVault</span></span>
* <span data-ttu-id="73100-248">Helyettesítő karakterek támogatásának hozzáadása a KeyVault-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="73100-248">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73100-249">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73100-249">Az.Network</span></span>
* <span data-ttu-id="73100-250">Az Intelligens veszélyforrás-felderítés támogatásának hozzáadása az Azure Firewallhoz</span><span class="sxs-lookup"><span data-stu-id="73100-250">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="73100-251">Az Application Gateway-tűzfalszabályzat legfelső szintű erőforrása és egyéni szabályok hozzáadva</span><span class="sxs-lookup"><span data-stu-id="73100-251">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73100-252">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73100-252">Az.RecoveryServices</span></span>
* <span data-ttu-id="73100-253">A SnapshotRetentionInDays hozzáadása az Azure-beli virtuális gépek szabályzatához az azonnali RP támogatása érdekében</span><span class="sxs-lookup"><span data-stu-id="73100-253">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="73100-254">Folyamat támogatásának hozzáadása a regisztrációtörlési tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="73100-254">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="73100-255">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73100-255">Az.Resources</span></span>
* <span data-ttu-id="73100-256">Helyettesítő karakterek támogatásának hozzáadása a Get-AzResource és Get-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="73100-256">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="73100-257">Az ARM általános hívása esetén használt hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="73100-257">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="73100-258">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73100-258">Az.Sql</span></span>
* <span data-ttu-id="73100-259">A Fenyegetésészlelés parancsmagjainak paramétere (ExcludeDetectionType) a DetectionType helyett string[] lett, hogy a jövőben is használható legyen az új DetectionType-ok hozzáadásakor, valamint az automatikus kitöltés támogatása érdekében.</span><span class="sxs-lookup"><span data-stu-id="73100-259">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73100-260">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73100-260">Az.Storage</span></span>
* <span data-ttu-id="73100-261">Tárfiók felügyeleti szabályzata lekérésének/beállításának/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="73100-261">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="73100-262">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="73100-262">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="73100-263">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="73100-263">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="73100-264">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="73100-264">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="73100-265">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="73100-265">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="73100-266">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="73100-266">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="73100-267">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="73100-267">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73100-268">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73100-268">Az.Websites</span></span>
* <span data-ttu-id="73100-269">Ki lett javítva az ARM-sablon azon hibája, amely miatt meghiúsul az összes tárolóhely a New-AzWebApp - IncludeSourceWebAppSlots használatával történő klónozása</span><span class="sxs-lookup"><span data-stu-id="73100-269">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="73100-270">1.5.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="73100-270">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73100-271">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73100-271">Az.Accounts</span></span>
* <span data-ttu-id="73100-272">A Register-AzModule parancs hozzáadása az AutoRest által létrehozott parancsmagok támogatásához</span><span class="sxs-lookup"><span data-stu-id="73100-272">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="73100-273">A Connect-AzAccount példáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="73100-273">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="73100-274">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73100-274">Az.Automation</span></span>
* <span data-ttu-id="73100-275">A bizonyos havi ütemezések lekérésekor jelentkező hiba kijavítva számos Azure Automation-parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="73100-275">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="73100-276">Ki lett javítva a hiba, amely miatt a Get-AzAutomationDscNode csak az első 20 csomópontot adta vissza.</span><span class="sxs-lookup"><span data-stu-id="73100-276">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="73100-277">Most már az összes csomópontot visszaadja</span><span class="sxs-lookup"><span data-stu-id="73100-277">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="73100-278">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="73100-278">Az.Cdn</span></span>
* <span data-ttu-id="73100-279">Új Powershell-parancsmagok hozzáadva az Egyéni tartományi Https engedélyezése/letiltása szolgáltatáshoz, a régiek elavultak</span><span class="sxs-lookup"><span data-stu-id="73100-279">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73100-280">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73100-280">Az.Compute</span></span>
* <span data-ttu-id="73100-281">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="73100-281">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73100-282">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73100-282">Az.DataFactory</span></span>
* <span data-ttu-id="73100-283">Az ADF .Net SDK verziója 3.0.1-re frissült</span><span class="sxs-lookup"><span data-stu-id="73100-283">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="73100-284">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="73100-284">Az.LogicApp</span></span>
* <span data-ttu-id="73100-285">Ki lett javítva a hiba, amely miatt a ListWorkflows csak az eredmények első oldalát kérte le</span><span class="sxs-lookup"><span data-stu-id="73100-285">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73100-286">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73100-286">Az.Network</span></span>
* <span data-ttu-id="73100-287">Helyettesítő karakterek támogatásának hozzáadása a Network-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="73100-287">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73100-288">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73100-288">Az.RecoveryServices</span></span>
* <span data-ttu-id="73100-289">Azure-beli virtuális gépen futtatott SQL Server támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="73100-289">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="73100-290">SDK-frissítés</span><span class="sxs-lookup"><span data-stu-id="73100-290">SDK Update</span></span>
* <span data-ttu-id="73100-291">VMappContainer ellenőrzés eltávolítva a Get-ProtectableItem parancsmagból</span><span class="sxs-lookup"><span data-stu-id="73100-291">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="73100-292">Name és ServerName paraméterek hozzáadva a Get-ProtectableItem parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="73100-292">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="73100-293">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73100-293">Az.Resources</span></span>
* <span data-ttu-id="73100-294">`-TemplateObject` paraméter hozzáadva az üzembe helyező parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="73100-294">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="73100-295">További információ: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="73100-295">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="73100-296">Ki lett javítva a hiba, amely akkor jelentkezett, amikor a(z) `Get-AzResource` eredménye át lett irányítva a következőbe: `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="73100-296">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="73100-297">További információ: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="73100-297">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="73100-298">Ki lett javítva a JSON-adattípus módosításával kapcsolatos probléma, amely a(z) `Set-AzResource` futtatásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="73100-298">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="73100-299">További információ: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="73100-299">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="73100-300">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73100-300">Az.Sql</span></span>
* <span data-ttu-id="73100-301">Az AuditingEndpointsCommunicator frissítése.</span><span class="sxs-lookup"><span data-stu-id="73100-301">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="73100-302">Ki lett javítva az új diagnosztikai beállítások létrehozásakor jelentkező ritka eset viselkedése.</span><span class="sxs-lookup"><span data-stu-id="73100-302">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73100-303">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73100-303">Az.Storage</span></span>
* <span data-ttu-id="73100-304">A BlockBlobStorage altípus támogatása a Storage-fiók létrehozásakor      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73100-304">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="73100-305">1.4.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="73100-305">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="73100-306">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="73100-306">Az.AnalysisServices</span></span>
* <span data-ttu-id="73100-307">Az AddAzureASAccount parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="73100-307">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="73100-308">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73100-308">Az.Automation</span></span>
* <span data-ttu-id="73100-309">Az Import-AzAutomationDscNodeConfiguration súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="73100-309">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="73100-310">A konfigurációnév-ellenőrzés hozzáadva az Import-AzAutomationDscConfiguration parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="73100-310">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="73100-311">Továbbfejlesztett hibakezelés az Import-AzAutomationDscConfiguration parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="73100-311">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="73100-312">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="73100-312">Az.CognitiveServices</span></span>
* <span data-ttu-id="73100-313">A CustomSubdomainName új választható paraméterként hozzáadva a New-AzCognitiveServicesAccount parancsmaghoz, amellyel altartomány adható meg az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="73100-313">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73100-314">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73100-314">Az.Compute</span></span>
* <span data-ttu-id="73100-315">Kijavítva az azonosító paraméterkészleteivel kapcsolatos probléma</span><span class="sxs-lookup"><span data-stu-id="73100-315">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="73100-316">Frissült a Get-AzVMExtension parancsmag, hogy az összes telepített bővítményt listázza, ha a Name paraméter nincs megadva</span><span class="sxs-lookup"><span data-stu-id="73100-316">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="73100-317">A Tag és a ResourceId paraméterek hozzáadva az Update-AzImage parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="73100-317">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="73100-318">A Get-AzVmssVM példányazonosító nélkül, az InstanceView használatával példánynézetben listázni tudja a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="73100-318">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73100-319">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73100-319">Az.DataLakeStore</span></span>
* <span data-ttu-id="73100-320">Parancsmagok hozzáadása a törölt ADL-elemek enumerálásához és visszaállításához</span><span class="sxs-lookup"><span data-stu-id="73100-320">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="73100-321">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="73100-321">Az.EventHub</span></span>
* <span data-ttu-id="73100-322">Új SkipEmptyArchives logikai tulajdonság hozzáadva az üres archívumok kihagyásához az Eventhub CaptureDescription osztályában</span><span class="sxs-lookup"><span data-stu-id="73100-322">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="73100-323">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73100-323">Az.KeyVault</span></span>
* <span data-ttu-id="73100-324">A Set-AzKeyVaultSecret címkézésének kijavítása</span><span class="sxs-lookup"><span data-stu-id="73100-324">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="73100-325">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="73100-325">Az.LogicApp</span></span>
* <span data-ttu-id="73100-326">Hozzáadva az integrációs fiókok alapszintű termékváltozatában</span><span class="sxs-lookup"><span data-stu-id="73100-326">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="73100-327">Hozzáadva az XSLT 2.0-ban, az XSLT 3.0-ban és a Liquid leképezéstípusok esetén</span><span class="sxs-lookup"><span data-stu-id="73100-327">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="73100-328">Új parancsmagok az integrációs fiók szerelvényeihez</span><span class="sxs-lookup"><span data-stu-id="73100-328">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="73100-329">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="73100-329">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="73100-330">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="73100-330">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="73100-331">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="73100-331">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="73100-332">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="73100-332">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="73100-333">Új parancsmagok az integrációs fiók kötegkonfigurációjához</span><span class="sxs-lookup"><span data-stu-id="73100-333">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="73100-334">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="73100-334">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="73100-335">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="73100-335">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="73100-336">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="73100-336">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="73100-337">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="73100-337">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="73100-338">A Logic Apps SDK frissítése a 4.1.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="73100-338">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="73100-339">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73100-339">Az.Monitor</span></span>
* <span data-ttu-id="73100-340">A Get-AzMetric súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="73100-340">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73100-341">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73100-341">Az.Network</span></span>
* <span data-ttu-id="73100-342">Az Add-AzApplicationGatewayCustomError súgójában lévő példa frissítése</span><span class="sxs-lookup"><span data-stu-id="73100-342">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="73100-343">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="73100-343">Az.OperationalInsights</span></span>
* <span data-ttu-id="73100-344">Kibővített támogatás a New és a Get ApplicationInsights adatforráshoz.</span><span class="sxs-lookup"><span data-stu-id="73100-344">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="73100-345">Új „ApplicationInsights” altípus hozzáadva az adott munkaterület Get specific és Get all Application Insights-adatforrásainak támogatásához.</span><span class="sxs-lookup"><span data-stu-id="73100-345">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="73100-346">A New-AzOperationalInsightsApplicationInsightsDataSource parancsmag hozzáadva adatforrás létrehozásához a következő Application Insights-erőforrásparaméterekkel: subscriptionId, resourceGroupName és name.</span><span class="sxs-lookup"><span data-stu-id="73100-346">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="73100-347">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73100-347">Az.Resources</span></span>
* <span data-ttu-id="73100-348">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="73100-348">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="73100-349">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="73100-349">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="73100-350">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="73100-350">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="73100-351">Ki lett javítva a KeyCredentials ismételt létrehozását megakadályozó hiba</span><span class="sxs-lookup"><span data-stu-id="73100-351">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="73100-352">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73100-352">Az.Sql</span></span>
* <span data-ttu-id="73100-353">Rugalmas SQL DB-skálázási szint támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="73100-353">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="73100-354">Ki lett javítva az a hiba, hogy a visszaállítási kérésben szereplő szükségtelen tulajdonságok megadása miatt a visszaállítás esetenként meghiúsult</span><span class="sxs-lookup"><span data-stu-id="73100-354">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73100-355">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73100-355">Az.Websites</span></span>
* <span data-ttu-id="73100-356">A Get-AzWebAppSlotMetrics példájának javítása</span><span class="sxs-lookup"><span data-stu-id="73100-356">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="73100-357">1.3.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="73100-357">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73100-358">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73100-358">Az.Accounts</span></span>
* <span data-ttu-id="73100-359">Frissítés a ClientRuntime legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="73100-359">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="73100-360">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="73100-360">Az.AnalysisServices</span></span>
<span data-ttu-id="73100-361">Az Az.AnalysisServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="73100-361">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73100-362">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73100-362">Az.Compute</span></span>
* <span data-ttu-id="73100-363">AEM-bővítmény: Mostantól az UltraSSD, valamint a P60, P70 és P80 lemezek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="73100-363">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="73100-364">A Set-AzVMBootDiagnostics súgóleírása frissült.</span><span class="sxs-lookup"><span data-stu-id="73100-364">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="73100-365">Az Update-AzImage súgóleírása és példája frissült.</span><span class="sxs-lookup"><span data-stu-id="73100-365">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73100-366">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73100-366">Az.RecoveryServices</span></span>
<span data-ttu-id="73100-367">Az Az.RecoveryServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="73100-367">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="73100-368">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73100-368">Az.Resources</span></span>
* <span data-ttu-id="73100-369">Az erőforráscsoportok címkézése ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="73100-369">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="73100-370">További információ: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="73100-370">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="73100-371">Ki lett javítva az a hiba, amikor a `Get-AzureRmRoleAssignment` nem vette figyelembe az -ErrorAction paramétert.</span><span class="sxs-lookup"><span data-stu-id="73100-371">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="73100-372">További információ: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="73100-372">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="73100-373">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73100-373">Az.Sql</span></span>
* <span data-ttu-id="73100-374">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hozzáadva</span><span class="sxs-lookup"><span data-stu-id="73100-374">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="73100-375">Ki lett javítva az a hiba, amikor az Azure-fiókba való bejelentkezés hiánya nullref kivételt eredményezett az SQL-parancsmagok végrehajtásakor.</span><span class="sxs-lookup"><span data-stu-id="73100-375">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="73100-376">A nullref kivétel ki lett javítva a Get-AzSqlCapabilityben.</span><span class="sxs-lookup"><span data-stu-id="73100-376">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="73100-377">1.2.1 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="73100-377">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73100-378">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73100-378">Az.Accounts</span></span>
* <span data-ttu-id="73100-379">A hitelesítés megfelelő verziójával rendelkező kiadás</span><span class="sxs-lookup"><span data-stu-id="73100-379">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="73100-380">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="73100-380">Az.AnalysisServices</span></span>
* <span data-ttu-id="73100-381">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="73100-381">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="73100-382">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73100-382">Az.RecoveryServices</span></span>
* <span data-ttu-id="73100-383">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="73100-383">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="73100-384">1.2.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="73100-384">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73100-385">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73100-385">Az.Accounts</span></span>
* <span data-ttu-id="73100-386">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="73100-386">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="73100-387">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="73100-387">Update incorrect online help URLs</span></span>
* <span data-ttu-id="73100-388">Az Uninstall-AzureRm figyelmeztető üzenete hozzáadva a PS Core-ban</span><span class="sxs-lookup"><span data-stu-id="73100-388">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="73100-389">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="73100-389">Az.Aks</span></span>
* <span data-ttu-id="73100-390">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="73100-390">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="73100-391">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73100-391">Az.Automation</span></span>
* <span data-ttu-id="73100-392">Mostantól támogatottak a Python 2-runbookok.</span><span class="sxs-lookup"><span data-stu-id="73100-392">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="73100-393">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="73100-393">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="73100-394">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="73100-394">Az.Cdn</span></span>
* <span data-ttu-id="73100-395">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="73100-395">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73100-396">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73100-396">Az.Compute</span></span>
* <span data-ttu-id="73100-397">Az Invoke-AzVMReimage parancsmag hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="73100-397">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="73100-398">A TempDisk paraméter hozzá lett adva a Set-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="73100-398">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="73100-399">A New-AzVM figyelmeztető üzenete ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="73100-399">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="73100-400">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="73100-400">Az.ContainerRegistry</span></span>
* <span data-ttu-id="73100-401">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="73100-401">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="73100-402">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="73100-402">Az.DataFactory</span></span>
* <span data-ttu-id="73100-403">Az ADF .Net SDK verziója 3.0.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="73100-403">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73100-404">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73100-404">Az.DataLakeStore</span></span>
* <span data-ttu-id="73100-405">Ki lett javítva az ADLS-végponttal kapcsolatos probléma az MSI használatakor.</span><span class="sxs-lookup"><span data-stu-id="73100-405">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="73100-406">További információ: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="73100-406">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="73100-407">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="73100-407">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="73100-408">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="73100-408">Az.IotHub</span></span>
* <span data-ttu-id="73100-409">Az Encoding formátum hozzá lett adva az Add-IotHubRoutingEndpoint parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="73100-409">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="73100-410">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73100-410">Az.KeyVault</span></span>
* <span data-ttu-id="73100-411">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="73100-411">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73100-412">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73100-412">Az.Network</span></span>
* <span data-ttu-id="73100-413">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="73100-413">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="73100-414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73100-414">Az.Resources</span></span>
* <span data-ttu-id="73100-415">A helytelen példák ki lettek javítva a New-AzADAppCredential és a New-AzADSpCredential referenciadokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="73100-415">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="73100-416">Ki lett javítva az a hiba, amikor a -TemplateFile paraméter nem lett feloldva az erőforráscsoportokat üzembe helyező parancsmagok végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="73100-416">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="73100-417">Az.Resources: A New-AzureRmPolicyDefinition -Mode alapértelmezett értékének dokumentációja ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="73100-417">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="73100-418">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="73100-418">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="73100-419">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="73100-419">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="73100-420">Ki lett javítva a „PSResourceGroupDeployment” objektum formázásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="73100-420">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="73100-421">További információ: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="73100-421">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="73100-422">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="73100-422">Az.ServiceFabric</span></span>
* <span data-ttu-id="73100-423">Visszaállítás a VMSS-modell tanúsítványának hozzáadásakor bekövetkező kivétel-visszaadás esetén; javított hiba: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="73100-423">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="73100-424">Bizonyos hibaüzenetek ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="73100-424">Fix some error messages.</span></span>
* <span data-ttu-id="73100-425">Ki lett javítva az alapértelmezett ARM-sablonnal való fürtlétrehozás a New-AzServiceFabriCluster esetében, amely nem működött az Az-ba történő migrálással.</span><span class="sxs-lookup"><span data-stu-id="73100-425">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="73100-426">Ki lett javítva a fürt-/alkalmazástanúsítvány létrehozása, így mostantól csak a fürtnek megfelelő virtuálisgép-méretezési csoportokhoz (Virtual Machine Scale Sets) lesznek hozzáadva, a fürtazonosító bővítményben való ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="73100-426">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="73100-427">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="73100-427">Az.SignalR</span></span>
* <span data-ttu-id="73100-428">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="73100-428">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="73100-429">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73100-429">Az.Sql</span></span>
* <span data-ttu-id="73100-430">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="73100-430">Update incorrect online help URLs</span></span>
* <span data-ttu-id="73100-431">A LicenseType paraméter paraméterleírása frissítve lett a lehetséges értékekkel.</span><span class="sxs-lookup"><span data-stu-id="73100-431">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="73100-432">Ki lett javítva az a hiba, amikor egy felügyelt példány identitásának frissítése nem működött, ha az volt az egyetlen frissített tulajdonság.</span><span class="sxs-lookup"><span data-stu-id="73100-432">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="73100-433">Egyéni rendezések támogatása a felügyelt példányokon</span><span class="sxs-lookup"><span data-stu-id="73100-433">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73100-434">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73100-434">Az.Storage</span></span>
* <span data-ttu-id="73100-435">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="73100-435">Update incorrect online help URLs</span></span>
* <span data-ttu-id="73100-436">Részletes hibaüzenet megjelenítése klasszikus naplózás/metrika get/set műveletei esetében a prémium szintű Storage-fiókon, mivel a prémium szintű Storage-fiók nem támogatja a klasszikus naplózást/metrikát.</span><span class="sxs-lookup"><span data-stu-id="73100-436">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="73100-437">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="73100-437">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="73100-438">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="73100-438">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="73100-439">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="73100-439">Az.TrafficManager</span></span>
* <span data-ttu-id="73100-440">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="73100-440">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73100-441">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73100-441">Az.Websites</span></span>
* <span data-ttu-id="73100-442">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="73100-442">Update incorrect online help URLs</span></span>
* <span data-ttu-id="73100-443">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól a megfelelő erőforráscsoportba és helyre tölti fel a tanúsítványt, ha az alkalmazás ASE-n üzemel.</span><span class="sxs-lookup"><span data-stu-id="73100-443">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="73100-444">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól nem írja felül a címkéket SSL-tanúsítvány alkalmazáshoz való kötésekor.</span><span class="sxs-lookup"><span data-stu-id="73100-444">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="73100-445">1.1.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="73100-445">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="73100-446">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73100-446">Az.Accounts</span></span>
* <span data-ttu-id="73100-447">A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz</span><span class="sxs-lookup"><span data-stu-id="73100-447">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73100-448">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73100-448">Az.Compute</span></span>
* <span data-ttu-id="73100-449">A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni</span><span class="sxs-lookup"><span data-stu-id="73100-449">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="73100-450">Frissült az azonosító leírása a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="73100-450">Updated the description of ID in help files</span></span>
* <span data-ttu-id="73100-451">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="73100-451">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73100-452">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73100-452">Az.DataLakeStore</span></span>
* <span data-ttu-id="73100-453">A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.</span><span class="sxs-lookup"><span data-stu-id="73100-453">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="73100-454">A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva</span><span class="sxs-lookup"><span data-stu-id="73100-454">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="73100-455">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="73100-455">Az.EventGrid</span></span>
* <span data-ttu-id="73100-456">Frissítve a 2019-01-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="73100-456">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="73100-457">A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához</span><span class="sxs-lookup"><span data-stu-id="73100-457">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="73100-458">New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="73100-458">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="73100-459">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="73100-459">Event Time-To-Live,</span></span>
        - <span data-ttu-id="73100-460">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="73100-460">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="73100-461">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="73100-461">Dead letter endpoint.</span></span>
    - <span data-ttu-id="73100-462">Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="73100-462">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="73100-463">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="73100-463">Event Time-To-Live,</span></span>
        - <span data-ttu-id="73100-464">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="73100-464">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="73100-465">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="73100-465">Dead letter endpoint.</span></span>
* <span data-ttu-id="73100-466">Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.</span><span class="sxs-lookup"><span data-stu-id="73100-466">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="73100-467">Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.</span><span class="sxs-lookup"><span data-stu-id="73100-467">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="73100-468">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="73100-468">Az.IotHub</span></span>
* <span data-ttu-id="73100-469">Frissítve az IoT Hub SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="73100-469">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="73100-470">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="73100-470">Az.LogicApp</span></span>
* <span data-ttu-id="73100-471">A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel</span><span class="sxs-lookup"><span data-stu-id="73100-471">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="73100-472">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73100-472">Az.Resources</span></span>
* <span data-ttu-id="73100-473">Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="73100-473">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="73100-474">További információ: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="73100-474">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="73100-475">Ki lett javítva a -Custom paraméter kezelése a New/Set-AzPolicyDefinition parancsban</span><span class="sxs-lookup"><span data-stu-id="73100-475">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="73100-476">Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="73100-476">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="73100-477">A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében</span><span class="sxs-lookup"><span data-stu-id="73100-477">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="73100-478">További információ: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="73100-478">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="73100-479">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="73100-479">Az.SignalR</span></span>
* <span data-ttu-id="73100-480">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="73100-480">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="73100-481">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73100-481">Az.Sql</span></span>
* <span data-ttu-id="73100-482">A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.</span><span class="sxs-lookup"><span data-stu-id="73100-482">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="73100-483">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73100-483">Az.Storage</span></span>
* <span data-ttu-id="73100-484">A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva</span><span class="sxs-lookup"><span data-stu-id="73100-484">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="73100-485">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="73100-485">New-AzStorageContext</span></span>
* <span data-ttu-id="73100-486">A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz</span><span class="sxs-lookup"><span data-stu-id="73100-486">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="73100-487">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="73100-487">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73100-488">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73100-488">Az.Websites</span></span>
* <span data-ttu-id="73100-489">Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban</span><span class="sxs-lookup"><span data-stu-id="73100-489">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="73100-490">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="73100-490">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="73100-491">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="73100-491">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="73100-492">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="73100-492">General</span></span>

- <span data-ttu-id="73100-493">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="73100-493">General Availability of Az Module</span></span>
- <span data-ttu-id="73100-494">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="73100-494">Online help for each module</span></span>
- <span data-ttu-id="73100-495">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="73100-495">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="73100-496">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="73100-496">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="73100-497">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73100-497">Az.Accounts</span></span>
- <span data-ttu-id="73100-498">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="73100-498">Changed from Az.Profile</span></span>
- <span data-ttu-id="73100-499">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="73100-499">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="73100-500">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73100-500">Az.ApiManagement</span></span>
- <span data-ttu-id="73100-501">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="73100-501">Fixes for #7002</span></span>
- <span data-ttu-id="73100-502">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="73100-502">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="73100-503">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="73100-503">Az.Batch</span></span>
- <span data-ttu-id="73100-504">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="73100-504">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="73100-505">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="73100-505">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="73100-506">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="73100-506">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="73100-507">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="73100-507">Az.Billing</span></span>
- <span data-ttu-id="73100-508">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="73100-508">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="73100-509">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="73100-509">Az.CognitivServices</span></span>
- <span data-ttu-id="73100-510">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="73100-510">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="73100-511">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="73100-511">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="73100-512">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="73100-512">Az.ContainerInstance</span></span>
- <span data-ttu-id="73100-513">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="73100-513">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="73100-514">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="73100-514">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="73100-515">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="73100-515">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="73100-516">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73100-516">Az.DataLakeStore</span></span>
- <span data-ttu-id="73100-517">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="73100-517">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="73100-518">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="73100-518">Az.Monitor</span></span>
- <span data-ttu-id="73100-519">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="73100-519">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="73100-520">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="73100-520">Az.KeyVault</span></span>
- <span data-ttu-id="73100-521">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="73100-521">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="73100-522">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="73100-522">Az.MachineLearning</span></span>
- <span data-ttu-id="73100-523">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="73100-523">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="73100-524">Az.Media</span><span class="sxs-lookup"><span data-stu-id="73100-524">Az.Media</span></span>
- <span data-ttu-id="73100-525">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="73100-525">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="73100-526">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73100-526">Az.Network</span></span>
<span data-ttu-id="73100-527">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="73100-527">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="73100-528">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="73100-528">New cmdlets added:</span></span>
        - <span data-ttu-id="73100-529">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="73100-529">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="73100-530">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="73100-530">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="73100-531">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="73100-531">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="73100-532">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="73100-532">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="73100-533">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="73100-533">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="73100-534">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="73100-534">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="73100-535">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="73100-535">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="73100-536">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="73100-536">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="73100-537">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="73100-537">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="73100-538">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73100-538">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="73100-539">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="73100-539">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="73100-540">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="73100-540">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="73100-541">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="73100-541">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="73100-542">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="73100-542">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="73100-543">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="73100-543">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="73100-544">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="73100-544">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="73100-545">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="73100-545">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="73100-546">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="73100-546">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="73100-547">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="73100-547">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="73100-548">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="73100-548">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="73100-549">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="73100-549">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="73100-550">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="73100-550">Az.OperationalInsights</span></span>
- <span data-ttu-id="73100-551">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="73100-551">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="73100-552">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="73100-552">Az.Profile</span></span>
- <span data-ttu-id="73100-553">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="73100-553">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="73100-554">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73100-554">Az.RecoveryServices</span></span>
- <span data-ttu-id="73100-555">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="73100-555">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="73100-556">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73100-556">Az.Resources</span></span>
- <span data-ttu-id="73100-557">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="73100-557">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="73100-558">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="73100-558">Az.ServiceFabric</span></span>
- <span data-ttu-id="73100-559">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="73100-559">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="73100-560">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="73100-560">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="73100-561">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="73100-561">Az.SIgnalR</span></span>
- <span data-ttu-id="73100-562">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="73100-562">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="73100-563">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73100-563">Az.Sql</span></span>
- <span data-ttu-id="73100-564">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="73100-564">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="73100-565">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="73100-565">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="73100-566">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="73100-566">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="73100-567">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73100-567">Az.Storage</span></span>
- <span data-ttu-id="73100-568">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="73100-568">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="73100-569">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73100-569">Az.Websites</span></span>
- <span data-ttu-id="73100-570">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="73100-570">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="73100-571">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="73100-571">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="73100-572">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="73100-572">General</span></span>

* <span data-ttu-id="73100-573">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="73100-573">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="73100-574">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73100-574">Az.Compute</span></span>

* <span data-ttu-id="73100-575">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="73100-575">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="73100-576">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73100-576">Az.DataLakeStore</span></span>

* <span data-ttu-id="73100-577">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="73100-577">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="73100-578">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="73100-578">Az.FrontDoor</span></span>

* <span data-ttu-id="73100-579">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="73100-579">Fixed some broken links</span></span>
    - <span data-ttu-id="73100-580">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="73100-580">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="73100-581">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="73100-581">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="73100-582">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="73100-582">Az.RecoveryServices</span></span>

* <span data-ttu-id="73100-583">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="73100-583">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="73100-584">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="73100-584">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="73100-585">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73100-585">Az.Resources</span></span>

* <span data-ttu-id="73100-586">[https://github.com/Azure/azure-powershell/issues/7679](https://github.com/Azure/azure-powershell/issues/7679 ) javítása</span><span class="sxs-lookup"><span data-stu-id="73100-586">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="73100-587">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="73100-587">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="73100-588">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73100-588">Az.Sql</span></span>

* <span data-ttu-id="73100-589">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="73100-589">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="73100-590">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="73100-590">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="73100-591">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="73100-591">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="73100-592">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="73100-592">Az.Storage</span></span>

* <span data-ttu-id="73100-593">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="73100-593">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="73100-594">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="73100-594">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="73100-595">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="73100-595">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="73100-596">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="73100-596">Support Static Website configuration</span></span>
    - <span data-ttu-id="73100-597">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="73100-597">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="73100-598">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="73100-598">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="73100-599">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73100-599">Az.Websites</span></span>

* <span data-ttu-id="73100-600">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="73100-600">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="73100-601">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="73100-601">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="73100-602">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="73100-602">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="73100-603">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="73100-603">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="73100-604">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73100-604">Az.ApiManagement</span></span>
* <span data-ttu-id="73100-605">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="73100-605">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="73100-606">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="73100-606">Az.Automation</span></span>
* <span data-ttu-id="73100-607">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="73100-607">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="73100-608">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="73100-608">Added Update Management cmdlets</span></span>
* <span data-ttu-id="73100-609">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="73100-609">Added Source Control cmdlets</span></span>
* <span data-ttu-id="73100-610">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="73100-610">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="73100-611">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="73100-611">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="73100-612">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73100-612">Az.Compute</span></span>
* <span data-ttu-id="73100-613">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="73100-613">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="73100-614">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="73100-614">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="73100-615">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="73100-615">Az.ContainerInstance</span></span>
* <span data-ttu-id="73100-616">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="73100-616">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="73100-617">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="73100-617">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="73100-618">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="73100-618">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="73100-619">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73100-619">Az.Network</span></span>
* <span data-ttu-id="73100-620">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="73100-620">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="73100-621">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="73100-621">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="73100-622">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="73100-622">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="73100-623">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="73100-623">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="73100-624">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="73100-624">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="73100-625">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="73100-625">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="73100-626">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="73100-626">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="73100-627">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="73100-627">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="73100-628">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="73100-628">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="73100-629">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="73100-629">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="73100-630">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="73100-630">Az.Relay</span></span>
* <span data-ttu-id="73100-631">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="73100-631">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="73100-632">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73100-632">Az.Resources</span></span>
* <span data-ttu-id="73100-633">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="73100-633">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="73100-634">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="73100-634">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="73100-635">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="73100-635">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="73100-636">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="73100-636">Az.ServiceFabric</span></span>
* <span data-ttu-id="73100-637">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="73100-637">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="73100-638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73100-638">Az.Sql</span></span>
* <span data-ttu-id="73100-639">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="73100-639">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="73100-640">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="73100-640">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="73100-641">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="73100-641">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="73100-642">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="73100-642">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="73100-643">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="73100-643">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="73100-644">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="73100-644">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="73100-645">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="73100-645">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="73100-646">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="73100-646">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="73100-647">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="73100-647">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="73100-648">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="73100-648">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="73100-649">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="73100-649">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="73100-650">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="73100-650">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="73100-651">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="73100-651">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="73100-652">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="73100-652">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="73100-653">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="73100-653">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="73100-654">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="73100-654">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="73100-655">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="73100-655">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="73100-656">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="73100-656">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="73100-657">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="73100-657">General</span></span>
* <span data-ttu-id="73100-658">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="73100-658">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="73100-659">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="73100-659">Az.Profile</span></span>
* <span data-ttu-id="73100-660">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="73100-660">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="73100-661">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="73100-661">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="73100-662">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="73100-662">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="73100-663">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="73100-663">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="73100-664">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="73100-664">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="73100-665">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="73100-665">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="73100-666">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="73100-666">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="73100-667">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="73100-667">Az.CognitiveServices</span></span>
* <span data-ttu-id="73100-668">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="73100-668">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73100-669">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73100-669">Az.Compute</span></span>
* <span data-ttu-id="73100-670">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="73100-670">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="73100-671">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="73100-671">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="73100-672">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="73100-672">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73100-673">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73100-673">Az.DataLakeStore</span></span>
* <span data-ttu-id="73100-674">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="73100-674">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="73100-675">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="73100-675">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="73100-676">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="73100-676">Az.Insights</span></span>
* <span data-ttu-id="73100-677">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="73100-677">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="73100-678">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="73100-678">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="73100-679">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="73100-679">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="73100-680">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="73100-680">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73100-681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73100-681">Az.Network</span></span>
* <span data-ttu-id="73100-682">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="73100-682">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="73100-683">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="73100-683">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="73100-684">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="73100-684">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="73100-685">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="73100-685">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="73100-686">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="73100-686">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="73100-687">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="73100-687">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="73100-688">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="73100-688">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="73100-689">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="73100-689">Az.PolicyInsights</span></span>
* <span data-ttu-id="73100-690">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="73100-690">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="73100-691">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73100-691">Az.Resources</span></span>
* <span data-ttu-id="73100-692">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402 ) javítása</span><span class="sxs-lookup"><span data-stu-id="73100-692">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="73100-693">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="73100-693">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="73100-694">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="73100-694">Az.ServiceBus</span></span>
* <span data-ttu-id="73100-695">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="73100-695">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="73100-696">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="73100-696">Az.ServiceFabric</span></span>
* <span data-ttu-id="73100-697">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="73100-697">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="73100-698">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="73100-698">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="73100-699">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="73100-699">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="73100-700">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="73100-700">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="73100-701">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="73100-701">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="73100-702">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="73100-702">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="73100-703">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="73100-703">Az.Profile</span></span>
* <span data-ttu-id="73100-704">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="73100-704">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="73100-705">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="73100-705">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73100-706">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73100-706">Az.Compute</span></span>
* <span data-ttu-id="73100-707">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="73100-707">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="73100-708">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="73100-708">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="73100-709">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="73100-709">Az.DataLakeStore</span></span>
* <span data-ttu-id="73100-710">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="73100-710">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="73100-711">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="73100-711">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="73100-712">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="73100-712">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="73100-713">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="73100-713">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="73100-714">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="73100-714">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73100-715">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73100-715">Az.Network</span></span>
* <span data-ttu-id="73100-716">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="73100-716">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="73100-717">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="73100-717">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="73100-718">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73100-718">Az.Resources</span></span>
* <span data-ttu-id="73100-719">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="73100-719">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="73100-720">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="73100-720">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="73100-721">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="73100-721">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="73100-722">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="73100-722">Azure.Storage</span></span>
* <span data-ttu-id="73100-723">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="73100-723">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="73100-724">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="73100-724">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="73100-725">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="73100-725">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="73100-726">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="73100-726">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="73100-727">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="73100-727">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="73100-728">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="73100-728">Az.CognitiveServices</span></span>
* <span data-ttu-id="73100-729">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="73100-729">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="73100-730">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="73100-730">Az.Compute</span></span>
* <span data-ttu-id="73100-731">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="73100-731">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="73100-732">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="73100-732">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="73100-733">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="73100-733">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="73100-734">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="73100-734">Az.DataFactoryV2</span></span>
* <span data-ttu-id="73100-735">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="73100-735">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="73100-736">Az.Network</span><span class="sxs-lookup"><span data-stu-id="73100-736">Az.Network</span></span>
* <span data-ttu-id="73100-737">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="73100-737">Added NetworkProfile functionality.</span></span> <span data-ttu-id="73100-738">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="73100-738">new cmdlets added</span></span>
    - <span data-ttu-id="73100-739">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="73100-739">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="73100-740">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="73100-740">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="73100-741">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="73100-741">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="73100-742">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="73100-742">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="73100-743">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="73100-743">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="73100-744">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="73100-744">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="73100-745">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="73100-745">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="73100-746">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="73100-746">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="73100-747">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="73100-747">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="73100-748">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="73100-748">Az.RedisCache</span></span>
* <span data-ttu-id="73100-749">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="73100-749">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="73100-750">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="73100-750">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="73100-751">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="73100-751">Az.Resources</span></span>
* <span data-ttu-id="73100-752">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="73100-752">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="73100-753">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="73100-753">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="73100-754">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="73100-754">Az.Sql</span></span>
* <span data-ttu-id="73100-755">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="73100-755">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="73100-756">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="73100-756">Az.Websites</span></span>
* <span data-ttu-id="73100-757">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="73100-757">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="73100-758">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="73100-758">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="73100-759">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="73100-759">0.2.0 - September 2018</span></span>
 <span data-ttu-id="73100-760">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="73100-760">Initial Release</span></span>
