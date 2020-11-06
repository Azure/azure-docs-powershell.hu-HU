---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryactivitywindow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryActivityWindow.md
ms.openlocfilehash: 79ac0191f7fe381be4985d53ed719fdeff9d0b88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503000"
---
# <span data-ttu-id="d9402-101">Get-AzureRmDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="d9402-101">Get-AzureRmDataFactoryActivityWindow</span></span>

## <span data-ttu-id="d9402-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d9402-102">SYNOPSIS</span></span>
<span data-ttu-id="d9402-103">Információt kap az adatgyárhoz társított tevékenység-ablakokról.</span><span class="sxs-lookup"><span data-stu-id="d9402-103">Gets information about activity windows associated with a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9402-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d9402-104">SYNTAX</span></span>

### <span data-ttu-id="d9402-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d9402-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9402-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d9402-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9402-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d9402-107">DESCRIPTION</span></span>
<span data-ttu-id="d9402-108">A **Get-AzureRmDataFactoryActivityWindow** parancsmag információt kap az adatfeldolgozó ablakokkal társított tevékenységekről.</span><span class="sxs-lookup"><span data-stu-id="d9402-108">The **Get-AzureRmDataFactoryActivityWindow** cmdlet gets information about the activity windows associated with a data factory.</span></span>

## <span data-ttu-id="d9402-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d9402-109">EXAMPLES</span></span>

### <span data-ttu-id="d9402-110">1. példa: az adatfeldolgozóhoz társított Windows-tevékenységek beszerzése</span><span class="sxs-lookup"><span data-stu-id="d9402-110">Example 1: Get activity windows associated with a data factory</span></span>
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

<span data-ttu-id="d9402-111">Ez a parancs információt kap a WikiADF nevű adatfeldolgozóval társított összes tevékenység ablakról.</span><span class="sxs-lookup"><span data-stu-id="d9402-111">This command gets information about all activity window associated with the data factory named WikiADF.</span></span>

## <span data-ttu-id="d9402-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d9402-112">PARAMETERS</span></span>

### <span data-ttu-id="d9402-113">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="d9402-113">-ActivityName</span></span>
<span data-ttu-id="d9402-114">A tevékenység nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9402-114">Specifies the name of the activity.</span></span>
<span data-ttu-id="d9402-115">Ez a parancsmag a Windows tevékenységeit a paraméter által megadott tevékenységhez kapja.</span><span class="sxs-lookup"><span data-stu-id="d9402-115">This cmdlet gets activity windows for the activity that this parameter specifies.</span></span>

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

### <span data-ttu-id="d9402-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d9402-116">-DataFactory</span></span>
<span data-ttu-id="d9402-117">Egy parancsmag által visszaadott **PSDataFactory** -objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9402-117">Specifies a **PSDataFactory** object returned by a cmdlet.</span></span>
<span data-ttu-id="d9402-118">Ez a parancsmag azokat a Windows-tevékenységeket kapja meg, amelyek az adatfeldolgozóhoz tartoznak, és ez a paraméter határozza meg.</span><span class="sxs-lookup"><span data-stu-id="d9402-118">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d9402-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d9402-119">-DataFactoryName</span></span>
<span data-ttu-id="d9402-120">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9402-120">Specifies the name of the data factory.</span></span>
<span data-ttu-id="d9402-121">Ez a parancsmag azokat a Windows-tevékenységeket kapja meg, amelyek az adatfeldolgozóhoz tartoznak, és ez a paraméter határozza meg.</span><span class="sxs-lookup"><span data-stu-id="d9402-121">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d9402-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="d9402-122">-DatasetName</span></span>
<span data-ttu-id="d9402-123">Az adatkészlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9402-123">Specifies the name of the dataset.</span></span>
<span data-ttu-id="d9402-124">Ez a parancsmag olyan Windows-tevékenységekre ad választ, amelyek a paraméter által megadott adatkészlethez tartoznak.</span><span class="sxs-lookup"><span data-stu-id="d9402-124">This cmdlet gets activity windows that belong to the dataset that this parameter specifies.</span></span>

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

### <span data-ttu-id="d9402-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9402-125">-DefaultProfile</span></span>
<span data-ttu-id="d9402-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d9402-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9402-127">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="d9402-127">-Filter</span></span>
<span data-ttu-id="d9402-128">A tevékenység ablak az Azure keresési szűrési nyelvhelyességi szolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="d9402-128">Specifies the activity window expressed by using Azure Search filter grammar.</span></span>
<span data-ttu-id="d9402-129">A nyelvhelyességről további információt az Azure Search OData kifejezés szintaxisa című témakörben talál https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx ( https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) az MSDN webhelyen.</span><span class="sxs-lookup"><span data-stu-id="d9402-129">For information about the grammar, see OData Expression Syntax for Azure Searchhttps://msdn.microsoft.com/en-us/library/azure/dn798921.aspx (https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span></span>
<span data-ttu-id="d9402-130">A tevékenység Windows-listáját a paraméter által megadott keresési karakterlánc szűri.</span><span class="sxs-lookup"><span data-stu-id="d9402-130">The activity windows list is filtered by the search string that this parameter specifies.</span></span>

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

### <span data-ttu-id="d9402-131">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="d9402-131">-OrderBy</span></span>
<span data-ttu-id="d9402-132">Azt adja meg, hogy a tevékenység ablak lista paramétereinek egyike szerint rendelje a választ.</span><span class="sxs-lookup"><span data-stu-id="d9402-132">Specifies to order the response by one of the activity window list parameters.</span></span>
<span data-ttu-id="d9402-133">Ez a pontosvesszővel tagolt tulajdonságok listája.</span><span class="sxs-lookup"><span data-stu-id="d9402-133">This is a list of comma separated properties.</span></span>
<span data-ttu-id="d9402-134">Például: WindowStart, KészültségiSzint paraméter értéke.</span><span class="sxs-lookup"><span data-stu-id="d9402-134">For example: WindowStart, PercentComplete.</span></span>
<span data-ttu-id="d9402-135">Alapértelmezés szerint a sorrend növekvő sorrendű (ASC).</span><span class="sxs-lookup"><span data-stu-id="d9402-135">By default, the order is ascending order (ASC).</span></span>
<span data-ttu-id="d9402-136">Ha csökkenő sorrendben szeretné rendezni a listát, adja meg a LEÍRÁSát.</span><span class="sxs-lookup"><span data-stu-id="d9402-136">Specify DESC if you want to order the list in descending order.</span></span>

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

### <span data-ttu-id="d9402-137">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="d9402-137">-PipelineName</span></span>
<span data-ttu-id="d9402-138">A csővezeték nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9402-138">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="d9402-139">Ez a parancsmag olyan Windows-tevékenységeket kap, amelyek a paraméter által megadott csővezetékhez tartoznak.</span><span class="sxs-lookup"><span data-stu-id="d9402-139">This cmdlet gets activity windows that belong to the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="d9402-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9402-140">-ResourceGroupName</span></span>
<span data-ttu-id="d9402-141">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9402-141">Specifies the name of the resource group.</span></span>
<span data-ttu-id="d9402-142">Ez a parancsmag olyan Windows-tevékenységekre ad választ, amelyek a paraméter által megadott erőforráscsoport csoportjába tartoznak.</span><span class="sxs-lookup"><span data-stu-id="d9402-142">This cmdlet gets activity windows that belong to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d9402-143">-RunEnd</span><span class="sxs-lookup"><span data-stu-id="d9402-143">-RunEnd</span></span>
<span data-ttu-id="d9402-144">A tevékenység ablak befejezési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9402-144">Specifies the end time of the activity window run.</span></span>
<span data-ttu-id="d9402-145">Ez a parancsmag olyan Windows-tevékenységeket kap, amelyek futási ideje a *RunStart* és a *RunEnd* között esik.</span><span class="sxs-lookup"><span data-stu-id="d9402-145">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="d9402-146">-RunStart</span><span class="sxs-lookup"><span data-stu-id="d9402-146">-RunStart</span></span>
<span data-ttu-id="d9402-147">A tevékenység ablak kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9402-147">Specifies the start time of the activity window run.</span></span>
<span data-ttu-id="d9402-148">Ez a parancsmag olyan Windows-tevékenységeket kap, amelyek futási ideje a *RunStart* és a *RunEnd* között esik.</span><span class="sxs-lookup"><span data-stu-id="d9402-148">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="d9402-149">-Top</span><span class="sxs-lookup"><span data-stu-id="d9402-149">-Top</span></span>
<span data-ttu-id="d9402-150">Itt adhatja meg, hogy a Windows hány tevékenységet ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="d9402-150">Specifies the maximum number of activity windows that this cmdlet returns.</span></span>

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

### <span data-ttu-id="d9402-151">-WindowEnd</span><span class="sxs-lookup"><span data-stu-id="d9402-151">-WindowEnd</span></span>
<span data-ttu-id="d9402-152">A tevékenység befejezése ablak befejezési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9402-152">Specifies the end time of activity window.</span></span>
<span data-ttu-id="d9402-153">Ez a parancsmag olyan Windows-tevékenységeket kap, amelyek időpontja a *WindowStart* és a *WindowEnd* időpontja között esik.</span><span class="sxs-lookup"><span data-stu-id="d9402-153">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="d9402-154">-WindowStart</span><span class="sxs-lookup"><span data-stu-id="d9402-154">-WindowStart</span></span>
<span data-ttu-id="d9402-155">A tevékenység ablak kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9402-155">Specifies the start time of activity window.</span></span>
<span data-ttu-id="d9402-156">Ez a parancsmag olyan Windows-tevékenységeket kap, amelyek időpontja a *WindowStart* és a *WindowEnd* időpontja között esik.</span><span class="sxs-lookup"><span data-stu-id="d9402-156">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="d9402-157">-WindowState</span><span class="sxs-lookup"><span data-stu-id="d9402-157">-WindowState</span></span>
<span data-ttu-id="d9402-158">A tevékenység ablak állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9402-158">Specifies the state of the activity window.</span></span>
<span data-ttu-id="d9402-159">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d9402-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d9402-160">Nincs</span><span class="sxs-lookup"><span data-stu-id="d9402-160">None</span></span>
- <span data-ttu-id="d9402-161">Várakozás</span><span class="sxs-lookup"><span data-stu-id="d9402-161">Waiting</span></span>
- <span data-ttu-id="d9402-162">Előrehaladás</span><span class="sxs-lookup"><span data-stu-id="d9402-162">InProgress</span></span>
- <span data-ttu-id="d9402-163">Kész</span><span class="sxs-lookup"><span data-stu-id="d9402-163">Ready</span></span>
- <span data-ttu-id="d9402-164">Sikertelen</span><span class="sxs-lookup"><span data-stu-id="d9402-164">Failed</span></span>
- <span data-ttu-id="d9402-165">Kihagyva: Ez a parancsmag olyan Windows-tevékenységeket kap, amelyek abban az állapotban vannak, hogy ez a paraméter adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9402-165">Skipped This cmdlet gets activity windows that are in the state that this parameter specifies.</span></span>

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

### <span data-ttu-id="d9402-166">-WindowSubstate</span><span class="sxs-lookup"><span data-stu-id="d9402-166">-WindowSubstate</span></span>
<span data-ttu-id="d9402-167">A tevékenység ablak alállapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9402-167">Specifies the substate of the activity window.</span></span>
<span data-ttu-id="d9402-168">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d9402-168">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d9402-169">Visszavont</span><span class="sxs-lookup"><span data-stu-id="d9402-169">Canceled</span></span>
- <span data-ttu-id="d9402-170">timedOut</span><span class="sxs-lookup"><span data-stu-id="d9402-170">timedOut</span></span>
- <span data-ttu-id="d9402-171">A parancsmag érvényesítése olyan Windows-tevékenységeket kap, amelyek abban az alállamban vannak, hogy ez a paraméter adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9402-171">Validating This cmdlet gets activity windows that are in the substate that this parameter specifies.</span></span>

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

### <span data-ttu-id="d9402-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9402-172">CommonParameters</span></span>
<span data-ttu-id="d9402-173">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d9402-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9402-174">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9402-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9402-175">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9402-175">INPUTS</span></span>

### <span data-ttu-id="d9402-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d9402-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="d9402-177">System. String</span><span class="sxs-lookup"><span data-stu-id="d9402-177">System.String</span></span>

### <span data-ttu-id="d9402-178">System. null ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d9402-178">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="d9402-179">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d9402-179">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="d9402-180">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9402-180">OUTPUTS</span></span>

### <span data-ttu-id="d9402-181">Microsoft. Azure. Command. DataFactories. models. PSActivityWindow</span><span class="sxs-lookup"><span data-stu-id="d9402-181">Microsoft.Azure.Commands.DataFactories.Models.PSActivityWindow</span></span>

## <span data-ttu-id="d9402-182">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d9402-182">NOTES</span></span>

## <span data-ttu-id="d9402-183">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d9402-183">RELATED LINKS</span></span>

[<span data-ttu-id="d9402-184">Azure adatgyárak parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d9402-184">Azure Data Factories Cmdlets</span></span>](./AzureRM.DataFactories.md)


