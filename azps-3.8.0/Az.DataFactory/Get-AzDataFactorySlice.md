---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
ms.openlocfilehash: cc970a03e0af625237ef9b8c72f5afbe95578751
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847318"
---
# <span data-ttu-id="d9730-101">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="d9730-101">Get-AzDataFactorySlice</span></span>

## <span data-ttu-id="d9730-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d9730-102">SYNOPSIS</span></span>
<span data-ttu-id="d9730-103">Adatszeletek beolvasása adatkészlethez az Azure Data Factory-ban</span><span class="sxs-lookup"><span data-stu-id="d9730-103">Gets data slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="d9730-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d9730-104">SYNTAX</span></span>

### <span data-ttu-id="d9730-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d9730-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d9730-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d9730-106">ByFactoryObject</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9730-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d9730-107">DESCRIPTION</span></span>
<span data-ttu-id="d9730-108">A **Get-AzDataFactorySlice** parancsmag adatszeleteket kap az adatkészletekhez az Azure Data Factory szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="d9730-108">The **Get-AzDataFactorySlice** cmdlet gets data slices for a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="d9730-109">Adja meg a kezdés időpontját és a befejezési időpontot, és adja meg a megtekinteni kívánt adatszeletek tartományát.</span><span class="sxs-lookup"><span data-stu-id="d9730-109">Specify a start time and an end time to define a range of data slices to view.</span></span>
<span data-ttu-id="d9730-110">Az adatszeletek állapota az alábbi értékek egyike:</span><span class="sxs-lookup"><span data-stu-id="d9730-110">The status of a data slice is one of the following values:</span></span> 
- <span data-ttu-id="d9730-111">PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="d9730-111">PendingExecution.</span></span>
<span data-ttu-id="d9730-112">Nem kezdődött el az adatfeldolgozás.</span><span class="sxs-lookup"><span data-stu-id="d9730-112">Data processing has not started.</span></span> 
- <span data-ttu-id="d9730-113">Folyamatban van.</span><span class="sxs-lookup"><span data-stu-id="d9730-113">InProgress.</span></span>
<span data-ttu-id="d9730-114">Folyamatban van az adatfeldolgozás.</span><span class="sxs-lookup"><span data-stu-id="d9730-114">Data processing is in progress.</span></span> 
- <span data-ttu-id="d9730-115">Kész.</span><span class="sxs-lookup"><span data-stu-id="d9730-115">Ready.</span></span>
<span data-ttu-id="d9730-116">Befejeződött az adatfeldolgozás.</span><span class="sxs-lookup"><span data-stu-id="d9730-116">Data processing is completed.</span></span>
<span data-ttu-id="d9730-117">Az adatszelet készen áll a függő szeletek elfogyasztására.</span><span class="sxs-lookup"><span data-stu-id="d9730-117">The data slice is ready for dependent slices to consume it.</span></span> 
- <span data-ttu-id="d9730-118">Sikertelen.</span><span class="sxs-lookup"><span data-stu-id="d9730-118">Failed.</span></span>
<span data-ttu-id="d9730-119">A szeletet előállító Futtatás sikertelen volt.</span><span class="sxs-lookup"><span data-stu-id="d9730-119">The run that produces the slice failed.</span></span> 
- <span data-ttu-id="d9730-120">Kihagyhatja.</span><span class="sxs-lookup"><span data-stu-id="d9730-120">Skip.</span></span>
<span data-ttu-id="d9730-121">Az Data Factory kihagyja a szelet feldolgozását.</span><span class="sxs-lookup"><span data-stu-id="d9730-121">Data Factory skips processing of the slice.</span></span> 
- <span data-ttu-id="d9730-122">Újra.</span><span class="sxs-lookup"><span data-stu-id="d9730-122">Retry.</span></span>
<span data-ttu-id="d9730-123">Az adatfeldolgozó újból megkísérli a szeletet előállító futtatást.</span><span class="sxs-lookup"><span data-stu-id="d9730-123">Data Factory retries the run that produces the slice.</span></span> 
- <span data-ttu-id="d9730-124">Időtúllépés. Az adatfeldolgozás időkorlátja lejárt.</span><span class="sxs-lookup"><span data-stu-id="d9730-124">Timed Out. Data processing has timed out.</span></span> 
- <span data-ttu-id="d9730-125">PendingValidation.</span><span class="sxs-lookup"><span data-stu-id="d9730-125">PendingValidation.</span></span>
<span data-ttu-id="d9730-126">Az adatszelet az érvényesítésre vár a feldolgozás előtt.</span><span class="sxs-lookup"><span data-stu-id="d9730-126">Data slice is waiting for validation before it is processed.</span></span> 
- <span data-ttu-id="d9730-127">Az érvényesítés ismételt ismétlése</span><span class="sxs-lookup"><span data-stu-id="d9730-127">Retry Validation.</span></span>
<span data-ttu-id="d9730-128">Az adatfeldolgozó újból megkísérli a szelet érvényesítését.</span><span class="sxs-lookup"><span data-stu-id="d9730-128">Data Factory retries the validation of the slice.</span></span> 
- <span data-ttu-id="d9730-129">Sikertelen érvényesítés</span><span class="sxs-lookup"><span data-stu-id="d9730-129">Failed Validation.</span></span>
<span data-ttu-id="d9730-130">Nem sikerült a szelet érvényesítése.</span><span class="sxs-lookup"><span data-stu-id="d9730-130">Validation of the slice failed.</span></span>
<span data-ttu-id="d9730-131">Minden egyes szeletre vonatkozóan további információkat találhat a szeletet előállító futtatásról a Get-AzDataFactoryRun parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="d9730-131">For each of the slices, you can see more information about the run that produces the slice by using the Get-AzDataFactoryRun cmdlet.</span></span>

## <span data-ttu-id="d9730-132">Példák</span><span class="sxs-lookup"><span data-stu-id="d9730-132">EXAMPLES</span></span>

### <span data-ttu-id="d9730-133">1. példa: adatszeletek beolvasása adatkészlethez</span><span class="sxs-lookup"><span data-stu-id="d9730-133">Example 1: Get data slices for a dataset</span></span>
```
PS C:\>Get-AzDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 1:00:00 AM
End               : 5/21/2014 2:00:00 AM
RetryCount        : 0
Status            : Ready

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 2:00:00 AM
End               : 5/21/2014 3:00:00 AM
RetryCount        : 0
Status            : Ready

. . . 

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 8:00:00 PM
End               : 5/21/2014 9:00:00 PM
RetryCount        : 0
Status            : PendingExecution

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 9:00:00 PM
End               : 5/21/2014 10:00:00 PM
RetryCount        : 0
Status            : PendingExecution

. . .
```

<span data-ttu-id="d9730-134">Ez a parancs a WikiAggregatedData nevű adatkészlethez tartozó összes adatszeletet megkapja az WikiADF nevű adatfeldolgozóban.</span><span class="sxs-lookup"><span data-stu-id="d9730-134">This command gets all the data slices for the dataset named WikiAggregatedData in the data factory named WikiADF.</span></span>
<span data-ttu-id="d9730-135">A parancs a StartDateTime paraméter által megadott időpont után a szeleteket kapja.</span><span class="sxs-lookup"><span data-stu-id="d9730-135">The command gets slices produced after the time that the StartDateTime parameter specifies.</span></span>
<span data-ttu-id="d9730-136">Az alábbi mintakód a JavaScript Object (JSON) fájlban az adatkészlet elérhetőségét óránkénti értékre állítja.</span><span class="sxs-lookup"><span data-stu-id="d9730-136">The following example code sets the availability for this dataset every hour in the JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="d9730-137">Elérhetőség: {időszak: "óra", periodMultiplier: 1} a találatok közül néhány elkészült, mások pedig PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="d9730-137">availability: { period: "Hour", periodMultiplier: 1 } Some of the results are Ready and others are PendingExecution.</span></span>
<span data-ttu-id="d9730-138">A kész Slice-elemek már futnak.</span><span class="sxs-lookup"><span data-stu-id="d9730-138">Ready slices have already run.</span></span>
<span data-ttu-id="d9730-139">A függőben lévő szeletek a Set-AzDataFactoryPipelineActivePeriod parancsmag által megadott intervallumban minden óra végén futnak.</span><span class="sxs-lookup"><span data-stu-id="d9730-139">The pending slices are waiting to run at the end of each hour in the interval that the Set-AzDataFactoryPipelineActivePeriod cmdlet specifies.</span></span>
<span data-ttu-id="d9730-140">Ebben a példában a csővezeték kezdési és befejezési időszakait (24 óra) is megtalálhatja.</span><span class="sxs-lookup"><span data-stu-id="d9730-140">In this example, both start and end periods for the pipeline and the slice have a value of one day (24 hours).</span></span>

## <span data-ttu-id="d9730-141">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d9730-141">PARAMETERS</span></span>

### <span data-ttu-id="d9730-142">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d9730-142">-DataFactory</span></span>
<span data-ttu-id="d9730-143">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="d9730-143">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="d9730-144">Ez a parancsmag az adatfeldolgozóhoz tartozó, a paraméter által megadott szeleteket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d9730-144">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d9730-145">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d9730-145">-DataFactoryName</span></span>
<span data-ttu-id="d9730-146">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9730-146">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d9730-147">Ez a parancsmag az adatfeldolgozóhoz tartozó, a paraméter által megadott szeleteket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d9730-147">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d9730-148">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="d9730-148">-DatasetName</span></span>
<span data-ttu-id="d9730-149">Annak az adatkészletnek a nevét adja meg, amelynek a parancsmagja a szeleteket kapja.</span><span class="sxs-lookup"><span data-stu-id="d9730-149">Specifies the name of the dataset for which this cmdlet gets slices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9730-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9730-150">-DefaultProfile</span></span>
<span data-ttu-id="d9730-151">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d9730-151">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9730-152">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="d9730-152">-EndDateTime</span></span>
<span data-ttu-id="d9730-153">Az időszak végét **datetime** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9730-153">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="d9730-154">Ez a parancsmag a paraméter által megadott időpont előtt a szeleteket kapja.</span><span class="sxs-lookup"><span data-stu-id="d9730-154">This cmdlet gets slices produced before the time that this parameter specifies.</span></span>
<span data-ttu-id="d9730-155">A **datetime** -objektumokkal kapcsolatos további tudnivalókért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="d9730-155">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="d9730-156">A *EndDateTime* a ISO8601 formátumban kell megadni: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (Pacific standard Time) az alapértelmezett időzóna-megjelölést az UTC adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9730-156">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9730-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9730-157">-ResourceGroupName</span></span>
<span data-ttu-id="d9730-158">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9730-158">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d9730-159">Ez a parancsmag olyan szeleteket kap, amelyek a paraméter által megadott csoportba tartoznak.</span><span class="sxs-lookup"><span data-stu-id="d9730-159">This cmdlet gets slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d9730-160">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="d9730-160">-StartDateTime</span></span>
<span data-ttu-id="d9730-161">Az időszak kezdését **datetime** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9730-161">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="d9730-162">Ez a parancsmag a paraméter által megadott időpont után kap szeleteket.</span><span class="sxs-lookup"><span data-stu-id="d9730-162">This cmdlet gets slices produced after the time that this parameter specifies.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9730-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9730-163">CommonParameters</span></span>
<span data-ttu-id="d9730-164">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d9730-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9730-165">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9730-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9730-166">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9730-166">INPUTS</span></span>

### <span data-ttu-id="d9730-167">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d9730-167">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="d9730-168">System. String</span><span class="sxs-lookup"><span data-stu-id="d9730-168">System.String</span></span>

## <span data-ttu-id="d9730-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9730-169">OUTPUTS</span></span>

### <span data-ttu-id="d9730-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span><span class="sxs-lookup"><span data-stu-id="d9730-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span></span>

## <span data-ttu-id="d9730-171">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d9730-171">NOTES</span></span>
* <span data-ttu-id="d9730-172">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="d9730-172">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d9730-173">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d9730-173">RELATED LINKS</span></span>

[<span data-ttu-id="d9730-174">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="d9730-174">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)

[<span data-ttu-id="d9730-175">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="d9730-175">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="d9730-176">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="d9730-176">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


