---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryactivitywindow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
ms.openlocfilehash: 5b18af8890d255dbd5514cccc0279acafe6bd611
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354605"
---
# <span data-ttu-id="ec60e-101">Get-AzDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="ec60e-101">Get-AzDataFactoryActivityWindow</span></span>

## <span data-ttu-id="ec60e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec60e-102">SYNOPSIS</span></span>
<span data-ttu-id="ec60e-103">Információkat kap egy adatüzemhez társított tevékenységablakról.</span><span class="sxs-lookup"><span data-stu-id="ec60e-103">Gets information about activity windows associated with a data factory.</span></span>

## <span data-ttu-id="ec60e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ec60e-104">SYNTAX</span></span>

### <span data-ttu-id="ec60e-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ec60e-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec60e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ec60e-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec60e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ec60e-107">DESCRIPTION</span></span>
<span data-ttu-id="ec60e-108">A **Get-AzDataFactoryActivityWindow** parancsmag információkat kap az adat factoryval társított tevékenységablakról.</span><span class="sxs-lookup"><span data-stu-id="ec60e-108">The **Get-AzDataFactoryActivityWindow** cmdlet gets information about the activity windows associated with a data factory.</span></span>

## <span data-ttu-id="ec60e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ec60e-109">EXAMPLES</span></span>

### <span data-ttu-id="ec60e-110">1. példa: Adatüzemhez társított tevékenységablakok lekérte</span><span class="sxs-lookup"><span data-stu-id="ec60e-110">Example 1: Get activity windows associated with a data factory</span></span>
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

<span data-ttu-id="ec60e-111">Ez a parancs információkat kap a WikiADF nevű adatüzemhez társított összes tevékenységablakról.</span><span class="sxs-lookup"><span data-stu-id="ec60e-111">This command gets information about all activity window associated with the data factory named WikiADF.</span></span>

## <span data-ttu-id="ec60e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec60e-112">PARAMETERS</span></span>

### <span data-ttu-id="ec60e-113">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="ec60e-113">-ActivityName</span></span>
<span data-ttu-id="ec60e-114">A tevékenység nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec60e-114">Specifies the name of the activity.</span></span>
<span data-ttu-id="ec60e-115">Ez a parancsmag a paraméter által megadott tevékenység tevékenységi ablakát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ec60e-115">This cmdlet gets activity windows for the activity that this parameter specifies.</span></span>

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

### <span data-ttu-id="ec60e-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ec60e-116">-DataFactory</span></span>
<span data-ttu-id="ec60e-117">Egy **parancsmag által visszaadott PSDataFactory-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="ec60e-117">Specifies a **PSDataFactory** object returned by a cmdlet.</span></span>
<span data-ttu-id="ec60e-118">Ez a parancsmag olyan tevékenységablakokat kap, amelyek a paraméter által megadott adatüzemhez tartoznak.</span><span class="sxs-lookup"><span data-stu-id="ec60e-118">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ec60e-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ec60e-119">-DataFactoryName</span></span>
<span data-ttu-id="ec60e-120">Az adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec60e-120">Specifies the name of the data factory.</span></span>
<span data-ttu-id="ec60e-121">Ez a parancsmag olyan tevékenységablakokat kap, amelyek a paraméter által megadott adatüzemhez tartoznak.</span><span class="sxs-lookup"><span data-stu-id="ec60e-121">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ec60e-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="ec60e-122">-DatasetName</span></span>
<span data-ttu-id="ec60e-123">Az adatkészlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec60e-123">Specifies the name of the dataset.</span></span>
<span data-ttu-id="ec60e-124">Ez a parancsmag olyan tevékenységablakokat kap, amelyek a paraméter által megadott adatkészlethez tartoznak.</span><span class="sxs-lookup"><span data-stu-id="ec60e-124">This cmdlet gets activity windows that belong to the dataset that this parameter specifies.</span></span>

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

### <span data-ttu-id="ec60e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec60e-125">-DefaultProfile</span></span>
<span data-ttu-id="ec60e-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ec60e-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec60e-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="ec60e-127">-Filter</span></span>
<span data-ttu-id="ec60e-128">Az Azure Search-szűrő nyelvhelyességi kifejezésével kifejezett tevékenységablak.</span><span class="sxs-lookup"><span data-stu-id="ec60e-128">Specifies the activity window expressed by using Azure Search filter grammar.</span></span>
<span data-ttu-id="ec60e-129">A nyelvhelyességi hibákról az Azure Search OData-kifejezésszintaxisában https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) (az MSDN-ban) található.</span><span class="sxs-lookup"><span data-stu-id="ec60e-129">For information about the grammar, see OData Expression Syntax for Azure Searchhttps://msdn.microsoft.com/en-us/library/azure/dn798921.aspx (https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span></span>
<span data-ttu-id="ec60e-130">A tevékenységablakok listáját a paraméter által megadott keresési karakterlánc szűri.</span><span class="sxs-lookup"><span data-stu-id="ec60e-130">The activity windows list is filtered by the search string that this parameter specifies.</span></span>

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

### <span data-ttu-id="ec60e-131">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="ec60e-131">-OrderBy</span></span>
<span data-ttu-id="ec60e-132">Azt adja meg, hogy a rendszer a tevékenységablak lista egyik paramétere alapján rendeli meg a választ.</span><span class="sxs-lookup"><span data-stu-id="ec60e-132">Specifies to order the response by one of the activity window list parameters.</span></span>
<span data-ttu-id="ec60e-133">Ez a vesszővel elválasztott tulajdonságok listája.</span><span class="sxs-lookup"><span data-stu-id="ec60e-133">This is a list of comma separated properties.</span></span>
<span data-ttu-id="ec60e-134">Például: WindowStart, PercentComplete.</span><span class="sxs-lookup"><span data-stu-id="ec60e-134">For example: WindowStart, PercentComplete.</span></span>
<span data-ttu-id="ec60e-135">A sorrend alapértelmezés szerint növekvő sorrendben (ASC).</span><span class="sxs-lookup"><span data-stu-id="ec60e-135">By default, the order is ascending order (ASC).</span></span>
<span data-ttu-id="ec60e-136">Ha csökkenő sorrendbe szeretné rendezni a listát, adja meg a DESC-t.</span><span class="sxs-lookup"><span data-stu-id="ec60e-136">Specify DESC if you want to order the list in descending order.</span></span>

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

### <span data-ttu-id="ec60e-137">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="ec60e-137">-PipelineName</span></span>
<span data-ttu-id="ec60e-138">A folyamat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec60e-138">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="ec60e-139">Ez a parancsmag a paraméter által megadott folyamathoz tartozó tevékenységablakokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ec60e-139">This cmdlet gets activity windows that belong to the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="ec60e-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec60e-140">-ResourceGroupName</span></span>
<span data-ttu-id="ec60e-141">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec60e-141">Specifies the name of the resource group.</span></span>
<span data-ttu-id="ec60e-142">Ez a parancsmag olyan tevékenységablakokat kap, amelyek a paraméter által megadott erőforráscsoporthoz tartoznak.</span><span class="sxs-lookup"><span data-stu-id="ec60e-142">This cmdlet gets activity windows that belong to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ec60e-143">-RunEnd</span><span class="sxs-lookup"><span data-stu-id="ec60e-143">-RunEnd</span></span>
<span data-ttu-id="ec60e-144">A tevékenységablak futtatásának záró idejét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec60e-144">Specifies the end time of the activity window run.</span></span>
<span data-ttu-id="ec60e-145">Ez a parancsmag olyan tevékenységablakokat kap, amelyek futási idői a *RunStart* és a *RunEnd* idő közé esnek.</span><span class="sxs-lookup"><span data-stu-id="ec60e-145">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="ec60e-146">-RunStart</span><span class="sxs-lookup"><span data-stu-id="ec60e-146">-RunStart</span></span>
<span data-ttu-id="ec60e-147">A tevékenységablak futtatásának kezdő idejét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec60e-147">Specifies the start time of the activity window run.</span></span>
<span data-ttu-id="ec60e-148">Ez a parancsmag olyan tevékenységablakokat kap, amelyek futási idői a *RunStart* és a *RunEnd* idő közé esnek.</span><span class="sxs-lookup"><span data-stu-id="ec60e-148">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="ec60e-149">-Top</span><span class="sxs-lookup"><span data-stu-id="ec60e-149">-Top</span></span>
<span data-ttu-id="ec60e-150">A parancsmag által visszaadott tevékenységablakok maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec60e-150">Specifies the maximum number of activity windows that this cmdlet returns.</span></span>

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

### <span data-ttu-id="ec60e-151">-WindowEnd</span><span class="sxs-lookup"><span data-stu-id="ec60e-151">-WindowEnd</span></span>
<span data-ttu-id="ec60e-152">A tevékenységablak záró idejét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec60e-152">Specifies the end time of activity window.</span></span>
<span data-ttu-id="ec60e-153">Ez a parancsmag olyan tevékenységablakokat kap, amelyek időkora *a WindowStart* és a *WindowEnd idő* közé esik.</span><span class="sxs-lookup"><span data-stu-id="ec60e-153">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="ec60e-154">-WindowStart</span><span class="sxs-lookup"><span data-stu-id="ec60e-154">-WindowStart</span></span>
<span data-ttu-id="ec60e-155">A tevékenységablak kezdési idejét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec60e-155">Specifies the start time of activity window.</span></span>
<span data-ttu-id="ec60e-156">Ez a parancsmag olyan tevékenységablakokat kap, amelyek időkora *a WindowStart* és a *WindowEnd idő* közé esik.</span><span class="sxs-lookup"><span data-stu-id="ec60e-156">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="ec60e-157">-WindowState</span><span class="sxs-lookup"><span data-stu-id="ec60e-157">-WindowState</span></span>
<span data-ttu-id="ec60e-158">A tevékenységablak állapotát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="ec60e-158">Specifies the state of the activity window.</span></span>
<span data-ttu-id="ec60e-159">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="ec60e-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ec60e-160">Nincs</span><span class="sxs-lookup"><span data-stu-id="ec60e-160">None</span></span>
- <span data-ttu-id="ec60e-161">Várakozás</span><span class="sxs-lookup"><span data-stu-id="ec60e-161">Waiting</span></span>
- <span data-ttu-id="ec60e-162">InProgress</span><span class="sxs-lookup"><span data-stu-id="ec60e-162">InProgress</span></span>
- <span data-ttu-id="ec60e-163">Kész</span><span class="sxs-lookup"><span data-stu-id="ec60e-163">Ready</span></span>
- <span data-ttu-id="ec60e-164">Nem sikerült</span><span class="sxs-lookup"><span data-stu-id="ec60e-164">Failed</span></span>
- <span data-ttu-id="ec60e-165">Kihagyva: Ez a parancsmag olyan tevékenységablakokat kap, amelyek a paraméter által megadott állapotban vannak.</span><span class="sxs-lookup"><span data-stu-id="ec60e-165">Skipped This cmdlet gets activity windows that are in the state that this parameter specifies.</span></span>

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

### <span data-ttu-id="ec60e-166">-WindowSubstate</span><span class="sxs-lookup"><span data-stu-id="ec60e-166">-WindowSubstate</span></span>
<span data-ttu-id="ec60e-167">A tevékenységablak alhálózatát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="ec60e-167">Specifies the substate of the activity window.</span></span>
<span data-ttu-id="ec60e-168">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="ec60e-168">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ec60e-169">Lemondva</span><span class="sxs-lookup"><span data-stu-id="ec60e-169">Canceled</span></span>
- <span data-ttu-id="ec60e-170">timedOut</span><span class="sxs-lookup"><span data-stu-id="ec60e-170">timedOut</span></span>
- <span data-ttu-id="ec60e-171">A parancsmag érvényességének igazolása a paraméter által megadott alértékben található tevékenységablakokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ec60e-171">Validating This cmdlet gets activity windows that are in the substate that this parameter specifies.</span></span>

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

### <span data-ttu-id="ec60e-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec60e-172">CommonParameters</span></span>
<span data-ttu-id="ec60e-173">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec60e-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec60e-174">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec60e-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec60e-175">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ec60e-175">INPUTS</span></span>

### <span data-ttu-id="ec60e-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ec60e-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="ec60e-177">System.String</span><span class="sxs-lookup"><span data-stu-id="ec60e-177">System.String</span></span>

### <span data-ttu-id="ec60e-178">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ec60e-178">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ec60e-179">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ec60e-179">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ec60e-180">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec60e-180">OUTPUTS</span></span>

### <span data-ttu-id="ec60e-181">Microsoft.Azure.Commands.DataFactories.Models.PSActivityWindow</span><span class="sxs-lookup"><span data-stu-id="ec60e-181">Microsoft.Azure.Commands.DataFactories.Models.PSActivityWindow</span></span>

## <span data-ttu-id="ec60e-182">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ec60e-182">NOTES</span></span>

## <span data-ttu-id="ec60e-183">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec60e-183">RELATED LINKS</span></span>

[<span data-ttu-id="ec60e-184">Azure Data Factories parancsmagok</span><span class="sxs-lookup"><span data-stu-id="ec60e-184">Azure Data Factories Cmdlets</span></span>](./Az.DataFactory.md)


