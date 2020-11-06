---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 438F549D-1AF6-49FE-83AC-B45BAB701AB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightssearchresults
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSearchResults.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSearchResults.md
ms.openlocfilehash: 547988d2079f35b82af3638e3e4f09b101d8fbe4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491889"
---
# <span data-ttu-id="f5aea-101">Get-AzureRmOperationalInsightsSearchResults</span><span class="sxs-lookup"><span data-stu-id="f5aea-101">Get-AzureRmOperationalInsightsSearchResults</span></span>

## <span data-ttu-id="f5aea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f5aea-102">SYNOPSIS</span></span>
<span data-ttu-id="f5aea-103">A megadott paraméterek alapján adja eredményül a találatokat.</span><span class="sxs-lookup"><span data-stu-id="f5aea-103">Returns search results based on the specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5aea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f5aea-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSearchResults [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Top] <Int64>] [[-PreHighlight] <String>] [[-PostHighlight] <String>] [[-Query] <String>]
 [[-Start] <DateTime>] [[-End] <DateTime>] [[-Id] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5aea-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f5aea-105">DESCRIPTION</span></span>
<span data-ttu-id="f5aea-106">A **Get-AzureRmOperationalInsightsSearchResults** parancsmag a megadott paraméterek alapján adja eredményül a találatokat.</span><span class="sxs-lookup"><span data-stu-id="f5aea-106">The **Get-AzureRmOperationalInsightsSearchResults** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="f5aea-107">A keresés állapotát a visszaadott objektum metaadat tulajdonságában érheti el.</span><span class="sxs-lookup"><span data-stu-id="f5aea-107">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="f5aea-108">Ha az állapot függőben van, akkor a keresés nem fejeződött be, és az eredmény az archívumból fog szerepelni.</span><span class="sxs-lookup"><span data-stu-id="f5aea-108">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="f5aea-109">A keresés eredményét a visszaadott objektum Value tulajdonságában olvashatja le.</span><span class="sxs-lookup"><span data-stu-id="f5aea-109">You can retrieve the results of the search from the Value property of the returned object.</span></span>

## <span data-ttu-id="f5aea-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f5aea-110">EXAMPLES</span></span>

### <span data-ttu-id="f5aea-111">1. példa: keresési eredmények lekérdezéssel történő beszerzése</span><span class="sxs-lookup"><span data-stu-id="f5aea-111">Example 1: Get search results using a query</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Query "Type=Event" -Top 100
```

<span data-ttu-id="f5aea-112">Ez a parancs lekérdezéssel kapja meg a találatokat.</span><span class="sxs-lookup"><span data-stu-id="f5aea-112">This command gets all search results by using a query.</span></span>

### <span data-ttu-id="f5aea-113">2. példa: a keresési eredmények beolvasása AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="f5aea-113">Example 2: Get search results using an ID</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Id "ContosoSearchId"
```

<span data-ttu-id="f5aea-114">Ez a parancs AZONOSÍTÓval nyeri a találatokat.</span><span class="sxs-lookup"><span data-stu-id="f5aea-114">This command gets search results by using an ID.</span></span>

### <span data-ttu-id="f5aea-115">3. példa: várakozás a keresésre az eredmények megjelenítése előtt</span><span class="sxs-lookup"><span data-stu-id="f5aea-115">Example 3: Wait for a search to complete before displaying results</span></span>
```
PS C:\>$error.clear()
$response = @{}
$StartTime = Get-Date

$resGroup = "ContosoResourceGroup"
$wrkspace = "ContosoWorkspace"

# Sample Query
$query = "Type=Event"

# Get Initial response
$response = Get-AzureRmOperationalInsightsSearchResults -WorkspaceName $wrkspace -ResourceGroupName $resGroup -Query $query -Top 15000
$elapsedTime = $(get-date) - $script:StartTime
Write-Host "Elapsed: " $elapsedTime "Status: " $response.Metadata.Status

# Split and extract request Id
$reqIdParts = $response.Id.Split("/")
$reqId = $reqIdParts[$reqIdParts.Count -1]

# Poll if pending
while($response.Metadata.Status -eq "Pending" -and $error.Count -eq 0) {
    $response = Get-AzureRmOperationalInsightsSearchResults -WorkspaceName $wrkspace -ResourceGroupName $resGroup -Id $reqId
    $elapsedTime = $(get-date) - $script:StartTime
    Write-Host "Elapsed: " $elapsedTime "Status: " $response.Metadata.Status
}

Write-Host "Returned " $response.Value.Count " documents"
Write-Host $error
```

<span data-ttu-id="f5aea-116">Ebben a parancsfájlban a keresés elindul, és addig vár, amíg az eredmény meg nem jelenik.</span><span class="sxs-lookup"><span data-stu-id="f5aea-116">This script starts a search and waits until it completes before displaying the results.</span></span>

## <span data-ttu-id="f5aea-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f5aea-117">PARAMETERS</span></span>

### <span data-ttu-id="f5aea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5aea-118">-DefaultProfile</span></span>
<span data-ttu-id="f5aea-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f5aea-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5aea-120">-End</span><span class="sxs-lookup"><span data-stu-id="f5aea-120">-End</span></span>
<span data-ttu-id="f5aea-121">A lekérdezett időtartomány vége</span><span class="sxs-lookup"><span data-stu-id="f5aea-121">End of the queried time range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5aea-122">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="f5aea-122">-Id</span></span>
<span data-ttu-id="f5aea-123">Ha meg van adva egy azonosító, az adott azonosító keresési eredményei az eredeti lekérdezési paraméterekkel lesznek beolvasva.</span><span class="sxs-lookup"><span data-stu-id="f5aea-123">If an id is given, the search results for that id will be retrieved using the original query parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5aea-124">-PostHighlight</span><span class="sxs-lookup"><span data-stu-id="f5aea-124">-PostHighlight</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5aea-125">-Kiemelés</span><span class="sxs-lookup"><span data-stu-id="f5aea-125">-PreHighlight</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5aea-126">-Query</span><span class="sxs-lookup"><span data-stu-id="f5aea-126">-Query</span></span>
<span data-ttu-id="f5aea-127">A végrehajtandó keresési lekérdezés.</span><span class="sxs-lookup"><span data-stu-id="f5aea-127">The search query that will be executed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5aea-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5aea-128">-ResourceGroupName</span></span>
<span data-ttu-id="f5aea-129">Annak a csoportnak a neve, amely a munkaterületet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="f5aea-129">The name of the resource group that contains the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5aea-130">– Első lépések</span><span class="sxs-lookup"><span data-stu-id="f5aea-130">-Start</span></span>
<span data-ttu-id="f5aea-131">A lekérdezett időtartomány kezdése</span><span class="sxs-lookup"><span data-stu-id="f5aea-131">Start of the queried time range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5aea-132">-Top</span><span class="sxs-lookup"><span data-stu-id="f5aea-132">-Top</span></span>
<span data-ttu-id="f5aea-133">A visszaadott találatok maximális száma, a 5000-ra korlátozva.</span><span class="sxs-lookup"><span data-stu-id="f5aea-133">The maximum number of results to be returned, limited to 5000.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: 10
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5aea-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f5aea-134">-WorkspaceName</span></span>
<span data-ttu-id="f5aea-135">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f5aea-135">Specifies a workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5aea-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5aea-136">CommonParameters</span></span>
<span data-ttu-id="f5aea-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f5aea-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5aea-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5aea-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5aea-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5aea-139">INPUTS</span></span>

### <span data-ttu-id="f5aea-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f5aea-140">System.String</span></span>

### <span data-ttu-id="f5aea-141">System. Int64</span><span class="sxs-lookup"><span data-stu-id="f5aea-141">System.Int64</span></span>

### <span data-ttu-id="f5aea-142">System. null ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f5aea-142">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="f5aea-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5aea-143">OUTPUTS</span></span>

### <span data-ttu-id="f5aea-144">Microsoft. Azure. Command. OperationalInsights. models. PSSearchGetSearchResultsResponse</span><span class="sxs-lookup"><span data-stu-id="f5aea-144">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="f5aea-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f5aea-145">NOTES</span></span>

## <span data-ttu-id="f5aea-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5aea-146">RELATED LINKS</span></span>

[<span data-ttu-id="f5aea-147">Get-AzureRmOperationalInsightsSavedSearchResults</span><span class="sxs-lookup"><span data-stu-id="f5aea-147">Get-AzureRmOperationalInsightsSavedSearchResults</span></span>](./Get-AzureRmOperationalInsightsSavedSearchResults.md)


