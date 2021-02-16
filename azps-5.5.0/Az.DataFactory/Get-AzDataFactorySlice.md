---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
ms.openlocfilehash: a71ccc37fe1c6b6811b955c5d84353dfecd66c2f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208758"
---
# <span data-ttu-id="a2935-101">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="a2935-101">Get-AzDataFactorySlice</span></span>

## <span data-ttu-id="a2935-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2935-102">SYNOPSIS</span></span>
<span data-ttu-id="a2935-103">Adatszeleteket kap egy adatkészlethez az Azure Data Factoryban.</span><span class="sxs-lookup"><span data-stu-id="a2935-103">Gets data slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="a2935-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a2935-104">SYNTAX</span></span>

### <span data-ttu-id="a2935-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a2935-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a2935-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a2935-106">ByFactoryObject</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2935-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a2935-107">DESCRIPTION</span></span>
<span data-ttu-id="a2935-108">A **Get-AzDataFactorySlice** parancsmag adatszeleteket kap egy adatkészlethez az Azure Data Factoryban.</span><span class="sxs-lookup"><span data-stu-id="a2935-108">The **Get-AzDataFactorySlice** cmdlet gets data slices for a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="a2935-109">Adjon meg egy kezdési és egy záró időt a megtekinteni kívánt adatszeleteket meghatározó adatszeleteket.</span><span class="sxs-lookup"><span data-stu-id="a2935-109">Specify a start time and an end time to define a range of data slices to view.</span></span>
<span data-ttu-id="a2935-110">Az adatszelet állapota az alábbi értékek egyike:</span><span class="sxs-lookup"><span data-stu-id="a2935-110">The status of a data slice is one of the following values:</span></span> 
- <span data-ttu-id="a2935-111">PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="a2935-111">PendingExecution.</span></span>
<span data-ttu-id="a2935-112">Az adatkezelés még nem kezdődött el.</span><span class="sxs-lookup"><span data-stu-id="a2935-112">Data processing has not started.</span></span> 
- <span data-ttu-id="a2935-113">InProgress.</span><span class="sxs-lookup"><span data-stu-id="a2935-113">InProgress.</span></span>
<span data-ttu-id="a2935-114">Folyamatban van az adatok feldolgozása.</span><span class="sxs-lookup"><span data-stu-id="a2935-114">Data processing is in progress.</span></span> 
- <span data-ttu-id="a2935-115">Kész.</span><span class="sxs-lookup"><span data-stu-id="a2935-115">Ready.</span></span>
<span data-ttu-id="a2935-116">Az adatkezelés befejeződött.</span><span class="sxs-lookup"><span data-stu-id="a2935-116">Data processing is completed.</span></span>
<span data-ttu-id="a2935-117">Az adatszelet készen áll arra, hogy a függő szeletek felhasználják.</span><span class="sxs-lookup"><span data-stu-id="a2935-117">The data slice is ready for dependent slices to consume it.</span></span> 
- <span data-ttu-id="a2935-118">Sikertelen.</span><span class="sxs-lookup"><span data-stu-id="a2935-118">Failed.</span></span>
<span data-ttu-id="a2935-119">A szeletet el nem sikerült hozó futtatás.</span><span class="sxs-lookup"><span data-stu-id="a2935-119">The run that produces the slice failed.</span></span> 
- <span data-ttu-id="a2935-120">Kihagyás.</span><span class="sxs-lookup"><span data-stu-id="a2935-120">Skip.</span></span>
<span data-ttu-id="a2935-121">A Data Factory kihagyja a szelet feldolgozását.</span><span class="sxs-lookup"><span data-stu-id="a2935-121">Data Factory skips processing of the slice.</span></span> 
- <span data-ttu-id="a2935-122">Próbálja meg újból.</span><span class="sxs-lookup"><span data-stu-id="a2935-122">Retry.</span></span>
<span data-ttu-id="a2935-123">A Data Factory újrafuttatja a szeletelő futást.</span><span class="sxs-lookup"><span data-stu-id="a2935-123">Data Factory retries the run that produces the slice.</span></span> 
- <span data-ttu-id="a2935-124">Időkorrekt. Az adatkezelés időkorrekta.</span><span class="sxs-lookup"><span data-stu-id="a2935-124">Timed Out. Data processing has timed out.</span></span> 
- <span data-ttu-id="a2935-125">Függőben lévőÉrték.</span><span class="sxs-lookup"><span data-stu-id="a2935-125">PendingValidation.</span></span>
<span data-ttu-id="a2935-126">Az adatszelet a feldolgozás előtt érvényesítésre vár.</span><span class="sxs-lookup"><span data-stu-id="a2935-126">Data slice is waiting for validation before it is processed.</span></span> 
- <span data-ttu-id="a2935-127">Próbálja meg újból az érvényesítést.</span><span class="sxs-lookup"><span data-stu-id="a2935-127">Retry Validation.</span></span>
<span data-ttu-id="a2935-128">A Data Factory újravágja a szelet érvényesítését.</span><span class="sxs-lookup"><span data-stu-id="a2935-128">Data Factory retries the validation of the slice.</span></span> 
- <span data-ttu-id="a2935-129">Sikertelen ellenőrzés.</span><span class="sxs-lookup"><span data-stu-id="a2935-129">Failed Validation.</span></span>
<span data-ttu-id="a2935-130">A szelet érvényesítése nem sikerült.</span><span class="sxs-lookup"><span data-stu-id="a2935-130">Validation of the slice failed.</span></span>
<span data-ttu-id="a2935-131">Minden egyes szelethez további információt láthat a futtatásról, amely a szeletet a Get-AzDataFactoryRun parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="a2935-131">For each of the slices, you can see more information about the run that produces the slice by using the Get-AzDataFactoryRun cmdlet.</span></span>

## <span data-ttu-id="a2935-132">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a2935-132">EXAMPLES</span></span>

### <span data-ttu-id="a2935-133">1. példa: Adatszeletek lekérte egy adatkészlethez</span><span class="sxs-lookup"><span data-stu-id="a2935-133">Example 1: Get data slices for a dataset</span></span>
```powershell
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

<span data-ttu-id="a2935-134">Ez a parancs a WikiADF nevű adatüzemben a WikiAggregatedData nevű adatkészlet összes adatszeletét begyűjte.</span><span class="sxs-lookup"><span data-stu-id="a2935-134">This command gets all the data slices for the dataset named WikiAggregatedData in the data factory named WikiADF.</span></span>
<span data-ttu-id="a2935-135">A parancs a StartDateTime paraméter által megadott idő után jön létre.</span><span class="sxs-lookup"><span data-stu-id="a2935-135">The command gets slices produced after the time that the StartDateTime parameter specifies.</span></span>
<span data-ttu-id="a2935-136">Az alábbi példakód óránként beállítja az adatkészlet elérhetőségét a JavaScript objektum-notation (JSON) fájlban.</span><span class="sxs-lookup"><span data-stu-id="a2935-136">The following example code sets the availability for this dataset every hour in the JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="a2935-137">elérhetőség: { period: "Hour", periodMultiplier: 1 } Az eredmények közül néhány készen áll, míg mások függőben lévőExecution.</span><span class="sxs-lookup"><span data-stu-id="a2935-137">availability: { period: "Hour", periodMultiplier: 1 } Some of the results are Ready and others are PendingExecution.</span></span>
<span data-ttu-id="a2935-138">A kész szeletek már futnak.</span><span class="sxs-lookup"><span data-stu-id="a2935-138">Ready slices have already run.</span></span>
<span data-ttu-id="a2935-139">A függőben lévő szeletek az egyes óra végén, a parancsmag által megadott intervallumban Set-AzDataFactoryPipelineActivePeriod futnak.</span><span class="sxs-lookup"><span data-stu-id="a2935-139">The pending slices are waiting to run at the end of each hour in the interval that the Set-AzDataFactoryPipelineActivePeriod cmdlet specifies.</span></span>
<span data-ttu-id="a2935-140">Ebben a példában a folyamat kezdő és záró periódusa is egy nap (24 óra) értékű.</span><span class="sxs-lookup"><span data-stu-id="a2935-140">In this example, both start and end periods for the pipeline and the slice have a value of one day (24 hours).</span></span>

### <span data-ttu-id="a2935-141">2. példa</span><span class="sxs-lookup"><span data-stu-id="a2935-141">Example 2</span></span>

<span data-ttu-id="a2935-142">Adatszeleteket kap egy adatkészlethez az Azure Data Factoryban.</span><span class="sxs-lookup"><span data-stu-id="a2935-142">Gets data slices for a dataset in Azure Data Factory.</span></span> <span data-ttu-id="a2935-143">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="a2935-143">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzDataFactorySlice -DataFactoryName 'WikiADF' -DatasetName 'DAWikiAggregatedData' -EndDateTime 2014-05-22T16:00:00Z -ResourceGroupName 'ADF' -StartDateTime 2014-05-20T10:00:00Z
```

## <span data-ttu-id="a2935-144">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2935-144">PARAMETERS</span></span>

### <span data-ttu-id="a2935-145">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a2935-145">-DataFactory</span></span>
<span data-ttu-id="a2935-146">EGY **PSDataFactory-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="a2935-146">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="a2935-147">Ez a parancsmag a paraméter által megadott adatüzembe tartozó szeleteket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a2935-147">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a2935-148">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a2935-148">-DataFactoryName</span></span>
<span data-ttu-id="a2935-149">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a2935-149">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a2935-150">Ez a parancsmag a paraméter által megadott adatüzembe tartozó szeleteket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a2935-150">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a2935-151">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="a2935-151">-DatasetName</span></span>
<span data-ttu-id="a2935-152">Annak az adatkészletnek a nevét adja meg, amelyhez a parancsmag szeleteket kap.</span><span class="sxs-lookup"><span data-stu-id="a2935-152">Specifies the name of the dataset for which this cmdlet gets slices.</span></span>

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

### <span data-ttu-id="a2935-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2935-153">-DefaultProfile</span></span>
<span data-ttu-id="a2935-154">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a2935-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2935-155">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="a2935-155">-EndDateTime</span></span>
<span data-ttu-id="a2935-156">Egy időtartomány végét adja meg **DateTime-objektumként.**</span><span class="sxs-lookup"><span data-stu-id="a2935-156">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="a2935-157">Ez a parancsmag a paraméter által megadott időpont előtt készült szeleteket kap.</span><span class="sxs-lookup"><span data-stu-id="a2935-157">This cmdlet gets slices produced before the time that this parameter specifies.</span></span>
<span data-ttu-id="a2935-158">A DateTime-objektumokról a **következőt** írja be: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="a2935-158">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="a2935-159">Az *EndDateTime* értéket ISO8601 formátumban kell megadni, az alábbi példák szerint: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Csendes-óceáni téli idő) Az alapértelmezett időzóna-tervező az UTC.</span><span class="sxs-lookup"><span data-stu-id="a2935-159">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="a2935-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2935-160">-ResourceGroupName</span></span>
<span data-ttu-id="a2935-161">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a2935-161">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a2935-162">Ez a parancsmag a paraméter által megadott csoporthoz tartozó szeleteket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a2935-162">This cmdlet gets slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a2935-163">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="a2935-163">-StartDateTime</span></span>
<span data-ttu-id="a2935-164">Egy időtartomány kezdő időpontját adja meg **DateTime-objektumként.**</span><span class="sxs-lookup"><span data-stu-id="a2935-164">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="a2935-165">Ez a parancsmag a paraméter által megadott idő után jön létre szeletekkel.</span><span class="sxs-lookup"><span data-stu-id="a2935-165">This cmdlet gets slices produced after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="a2935-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2935-166">CommonParameters</span></span>
<span data-ttu-id="a2935-167">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2935-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2935-168">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2935-168">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2935-169">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2935-169">INPUTS</span></span>

### <span data-ttu-id="a2935-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a2935-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="a2935-171">System.String</span><span class="sxs-lookup"><span data-stu-id="a2935-171">System.String</span></span>

## <span data-ttu-id="a2935-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2935-172">OUTPUTS</span></span>

### <span data-ttu-id="a2935-173">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span><span class="sxs-lookup"><span data-stu-id="a2935-173">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span></span>

## <span data-ttu-id="a2935-174">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a2935-174">NOTES</span></span>
* <span data-ttu-id="a2935-175">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="a2935-175">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a2935-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2935-176">RELATED LINKS</span></span>

[<span data-ttu-id="a2935-177">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="a2935-177">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)

[<span data-ttu-id="a2935-178">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="a2935-178">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="a2935-179">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="a2935-179">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


