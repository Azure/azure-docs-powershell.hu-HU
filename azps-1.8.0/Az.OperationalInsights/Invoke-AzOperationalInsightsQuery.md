---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/invoke-azoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
ms.openlocfilehash: 64a7835f1401e8b256e6f549203baaf8e8191606
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669856"
---
# <span data-ttu-id="3916e-101">Invoke-AzOperationalInsightsQuery</span><span class="sxs-lookup"><span data-stu-id="3916e-101">Invoke-AzOperationalInsightsQuery</span></span>

## <span data-ttu-id="3916e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3916e-102">SYNOPSIS</span></span>
<span data-ttu-id="3916e-103">A megadott paraméterek alapján adja eredményül a találatokat.</span><span class="sxs-lookup"><span data-stu-id="3916e-103">Returns search results based on the specified parameters.</span></span>

## <span data-ttu-id="3916e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3916e-104">SYNTAX</span></span>

### <span data-ttu-id="3916e-105">ByWorkspaceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3916e-105">ByWorkspaceId (Default)</span></span>
```
Invoke-AzOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>] [-Wait <Int32>]
 [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3916e-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3916e-106">ByWorkspaceObject</span></span>
```
Invoke-AzOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3916e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3916e-107">DESCRIPTION</span></span>
<span data-ttu-id="3916e-108">A **meghívó-AzOperationalInsightsQuery** parancsmag a megadott paraméterek alapján adja eredményül a találatokat.</span><span class="sxs-lookup"><span data-stu-id="3916e-108">The **Invoke-AzOperationalInsightsQuery** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="3916e-109">A keresés állapotát a visszaadott objektum metaadat tulajdonságában érheti el.</span><span class="sxs-lookup"><span data-stu-id="3916e-109">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="3916e-110">Ha az állapot függőben van, akkor a keresés nem fejeződött be, és az eredmény az archívumból fog szerepelni.</span><span class="sxs-lookup"><span data-stu-id="3916e-110">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="3916e-111">A keresés eredményét a visszaadott objektum Value tulajdonságában olvashatja le.</span><span class="sxs-lookup"><span data-stu-id="3916e-111">You can retrieve the results of the search from the Value property of the returned object.</span></span>

## <span data-ttu-id="3916e-112">Példák</span><span class="sxs-lookup"><span data-stu-id="3916e-112">EXAMPLES</span></span>

### <span data-ttu-id="3916e-113">1. példa: keresési eredmények lekérdezéssel történő beszerzése</span><span class="sxs-lookup"><span data-stu-id="3916e-113">Example 1: Get search results using a query</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="3916e-114">A meghívást követően a $queryResults. Results a lekérdezésből származó összes sort fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="3916e-114">Once invoked, $queryResults.Results will contain all of the resulting rows from your query.</span></span>

### <span data-ttu-id="3916e-115">2. példa: $results konvertálása Eredmény IEnumberable egy tömbhöz</span><span class="sxs-lookup"><span data-stu-id="3916e-115">Example 2: Convert $results.Result IEnumberable to an array</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($results.Results)
...
```

<span data-ttu-id="3916e-116">Egyes lekérdezések nagyon nagy mennyiségű adatkészletet adhatnak eredményül.</span><span class="sxs-lookup"><span data-stu-id="3916e-116">Some queries can result in very large data sets being returned.</span></span> <span data-ttu-id="3916e-117">Emiatt a parancsmag alapértelmezett viselkedése egy IEnumerable visszaadása a memória költségeinek csökkentéséhez.</span><span class="sxs-lookup"><span data-stu-id="3916e-117">Because of this, the default behavior of the cmdlet is to return an IEnumerable to reduce memory costs.</span></span> <span data-ttu-id="3916e-118">Ha a találatok tömbjét szeretné használni, a LINQ enumerable. ToArray () kiterjesztési módszerrel konvertálhatja a IEnumerable tömböra.</span><span class="sxs-lookup"><span data-stu-id="3916e-118">If you'd prefer to have an array of results, you can use the LINQ Enumerable.ToArray() extension method to convert the IEnumerable to an array.</span></span>

### <span data-ttu-id="3916e-119">3. példa: a keresési eredmények lekérdezése meghatározott időkereten keresztüli lekérdezéssel</span><span class="sxs-lookup"><span data-stu-id="3916e-119">Example 3: Get search results using a query over a specific timeframe</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="3916e-120">A lekérdezés eredményei az elmúlt 24 órára korlátozódnak.</span><span class="sxs-lookup"><span data-stu-id="3916e-120">The results from this query will be limited to the past 24 hours.</span></span>

### <span data-ttu-id="3916e-121">Példa 4: a lekérdezés eredményében megjelenített & statisztikájának befoglalása</span><span class="sxs-lookup"><span data-stu-id="3916e-121">Example 4: Include render & statistics in query result</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

<span data-ttu-id="3916e-122">További információt a [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) Megjelenítés és a statisztikai adatok című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="3916e-122">See [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) for details on the render and statistics info.</span></span>

## <span data-ttu-id="3916e-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3916e-123">PARAMETERS</span></span>

### <span data-ttu-id="3916e-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3916e-124">-AsJob</span></span>
<span data-ttu-id="3916e-125">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3916e-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3916e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3916e-126">-DefaultProfile</span></span>
<span data-ttu-id="3916e-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3916e-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3916e-128">-IncludeRender</span><span class="sxs-lookup"><span data-stu-id="3916e-128">-IncludeRender</span></span>
<span data-ttu-id="3916e-129">Ha meg van adva, akkor a metrika-lekérdezések megjelenítési adatai is szerepelni fognak a válaszban.</span><span class="sxs-lookup"><span data-stu-id="3916e-129">If specified, rendering information for metric queries will be included in the response.</span></span>

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

### <span data-ttu-id="3916e-130">-IncludeStatistics</span><span class="sxs-lookup"><span data-stu-id="3916e-130">-IncludeStatistics</span></span>
<span data-ttu-id="3916e-131">Ha meg van adva, a lekérdezés statisztikája is szerepelni fog a válaszban.</span><span class="sxs-lookup"><span data-stu-id="3916e-131">If specified, query statistics will be included in the response.</span></span>

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

### <span data-ttu-id="3916e-132">-Query</span><span class="sxs-lookup"><span data-stu-id="3916e-132">-Query</span></span>
<span data-ttu-id="3916e-133">A végrehajtandó lekérdezés.</span><span class="sxs-lookup"><span data-stu-id="3916e-133">The query to execute.</span></span>

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

### <span data-ttu-id="3916e-134">-Időszak</span><span class="sxs-lookup"><span data-stu-id="3916e-134">-Timespan</span></span>
<span data-ttu-id="3916e-135">A lekérdezés által kötött időszak.</span><span class="sxs-lookup"><span data-stu-id="3916e-135">The timespan to bound the query by.</span></span>

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

### <span data-ttu-id="3916e-136">– Várjon</span><span class="sxs-lookup"><span data-stu-id="3916e-136">-Wait</span></span>
<span data-ttu-id="3916e-137">Felső határt ad arra az időmennyiségre, amikor a kiszolgáló a lekérdezés feldolgozását fogja tölteni.</span><span class="sxs-lookup"><span data-stu-id="3916e-137">Puts an upper bound on the amount of time the server will spend processing the query.</span></span>
<span data-ttu-id="3916e-138">Olvassa el https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span><span class="sxs-lookup"><span data-stu-id="3916e-138">See: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span></span>

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

### <span data-ttu-id="3916e-139">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="3916e-139">-Workspace</span></span>
<span data-ttu-id="3916e-140">A munkaterület</span><span class="sxs-lookup"><span data-stu-id="3916e-140">The workspace</span></span>

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

### <span data-ttu-id="3916e-141">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="3916e-141">-WorkspaceId</span></span>
<span data-ttu-id="3916e-142">A munkaterület-azonosító.</span><span class="sxs-lookup"><span data-stu-id="3916e-142">The workspace ID.</span></span>

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

### <span data-ttu-id="3916e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3916e-143">CommonParameters</span></span>
<span data-ttu-id="3916e-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3916e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3916e-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3916e-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3916e-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3916e-146">INPUTS</span></span>

### <span data-ttu-id="3916e-147">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="3916e-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="3916e-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3916e-148">OUTPUTS</span></span>

### <span data-ttu-id="3916e-149">Microsoft. Azure. Command. OperationalInsights. models. PSQueryResponse</span><span class="sxs-lookup"><span data-stu-id="3916e-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span></span>

## <span data-ttu-id="3916e-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3916e-150">NOTES</span></span>

## <span data-ttu-id="3916e-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3916e-151">RELATED LINKS</span></span>
