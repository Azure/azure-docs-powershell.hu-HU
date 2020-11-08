---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryactivitywindow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
ms.openlocfilehash: 5b18af8890d255dbd5514cccc0279acafe6bd611
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014553"
---
# <span data-ttu-id="dd4a5-101">Get-AzDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="dd4a5-101">Get-AzDataFactoryActivityWindow</span></span>

## <span data-ttu-id="dd4a5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dd4a5-102">SYNOPSIS</span></span>
<span data-ttu-id="dd4a5-103">Információt kap az adatgyárhoz társított tevékenység-ablakokról.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-103">Gets information about activity windows associated with a data factory.</span></span>

## <span data-ttu-id="dd4a5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dd4a5-104">SYNTAX</span></span>

### <span data-ttu-id="dd4a5-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dd4a5-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd4a5-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="dd4a5-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd4a5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="dd4a5-107">DESCRIPTION</span></span>
<span data-ttu-id="dd4a5-108">A **Get-AzDataFactoryActivityWindow** parancsmag információt kap az adatfeldolgozó ablakokkal társított tevékenységekről.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-108">The **Get-AzDataFactoryActivityWindow** cmdlet gets information about the activity windows associated with a data factory.</span></span>

## <span data-ttu-id="dd4a5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="dd4a5-109">EXAMPLES</span></span>

### <span data-ttu-id="dd4a5-110">1. példa: az adatfeldolgozóhoz társított Windows-tevékenységek beszerzése</span><span class="sxs-lookup"><span data-stu-id="dd4a5-110">Example 1: Get activity windows associated with a data factory</span></span>
```
PS C:\>Get-AzDataFactoryActivityWindow -DataFactoryName "WikiADF" -ResourceGroupName "ADF" -Top 3
ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : BlobToSqlCopyActivity
ActivityType      : Copy
LinkedServiceName : 
WindowState       : Waiting
WindowSubstate    : ConcurrencyLimit
Duration          : 00:00:00
InputDatasets     : {DA_CuratedWikiData}
OutputDatasets    : {DA_WikiAggregatedData}
PercentComplete   : 0
RunAttempts       : 1
RunStart          : 8/17/2016 10:05:51 PM
RunEnd            : 8/17/2016 10:05:51 PM
WindowStart       : 8/17/2016 6:00:00 AM
WindowEnd         : 8/17/2016 7:00:00 AM


ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : BlobToSqlCopyActivity
ActivityType      : Copy
LinkedServiceName : 
WindowState       : Waiting
WindowSubstate    : ConcurrencyLimit
Duration          : 00:00:00
InputDatasets     : {DA_CuratedWikiData}
OutputDatasets    : {DA_WikiAggregatedData}
PercentComplete   : 0
RunAttempts       : 1
RunStart          : 8/17/2016 10:05:51 PM
RunEnd            : 8/17/2016 10:05:51 PM
WindowStart       : 8/16/2016 10:00:00 PM
WindowEnd         : 8/16/2016 11:00:00 PM


ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : WikiHiveActivity
ActivityType      : HDInsightHive
LinkedServiceName : HDILinkedService
WindowState       : Ready
WindowSubstate    : 
Duration          : 00:03:37.8020000
InputDatasets     : {DA_WikipediaClickEvents}
OutputDatasets    : {DA_CuratedWikiData}
PercentComplete   : 100
RunAttempts       : 1
RunStart          : 8/17/2016 11:09:23 PM
RunEnd            : 8/17/2016 11:13:01 PM
WindowStart       : 8/17/2016 3:00:00 AM
WindowEnd         : 8/17/2016 4:00:00 AM
```

<span data-ttu-id="dd4a5-111">Ez a parancs információt kap a WikiADF nevű adatfeldolgozóval társított összes tevékenység ablakról.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-111">This command gets information about all activity window associated with the data factory named WikiADF.</span></span>

## <span data-ttu-id="dd4a5-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dd4a5-112">PARAMETERS</span></span>

### <span data-ttu-id="dd4a5-113">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="dd4a5-113">-ActivityName</span></span>
<span data-ttu-id="dd4a5-114">A tevékenység nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-114">Specifies the name of the activity.</span></span>
<span data-ttu-id="dd4a5-115">Ez a parancsmag a Windows tevékenységeit a paraméter által megadott tevékenységhez kapja.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-115">This cmdlet gets activity windows for the activity that this parameter specifies.</span></span>

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

### <span data-ttu-id="dd4a5-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="dd4a5-116">-DataFactory</span></span>
<span data-ttu-id="dd4a5-117">Egy parancsmag által visszaadott **PSDataFactory** -objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-117">Specifies a **PSDataFactory** object returned by a cmdlet.</span></span>
<span data-ttu-id="dd4a5-118">Ez a parancsmag azokat a Windows-tevékenységeket kapja meg, amelyek az adatfeldolgozóhoz tartoznak, és ez a paraméter határozza meg.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-118">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd4a5-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="dd4a5-119">-DataFactoryName</span></span>
<span data-ttu-id="dd4a5-120">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-120">Specifies the name of the data factory.</span></span>
<span data-ttu-id="dd4a5-121">Ez a parancsmag azokat a Windows-tevékenységeket kapja meg, amelyek az adatfeldolgozóhoz tartoznak, és ez a paraméter határozza meg.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-121">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd4a5-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="dd4a5-122">-DatasetName</span></span>
<span data-ttu-id="dd4a5-123">Az adatkészlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-123">Specifies the name of the dataset.</span></span>
<span data-ttu-id="dd4a5-124">Ez a parancsmag olyan Windows-tevékenységekre ad választ, amelyek a paraméter által megadott adatkészlethez tartoznak.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-124">This cmdlet gets activity windows that belong to the dataset that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd4a5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd4a5-125">-DefaultProfile</span></span>
<span data-ttu-id="dd4a5-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dd4a5-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd4a5-127">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="dd4a5-127">-Filter</span></span>
<span data-ttu-id="dd4a5-128">A tevékenység ablak az Azure keresési szűrési nyelvhelyességi szolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-128">Specifies the activity window expressed by using Azure Search filter grammar.</span></span>
<span data-ttu-id="dd4a5-129">A nyelvhelyességről további információt az Azure Search OData kifejezés szintaxisa című témakörben talál https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx ( https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) az MSDN webhelyen.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-129">For information about the grammar, see OData Expression Syntax for Azure Searchhttps://msdn.microsoft.com/en-us/library/azure/dn798921.aspx (https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span></span>
<span data-ttu-id="dd4a5-130">A tevékenység Windows-listáját a paraméter által megadott keresési karakterlánc szűri.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-130">The activity windows list is filtered by the search string that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd4a5-131">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="dd4a5-131">-OrderBy</span></span>
<span data-ttu-id="dd4a5-132">Azt adja meg, hogy a tevékenység ablak lista paramétereinek egyike szerint rendelje a választ.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-132">Specifies to order the response by one of the activity window list parameters.</span></span>
<span data-ttu-id="dd4a5-133">Ez a pontosvesszővel tagolt tulajdonságok listája.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-133">This is a list of comma separated properties.</span></span>
<span data-ttu-id="dd4a5-134">Például: WindowStart, KészültségiSzint paraméter értéke.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-134">For example: WindowStart, PercentComplete.</span></span>
<span data-ttu-id="dd4a5-135">Alapértelmezés szerint a sorrend növekvő sorrendű (ASC).</span><span class="sxs-lookup"><span data-stu-id="dd4a5-135">By default, the order is ascending order (ASC).</span></span>
<span data-ttu-id="dd4a5-136">Ha csökkenő sorrendben szeretné rendezni a listát, adja meg a LEÍRÁSát.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-136">Specify DESC if you want to order the list in descending order.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd4a5-137">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="dd4a5-137">-PipelineName</span></span>
<span data-ttu-id="dd4a5-138">A csővezeték nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-138">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="dd4a5-139">Ez a parancsmag olyan Windows-tevékenységeket kap, amelyek a paraméter által megadott csővezetékhez tartoznak.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-139">This cmdlet gets activity windows that belong to the pipeline that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd4a5-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd4a5-140">-ResourceGroupName</span></span>
<span data-ttu-id="dd4a5-141">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-141">Specifies the name of the resource group.</span></span>
<span data-ttu-id="dd4a5-142">Ez a parancsmag olyan Windows-tevékenységekre ad választ, amelyek a paraméter által megadott erőforráscsoport csoportjába tartoznak.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-142">This cmdlet gets activity windows that belong to the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd4a5-143">-RunEnd</span><span class="sxs-lookup"><span data-stu-id="dd4a5-143">-RunEnd</span></span>
<span data-ttu-id="dd4a5-144">A tevékenység ablak befejezési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-144">Specifies the end time of the activity window run.</span></span>
<span data-ttu-id="dd4a5-145">Ez a parancsmag olyan Windows-tevékenységeket kap, amelyek futási ideje a *RunStart* és a *RunEnd* között esik.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-145">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd4a5-146">-RunStart</span><span class="sxs-lookup"><span data-stu-id="dd4a5-146">-RunStart</span></span>
<span data-ttu-id="dd4a5-147">A tevékenység ablak kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-147">Specifies the start time of the activity window run.</span></span>
<span data-ttu-id="dd4a5-148">Ez a parancsmag olyan Windows-tevékenységeket kap, amelyek futási ideje a *RunStart* és a *RunEnd* között esik.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-148">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd4a5-149">-Top</span><span class="sxs-lookup"><span data-stu-id="dd4a5-149">-Top</span></span>
<span data-ttu-id="dd4a5-150">Itt adhatja meg, hogy a Windows hány tevékenységet ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-150">Specifies the maximum number of activity windows that this cmdlet returns.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd4a5-151">-WindowEnd</span><span class="sxs-lookup"><span data-stu-id="dd4a5-151">-WindowEnd</span></span>
<span data-ttu-id="dd4a5-152">A tevékenység befejezése ablak befejezési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-152">Specifies the end time of activity window.</span></span>
<span data-ttu-id="dd4a5-153">Ez a parancsmag olyan Windows-tevékenységeket kap, amelyek időpontja a *WindowStart* és a *WindowEnd* időpontja között esik.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-153">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd4a5-154">-WindowStart</span><span class="sxs-lookup"><span data-stu-id="dd4a5-154">-WindowStart</span></span>
<span data-ttu-id="dd4a5-155">A tevékenység ablak kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-155">Specifies the start time of activity window.</span></span>
<span data-ttu-id="dd4a5-156">Ez a parancsmag olyan Windows-tevékenységeket kap, amelyek időpontja a *WindowStart* és a *WindowEnd* időpontja között esik.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-156">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd4a5-157">-WindowState</span><span class="sxs-lookup"><span data-stu-id="dd4a5-157">-WindowState</span></span>
<span data-ttu-id="dd4a5-158">A tevékenység ablak állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-158">Specifies the state of the activity window.</span></span>
<span data-ttu-id="dd4a5-159">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="dd4a5-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dd4a5-160">Nincs</span><span class="sxs-lookup"><span data-stu-id="dd4a5-160">None</span></span>
- <span data-ttu-id="dd4a5-161">Várakozás</span><span class="sxs-lookup"><span data-stu-id="dd4a5-161">Waiting</span></span>
- <span data-ttu-id="dd4a5-162">Előrehaladás</span><span class="sxs-lookup"><span data-stu-id="dd4a5-162">InProgress</span></span>
- <span data-ttu-id="dd4a5-163">Kész</span><span class="sxs-lookup"><span data-stu-id="dd4a5-163">Ready</span></span>
- <span data-ttu-id="dd4a5-164">Sikertelen</span><span class="sxs-lookup"><span data-stu-id="dd4a5-164">Failed</span></span>
- <span data-ttu-id="dd4a5-165">Kihagyva: Ez a parancsmag olyan Windows-tevékenységeket kap, amelyek abban az állapotban vannak, hogy ez a paraméter adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-165">Skipped This cmdlet gets activity windows that are in the state that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd4a5-166">-WindowSubstate</span><span class="sxs-lookup"><span data-stu-id="dd4a5-166">-WindowSubstate</span></span>
<span data-ttu-id="dd4a5-167">A tevékenység ablak alállapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-167">Specifies the substate of the activity window.</span></span>
<span data-ttu-id="dd4a5-168">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="dd4a5-168">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dd4a5-169">Visszavont</span><span class="sxs-lookup"><span data-stu-id="dd4a5-169">Canceled</span></span>
- <span data-ttu-id="dd4a5-170">timedOut</span><span class="sxs-lookup"><span data-stu-id="dd4a5-170">timedOut</span></span>
- <span data-ttu-id="dd4a5-171">A parancsmag érvényesítése olyan Windows-tevékenységeket kap, amelyek abban az alállamban vannak, hogy ez a paraméter adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd4a5-171">Validating This cmdlet gets activity windows that are in the substate that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd4a5-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd4a5-172">CommonParameters</span></span>
<span data-ttu-id="dd4a5-173">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dd4a5-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd4a5-174">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd4a5-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd4a5-175">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd4a5-175">INPUTS</span></span>

### <span data-ttu-id="dd4a5-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="dd4a5-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="dd4a5-177">System. String</span><span class="sxs-lookup"><span data-stu-id="dd4a5-177">System.String</span></span>

### <span data-ttu-id="dd4a5-178">System. null ' 1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="dd4a5-178">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="dd4a5-179">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="dd4a5-179">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="dd4a5-180">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd4a5-180">OUTPUTS</span></span>

### <span data-ttu-id="dd4a5-181">Microsoft. Azure. Command. DataFactories. models. PSActivityWindow</span><span class="sxs-lookup"><span data-stu-id="dd4a5-181">Microsoft.Azure.Commands.DataFactories.Models.PSActivityWindow</span></span>

## <span data-ttu-id="dd4a5-182">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dd4a5-182">NOTES</span></span>

## <span data-ttu-id="dd4a5-183">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd4a5-183">RELATED LINKS</span></span>

[<span data-ttu-id="dd4a5-184">Azure adatgyárak parancsmagok</span><span class="sxs-lookup"><span data-stu-id="dd4a5-184">Azure Data Factories Cmdlets</span></span>](./Az.DataFactory.md)


