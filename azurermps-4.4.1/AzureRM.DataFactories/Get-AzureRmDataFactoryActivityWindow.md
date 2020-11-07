---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryActivityWindow.md
ms.openlocfilehash: 95d0ce0ffe48f845c15f7f00de59a70bfc466fe3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672230"
---
# <span data-ttu-id="100f8-101">Get-AzureRmDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="100f8-101">Get-AzureRmDataFactoryActivityWindow</span></span>

## <span data-ttu-id="100f8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="100f8-102">SYNOPSIS</span></span>
<span data-ttu-id="100f8-103">Információt kap az adatgyárhoz társított tevékenység-ablakokról.</span><span class="sxs-lookup"><span data-stu-id="100f8-103">Gets information about activity windows associated with a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="100f8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="100f8-104">SYNTAX</span></span>

### <span data-ttu-id="100f8-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="100f8-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="100f8-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="100f8-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="100f8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="100f8-107">DESCRIPTION</span></span>
<span data-ttu-id="100f8-108">A **Get-AzureRmDataFactoryActivityWindow** parancsmag információt kap az adatfeldolgozó ablakokkal társított tevékenységekről.</span><span class="sxs-lookup"><span data-stu-id="100f8-108">The **Get-AzureRmDataFactoryActivityWindow** cmdlet gets information about the activity windows associated with a data factory.</span></span>

## <span data-ttu-id="100f8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="100f8-109">EXAMPLES</span></span>

### <span data-ttu-id="100f8-110">1. példa: az adatfeldolgozóhoz társított Windows-tevékenységek beszerzése</span><span class="sxs-lookup"><span data-stu-id="100f8-110">Example 1: Get activity windows associated with a data factory</span></span>
```
PS C:\>Get-AzureRmDataFactoryActivityWindow -DataFactoryName "WikiADF" -ResourceGroupName "ADF" -Top 3
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

<span data-ttu-id="100f8-111">Ez a parancs információt kap a WikiADF nevű adatfeldolgozóval társított összes tevékenység ablakról.</span><span class="sxs-lookup"><span data-stu-id="100f8-111">This command gets information about all activity window associated with the data factory named WikiADF.</span></span>

## <span data-ttu-id="100f8-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="100f8-112">PARAMETERS</span></span>

### <span data-ttu-id="100f8-113">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="100f8-113">-ActivityName</span></span>
<span data-ttu-id="100f8-114">A tevékenység nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="100f8-114">Specifies the name of the activity.</span></span>
<span data-ttu-id="100f8-115">Ez a parancsmag a Windows tevékenységeit a paraméter által megadott tevékenységhez kapja.</span><span class="sxs-lookup"><span data-stu-id="100f8-115">This cmdlet gets activity windows for the activity that this parameter specifies.</span></span>

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

### <span data-ttu-id="100f8-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="100f8-116">-DataFactory</span></span>
<span data-ttu-id="100f8-117">Egy parancsmag által visszaadott **PSDataFactory** -objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="100f8-117">Specifies a **PSDataFactory** object returned by a cmdlet.</span></span>
<span data-ttu-id="100f8-118">Ez a parancsmag azokat a Windows-tevékenységeket kapja meg, amelyek az adatfeldolgozóhoz tartoznak, és ez a paraméter határozza meg.</span><span class="sxs-lookup"><span data-stu-id="100f8-118">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="100f8-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="100f8-119">-DataFactoryName</span></span>
<span data-ttu-id="100f8-120">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="100f8-120">Specifies the name of the data factory.</span></span>
<span data-ttu-id="100f8-121">Ez a parancsmag azokat a Windows-tevékenységeket kapja meg, amelyek az adatfeldolgozóhoz tartoznak, és ez a paraméter határozza meg.</span><span class="sxs-lookup"><span data-stu-id="100f8-121">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="100f8-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="100f8-122">-DatasetName</span></span>
<span data-ttu-id="100f8-123">Az adatkészlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="100f8-123">Specifies the name of the dataset.</span></span>
<span data-ttu-id="100f8-124">Ez a parancsmag olyan Windows-tevékenységekre ad választ, amelyek a paraméter által megadott adatkészlethez tartoznak.</span><span class="sxs-lookup"><span data-stu-id="100f8-124">This cmdlet gets activity windows that belong to the dataset that this parameter specifies.</span></span>

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

### <span data-ttu-id="100f8-125">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="100f8-125">-Filter</span></span>
<span data-ttu-id="100f8-126">A tevékenység ablak az Azure keresési szűrési nyelvhelyességi szolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="100f8-126">Specifies the activity window expressed by using Azure Search filter grammar.</span></span>
<span data-ttu-id="100f8-127">A nyelvhelyességről további információt az Azure Search OData kifejezés szintaxisa című témakörben talál https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx ( https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) az MSDN webhelyen.</span><span class="sxs-lookup"><span data-stu-id="100f8-127">For information about the grammar, see OData Expression Syntax for Azure Searchhttps://msdn.microsoft.com/en-us/library/azure/dn798921.aspx (https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span></span>
<span data-ttu-id="100f8-128">A tevékenység Windows-listáját a paraméter által megadott keresési karakterlánc szűri.</span><span class="sxs-lookup"><span data-stu-id="100f8-128">The activity windows list is filtered by the search string that this parameter specifies.</span></span>

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

### <span data-ttu-id="100f8-129">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="100f8-129">-OrderBy</span></span>
<span data-ttu-id="100f8-130">Azt adja meg, hogy a tevékenység ablak lista paramétereinek egyike szerint rendelje a választ.</span><span class="sxs-lookup"><span data-stu-id="100f8-130">Specifies to order the response by one of the activity window list parameters.</span></span>
<span data-ttu-id="100f8-131">Ez a pontosvesszővel tagolt tulajdonságok listája.</span><span class="sxs-lookup"><span data-stu-id="100f8-131">This is a list of comma separated properties.</span></span>
<span data-ttu-id="100f8-132">Például: WindowStart, KészültségiSzint paraméter értéke.</span><span class="sxs-lookup"><span data-stu-id="100f8-132">For example: WindowStart, PercentComplete.</span></span>

<span data-ttu-id="100f8-133">Alapértelmezés szerint a sorrend növekvő sorrendű (ASC).</span><span class="sxs-lookup"><span data-stu-id="100f8-133">By default, the order is ascending order (ASC).</span></span>
<span data-ttu-id="100f8-134">Ha csökkenő sorrendben szeretné rendezni a listát, adja meg a LEÍRÁSát.</span><span class="sxs-lookup"><span data-stu-id="100f8-134">Specify DESC if you want to order the list in descending order.</span></span>

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

### <span data-ttu-id="100f8-135">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="100f8-135">-PipelineName</span></span>
<span data-ttu-id="100f8-136">A csővezeték nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="100f8-136">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="100f8-137">Ez a parancsmag olyan Windows-tevékenységeket kap, amelyek a paraméter által megadott csővezetékhez tartoznak.</span><span class="sxs-lookup"><span data-stu-id="100f8-137">This cmdlet gets activity windows that belong to the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="100f8-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="100f8-138">-ResourceGroupName</span></span>
<span data-ttu-id="100f8-139">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="100f8-139">Specifies the name of the resource group.</span></span>
<span data-ttu-id="100f8-140">Ez a parancsmag olyan Windows-tevékenységekre ad választ, amelyek a paraméter által megadott erőforráscsoport csoportjába tartoznak.</span><span class="sxs-lookup"><span data-stu-id="100f8-140">This cmdlet gets activity windows that belong to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="100f8-141">-RunEnd</span><span class="sxs-lookup"><span data-stu-id="100f8-141">-RunEnd</span></span>
<span data-ttu-id="100f8-142">A tevékenység ablak befejezési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="100f8-142">Specifies the end time of the activity window run.</span></span>
<span data-ttu-id="100f8-143">Ez a parancsmag olyan Windows-tevékenységeket kap, amelyek futási ideje a *RunStart* és a *RunEnd* között esik.</span><span class="sxs-lookup"><span data-stu-id="100f8-143">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="100f8-144">-RunStart</span><span class="sxs-lookup"><span data-stu-id="100f8-144">-RunStart</span></span>
<span data-ttu-id="100f8-145">A tevékenység ablak kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="100f8-145">Specifies the start time of the activity window run.</span></span>
<span data-ttu-id="100f8-146">Ez a parancsmag olyan Windows-tevékenységeket kap, amelyek futási ideje a *RunStart* és a *RunEnd* között esik.</span><span class="sxs-lookup"><span data-stu-id="100f8-146">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="100f8-147">-Top</span><span class="sxs-lookup"><span data-stu-id="100f8-147">-Top</span></span>
<span data-ttu-id="100f8-148">Itt adhatja meg, hogy a Windows hány tevékenységet ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="100f8-148">Specifies the maximum number of activity windows that this cmdlet returns.</span></span>

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

### <span data-ttu-id="100f8-149">-WindowEnd</span><span class="sxs-lookup"><span data-stu-id="100f8-149">-WindowEnd</span></span>
<span data-ttu-id="100f8-150">A tevékenység befejezése ablak befejezési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="100f8-150">Specifies the end time of activity window.</span></span>
<span data-ttu-id="100f8-151">Ez a parancsmag olyan Windows-tevékenységeket kap, amelyek időpontja a *WindowStart* és a *WindowEnd* időpontja között esik.</span><span class="sxs-lookup"><span data-stu-id="100f8-151">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="100f8-152">-WindowStart</span><span class="sxs-lookup"><span data-stu-id="100f8-152">-WindowStart</span></span>
<span data-ttu-id="100f8-153">A tevékenység ablak kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="100f8-153">Specifies the start time of activity window.</span></span>
<span data-ttu-id="100f8-154">Ez a parancsmag olyan Windows-tevékenységeket kap, amelyek időpontja a *WindowStart* és a *WindowEnd* időpontja között esik.</span><span class="sxs-lookup"><span data-stu-id="100f8-154">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="100f8-155">-WindowState</span><span class="sxs-lookup"><span data-stu-id="100f8-155">-WindowState</span></span>
<span data-ttu-id="100f8-156">A tevékenység ablak állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="100f8-156">Specifies the state of the activity window.</span></span>
<span data-ttu-id="100f8-157">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="100f8-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="100f8-158">Nincs</span><span class="sxs-lookup"><span data-stu-id="100f8-158">None</span></span>
- <span data-ttu-id="100f8-159">Várakozás</span><span class="sxs-lookup"><span data-stu-id="100f8-159">Waiting</span></span>
- <span data-ttu-id="100f8-160">Előrehaladás</span><span class="sxs-lookup"><span data-stu-id="100f8-160">InProgress</span></span>
- <span data-ttu-id="100f8-161">Kész</span><span class="sxs-lookup"><span data-stu-id="100f8-161">Ready</span></span>
- <span data-ttu-id="100f8-162">Sikertelen</span><span class="sxs-lookup"><span data-stu-id="100f8-162">Failed</span></span>
- <span data-ttu-id="100f8-163">Kihagyott</span><span class="sxs-lookup"><span data-stu-id="100f8-163">Skipped</span></span>

<span data-ttu-id="100f8-164">Ez a parancsmag olyan Windows-tevékenységeket kap, amelyek abban az állapotban vannak, hogy ez a paraméter adja meg.</span><span class="sxs-lookup"><span data-stu-id="100f8-164">This cmdlet gets activity windows that are in the state that this parameter specifies.</span></span>

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

### <span data-ttu-id="100f8-165">-WindowSubstate</span><span class="sxs-lookup"><span data-stu-id="100f8-165">-WindowSubstate</span></span>
<span data-ttu-id="100f8-166">A tevékenység ablak alállapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="100f8-166">Specifies the substate of the activity window.</span></span>
<span data-ttu-id="100f8-167">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="100f8-167">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="100f8-168">Visszavont</span><span class="sxs-lookup"><span data-stu-id="100f8-168">Canceled</span></span>
- <span data-ttu-id="100f8-169">timedOut</span><span class="sxs-lookup"><span data-stu-id="100f8-169">timedOut</span></span>
- <span data-ttu-id="100f8-170">Érvényesítése</span><span class="sxs-lookup"><span data-stu-id="100f8-170">Validating</span></span>

<span data-ttu-id="100f8-171">Ez a parancsmag olyan Windows-tevékenységeket kap, amelyek abban az alállamban vannak, hogy ez a paraméter adja meg.</span><span class="sxs-lookup"><span data-stu-id="100f8-171">This cmdlet gets activity windows that are in the substate that this parameter specifies.</span></span>

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

### <span data-ttu-id="100f8-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="100f8-172">-DefaultProfile</span></span>
<span data-ttu-id="100f8-173">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="100f8-173">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="100f8-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="100f8-174">CommonParameters</span></span>
<span data-ttu-id="100f8-175">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="100f8-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="100f8-176">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="100f8-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="100f8-177">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="100f8-177">INPUTS</span></span>

## <span data-ttu-id="100f8-178">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="100f8-178">OUTPUTS</span></span>

### <span data-ttu-id="100f8-179">System. Collections. Generic. list ' 1 [[Microsoft. WindowsAzure. Command. Utilities. PSActivyWindow, Microsoft. WindowsAzure. commands. Utilities, Version = 0.8.2.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="100f8-179">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSActivyWindow, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="100f8-180">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="100f8-180">NOTES</span></span>

## <span data-ttu-id="100f8-181">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="100f8-181">RELATED LINKS</span></span>

[<span data-ttu-id="100f8-182">Azure adatgyárak parancsmagok</span><span class="sxs-lookup"><span data-stu-id="100f8-182">Azure Data Factories Cmdlets</span></span>](./AzureRM.DataFactories.md)


