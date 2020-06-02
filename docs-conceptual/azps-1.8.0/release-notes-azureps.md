---
title: Az Azure PowerShell kibocsátási megjegyzései
description: Megismerheti az Azure PowerShell-modulok legújabb frissítéseit.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/30/2019
ms.openlocfilehash: 34b21292ccc47bb53b6609cd637ef18338a45cd3
ms.sourcegitcommit: 9f5c7d231b069ad501729bf015a829f3fe89bc6a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/28/2020
ms.locfileid: "84121454"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="3a667-103">Az Azure PowerShell kibocsátási megjegyzései</span><span class="sxs-lookup"><span data-stu-id="3a667-103">Azure PowerShell release notes</span></span>
## <a name="180---april-2019"></a><span data-ttu-id="3a667-104">1.8.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="3a667-104">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="3a667-105">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="3a667-105">Highlights since the last major release</span></span>
* <span data-ttu-id="3a667-106">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="3a667-106">General availability of `Az` module</span></span>
* <span data-ttu-id="3a667-107">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="3a667-107">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="3a667-108">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="3a667-108">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="3a667-109">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="3a667-109">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="3a667-110">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="3a667-110">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="3a667-111">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="3a667-111">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="3a667-112">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="3a667-112">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3a667-113">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a667-113">Az.Accounts</span></span>
* <span data-ttu-id="3a667-114">Eltávolítás-AzureRm megfelelően törölni a Mac modulok frissítése</span><span class="sxs-lookup"><span data-stu-id="3a667-114">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="3a667-115">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3a667-115">Az.Batch</span></span>
* <span data-ttu-id="3a667-116">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3a667-116">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="3a667-117">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3a667-117">Az.Cdn</span></span>
* <span data-ttu-id="3a667-118">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3a667-118">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3a667-119">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3a667-119">Az.CognitiveServices</span></span>
* <span data-ttu-id="3a667-120">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3a667-120">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a667-121">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a667-121">Az.Compute</span></span>
* <span data-ttu-id="3a667-122">Az AEM telepítési kapcsolatos problémák megoldásához, ha a lemezek erőforrás-azonosítók kisbetűs resourcegroups volt az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="3a667-122">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="3a667-123">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3a667-123">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3a667-124">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="3a667-124">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3a667-125">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3a667-125">Az.DataFactory</span></span>
* <span data-ttu-id="3a667-126">Adjon hozzá SsisProperties, ha a NodeCount felügyelt integrációs modul nem null értékű.</span><span class="sxs-lookup"><span data-stu-id="3a667-126">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3a667-127">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a667-127">Az.DataLakeStore</span></span>
* <span data-ttu-id="3a667-128">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3a667-128">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="3a667-129">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3a667-129">Az.EventGrid</span></span>
* <span data-ttu-id="3a667-130">A Súgó szöveg jelzi, hogy erőforrásokat kell létrehozni a create/update eseményt előfizetés parancsmagok használata előtt végpont frissítése.</span><span class="sxs-lookup"><span data-stu-id="3a667-130">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3a667-131">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3a667-131">Az.EventHub</span></span>
* <span data-ttu-id="3a667-132">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="3a667-132">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="3a667-133">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3a667-133">Az.HDInsight</span></span>
* <span data-ttu-id="3a667-134">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3a667-134">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3a667-135">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3a667-135">Az.IotHub</span></span>
* <span data-ttu-id="3a667-136">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3a667-136">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3a667-137">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3a667-137">Az.KeyVault</span></span>
* <span data-ttu-id="3a667-138">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3a667-138">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3a667-139">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="3a667-139">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="3a667-140">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="3a667-140">Az.MachineLearning</span></span>
* <span data-ttu-id="3a667-141">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3a667-141">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="3a667-142">Az.Media</span><span class="sxs-lookup"><span data-stu-id="3a667-142">Az.Media</span></span>
* <span data-ttu-id="3a667-143">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3a667-143">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3a667-144">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3a667-144">Az.Monitor</span></span>
  * <span data-ttu-id="3a667-145">Riasztási szabály (nem klasszikus) GenV2 mérőszám-alapú új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3a667-145">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="3a667-146">Új AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="3a667-146">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="3a667-147">Új AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="3a667-147">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="3a667-148">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="3a667-148">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="3a667-149">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="3a667-149">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="3a667-150">Adjon hozzá AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="3a667-150">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="3a667-151">Frissített verzió 0.22.0-preview figyelő SDK</span><span class="sxs-lookup"><span data-stu-id="3a667-151">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a667-152">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a667-152">Az.Network</span></span>
* <span data-ttu-id="3a667-153">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3a667-153">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3a667-154">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="3a667-154">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="3a667-155">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="3a667-155">Az.NotificationHubs</span></span>
* <span data-ttu-id="3a667-156">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3a667-156">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3a667-157">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3a667-157">Az.OperationalInsights</span></span>
* <span data-ttu-id="3a667-158">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3a667-158">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="3a667-159">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="3a667-159">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="3a667-160">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3a667-160">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3a667-161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a667-161">Az.RecoveryServices</span></span>
* <span data-ttu-id="3a667-162">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3a667-162">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3a667-163">Frissített táblázatos formában az SQL azure-beli virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="3a667-163">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="3a667-164">A hozzáadott alternatív módszert AzureFileShare hely beolvasása</span><span class="sxs-lookup"><span data-stu-id="3a667-164">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="3a667-165">Frissített ScheduleRunDays SchedulePolicy objektumban időzóna szerint</span><span class="sxs-lookup"><span data-stu-id="3a667-165">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="3a667-166">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="3a667-166">Az.RedisCache</span></span>
* <span data-ttu-id="3a667-167">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3a667-167">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a667-168">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a667-168">Az.Resources</span></span>
* <span data-ttu-id="3a667-169">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="3a667-169">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a667-170">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a667-170">Az.Sql</span></span>
* <span data-ttu-id="3a667-171">Cserélje le a függőségi figyelő SDK közös kód</span><span class="sxs-lookup"><span data-stu-id="3a667-171">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="3a667-172">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3a667-172">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3a667-173">Továbbfejlesztett folyamat, amely több oszlop osztályozási.</span><span class="sxs-lookup"><span data-stu-id="3a667-173">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="3a667-174">Termékváltozat tulajdonságok (termékváltozat neve, családi, kapacitás) válasz a Get-AzSqlServerServiceObjective és formátum táblaként alapértelmezés szerint tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="3a667-174">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="3a667-175">Lehetővé teszi a Get-AzSqlServerServiceObjective anélkül, hogy a régióban egy már létező kiszolgáló hely alapján.</span><span class="sxs-lookup"><span data-stu-id="3a667-175">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="3a667-176">Hozzon létre felügyelt példányt az időzóna-paraméter támogatása.</span><span class="sxs-lookup"><span data-stu-id="3a667-176">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="3a667-177">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="3a667-177">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3a667-178">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a667-178">Az.Websites</span></span>
* <span data-ttu-id="3a667-179">a Set-AzWebApp és a Set-AzWebAppSlot távolítja el a címkék a végrehajtási javítások</span><span class="sxs-lookup"><span data-stu-id="3a667-179">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="3a667-180">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="3a667-180">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3a667-181">A webhelyek SDK frissítése.</span><span class="sxs-lookup"><span data-stu-id="3a667-181">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="3a667-182">A AdminSiteName tulajdonság PSAppServicePlan eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="3a667-182">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="3a667-183">1.7.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="3a667-183">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="3a667-184">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="3a667-184">Highlights since the last major release</span></span>
* <span data-ttu-id="3a667-185">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="3a667-185">General availability of `Az` module</span></span>
* <span data-ttu-id="3a667-186">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="3a667-186">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="3a667-187">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="3a667-187">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="3a667-188">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="3a667-188">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="3a667-189">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="3a667-189">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="3a667-190">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="3a667-190">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="3a667-191">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="3a667-191">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3a667-192">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a667-192">Az.Accounts</span></span>
* <span data-ttu-id="3a667-193">Frissített Add-AzEnvironment és Set-AzEnvironment parancsmag az AzureAnalysisServicesEndpointResourceId paraméter elfogadásához</span><span class="sxs-lookup"><span data-stu-id="3a667-193">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="3a667-194">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3a667-194">Az.AnalysisServices</span></span>
* <span data-ttu-id="3a667-195">ServiceClient használata DataPlane-parancsmagokban és az eredeti hitelesítési logika eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3a667-195">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="3a667-196">Az Add-AzureASAccount burkolóként való megadása a Connect-AzAccount számára a kompatibilitástörő változás elkerüléséhez</span><span class="sxs-lookup"><span data-stu-id="3a667-196">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3a667-197">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3a667-197">Az.Automation</span></span>
* <span data-ttu-id="3a667-198">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag belefoglalásokat érintő hibája.</span><span class="sxs-lookup"><span data-stu-id="3a667-198">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="3a667-199">Az IncludedKbNumber és az IncludedPackageNameMask paraméter mostantól működőképes.</span><span class="sxs-lookup"><span data-stu-id="3a667-199">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="3a667-200">Hibajavítás az Azure Automation frissítéskezelési dinamikus csoportja esetében</span><span class="sxs-lookup"><span data-stu-id="3a667-200">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a667-201">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a667-201">Az.Compute</span></span>
* <span data-ttu-id="3a667-202">HyperVGeneration paraméter hozzáadása a New-AzDiskConfig és a New-AzSnapshotConfig parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="3a667-202">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="3a667-203">Virtuális gépek más bérlők katalógus-rendszerképével való létrehozásának engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="3a667-203">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="3a667-204">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3a667-204">Az.ContainerInstance</span></span>
* <span data-ttu-id="3a667-205">Ki lett javítva a New-AzContainerGroup üres záró argumentumot hozzáadó -Command paraméterével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="3a667-205">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3a667-206">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3a667-206">Az.DataFactory</span></span>
* <span data-ttu-id="3a667-207">Az ADF .Net SDK verziója 3.0.2-re frissült.</span><span class="sxs-lookup"><span data-stu-id="3a667-207">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="3a667-208">A Set-AzDataFactoryV2 parancsmag a RepoConfiguration beállításaihoz tartozó kiegészítő paraméterekkel lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="3a667-208">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a667-209">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a667-209">Az.Resources</span></span>
* <span data-ttu-id="3a667-210">Továbbfejlesztett szolgáltatókezelés a Get-AzResource esetében, -ResourceId vagy -ResourceGroupName, -Name és -ResourceType paraméterek megadásakor</span><span class="sxs-lookup"><span data-stu-id="3a667-210">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="3a667-211">Továbbfejlesztett hibakezelés a Test-AzDeployment és a Test-AzResourceGroupDeployment esetében</span><span class="sxs-lookup"><span data-stu-id="3a667-211">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="3a667-212">A hibákat nem a telepítés ellenőrzése során kezeli, hanem a parancs kimenetébe foglalja bele</span><span class="sxs-lookup"><span data-stu-id="3a667-212">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="3a667-213">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="3a667-213">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="3a667-214">-IgnoreDynamicParameters kapcsolóparaméter hozzáadása telepítési parancsmagokhoz a rendszer által feltett kérdések szkriptekben és feladatokban való mellőzéséhez</span><span class="sxs-lookup"><span data-stu-id="3a667-214">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="3a667-215">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="3a667-215">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a667-216">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a667-216">Az.Sql</span></span>
* <span data-ttu-id="3a667-217">Adatbázisadat-besorolás támogatása.</span><span class="sxs-lookup"><span data-stu-id="3a667-217">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3a667-218">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a667-218">Az.Storage</span></span>
* <span data-ttu-id="3a667-219">Részletes hibaüzenet megjelenítése Storage-környezet -UseConnectedAccount paraméterrel történő létrehozásakor az Azure-fiókba való bejelentkezés nélkül</span><span class="sxs-lookup"><span data-stu-id="3a667-219">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="3a667-220">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3a667-220">New-AzStorageContext</span></span>
* <span data-ttu-id="3a667-221">Adott Storage-fiók Blob service-tulajdonságai kezelésének támogatása Management plane API-val</span><span class="sxs-lookup"><span data-stu-id="3a667-221">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="3a667-222">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="3a667-222">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="3a667-223">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="3a667-223">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="3a667-224">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3a667-224">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="3a667-225">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3a667-225">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="3a667-226">Az -AsJob támogatása blobok és fájlok feltöltéséhez, valamint parancsmagok letöltéséhez</span><span class="sxs-lookup"><span data-stu-id="3a667-226">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="3a667-227">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3a667-227">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="3a667-228">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3a667-228">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="3a667-229">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3a667-229">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="3a667-230">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3a667-230">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="3a667-231">1.6.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="3a667-231">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="3a667-232">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="3a667-232">Highlights since the last major release</span></span>
* <span data-ttu-id="3a667-233">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="3a667-233">General availability of `Az` module</span></span>
* <span data-ttu-id="3a667-234">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="3a667-234">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="3a667-235">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="3a667-235">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="3a667-236">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="3a667-236">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="3a667-237">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="3a667-237">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="3a667-238">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="3a667-238">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="3a667-239">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="3a667-239">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3a667-240">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3a667-240">Az.Automation</span></span>
* <span data-ttu-id="3a667-241">Az Azure Automation frissítéskezelése módosult, hogy támogassa az alábbi új funkciókat:</span><span class="sxs-lookup"><span data-stu-id="3a667-241">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="3a667-242">Dinamikus csoportosítás</span><span class="sxs-lookup"><span data-stu-id="3a667-242">Dynamic grouping</span></span>
    * <span data-ttu-id="3a667-243">Előzetesen és utólagosan futtatandó szkriptek</span><span class="sxs-lookup"><span data-stu-id="3a667-243">Pre-Post script</span></span>
    * <span data-ttu-id="3a667-244">Újraindítási beállítás</span><span class="sxs-lookup"><span data-stu-id="3a667-244">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a667-245">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a667-245">Az.Compute</span></span>
* <span data-ttu-id="3a667-246">Ki lett javítva az elérési útvonal feloldásával kapcsolatos hiba a Get-AzVmBootDiagnosticsData esetében</span><span class="sxs-lookup"><span data-stu-id="3a667-246">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="3a667-247">A Compute ügyfélkódtár frissült a 25.0.0 verzióra</span><span class="sxs-lookup"><span data-stu-id="3a667-247">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3a667-248">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3a667-248">Az.KeyVault</span></span>
* <span data-ttu-id="3a667-249">Helyettesítő karakterek támogatásának hozzáadása a KeyVault-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="3a667-249">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a667-250">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a667-250">Az.Network</span></span>
* <span data-ttu-id="3a667-251">Az Intelligens veszélyforrás-felderítés támogatásának hozzáadása az Azure Firewallhoz</span><span class="sxs-lookup"><span data-stu-id="3a667-251">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="3a667-252">Az Application Gateway-tűzfalszabályzat legfelső szintű erőforrása és egyéni szabályok hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3a667-252">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3a667-253">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a667-253">Az.RecoveryServices</span></span>
* <span data-ttu-id="3a667-254">A SnapshotRetentionInDays hozzáadása az Azure-beli virtuális gépek szabályzatához az azonnali RP támogatása érdekében</span><span class="sxs-lookup"><span data-stu-id="3a667-254">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="3a667-255">Folyamat támogatásának hozzáadása a regisztrációtörlési tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="3a667-255">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a667-256">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a667-256">Az.Resources</span></span>
* <span data-ttu-id="3a667-257">Helyettesítő karakterek támogatásának hozzáadása a Get-AzResource és Get-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="3a667-257">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="3a667-258">Az ARM általános hívása esetén használt hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="3a667-258">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a667-259">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a667-259">Az.Sql</span></span>
* <span data-ttu-id="3a667-260">A Fenyegetésészlelés parancsmagjainak paramétere (ExcludeDetectionType) a DetectionType helyett string[] lett, hogy a jövőben is használható legyen az új DetectionType-ok hozzáadásakor, valamint az automatikus kitöltés támogatása érdekében.</span><span class="sxs-lookup"><span data-stu-id="3a667-260">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3a667-261">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a667-261">Az.Storage</span></span>
* <span data-ttu-id="3a667-262">Tárfiók felügyeleti szabályzata lekérésének/beállításának/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="3a667-262">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="3a667-263">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="3a667-263">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="3a667-264">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="3a667-264">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="3a667-265">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="3a667-265">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="3a667-266">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="3a667-266">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="3a667-267">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="3a667-267">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="3a667-268">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="3a667-268">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3a667-269">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a667-269">Az.Websites</span></span>
* <span data-ttu-id="3a667-270">Ki lett javítva az ARM-sablon azon hibája, amely miatt meghiúsul az összes tárolóhely a New-AzWebApp - IncludeSourceWebAppSlots használatával történő klónozása</span><span class="sxs-lookup"><span data-stu-id="3a667-270">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="3a667-271">1.5.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="3a667-271">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3a667-272">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a667-272">Az.Accounts</span></span>
* <span data-ttu-id="3a667-273">A Register-AzModule parancs hozzáadása az AutoRest által létrehozott parancsmagok támogatásához</span><span class="sxs-lookup"><span data-stu-id="3a667-273">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="3a667-274">A Connect-AzAccount példáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="3a667-274">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3a667-275">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3a667-275">Az.Automation</span></span>
* <span data-ttu-id="3a667-276">A bizonyos havi ütemezések lekérésekor jelentkező hiba kijavítva számos Azure Automation-parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="3a667-276">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="3a667-277">Ki lett javítva a hiba, amely miatt a Get-AzAutomationDscNode csak az első 20 csomópontot adta vissza.</span><span class="sxs-lookup"><span data-stu-id="3a667-277">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="3a667-278">Most már az összes csomópontot visszaadja</span><span class="sxs-lookup"><span data-stu-id="3a667-278">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="3a667-279">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3a667-279">Az.Cdn</span></span>
* <span data-ttu-id="3a667-280">Új Powershell-parancsmagok hozzáadva az Egyéni tartományi Https engedélyezése/letiltása szolgáltatáshoz, a régiek elavultak</span><span class="sxs-lookup"><span data-stu-id="3a667-280">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a667-281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a667-281">Az.Compute</span></span>
* <span data-ttu-id="3a667-282">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="3a667-282">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3a667-283">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3a667-283">Az.DataFactory</span></span>
* <span data-ttu-id="3a667-284">Az ADF .Net SDK verziója 3.0.1-re frissült</span><span class="sxs-lookup"><span data-stu-id="3a667-284">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="3a667-285">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3a667-285">Az.LogicApp</span></span>
* <span data-ttu-id="3a667-286">Ki lett javítva a hiba, amely miatt a ListWorkflows csak az eredmények első oldalát kérte le</span><span class="sxs-lookup"><span data-stu-id="3a667-286">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a667-287">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a667-287">Az.Network</span></span>
* <span data-ttu-id="3a667-288">Helyettesítő karakterek támogatásának hozzáadása a Network-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="3a667-288">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3a667-289">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a667-289">Az.RecoveryServices</span></span>
* <span data-ttu-id="3a667-290">Azure-beli virtuális gépen futtatott SQL Server támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="3a667-290">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="3a667-291">SDK-frissítés</span><span class="sxs-lookup"><span data-stu-id="3a667-291">SDK Update</span></span>
* <span data-ttu-id="3a667-292">VMappContainer ellenőrzés eltávolítva a Get-ProtectableItem parancsmagból</span><span class="sxs-lookup"><span data-stu-id="3a667-292">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="3a667-293">Name és ServerName paraméterek hozzáadva a Get-ProtectableItem parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3a667-293">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a667-294">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a667-294">Az.Resources</span></span>
* <span data-ttu-id="3a667-295">`-TemplateObject` paraméter hozzáadva az üzembe helyező parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="3a667-295">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="3a667-296">További információ: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="3a667-296">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="3a667-297">Ki lett javítva a hiba, amely akkor jelentkezett, amikor a(z) `Get-AzResource` eredménye át lett irányítva a következőbe: `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="3a667-297">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="3a667-298">További információ: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="3a667-298">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="3a667-299">Ki lett javítva a JSON-adattípus módosításával kapcsolatos probléma, amely a(z) `Set-AzResource` futtatásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="3a667-299">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="3a667-300">További információ: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="3a667-300">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a667-301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a667-301">Az.Sql</span></span>
* <span data-ttu-id="3a667-302">Az AuditingEndpointsCommunicator frissítése.</span><span class="sxs-lookup"><span data-stu-id="3a667-302">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="3a667-303">Ki lett javítva az új diagnosztikai beállítások létrehozásakor jelentkező ritka eset viselkedése.</span><span class="sxs-lookup"><span data-stu-id="3a667-303">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3a667-304">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a667-304">Az.Storage</span></span>
* <span data-ttu-id="3a667-305">A BlockBlobStorage altípus támogatása a Storage-fiók létrehozásakor      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3a667-305">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="3a667-306">1.4.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="3a667-306">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="3a667-307">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3a667-307">Az.AnalysisServices</span></span>
* <span data-ttu-id="3a667-308">Az AddAzureASAccount parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="3a667-308">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3a667-309">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3a667-309">Az.Automation</span></span>
* <span data-ttu-id="3a667-310">Az Import-AzAutomationDscNodeConfiguration súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="3a667-310">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="3a667-311">A konfigurációnév-ellenőrzés hozzáadva az Import-AzAutomationDscConfiguration parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3a667-311">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="3a667-312">Továbbfejlesztett hibakezelés az Import-AzAutomationDscConfiguration parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="3a667-312">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3a667-313">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3a667-313">Az.CognitiveServices</span></span>
* <span data-ttu-id="3a667-314">A CustomSubdomainName új választható paraméterként hozzáadva a New-AzCognitiveServicesAccount parancsmaghoz, amellyel altartomány adható meg az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="3a667-314">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a667-315">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a667-315">Az.Compute</span></span>
* <span data-ttu-id="3a667-316">Kijavítva az azonosító paraméterkészleteivel kapcsolatos probléma</span><span class="sxs-lookup"><span data-stu-id="3a667-316">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="3a667-317">Frissült a Get-AzVMExtension parancsmag, hogy az összes telepített bővítményt listázza, ha a Name paraméter nincs megadva</span><span class="sxs-lookup"><span data-stu-id="3a667-317">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="3a667-318">A Tag és a ResourceId paraméterek hozzáadva az Update-AzImage parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3a667-318">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="3a667-319">A Get-AzVmssVM példányazonosító nélkül, az InstanceView használatával példánynézetben listázni tudja a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="3a667-319">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3a667-320">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a667-320">Az.DataLakeStore</span></span>
* <span data-ttu-id="3a667-321">Parancsmagok hozzáadása a törölt ADL-elemek enumerálásához és visszaállításához</span><span class="sxs-lookup"><span data-stu-id="3a667-321">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3a667-322">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3a667-322">Az.EventHub</span></span>
* <span data-ttu-id="3a667-323">Új SkipEmptyArchives logikai tulajdonság hozzáadva az üres archívumok kihagyásához az Eventhub CaptureDescription osztályában</span><span class="sxs-lookup"><span data-stu-id="3a667-323">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3a667-324">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3a667-324">Az.KeyVault</span></span>
* <span data-ttu-id="3a667-325">A Set-AzKeyVaultSecret címkézésének kijavítása</span><span class="sxs-lookup"><span data-stu-id="3a667-325">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="3a667-326">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3a667-326">Az.LogicApp</span></span>
* <span data-ttu-id="3a667-327">Hozzáadva az integrációs fiókok alapszintű termékváltozatában</span><span class="sxs-lookup"><span data-stu-id="3a667-327">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="3a667-328">Hozzáadva az XSLT 2.0-ban, az XSLT 3.0-ban és a Liquid leképezéstípusok esetén</span><span class="sxs-lookup"><span data-stu-id="3a667-328">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="3a667-329">Új parancsmagok az integrációs fiók szerelvényeihez</span><span class="sxs-lookup"><span data-stu-id="3a667-329">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="3a667-330">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="3a667-330">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="3a667-331">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="3a667-331">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="3a667-332">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="3a667-332">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="3a667-333">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="3a667-333">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="3a667-334">Új parancsmagok az integrációs fiók kötegkonfigurációjához</span><span class="sxs-lookup"><span data-stu-id="3a667-334">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="3a667-335">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a667-335">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="3a667-336">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a667-336">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="3a667-337">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a667-337">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="3a667-338">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a667-338">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="3a667-339">A Logic Apps SDK frissítése a 4.1.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="3a667-339">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3a667-340">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3a667-340">Az.Monitor</span></span>
* <span data-ttu-id="3a667-341">A Get-AzMetric súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="3a667-341">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a667-342">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a667-342">Az.Network</span></span>
* <span data-ttu-id="3a667-343">Az Add-AzApplicationGatewayCustomError súgójában lévő példa frissítése</span><span class="sxs-lookup"><span data-stu-id="3a667-343">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3a667-344">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3a667-344">Az.OperationalInsights</span></span>
* <span data-ttu-id="3a667-345">Kibővített támogatás a New és a Get ApplicationInsights adatforráshoz.</span><span class="sxs-lookup"><span data-stu-id="3a667-345">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="3a667-346">Új „ApplicationInsights” altípus hozzáadva az adott munkaterület Get specific és Get all Application Insights-adatforrásainak támogatásához.</span><span class="sxs-lookup"><span data-stu-id="3a667-346">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="3a667-347">A New-AzOperationalInsightsApplicationInsightsDataSource parancsmag hozzáadva adatforrás létrehozásához a következő Application Insights-erőforrásparaméterekkel: subscriptionId, resourceGroupName és name.</span><span class="sxs-lookup"><span data-stu-id="3a667-347">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a667-348">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a667-348">Az.Resources</span></span>
* <span data-ttu-id="3a667-349">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="3a667-349">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="3a667-350">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="3a667-350">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="3a667-351">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="3a667-351">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="3a667-352">Ki lett javítva a KeyCredentials ismételt létrehozását megakadályozó hiba</span><span class="sxs-lookup"><span data-stu-id="3a667-352">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a667-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a667-353">Az.Sql</span></span>
* <span data-ttu-id="3a667-354">Rugalmas SQL DB-skálázási szint támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3a667-354">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="3a667-355">Ki lett javítva az a hiba, hogy a visszaállítási kérésben szereplő szükségtelen tulajdonságok megadása miatt a visszaállítás esetenként meghiúsult</span><span class="sxs-lookup"><span data-stu-id="3a667-355">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3a667-356">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a667-356">Az.Websites</span></span>
* <span data-ttu-id="3a667-357">A Get-AzWebAppSlotMetrics példájának javítása</span><span class="sxs-lookup"><span data-stu-id="3a667-357">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="3a667-358">1.3.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="3a667-358">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3a667-359">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a667-359">Az.Accounts</span></span>
* <span data-ttu-id="3a667-360">Frissítés a ClientRuntime legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="3a667-360">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="3a667-361">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3a667-361">Az.AnalysisServices</span></span>
<span data-ttu-id="3a667-362">Az Az.AnalysisServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="3a667-362">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a667-363">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a667-363">Az.Compute</span></span>
* <span data-ttu-id="3a667-364">AEM-bővítmény: Mostantól az UltraSSD, valamint a P60, P70 és P80 lemezek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="3a667-364">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="3a667-365">A Set-AzVMBootDiagnostics súgóleírása frissült.</span><span class="sxs-lookup"><span data-stu-id="3a667-365">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="3a667-366">Az Update-AzImage súgóleírása és példája frissült.</span><span class="sxs-lookup"><span data-stu-id="3a667-366">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3a667-367">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a667-367">Az.RecoveryServices</span></span>
<span data-ttu-id="3a667-368">Az Az.RecoveryServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="3a667-368">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a667-369">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a667-369">Az.Resources</span></span>
* <span data-ttu-id="3a667-370">Az erőforráscsoportok címkézése ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="3a667-370">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="3a667-371">További információ: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="3a667-371">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="3a667-372">Ki lett javítva az a hiba, amikor a `Get-AzureRmRoleAssignment` nem vette figyelembe az -ErrorAction paramétert.</span><span class="sxs-lookup"><span data-stu-id="3a667-372">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="3a667-373">További információ: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="3a667-373">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a667-374">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a667-374">Az.Sql</span></span>
* <span data-ttu-id="3a667-375">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3a667-375">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="3a667-376">Ki lett javítva az a hiba, amikor az Azure-fiókba való bejelentkezés hiánya nullref kivételt eredményezett az SQL-parancsmagok végrehajtásakor.</span><span class="sxs-lookup"><span data-stu-id="3a667-376">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="3a667-377">A nullref kivétel ki lett javítva a Get-AzSqlCapabilityben.</span><span class="sxs-lookup"><span data-stu-id="3a667-377">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="3a667-378">1.2.1 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="3a667-378">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3a667-379">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a667-379">Az.Accounts</span></span>
* <span data-ttu-id="3a667-380">A hitelesítés megfelelő verziójával rendelkező kiadás</span><span class="sxs-lookup"><span data-stu-id="3a667-380">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="3a667-381">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3a667-381">Az.AnalysisServices</span></span>
* <span data-ttu-id="3a667-382">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="3a667-382">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3a667-383">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a667-383">Az.RecoveryServices</span></span>
* <span data-ttu-id="3a667-384">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="3a667-384">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="3a667-385">1.2.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="3a667-385">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3a667-386">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a667-386">Az.Accounts</span></span>
* <span data-ttu-id="3a667-387">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="3a667-387">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="3a667-388">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="3a667-388">Update incorrect online help URLs</span></span>
* <span data-ttu-id="3a667-389">Az Uninstall-AzureRm figyelmeztető üzenete hozzáadva a PS Core-ban</span><span class="sxs-lookup"><span data-stu-id="3a667-389">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="3a667-390">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="3a667-390">Az.Aks</span></span>
* <span data-ttu-id="3a667-391">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="3a667-391">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3a667-392">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3a667-392">Az.Automation</span></span>
* <span data-ttu-id="3a667-393">Mostantól támogatottak a Python 2-runbookok.</span><span class="sxs-lookup"><span data-stu-id="3a667-393">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="3a667-394">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="3a667-394">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="3a667-395">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3a667-395">Az.Cdn</span></span>
* <span data-ttu-id="3a667-396">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="3a667-396">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a667-397">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a667-397">Az.Compute</span></span>
* <span data-ttu-id="3a667-398">Az Invoke-AzVMReimage parancsmag hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="3a667-398">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="3a667-399">A TempDisk paraméter hozzá lett adva a Set-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="3a667-399">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="3a667-400">A New-AzVM figyelmeztető üzenete ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="3a667-400">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="3a667-401">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3a667-401">Az.ContainerRegistry</span></span>
* <span data-ttu-id="3a667-402">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="3a667-402">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3a667-403">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3a667-403">Az.DataFactory</span></span>
* <span data-ttu-id="3a667-404">Az ADF .Net SDK verziója 3.0.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="3a667-404">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3a667-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a667-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="3a667-406">Ki lett javítva az ADLS-végponttal kapcsolatos probléma az MSI használatakor.</span><span class="sxs-lookup"><span data-stu-id="3a667-406">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="3a667-407">További információ: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="3a667-407">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="3a667-408">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="3a667-408">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3a667-409">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3a667-409">Az.IotHub</span></span>
* <span data-ttu-id="3a667-410">Az Encoding formátum hozzá lett adva az Add-IotHubRoutingEndpoint parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="3a667-410">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3a667-411">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3a667-411">Az.KeyVault</span></span>
* <span data-ttu-id="3a667-412">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="3a667-412">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a667-413">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a667-413">Az.Network</span></span>
* <span data-ttu-id="3a667-414">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="3a667-414">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a667-415">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a667-415">Az.Resources</span></span>
* <span data-ttu-id="3a667-416">A helytelen példák ki lettek javítva a New-AzADAppCredential és a New-AzADSpCredential referenciadokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="3a667-416">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="3a667-417">Ki lett javítva az a hiba, amikor a -TemplateFile paraméter nem lett feloldva az erőforráscsoportokat üzembe helyező parancsmagok végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="3a667-417">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="3a667-418">Az.Resources: A New-AzureRmPolicyDefinition -Mode alapértelmezett értékének dokumentációja ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="3a667-418">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="3a667-419">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="3a667-419">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="3a667-420">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="3a667-420">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="3a667-421">Ki lett javítva a „PSResourceGroupDeployment” objektum formázásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="3a667-421">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="3a667-422">További információ: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="3a667-422">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3a667-423">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3a667-423">Az.ServiceFabric</span></span>
* <span data-ttu-id="3a667-424">Visszaállítás a VMSS-modell tanúsítványának hozzáadásakor bekövetkező kivétel-visszaadás esetén; javított hiba: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="3a667-424">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="3a667-425">Bizonyos hibaüzenetek ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="3a667-425">Fix some error messages.</span></span>
* <span data-ttu-id="3a667-426">Ki lett javítva az alapértelmezett ARM-sablonnal való fürtlétrehozás a New-AzServiceFabriCluster esetében, amely nem működött az Az-ba történő migrálással.</span><span class="sxs-lookup"><span data-stu-id="3a667-426">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="3a667-427">Ki lett javítva a fürt-/alkalmazástanúsítvány létrehozása, így mostantól csak a fürtnek megfelelő virtuálisgép-méretezési csoportokhoz (Virtual Machine Scale Sets) lesznek hozzáadva, a fürtazonosító bővítményben való ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="3a667-427">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="3a667-428">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="3a667-428">Az.SignalR</span></span>
* <span data-ttu-id="3a667-429">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="3a667-429">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a667-430">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a667-430">Az.Sql</span></span>
* <span data-ttu-id="3a667-431">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="3a667-431">Update incorrect online help URLs</span></span>
* <span data-ttu-id="3a667-432">A LicenseType paraméter paraméterleírása frissítve lett a lehetséges értékekkel.</span><span class="sxs-lookup"><span data-stu-id="3a667-432">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="3a667-433">Ki lett javítva az a hiba, amikor egy felügyelt példány identitásának frissítése nem működött, ha az volt az egyetlen frissített tulajdonság.</span><span class="sxs-lookup"><span data-stu-id="3a667-433">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="3a667-434">Egyéni rendezések támogatása a felügyelt példányokon</span><span class="sxs-lookup"><span data-stu-id="3a667-434">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3a667-435">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a667-435">Az.Storage</span></span>
* <span data-ttu-id="3a667-436">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="3a667-436">Update incorrect online help URLs</span></span>
* <span data-ttu-id="3a667-437">Részletes hibaüzenet megjelenítése klasszikus naplózás/metrika get/set műveletei esetében a prémium szintű Storage-fiókon, mivel a prémium szintű Storage-fiók nem támogatja a klasszikus naplózást/metrikát.</span><span class="sxs-lookup"><span data-stu-id="3a667-437">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="3a667-438">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="3a667-438">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="3a667-439">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="3a667-439">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="3a667-440">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="3a667-440">Az.TrafficManager</span></span>
* <span data-ttu-id="3a667-441">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="3a667-441">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3a667-442">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a667-442">Az.Websites</span></span>
* <span data-ttu-id="3a667-443">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="3a667-443">Update incorrect online help URLs</span></span>
* <span data-ttu-id="3a667-444">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól a megfelelő erőforráscsoportba és helyre tölti fel a tanúsítványt, ha az alkalmazás ASE-n üzemel.</span><span class="sxs-lookup"><span data-stu-id="3a667-444">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="3a667-445">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól nem írja felül a címkéket SSL-tanúsítvány alkalmazáshoz való kötésekor.</span><span class="sxs-lookup"><span data-stu-id="3a667-445">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="3a667-446">1.1.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="3a667-446">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3a667-447">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a667-447">Az.Accounts</span></span>
* <span data-ttu-id="3a667-448">A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz</span><span class="sxs-lookup"><span data-stu-id="3a667-448">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a667-449">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a667-449">Az.Compute</span></span>
* <span data-ttu-id="3a667-450">A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni</span><span class="sxs-lookup"><span data-stu-id="3a667-450">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="3a667-451">Frissült az azonosító leírása a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="3a667-451">Updated the description of ID in help files</span></span>
* <span data-ttu-id="3a667-452">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="3a667-452">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3a667-453">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a667-453">Az.DataLakeStore</span></span>
* <span data-ttu-id="3a667-454">A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.</span><span class="sxs-lookup"><span data-stu-id="3a667-454">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="3a667-455">A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva</span><span class="sxs-lookup"><span data-stu-id="3a667-455">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="3a667-456">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3a667-456">Az.EventGrid</span></span>
* <span data-ttu-id="3a667-457">Frissítve a 2019-01-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="3a667-457">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="3a667-458">A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához</span><span class="sxs-lookup"><span data-stu-id="3a667-458">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="3a667-459">New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="3a667-459">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="3a667-460">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="3a667-460">Event Time-To-Live,</span></span>
        - <span data-ttu-id="3a667-461">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="3a667-461">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="3a667-462">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="3a667-462">Dead letter endpoint.</span></span>
    - <span data-ttu-id="3a667-463">Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="3a667-463">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="3a667-464">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="3a667-464">Event Time-To-Live,</span></span>
        - <span data-ttu-id="3a667-465">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="3a667-465">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="3a667-466">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="3a667-466">Dead letter endpoint.</span></span>
* <span data-ttu-id="3a667-467">Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.</span><span class="sxs-lookup"><span data-stu-id="3a667-467">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="3a667-468">Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.</span><span class="sxs-lookup"><span data-stu-id="3a667-468">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3a667-469">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3a667-469">Az.IotHub</span></span>
* <span data-ttu-id="3a667-470">Frissítve az IoT Hub SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="3a667-470">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="3a667-471">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3a667-471">Az.LogicApp</span></span>
* <span data-ttu-id="3a667-472">A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel</span><span class="sxs-lookup"><span data-stu-id="3a667-472">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a667-473">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a667-473">Az.Resources</span></span>
* <span data-ttu-id="3a667-474">Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="3a667-474">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="3a667-475">További információ: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="3a667-475">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="3a667-476">Ki lett javítva a -Custom paraméter kezelése a New/Set-AzPolicyDefinition parancsban</span><span class="sxs-lookup"><span data-stu-id="3a667-476">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="3a667-477">Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="3a667-477">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="3a667-478">A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében</span><span class="sxs-lookup"><span data-stu-id="3a667-478">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="3a667-479">További információ: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="3a667-479">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="3a667-480">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="3a667-480">Az.SignalR</span></span>
* <span data-ttu-id="3a667-481">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="3a667-481">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a667-482">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a667-482">Az.Sql</span></span>
* <span data-ttu-id="3a667-483">A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.</span><span class="sxs-lookup"><span data-stu-id="3a667-483">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3a667-484">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a667-484">Az.Storage</span></span>
* <span data-ttu-id="3a667-485">A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva</span><span class="sxs-lookup"><span data-stu-id="3a667-485">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="3a667-486">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3a667-486">New-AzStorageContext</span></span>
* <span data-ttu-id="3a667-487">A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz</span><span class="sxs-lookup"><span data-stu-id="3a667-487">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="3a667-488">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="3a667-488">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3a667-489">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a667-489">Az.Websites</span></span>
* <span data-ttu-id="3a667-490">Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban</span><span class="sxs-lookup"><span data-stu-id="3a667-490">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="3a667-491">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="3a667-491">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="3a667-492">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="3a667-492">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="3a667-493">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="3a667-493">General</span></span>

- <span data-ttu-id="3a667-494">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="3a667-494">General Availability of Az Module</span></span>
- <span data-ttu-id="3a667-495">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="3a667-495">Online help for each module</span></span>
- <span data-ttu-id="3a667-496">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="3a667-496">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="3a667-497">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3a667-497">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="3a667-498">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a667-498">Az.Accounts</span></span>
- <span data-ttu-id="3a667-499">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="3a667-499">Changed from Az.Profile</span></span>
- <span data-ttu-id="3a667-500">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="3a667-500">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="3a667-501">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a667-501">Az.ApiManagement</span></span>
- <span data-ttu-id="3a667-502">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="3a667-502">Fixes for #7002</span></span>
- <span data-ttu-id="3a667-503">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3a667-503">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="3a667-504">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3a667-504">Az.Batch</span></span>
- <span data-ttu-id="3a667-505">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="3a667-505">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="3a667-506">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="3a667-506">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="3a667-507">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3a667-507">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="3a667-508">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="3a667-508">Az.Billing</span></span>
- <span data-ttu-id="3a667-509">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="3a667-509">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="3a667-510">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="3a667-510">Az.CognitivServices</span></span>
- <span data-ttu-id="3a667-511">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="3a667-511">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="3a667-512">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="3a667-512">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="3a667-513">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3a667-513">Az.ContainerInstance</span></span>
- <span data-ttu-id="3a667-514">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="3a667-514">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="3a667-515">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="3a667-515">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="3a667-516">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3a667-516">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="3a667-517">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a667-517">Az.DataLakeStore</span></span>
- <span data-ttu-id="3a667-518">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3a667-518">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="3a667-519">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3a667-519">Az.Monitor</span></span>
- <span data-ttu-id="3a667-520">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3a667-520">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="3a667-521">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3a667-521">Az.KeyVault</span></span>
- <span data-ttu-id="3a667-522">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="3a667-522">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="3a667-523">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="3a667-523">Az.MachineLearning</span></span>
- <span data-ttu-id="3a667-524">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="3a667-524">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="3a667-525">Az.Media</span><span class="sxs-lookup"><span data-stu-id="3a667-525">Az.Media</span></span>
- <span data-ttu-id="3a667-526">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="3a667-526">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="3a667-527">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a667-527">Az.Network</span></span>
<span data-ttu-id="3a667-528">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="3a667-528">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="3a667-529">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="3a667-529">New cmdlets added:</span></span>
        - <span data-ttu-id="3a667-530">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3a667-530">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3a667-531">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3a667-531">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3a667-532">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3a667-532">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3a667-533">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3a667-533">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3a667-534">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3a667-534">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3a667-535">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="3a667-535">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="3a667-536">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="3a667-536">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="3a667-537">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a667-537">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="3a667-538">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3a667-538">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="3a667-539">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3a667-539">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="3a667-540">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3a667-540">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="3a667-541">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3a667-541">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="3a667-542">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3a667-542">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="3a667-543">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3a667-543">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="3a667-544">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="3a667-544">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="3a667-545">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3a667-545">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="3a667-546">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3a667-546">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="3a667-547">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3a667-547">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="3a667-548">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3a667-548">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="3a667-549">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="3a667-549">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="3a667-550">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3a667-550">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="3a667-551">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3a667-551">Az.OperationalInsights</span></span>
- <span data-ttu-id="3a667-552">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3a667-552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="3a667-553">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="3a667-553">Az.Profile</span></span>
- <span data-ttu-id="3a667-554">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a667-554">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="3a667-555">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a667-555">Az.RecoveryServices</span></span>
- <span data-ttu-id="3a667-556">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3a667-556">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="3a667-557">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a667-557">Az.Resources</span></span>
- <span data-ttu-id="3a667-558">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3a667-558">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="3a667-559">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3a667-559">Az.ServiceFabric</span></span>
- <span data-ttu-id="3a667-560">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="3a667-560">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="3a667-561">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3a667-561">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="3a667-562">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="3a667-562">Az.SIgnalR</span></span>
- <span data-ttu-id="3a667-563">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="3a667-563">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="3a667-564">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a667-564">Az.Sql</span></span>
- <span data-ttu-id="3a667-565">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="3a667-565">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="3a667-566">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="3a667-566">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="3a667-567">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3a667-567">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="3a667-568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a667-568">Az.Storage</span></span>
- <span data-ttu-id="3a667-569">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3a667-569">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="3a667-570">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a667-570">Az.Websites</span></span>
- <span data-ttu-id="3a667-571">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3a667-571">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="3a667-572">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="3a667-572">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="3a667-573">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="3a667-573">General</span></span>

* <span data-ttu-id="3a667-574">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="3a667-574">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="3a667-575">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a667-575">Az.Compute</span></span>

* <span data-ttu-id="3a667-576">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="3a667-576">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="3a667-577">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a667-577">Az.DataLakeStore</span></span>

* <span data-ttu-id="3a667-578">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="3a667-578">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="3a667-579">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3a667-579">Az.FrontDoor</span></span>

* <span data-ttu-id="3a667-580">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="3a667-580">Fixed some broken links</span></span>
    - <span data-ttu-id="3a667-581">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="3a667-581">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="3a667-582">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="3a667-582">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="3a667-583">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a667-583">Az.RecoveryServices</span></span>

* <span data-ttu-id="3a667-584">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="3a667-584">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="3a667-585">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="3a667-585">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="3a667-586">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a667-586">Az.Resources</span></span>

* <span data-ttu-id="3a667-587">[https://github.com/Azure/azure-powershell/issues/7679](https://github.com/Azure/azure-powershell/issues/7679 ) javítása</span><span class="sxs-lookup"><span data-stu-id="3a667-587">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="3a667-588">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="3a667-588">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="3a667-589">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a667-589">Az.Sql</span></span>

* <span data-ttu-id="3a667-590">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="3a667-590">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="3a667-591">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="3a667-591">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="3a667-592">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="3a667-592">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="3a667-593">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a667-593">Az.Storage</span></span>

* <span data-ttu-id="3a667-594">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3a667-594">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="3a667-595">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="3a667-595">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="3a667-596">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="3a667-596">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="3a667-597">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="3a667-597">Support Static Website configuration</span></span>
    - <span data-ttu-id="3a667-598">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="3a667-598">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="3a667-599">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="3a667-599">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="3a667-600">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a667-600">Az.Websites</span></span>

* <span data-ttu-id="3a667-601">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3a667-601">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="3a667-602">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="3a667-602">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="3a667-603">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="3a667-603">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="3a667-604">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="3a667-604">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="3a667-605">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a667-605">Az.ApiManagement</span></span>
* <span data-ttu-id="3a667-606">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="3a667-606">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="3a667-607">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3a667-607">Az.Automation</span></span>
* <span data-ttu-id="3a667-608">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="3a667-608">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="3a667-609">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="3a667-609">Added Update Management cmdlets</span></span>
* <span data-ttu-id="3a667-610">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="3a667-610">Added Source Control cmdlets</span></span>
* <span data-ttu-id="3a667-611">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="3a667-611">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="3a667-612">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="3a667-612">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="3a667-613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a667-613">Az.Compute</span></span>
* <span data-ttu-id="3a667-614">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="3a667-614">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="3a667-615">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="3a667-615">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="3a667-616">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3a667-616">Az.ContainerInstance</span></span>
* <span data-ttu-id="3a667-617">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="3a667-617">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="3a667-618">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="3a667-618">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="3a667-619">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="3a667-619">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="3a667-620">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a667-620">Az.Network</span></span>
* <span data-ttu-id="3a667-621">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="3a667-621">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="3a667-622">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="3a667-622">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="3a667-623">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="3a667-623">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="3a667-624">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="3a667-624">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="3a667-625">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="3a667-625">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="3a667-626">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="3a667-626">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="3a667-627">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="3a667-627">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="3a667-628">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="3a667-628">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="3a667-629">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="3a667-629">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="3a667-630">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="3a667-630">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="3a667-631">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="3a667-631">Az.Relay</span></span>
* <span data-ttu-id="3a667-632">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="3a667-632">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="3a667-633">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a667-633">Az.Resources</span></span>
* <span data-ttu-id="3a667-634">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="3a667-634">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="3a667-635">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="3a667-635">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="3a667-636">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="3a667-636">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="3a667-637">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3a667-637">Az.ServiceFabric</span></span>
* <span data-ttu-id="3a667-638">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="3a667-638">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="3a667-639">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a667-639">Az.Sql</span></span>
* <span data-ttu-id="3a667-640">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="3a667-640">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="3a667-641">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3a667-641">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="3a667-642">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3a667-642">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="3a667-643">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3a667-643">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="3a667-644">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3a667-644">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="3a667-645">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="3a667-645">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="3a667-646">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="3a667-646">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="3a667-647">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="3a667-647">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="3a667-648">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="3a667-648">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="3a667-649">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="3a667-649">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="3a667-650">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="3a667-650">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="3a667-651">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="3a667-651">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="3a667-652">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="3a667-652">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="3a667-653">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="3a667-653">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="3a667-654">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="3a667-654">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="3a667-655">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="3a667-655">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="3a667-656">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="3a667-656">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="3a667-657">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="3a667-657">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="3a667-658">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="3a667-658">General</span></span>
* <span data-ttu-id="3a667-659">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="3a667-659">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="3a667-660">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="3a667-660">Az.Profile</span></span>
* <span data-ttu-id="3a667-661">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="3a667-661">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="3a667-662">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="3a667-662">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="3a667-663">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="3a667-663">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="3a667-664">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="3a667-664">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="3a667-665">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="3a667-665">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="3a667-666">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="3a667-666">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="3a667-667">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="3a667-667">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="3a667-668">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3a667-668">Az.CognitiveServices</span></span>
* <span data-ttu-id="3a667-669">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="3a667-669">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a667-670">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a667-670">Az.Compute</span></span>
* <span data-ttu-id="3a667-671">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="3a667-671">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="3a667-672">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="3a667-672">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="3a667-673">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="3a667-673">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3a667-674">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a667-674">Az.DataLakeStore</span></span>
* <span data-ttu-id="3a667-675">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="3a667-675">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="3a667-676">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="3a667-676">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="3a667-677">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="3a667-677">Az.Insights</span></span>
* <span data-ttu-id="3a667-678">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="3a667-678">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="3a667-679">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="3a667-679">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="3a667-680">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="3a667-680">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="3a667-681">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="3a667-681">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a667-682">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a667-682">Az.Network</span></span>
* <span data-ttu-id="3a667-683">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="3a667-683">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="3a667-684">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="3a667-684">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="3a667-685">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="3a667-685">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="3a667-686">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="3a667-686">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="3a667-687">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="3a667-687">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="3a667-688">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="3a667-688">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="3a667-689">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="3a667-689">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3a667-690">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3a667-690">Az.PolicyInsights</span></span>
* <span data-ttu-id="3a667-691">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3a667-691">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a667-692">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a667-692">Az.Resources</span></span>
* <span data-ttu-id="3a667-693">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402 ) javítása</span><span class="sxs-lookup"><span data-stu-id="3a667-693">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="3a667-694">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="3a667-694">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3a667-695">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3a667-695">Az.ServiceBus</span></span>
* <span data-ttu-id="3a667-696">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="3a667-696">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3a667-697">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3a667-697">Az.ServiceFabric</span></span>
* <span data-ttu-id="3a667-698">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="3a667-698">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="3a667-699">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="3a667-699">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="3a667-700">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="3a667-700">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="3a667-701">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="3a667-701">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="3a667-702">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="3a667-702">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="3a667-703">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="3a667-703">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="3a667-704">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="3a667-704">Az.Profile</span></span>
* <span data-ttu-id="3a667-705">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="3a667-705">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="3a667-706">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="3a667-706">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a667-707">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a667-707">Az.Compute</span></span>
* <span data-ttu-id="3a667-708">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="3a667-708">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="3a667-709">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="3a667-709">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3a667-710">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a667-710">Az.DataLakeStore</span></span>
* <span data-ttu-id="3a667-711">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="3a667-711">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="3a667-712">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="3a667-712">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="3a667-713">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="3a667-713">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="3a667-714">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="3a667-714">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="3a667-715">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="3a667-715">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a667-716">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a667-716">Az.Network</span></span>
* <span data-ttu-id="3a667-717">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="3a667-717">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="3a667-718">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="3a667-718">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a667-719">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a667-719">Az.Resources</span></span>
* <span data-ttu-id="3a667-720">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="3a667-720">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="3a667-721">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="3a667-721">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="3a667-722">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="3a667-722">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="3a667-723">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="3a667-723">Azure.Storage</span></span>
* <span data-ttu-id="3a667-724">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="3a667-724">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="3a667-725">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="3a667-725">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="3a667-726">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="3a667-726">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="3a667-727">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="3a667-727">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="3a667-728">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="3a667-728">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3a667-729">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3a667-729">Az.CognitiveServices</span></span>
* <span data-ttu-id="3a667-730">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="3a667-730">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a667-731">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a667-731">Az.Compute</span></span>
* <span data-ttu-id="3a667-732">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="3a667-732">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="3a667-733">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="3a667-733">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="3a667-734">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="3a667-734">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="3a667-735">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3a667-735">Az.DataFactoryV2</span></span>
* <span data-ttu-id="3a667-736">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="3a667-736">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a667-737">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a667-737">Az.Network</span></span>
* <span data-ttu-id="3a667-738">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="3a667-738">Added NetworkProfile functionality.</span></span> <span data-ttu-id="3a667-739">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="3a667-739">new cmdlets added</span></span>
    - <span data-ttu-id="3a667-740">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3a667-740">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="3a667-741">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3a667-741">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="3a667-742">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3a667-742">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="3a667-743">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3a667-743">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="3a667-744">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="3a667-744">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="3a667-745">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="3a667-745">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="3a667-746">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="3a667-746">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="3a667-747">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="3a667-747">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="3a667-748">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="3a667-748">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="3a667-749">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="3a667-749">Az.RedisCache</span></span>
* <span data-ttu-id="3a667-750">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="3a667-750">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="3a667-751">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="3a667-751">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a667-752">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a667-752">Az.Resources</span></span>
* <span data-ttu-id="3a667-753">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="3a667-753">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="3a667-754">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="3a667-754">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a667-755">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a667-755">Az.Sql</span></span>
* <span data-ttu-id="3a667-756">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="3a667-756">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3a667-757">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a667-757">Az.Websites</span></span>
* <span data-ttu-id="3a667-758">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="3a667-758">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="3a667-759">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="3a667-759">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="3a667-760">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="3a667-760">0.2.0 - September 2018</span></span>
 <span data-ttu-id="3a667-761">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="3a667-761">Initial Release</span></span>
