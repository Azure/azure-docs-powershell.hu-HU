---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
ms.openlocfilehash: ce1d81fc0226c7c44682d67cb666e3e63dfd5816
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496276"
---
# <span data-ttu-id="b8950-101">Set-AzureRmDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="b8950-101">Set-AzureRmDataFactorySliceStatus</span></span>

## <span data-ttu-id="b8950-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b8950-102">SYNOPSIS</span></span>
<span data-ttu-id="b8950-103">A szeletek állapotát állítja be egy adatkészlethez az Azure Data Factory-ban.</span><span class="sxs-lookup"><span data-stu-id="b8950-103">Sets the status of slices for a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8950-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b8950-104">SYNTAX</span></span>

### <span data-ttu-id="b8950-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b8950-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8950-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b8950-106">ByFactoryObject</span></span>
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8950-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b8950-107">DESCRIPTION</span></span>
<span data-ttu-id="b8950-108">A **set-AzureRmDataFactorySliceStatus** parancsmag az Azure Data Factory adatkészlethez tartozó szeletek állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="b8950-108">The **Set-AzureRmDataFactorySliceStatus** cmdlet sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="b8950-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b8950-109">EXAMPLES</span></span>

### <span data-ttu-id="b8950-110">Példa 1: az összes szelet állapotának beállítása</span><span class="sxs-lookup"><span data-stu-id="b8950-110">Example 1: Set the status of all slices</span></span>
```
PS C:\>Set-AzureRmDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

<span data-ttu-id="b8950-111">Ez a parancs beállítja a DAWikiAggregatedData nevű adatkészlet összes szeletének állapotát a WikiADF nevű adatgyárban való várakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="b8950-111">This command sets the status of all slices for the dataset named DAWikiAggregatedData to Waiting in the data factory named WikiADF.</span></span>
<span data-ttu-id="b8950-112">A *UpdateType* paraméter a UpstreamInPipeline értékét tartalmazza, így a parancs az adatkészlet minden egyes szeletének állapotát és a függő adatkészletek állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="b8950-112">The *UpdateType* parameter has a value of UpstreamInPipeline, and so the command sets the status of each slice for the dataset and all dependent datasets.</span></span>
<span data-ttu-id="b8950-113">A függő adatkészletek beviteli adatkészletként használhatók a csővezetéken végzett tevékenységekhez.</span><span class="sxs-lookup"><span data-stu-id="b8950-113">Dependent datasets are used as input datasets for activities in the pipeline.</span></span>
<span data-ttu-id="b8950-114">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="b8950-114">This command returns a value of $True.</span></span>

## <span data-ttu-id="b8950-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b8950-115">PARAMETERS</span></span>

### <span data-ttu-id="b8950-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b8950-116">-DataFactory</span></span>
<span data-ttu-id="b8950-117">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="b8950-117">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="b8950-118">Ez a parancsmag módosítja az adatfeldolgozóhoz tartozó szeletek állapotát, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8950-118">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b8950-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b8950-119">-DataFactoryName</span></span>
<span data-ttu-id="b8950-120">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8950-120">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b8950-121">Ez a parancsmag módosítja az adatfeldolgozóhoz tartozó szeletek állapotát, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8950-121">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b8950-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="b8950-122">-DatasetName</span></span>
<span data-ttu-id="b8950-123">Annak az adatkészletnek a neve, amelyhez ez a parancsmag módosítja a szeleteket.</span><span class="sxs-lookup"><span data-stu-id="b8950-123">Specifies the name of the dataset for which this cmdlet modifies slices.</span></span>

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

### <span data-ttu-id="b8950-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8950-124">-DefaultProfile</span></span>
<span data-ttu-id="b8950-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b8950-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8950-126">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="b8950-126">-EndDateTime</span></span>
<span data-ttu-id="b8950-127">Az időszak végét **datetime** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8950-127">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="b8950-128">Ez az idő az adatszeletek vége.</span><span class="sxs-lookup"><span data-stu-id="b8950-128">This time is the end of a data slice.</span></span>
<span data-ttu-id="b8950-129">A **datetime** -objektumokkal kapcsolatos további tudnivalókért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="b8950-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="b8950-130">A *EndDateTime* a ISO8601 formátumban kell megadni: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (Pacific standard Time) az alapértelmezett időzóna-megjelölést az UTC adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8950-130">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="b8950-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8950-131">-ResourceGroupName</span></span>
<span data-ttu-id="b8950-132">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8950-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b8950-133">Ez a parancsmag módosítja annak a csoportnak a szeletét, amelyhez a paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="b8950-133">This cmdlet modifies the status of slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b8950-134">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="b8950-134">-StartDateTime</span></span>
<span data-ttu-id="b8950-135">Az időszak kezdését **datetime** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8950-135">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="b8950-136">Ez az idő az adatszeletek kezdetét jelentik.</span><span class="sxs-lookup"><span data-stu-id="b8950-136">This time is the beginning of a data slice.</span></span>

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

### <span data-ttu-id="b8950-137">-Állapot</span><span class="sxs-lookup"><span data-stu-id="b8950-137">-Status</span></span>
<span data-ttu-id="b8950-138">Az adatszelethez hozzárendelni kívánt állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8950-138">Specifies a status to assign to the data slice.</span></span>
<span data-ttu-id="b8950-139">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b8950-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b8950-140">Várakozás.</span><span class="sxs-lookup"><span data-stu-id="b8950-140">Waiting.</span></span>
<span data-ttu-id="b8950-141">Az adatszeletek az érvényesítési szabályoknak a feldolgozás előtt való érvényesítésére várnak.</span><span class="sxs-lookup"><span data-stu-id="b8950-141">Data slice is waiting for validation against validation policies before being processed.</span></span> 
- <span data-ttu-id="b8950-142">Kész.</span><span class="sxs-lookup"><span data-stu-id="b8950-142">Ready.</span></span>
<span data-ttu-id="b8950-143">Az adatfeldolgozás befejeződött, és az adatszelet készen áll.</span><span class="sxs-lookup"><span data-stu-id="b8950-143">Data processing has completed and the data slice is ready.</span></span>
- <span data-ttu-id="b8950-144">Folyamatban van.</span><span class="sxs-lookup"><span data-stu-id="b8950-144">InProgress.</span></span>
<span data-ttu-id="b8950-145">Folyamatban van az adatfeldolgozás.</span><span class="sxs-lookup"><span data-stu-id="b8950-145">Data processing is in-progress.</span></span> 
- <span data-ttu-id="b8950-146">Sikertelen.</span><span class="sxs-lookup"><span data-stu-id="b8950-146">Failed.</span></span>
<span data-ttu-id="b8950-147">Sikertelen az adatfeldolgozás.</span><span class="sxs-lookup"><span data-stu-id="b8950-147">Data processing failed.</span></span>
- <span data-ttu-id="b8950-148">Kihagyott.</span><span class="sxs-lookup"><span data-stu-id="b8950-148">Skipped.</span></span>
<span data-ttu-id="b8950-149">Az adatszelet feldolgozása kihagyva.</span><span class="sxs-lookup"><span data-stu-id="b8950-149">Skipped processing the data slice.</span></span>

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

### <span data-ttu-id="b8950-150">-UpdateType</span><span class="sxs-lookup"><span data-stu-id="b8950-150">-UpdateType</span></span>
<span data-ttu-id="b8950-151">A szelet frissítésének típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8950-151">Specifies the type of update to the slice.</span></span>
<span data-ttu-id="b8950-152">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b8950-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b8950-153">Egyéni.</span><span class="sxs-lookup"><span data-stu-id="b8950-153">Individual.</span></span>
<span data-ttu-id="b8950-154">A megadott időtartományban beállítja az adatkészlet minden egyes szeletének állapotát.</span><span class="sxs-lookup"><span data-stu-id="b8950-154">Sets the status of each slice for the dataset in the specified time range.</span></span> 
- <span data-ttu-id="b8950-155">UpstreamInPipeline.</span><span class="sxs-lookup"><span data-stu-id="b8950-155">UpstreamInPipeline.</span></span>
<span data-ttu-id="b8950-156">Beállítja az adatkészlet minden egyes szeletének állapotát, valamint az összes függő adatkészletet, amely a csővezetéken végzett tevékenységekhez bemeneti adatkészletként van használatban.</span><span class="sxs-lookup"><span data-stu-id="b8950-156">Sets the status of each slice for the dataset and all the dependent datasets, which are used as input datasets for activities in the pipeline.</span></span>

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

### <span data-ttu-id="b8950-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8950-157">CommonParameters</span></span>
<span data-ttu-id="b8950-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b8950-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8950-159">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8950-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8950-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8950-160">INPUTS</span></span>

### <span data-ttu-id="b8950-161">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b8950-161">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="b8950-162">System. String</span><span class="sxs-lookup"><span data-stu-id="b8950-162">System.String</span></span>

## <span data-ttu-id="b8950-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8950-163">OUTPUTS</span></span>

### <span data-ttu-id="b8950-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b8950-164">System.Boolean</span></span>

## <span data-ttu-id="b8950-165">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b8950-165">NOTES</span></span>
* <span data-ttu-id="b8950-166">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="b8950-166">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b8950-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8950-167">RELATED LINKS</span></span>

[<span data-ttu-id="b8950-168">Get-AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="b8950-168">Get-AzureRmDataFactorySlice</span></span>](./Get-AzureRmDataFactorySlice.md)


