---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
ms.openlocfilehash: 8e1d189173c9825876018351ef36a2b73f285a24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493153"
---
# <span data-ttu-id="f4ed8-101">Set-AzureRmDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="f4ed8-101">Set-AzureRmDataFactorySliceStatus</span></span>

## <span data-ttu-id="f4ed8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f4ed8-102">SYNOPSIS</span></span>
<span data-ttu-id="f4ed8-103">A szeletek állapotát állítja be egy adatkészlethez az Azure Data Factory-ban.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-103">Sets the status of slices for a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4ed8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f4ed8-104">SYNTAX</span></span>

### <span data-ttu-id="f4ed8-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f4ed8-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4ed8-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f4ed8-106">ByFactoryObject</span></span>
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4ed8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f4ed8-107">DESCRIPTION</span></span>
<span data-ttu-id="f4ed8-108">A **set-AzureRmDataFactorySliceStatus** parancsmag az Azure Data Factory adatkészlethez tartozó szeletek állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-108">The **Set-AzureRmDataFactorySliceStatus** cmdlet sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="f4ed8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f4ed8-109">EXAMPLES</span></span>

### <span data-ttu-id="f4ed8-110">Példa 1: az összes szelet állapotának beállítása</span><span class="sxs-lookup"><span data-stu-id="f4ed8-110">Example 1: Set the status of all slices</span></span>
```
PS C:\>Set-AzureRmDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

<span data-ttu-id="f4ed8-111">Ez a parancs beállítja a DAWikiAggregatedData nevű adatkészlet összes szeletének állapotát a WikiADF nevű adatgyárban való várakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-111">This command sets the status of all slices for the dataset named DAWikiAggregatedData to Waiting in the data factory named WikiADF.</span></span>
<span data-ttu-id="f4ed8-112">A *UpdateType* paraméter a UpstreamInPipeline értékét tartalmazza, így a parancs az adatkészlet minden egyes szeletének állapotát és a függő adatkészletek állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-112">The *UpdateType* parameter has a value of UpstreamInPipeline, and so the command sets the status of each slice for the dataset and all dependent datasets.</span></span>
<span data-ttu-id="f4ed8-113">A függő adatkészletek beviteli adatkészletként használhatók a csővezetéken végzett tevékenységekhez.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-113">Dependent datasets are used as input datasets for activities in the pipeline.</span></span>
<span data-ttu-id="f4ed8-114">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-114">This command returns a value of $True.</span></span>

## <span data-ttu-id="f4ed8-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f4ed8-115">PARAMETERS</span></span>

### <span data-ttu-id="f4ed8-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f4ed8-116">-DataFactory</span></span>
<span data-ttu-id="f4ed8-117">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-117">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="f4ed8-118">Ez a parancsmag módosítja az adatfeldolgozóhoz tartozó szeletek állapotát, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-118">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed8-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f4ed8-119">-DataFactoryName</span></span>
<span data-ttu-id="f4ed8-120">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-120">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f4ed8-121">Ez a parancsmag módosítja az adatfeldolgozóhoz tartozó szeletek állapotát, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-121">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed8-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="f4ed8-122">-DatasetName</span></span>
<span data-ttu-id="f4ed8-123">Annak az adatkészletnek a neve, amelyhez ez a parancsmag módosítja a szeleteket.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-123">Specifies the name of the dataset for which this cmdlet modifies slices.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4ed8-124">-DefaultProfile</span></span>
<span data-ttu-id="f4ed8-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f4ed8-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed8-126">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="f4ed8-126">-EndDateTime</span></span>
<span data-ttu-id="f4ed8-127">Az időszak végét **datetime** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-127">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="f4ed8-128">Ez az idő az adatszeletek vége.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-128">This time is the end of a data slice.</span></span>
<span data-ttu-id="f4ed8-129">A **datetime** -objektumokkal kapcsolatos további tudnivalókért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="f4ed8-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="f4ed8-130">A *EndDateTime* a ISO8601 formátumban kell megadni az alábbi példákban:</span><span class="sxs-lookup"><span data-stu-id="f4ed8-130">*EndDateTime* must be specified in the ISO8601 format as in the following examples:</span></span> 

<span data-ttu-id="f4ed8-131">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific standard Time)</span><span class="sxs-lookup"><span data-stu-id="f4ed8-131">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time)</span></span>

<span data-ttu-id="f4ed8-132">Az alapértelmezett időzóna-kijelölés az UTC.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-132">The default time zone designator is UTC.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4ed8-133">-ResourceGroupName</span></span>
<span data-ttu-id="f4ed8-134">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f4ed8-135">Ez a parancsmag módosítja annak a csoportnak a szeletét, amelyhez a paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-135">This cmdlet modifies the status of slices that belong to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed8-136">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="f4ed8-136">-StartDateTime</span></span>
<span data-ttu-id="f4ed8-137">Az időszak kezdését **datetime** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-137">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="f4ed8-138">Ez az idő az adatszeletek kezdetét jelentik.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-138">This time is the beginning of a data slice.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed8-139">-Állapot</span><span class="sxs-lookup"><span data-stu-id="f4ed8-139">-Status</span></span>
<span data-ttu-id="f4ed8-140">Az adatszelethez hozzárendelni kívánt állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-140">Specifies a status to assign to the data slice.</span></span>
<span data-ttu-id="f4ed8-141">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f4ed8-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f4ed8-142">Várakozás.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-142">Waiting.</span></span>
<span data-ttu-id="f4ed8-143">Az adatszeletek az érvényesítési szabályoknak a feldolgozás előtt való érvényesítésére várnak.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-143">Data slice is waiting for validation against validation policies before being processed.</span></span> 
- <span data-ttu-id="f4ed8-144">Kész.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-144">Ready.</span></span>
<span data-ttu-id="f4ed8-145">Az adatfeldolgozás befejeződött, és az adatszelet készen áll.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-145">Data processing has completed and the data slice is ready.</span></span>
- <span data-ttu-id="f4ed8-146">Folyamatban van.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-146">InProgress.</span></span>
<span data-ttu-id="f4ed8-147">Folyamatban van az adatfeldolgozás.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-147">Data processing is in-progress.</span></span> 
- <span data-ttu-id="f4ed8-148">Sikertelen.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-148">Failed.</span></span>
<span data-ttu-id="f4ed8-149">Sikertelen az adatfeldolgozás.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-149">Data processing failed.</span></span>
- <span data-ttu-id="f4ed8-150">Kihagyott.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-150">Skipped.</span></span>
<span data-ttu-id="f4ed8-151">Az adatszelet feldolgozása kihagyva.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-151">Skipped processing the data slice.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Failed, InProgress, Ready, Skipped, Waiting

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed8-152">-UpdateType</span><span class="sxs-lookup"><span data-stu-id="f4ed8-152">-UpdateType</span></span>
<span data-ttu-id="f4ed8-153">A szelet frissítésének típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-153">Specifies the type of update to the slice.</span></span>
<span data-ttu-id="f4ed8-154">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f4ed8-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f4ed8-155">Egyéni.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-155">Individual.</span></span>
<span data-ttu-id="f4ed8-156">A megadott időtartományban beállítja az adatkészlet minden egyes szeletének állapotát.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-156">Sets the status of each slice for the dataset in the specified time range.</span></span> 
- <span data-ttu-id="f4ed8-157">UpstreamInPipeline.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-157">UpstreamInPipeline.</span></span>
<span data-ttu-id="f4ed8-158">Beállítja az adatkészlet minden egyes szeletének állapotát, valamint az összes függő adatkészletet, amely a csővezetéken végzett tevékenységekhez bemeneti adatkészletként van használatban.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-158">Sets the status of each slice for the dataset and all the dependent datasets, which are used as input datasets for activities in the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Individual, UpstreamInPipeline

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ed8-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4ed8-159">CommonParameters</span></span>
<span data-ttu-id="f4ed8-160">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f4ed8-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4ed8-161">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4ed8-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4ed8-162">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4ed8-162">INPUTS</span></span>

### <span data-ttu-id="f4ed8-163">Nincs</span><span class="sxs-lookup"><span data-stu-id="f4ed8-163">None</span></span>
<span data-ttu-id="f4ed8-164">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="f4ed8-164">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f4ed8-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4ed8-165">OUTPUTS</span></span>

### <span data-ttu-id="f4ed8-166">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f4ed8-166">System.Boolean</span></span>

## <span data-ttu-id="f4ed8-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f4ed8-167">NOTES</span></span>
* <span data-ttu-id="f4ed8-168">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="f4ed8-168">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f4ed8-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4ed8-169">RELATED LINKS</span></span>

[<span data-ttu-id="f4ed8-170">Get-AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="f4ed8-170">Get-AzureRmDataFactorySlice</span></span>](./Get-AzureRmDataFactorySlice.md)


