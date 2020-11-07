---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
ms.openlocfilehash: a7418dd1e0570d4e92310371e658dd130b36bc44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671119"
---
# <span data-ttu-id="9f412-101">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="9f412-101">Set-AzDataFactorySliceStatus</span></span>

## <span data-ttu-id="9f412-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9f412-102">SYNOPSIS</span></span>
<span data-ttu-id="9f412-103">A szeletek állapotát állítja be egy adatkészlethez az Azure Data Factory-ban.</span><span class="sxs-lookup"><span data-stu-id="9f412-103">Sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="9f412-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9f412-104">SYNTAX</span></span>

### <span data-ttu-id="9f412-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9f412-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f412-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9f412-106">ByFactoryObject</span></span>
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f412-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9f412-107">DESCRIPTION</span></span>
<span data-ttu-id="9f412-108">A **set-AzDataFactorySliceStatus** parancsmag az Azure Data Factory adatkészlethez tartozó szeletek állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="9f412-108">The **Set-AzDataFactorySliceStatus** cmdlet sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="9f412-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9f412-109">EXAMPLES</span></span>

### <span data-ttu-id="9f412-110">Példa 1: az összes szelet állapotának beállítása</span><span class="sxs-lookup"><span data-stu-id="9f412-110">Example 1: Set the status of all slices</span></span>
```
PS C:\>Set-AzDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

<span data-ttu-id="9f412-111">Ez a parancs beállítja a DAWikiAggregatedData nevű adatkészlet összes szeletének állapotát a WikiADF nevű adatgyárban való várakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="9f412-111">This command sets the status of all slices for the dataset named DAWikiAggregatedData to Waiting in the data factory named WikiADF.</span></span>
<span data-ttu-id="9f412-112">A *UpdateType* paraméter a UpstreamInPipeline értékét tartalmazza, így a parancs az adatkészlet minden egyes szeletének állapotát és a függő adatkészletek állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="9f412-112">The *UpdateType* parameter has a value of UpstreamInPipeline, and so the command sets the status of each slice for the dataset and all dependent datasets.</span></span>
<span data-ttu-id="9f412-113">A függő adatkészletek beviteli adatkészletként használhatók a csővezetéken végzett tevékenységekhez.</span><span class="sxs-lookup"><span data-stu-id="9f412-113">Dependent datasets are used as input datasets for activities in the pipeline.</span></span>
<span data-ttu-id="9f412-114">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="9f412-114">This command returns a value of $True.</span></span>

## <span data-ttu-id="9f412-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9f412-115">PARAMETERS</span></span>

### <span data-ttu-id="9f412-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="9f412-116">-DataFactory</span></span>
<span data-ttu-id="9f412-117">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="9f412-117">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="9f412-118">Ez a parancsmag módosítja az adatfeldolgozóhoz tartozó szeletek állapotát, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f412-118">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9f412-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9f412-119">-DataFactoryName</span></span>
<span data-ttu-id="9f412-120">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f412-120">Specifies the name of a data factory.</span></span>
<span data-ttu-id="9f412-121">Ez a parancsmag módosítja az adatfeldolgozóhoz tartozó szeletek állapotát, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f412-121">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9f412-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="9f412-122">-DatasetName</span></span>
<span data-ttu-id="9f412-123">Annak az adatkészletnek a neve, amelyhez ez a parancsmag módosítja a szeleteket.</span><span class="sxs-lookup"><span data-stu-id="9f412-123">Specifies the name of the dataset for which this cmdlet modifies slices.</span></span>

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

### <span data-ttu-id="9f412-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f412-124">-DefaultProfile</span></span>
<span data-ttu-id="9f412-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9f412-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f412-126">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="9f412-126">-EndDateTime</span></span>
<span data-ttu-id="9f412-127">Az időszak végét **datetime** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f412-127">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="9f412-128">Ez az idő az adatszeletek vége.</span><span class="sxs-lookup"><span data-stu-id="9f412-128">This time is the end of a data slice.</span></span>
<span data-ttu-id="9f412-129">A **datetime** -objektumokkal kapcsolatos további tudnivalókért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="9f412-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="9f412-130">A *EndDateTime* a ISO8601 formátumban kell megadni: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (Pacific standard Time) az alapértelmezett időzóna-megjelölést az UTC adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f412-130">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="9f412-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f412-131">-ResourceGroupName</span></span>
<span data-ttu-id="9f412-132">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f412-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9f412-133">Ez a parancsmag módosítja annak a csoportnak a szeletét, amelyhez a paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="9f412-133">This cmdlet modifies the status of slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9f412-134">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="9f412-134">-StartDateTime</span></span>
<span data-ttu-id="9f412-135">Az időszak kezdését **datetime** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f412-135">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="9f412-136">Ez az idő az adatszeletek kezdetét jelentik.</span><span class="sxs-lookup"><span data-stu-id="9f412-136">This time is the beginning of a data slice.</span></span>

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

### <span data-ttu-id="9f412-137">-Állapot</span><span class="sxs-lookup"><span data-stu-id="9f412-137">-Status</span></span>
<span data-ttu-id="9f412-138">Az adatszelethez hozzárendelni kívánt állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f412-138">Specifies a status to assign to the data slice.</span></span>
<span data-ttu-id="9f412-139">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="9f412-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9f412-140">Várakozás.</span><span class="sxs-lookup"><span data-stu-id="9f412-140">Waiting.</span></span>
<span data-ttu-id="9f412-141">Az adatszeletek az érvényesítési szabályoknak a feldolgozás előtt való érvényesítésére várnak.</span><span class="sxs-lookup"><span data-stu-id="9f412-141">Data slice is waiting for validation against validation policies before being processed.</span></span> 
- <span data-ttu-id="9f412-142">Kész.</span><span class="sxs-lookup"><span data-stu-id="9f412-142">Ready.</span></span>
<span data-ttu-id="9f412-143">Az adatfeldolgozás befejeződött, és az adatszelet készen áll.</span><span class="sxs-lookup"><span data-stu-id="9f412-143">Data processing has completed and the data slice is ready.</span></span>
- <span data-ttu-id="9f412-144">Folyamatban van.</span><span class="sxs-lookup"><span data-stu-id="9f412-144">InProgress.</span></span>
<span data-ttu-id="9f412-145">Folyamatban van az adatfeldolgozás.</span><span class="sxs-lookup"><span data-stu-id="9f412-145">Data processing is in-progress.</span></span> 
- <span data-ttu-id="9f412-146">Sikertelen.</span><span class="sxs-lookup"><span data-stu-id="9f412-146">Failed.</span></span>
<span data-ttu-id="9f412-147">Sikertelen az adatfeldolgozás.</span><span class="sxs-lookup"><span data-stu-id="9f412-147">Data processing failed.</span></span>
- <span data-ttu-id="9f412-148">Kihagyott.</span><span class="sxs-lookup"><span data-stu-id="9f412-148">Skipped.</span></span>
<span data-ttu-id="9f412-149">Az adatszelet feldolgozása kihagyva.</span><span class="sxs-lookup"><span data-stu-id="9f412-149">Skipped processing the data slice.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Failed, InProgress, Ready, Skipped, Waiting

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f412-150">-UpdateType</span><span class="sxs-lookup"><span data-stu-id="9f412-150">-UpdateType</span></span>
<span data-ttu-id="9f412-151">A szelet frissítésének típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f412-151">Specifies the type of update to the slice.</span></span>
<span data-ttu-id="9f412-152">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="9f412-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9f412-153">Egyéni.</span><span class="sxs-lookup"><span data-stu-id="9f412-153">Individual.</span></span>
<span data-ttu-id="9f412-154">A megadott időtartományban beállítja az adatkészlet minden egyes szeletének állapotát.</span><span class="sxs-lookup"><span data-stu-id="9f412-154">Sets the status of each slice for the dataset in the specified time range.</span></span> 
- <span data-ttu-id="9f412-155">UpstreamInPipeline.</span><span class="sxs-lookup"><span data-stu-id="9f412-155">UpstreamInPipeline.</span></span>
<span data-ttu-id="9f412-156">Beállítja az adatkészlet minden egyes szeletének állapotát, valamint az összes függő adatkészletet, amely a csővezetéken végzett tevékenységekhez bemeneti adatkészletként van használatban.</span><span class="sxs-lookup"><span data-stu-id="9f412-156">Sets the status of each slice for the dataset and all the dependent datasets, which are used as input datasets for activities in the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Individual, UpstreamInPipeline

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f412-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f412-157">CommonParameters</span></span>
<span data-ttu-id="9f412-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9f412-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f412-159">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f412-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f412-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f412-160">INPUTS</span></span>

### <span data-ttu-id="9f412-161">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9f412-161">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="9f412-162">System. String</span><span class="sxs-lookup"><span data-stu-id="9f412-162">System.String</span></span>

## <span data-ttu-id="9f412-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f412-163">OUTPUTS</span></span>

### <span data-ttu-id="9f412-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9f412-164">System.Boolean</span></span>

## <span data-ttu-id="9f412-165">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9f412-165">NOTES</span></span>
* <span data-ttu-id="9f412-166">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="9f412-166">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9f412-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f412-167">RELATED LINKS</span></span>

[<span data-ttu-id="9f412-168">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="9f412-168">Get-AzDataFactorySlice</span></span>](./Get-AzDataFactorySlice.md)


