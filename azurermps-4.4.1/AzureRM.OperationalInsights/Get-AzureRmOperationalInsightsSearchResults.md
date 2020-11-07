---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 438F549D-1AF6-49FE-83AC-B45BAB701AB6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSearchResults.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSearchResults.md
ms.openlocfilehash: 161365ee947a118221fa922ab9e7d05486d3908d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679381"
---
# <span data-ttu-id="2fa96-101">Get-AzureRmOperationalInsightsSearchResults</span><span class="sxs-lookup"><span data-stu-id="2fa96-101">Get-AzureRmOperationalInsightsSearchResults</span></span>

## <span data-ttu-id="2fa96-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2fa96-102">SYNOPSIS</span></span>
<span data-ttu-id="2fa96-103">A megadott paraméterek alapján adja eredményül a találatokat.</span><span class="sxs-lookup"><span data-stu-id="2fa96-103">Returns search results based on the specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fa96-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2fa96-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSearchResults [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Top] <Int64>] [[-PreHighlight] <String>] [[-PostHighlight] <String>] [[-Query] <String>]
 [[-Start] <DateTime>] [[-End] <DateTime>] [[-Id] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2fa96-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2fa96-105">DESCRIPTION</span></span>
<span data-ttu-id="2fa96-106">A **Get-AzureRmOperationalInsightsSearchResults** parancsmag a megadott paraméterek alapján adja eredményül a találatokat.</span><span class="sxs-lookup"><span data-stu-id="2fa96-106">The **Get-AzureRmOperationalInsightsSearchResults** cmdlet returns the search results based on the specified parameters.</span></span>

<span data-ttu-id="2fa96-107">A keresés állapotát a visszaadott objektum metaadat tulajdonságában érheti el.</span><span class="sxs-lookup"><span data-stu-id="2fa96-107">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="2fa96-108">Ha az állapot függőben van, akkor a keresés nem fejeződött be, és az eredmény az archívumból fog szerepelni.</span><span class="sxs-lookup"><span data-stu-id="2fa96-108">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>

<span data-ttu-id="2fa96-109">A keresés eredményét a visszaadott objektum Value tulajdonságában olvashatja le.</span><span class="sxs-lookup"><span data-stu-id="2fa96-109">You can retrieve the results of the search from the Value property of the returned object.</span></span>

## <span data-ttu-id="2fa96-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2fa96-110">EXAMPLES</span></span>

### <span data-ttu-id="2fa96-111">1. példa: keresési eredmények lekérdezéssel történő beszerzése</span><span class="sxs-lookup"><span data-stu-id="2fa96-111">Example 1: Get search results using a query</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Query "Type=Event" -Top 100
```

<span data-ttu-id="2fa96-112">Ez a parancs lekérdezéssel kapja meg a találatokat.</span><span class="sxs-lookup"><span data-stu-id="2fa96-112">This command gets all search results by using a query.</span></span>

### <span data-ttu-id="2fa96-113">2. példa: a keresési eredmények beolvasása AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="2fa96-113">Example 2: Get search results using an ID</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Id "ContosoSearchId"
```

<span data-ttu-id="2fa96-114">Ez a parancs AZONOSÍTÓval nyeri a találatokat.</span><span class="sxs-lookup"><span data-stu-id="2fa96-114">This command gets search results by using an ID.</span></span>

### <span data-ttu-id="2fa96-115">3. példa: várakozás a keresésre az eredmények megjelenítése előtt</span><span class="sxs-lookup"><span data-stu-id="2fa96-115">Example 3: Wait for a search to complete before displaying results</span></span>
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

<span data-ttu-id="2fa96-116">Ebben a parancsfájlban a keresés elindul, és addig vár, amíg az eredmény meg nem jelenik.</span><span class="sxs-lookup"><span data-stu-id="2fa96-116">This script starts a search and waits until it completes before displaying the results.</span></span>

## <span data-ttu-id="2fa96-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2fa96-117">PARAMETERS</span></span>

### <span data-ttu-id="2fa96-118">-End</span><span class="sxs-lookup"><span data-stu-id="2fa96-118">-End</span></span>
<span data-ttu-id="2fa96-119">A lekérdezett időtartomány vége</span><span class="sxs-lookup"><span data-stu-id="2fa96-119">End of the queried time range.</span></span>

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

### <span data-ttu-id="2fa96-120">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="2fa96-120">-Id</span></span>
<span data-ttu-id="2fa96-121">Ha meg van adva egy azonosító, az adott azonosító keresési eredményei az eredeti lekérdezési paraméterekkel lesznek beolvasva.</span><span class="sxs-lookup"><span data-stu-id="2fa96-121">If an id is given, the search results for that id will be retrieved using the original query parameters.</span></span>

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

### <span data-ttu-id="2fa96-122">-PostHighlight</span><span class="sxs-lookup"><span data-stu-id="2fa96-122">-PostHighlight</span></span>
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

### <span data-ttu-id="2fa96-123">-Kiemelés</span><span class="sxs-lookup"><span data-stu-id="2fa96-123">-PreHighlight</span></span>
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

### <span data-ttu-id="2fa96-124">-Query</span><span class="sxs-lookup"><span data-stu-id="2fa96-124">-Query</span></span>
<span data-ttu-id="2fa96-125">A végrehajtandó keresési lekérdezés.</span><span class="sxs-lookup"><span data-stu-id="2fa96-125">The search query that will be executed.</span></span>

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

### <span data-ttu-id="2fa96-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fa96-126">-ResourceGroupName</span></span>
<span data-ttu-id="2fa96-127">Annak a csoportnak a neve, amely a munkaterületet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="2fa96-127">The name of the resource group that contains the workspace.</span></span>

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

### <span data-ttu-id="2fa96-128">– Első lépések</span><span class="sxs-lookup"><span data-stu-id="2fa96-128">-Start</span></span>
<span data-ttu-id="2fa96-129">A lekérdezett időtartomány kezdése</span><span class="sxs-lookup"><span data-stu-id="2fa96-129">Start of the queried time range.</span></span>

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

### <span data-ttu-id="2fa96-130">-Top</span><span class="sxs-lookup"><span data-stu-id="2fa96-130">-Top</span></span>
<span data-ttu-id="2fa96-131">A visszaadott találatok maximális száma, a 5000-ra korlátozva.</span><span class="sxs-lookup"><span data-stu-id="2fa96-131">The maximum number of results to be returned, limited to 5000.</span></span>

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

### <span data-ttu-id="2fa96-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2fa96-132">-WorkspaceName</span></span>
<span data-ttu-id="2fa96-133">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fa96-133">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="2fa96-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fa96-134">-DefaultProfile</span></span>
<span data-ttu-id="2fa96-135">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2fa96-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fa96-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fa96-136">CommonParameters</span></span>
<span data-ttu-id="2fa96-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2fa96-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fa96-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fa96-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fa96-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2fa96-139">INPUTS</span></span>

## <span data-ttu-id="2fa96-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2fa96-140">OUTPUTS</span></span>

### <span data-ttu-id="2fa96-141">PSSearchGetSearchResultsResponse</span><span class="sxs-lookup"><span data-stu-id="2fa96-141">PSSearchGetSearchResultsResponse</span></span>
<span data-ttu-id="2fa96-142">A **PSSearchGetSearchResultsResponse** objektum tartalmaz egy olyan Value tulajdonságot, amely tartalmazza a keresésből JSON formátumban visszaadott rekordokat, valamint egy metaadat-objektumot, amely a keresés eredményére vonatkozó információkat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="2fa96-142">The **PSSearchGetSearchResultsResponse** object includes a Value property that includes the records returned from the search in JSON format and a metadata object that includes information about the results of the search.</span></span>

## <span data-ttu-id="2fa96-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2fa96-143">NOTES</span></span>

## <span data-ttu-id="2fa96-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2fa96-144">RELATED LINKS</span></span>

[<span data-ttu-id="2fa96-145">Get-AzureRmOperationalInsightsSavedSearchResults</span><span class="sxs-lookup"><span data-stu-id="2fa96-145">Get-AzureRmOperationalInsightsSavedSearchResults</span></span>](./Get-AzureRmOperationalInsightsSavedSearchResults.md)


