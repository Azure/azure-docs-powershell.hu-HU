---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/invoke-azoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
ms.openlocfilehash: bdba6d4da6df49d1975e2cfd1cc6e47f6ce6d776
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010293"
---
# <span data-ttu-id="984db-101">Invoke-AzOperationalInsightsQuery</span><span class="sxs-lookup"><span data-stu-id="984db-101">Invoke-AzOperationalInsightsQuery</span></span>

## <span data-ttu-id="984db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="984db-102">SYNOPSIS</span></span>
<span data-ttu-id="984db-103">A megadott paraméterek alapján találatokat ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="984db-103">Returns search results based on the specified parameters.</span></span>

## <span data-ttu-id="984db-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="984db-104">SYNTAX</span></span>

### <span data-ttu-id="984db-105">ByWorkspaceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="984db-105">ByWorkspaceId (Default)</span></span>
```
Invoke-AzOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>] [-Wait <Int32>]
 [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="984db-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="984db-106">ByWorkspaceObject</span></span>
```
Invoke-AzOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="984db-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="984db-107">DESCRIPTION</span></span>
<span data-ttu-id="984db-108">Az **Invoke-AzOperationalInsightsQuery** parancsmag a megadott paraméterek alapján adja vissza a találatokat.</span><span class="sxs-lookup"><span data-stu-id="984db-108">The **Invoke-AzOperationalInsightsQuery** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="984db-109">A keresés állapotát a visszaadott objektum Metaadat tulajdonságában tudja elérni.</span><span class="sxs-lookup"><span data-stu-id="984db-109">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="984db-110">Ha az állapot függőben van, akkor a keresés nem fejeződött be, és az eredmények az archívumból fognak kikeresni.</span><span class="sxs-lookup"><span data-stu-id="984db-110">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="984db-111">A keresés eredményét a visszaadott objektum Érték tulajdonságában kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="984db-111">You can retrieve the results of the search from the Value property of the returned object.</span></span>
<span data-ttu-id="984db-112">A lekérdezésre vonatkozó általános korlátozásokat itt ellenőrizheti: https://docs.microsoft.com/azure/azure-monitor/service-limits#log-queries-and-language .</span><span class="sxs-lookup"><span data-stu-id="984db-112">Please check detail of general query limits here: https://docs.microsoft.com/azure/azure-monitor/service-limits#log-queries-and-language.</span></span>

## <span data-ttu-id="984db-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="984db-113">EXAMPLES</span></span>

### <span data-ttu-id="984db-114">1. példa: Keresési eredmények lekérdezése lekérdezéssel</span><span class="sxs-lookup"><span data-stu-id="984db-114">Example 1: Get search results using a query</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="984db-115">Miután meghívta, $queryResults.Results a lekérdezés összes létrehozott sorát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="984db-115">Once invoked, $queryResults.Results will contain all of the resulting rows from your query.</span></span>

### <span data-ttu-id="984db-116">2. példa: $results. Tömbhöz megszámolható eredmény</span><span class="sxs-lookup"><span data-stu-id="984db-116">Example 2: Convert $results.Result IEnumerable to an array</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($queryResults.Results)
...
```

<span data-ttu-id="984db-117">Egyes lekérdezések nagyon nagy adatkészletek visszaadása esetén is előfordulhat.</span><span class="sxs-lookup"><span data-stu-id="984db-117">Some queries can result in very large data sets being returned.</span></span> <span data-ttu-id="984db-118">Emiatt a parancsmag alapértelmezett viselkedése a memóriaköltségek csökkentése érdekében egy számérték visszaadott értéke.</span><span class="sxs-lookup"><span data-stu-id="984db-118">Because of this, the default behavior of the cmdlet is to return an IEnumerable to reduce memory costs.</span></span> <span data-ttu-id="984db-119">Ha egy tömböt szeretne eredménytömbként használni, a LINQ Enumerable.ToArray() kiterjesztési módszerrel tömbké konvertálhatja az IEnumerable értékeket.</span><span class="sxs-lookup"><span data-stu-id="984db-119">If you'd prefer to have an array of results, you can use the LINQ Enumerable.ToArray() extension method to convert the IEnumerable to an array.</span></span>

### <span data-ttu-id="984db-120">3. példa: Keresési eredmények lekérdezése egy adott időkereten keresztüli lekérdezéssel</span><span class="sxs-lookup"><span data-stu-id="984db-120">Example 3: Get search results using a query over a specific timeframe</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="984db-121">A lekérdezés eredményei az elmúlt 24 órára korlátozódnak.</span><span class="sxs-lookup"><span data-stu-id="984db-121">The results from this query will be limited to the past 24 hours.</span></span>

### <span data-ttu-id="984db-122">4. példa: Leképezési & megjelenítése a lekérdezés eredményében</span><span class="sxs-lookup"><span data-stu-id="984db-122">Example 4: Include render & statistics in query result</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

<span data-ttu-id="984db-123">A megjelenítésről és a statisztikai adatokról [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) részletesen olvashat.</span><span class="sxs-lookup"><span data-stu-id="984db-123">See [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) for details on the render and statistics info.</span></span>

## <span data-ttu-id="984db-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="984db-124">PARAMETERS</span></span>

### <span data-ttu-id="984db-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="984db-125">-AsJob</span></span>
<span data-ttu-id="984db-126">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="984db-126">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="984db-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="984db-127">-DefaultProfile</span></span>
<span data-ttu-id="984db-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="984db-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="984db-129">-IncludeRender</span><span class="sxs-lookup"><span data-stu-id="984db-129">-IncludeRender</span></span>
<span data-ttu-id="984db-130">Ha meg van adva, akkor a metrikus lekérdezések információinak megjelenítése szerepelni fog a válaszban.</span><span class="sxs-lookup"><span data-stu-id="984db-130">If specified, rendering information for metric queries will be included in the response.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="984db-131">-IncludeStatistics</span><span class="sxs-lookup"><span data-stu-id="984db-131">-IncludeStatistics</span></span>
<span data-ttu-id="984db-132">Ha meg van adva, a lekérdezési statisztika szerepelni fog a válaszban.</span><span class="sxs-lookup"><span data-stu-id="984db-132">If specified, query statistics will be included in the response.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="984db-133">-Query</span><span class="sxs-lookup"><span data-stu-id="984db-133">-Query</span></span>
<span data-ttu-id="984db-134">A végrehajtani szükséges lekérdezés.</span><span class="sxs-lookup"><span data-stu-id="984db-134">The query to execute.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="984db-135">-Timespan</span><span class="sxs-lookup"><span data-stu-id="984db-135">-Timespan</span></span>
<span data-ttu-id="984db-136">Az az időkeret, amely szerint a lekérdezést meg kell kötni.</span><span class="sxs-lookup"><span data-stu-id="984db-136">The timespan to bound the query by.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="984db-137">-Wait</span><span class="sxs-lookup"><span data-stu-id="984db-137">-Wait</span></span>
<span data-ttu-id="984db-138">A lekérdezés feldolgozásával töltött idő felső határát köti.</span><span class="sxs-lookup"><span data-stu-id="984db-138">Puts an upper bound on the amount of time the server will spend processing the query.</span></span>
<span data-ttu-id="984db-139">Lásd: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span><span class="sxs-lookup"><span data-stu-id="984db-139">See: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="984db-140">-Workspace</span><span class="sxs-lookup"><span data-stu-id="984db-140">-Workspace</span></span>
<span data-ttu-id="984db-141">A munkaterület</span><span class="sxs-lookup"><span data-stu-id="984db-141">The workspace</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="984db-142">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="984db-142">-WorkspaceId</span></span>
<span data-ttu-id="984db-143">A munkaterület azonosítója.</span><span class="sxs-lookup"><span data-stu-id="984db-143">The workspace ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="984db-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="984db-144">CommonParameters</span></span>
<span data-ttu-id="984db-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="984db-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="984db-146">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="984db-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="984db-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="984db-147">INPUTS</span></span>

### <span data-ttu-id="984db-148">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="984db-148">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="984db-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="984db-149">OUTPUTS</span></span>

### <span data-ttu-id="984db-150">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span><span class="sxs-lookup"><span data-stu-id="984db-150">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span></span>

## <span data-ttu-id="984db-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="984db-151">NOTES</span></span>

## <span data-ttu-id="984db-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="984db-152">RELATED LINKS</span></span>
