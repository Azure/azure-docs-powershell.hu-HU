---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
ms.openlocfilehash: 80a471b88856ff4c7425e89fd6e5b73168370789
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942881"
---
# <span data-ttu-id="f561c-101">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="f561c-101">Set-AzDataFactorySliceStatus</span></span>

## <span data-ttu-id="f561c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f561c-102">SYNOPSIS</span></span>
<span data-ttu-id="f561c-103">Egy adatkészlet szeletének állapotát állítja be az Azure Data Factoryban.</span><span class="sxs-lookup"><span data-stu-id="f561c-103">Sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="f561c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f561c-104">SYNTAX</span></span>

### <span data-ttu-id="f561c-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f561c-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f561c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f561c-106">ByFactoryObject</span></span>
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f561c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f561c-107">DESCRIPTION</span></span>
<span data-ttu-id="f561c-108">A **Set-AzDataFactorySliceStatus** parancsmag beállítja egy adatkészlet szeletének állapotát az Azure Data Factoryban.</span><span class="sxs-lookup"><span data-stu-id="f561c-108">The **Set-AzDataFactorySliceStatus** cmdlet sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="f561c-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f561c-109">EXAMPLES</span></span>

### <span data-ttu-id="f561c-110">1. példa: Az összes szelet állapotának beállítása</span><span class="sxs-lookup"><span data-stu-id="f561c-110">Example 1: Set the status of all slices</span></span>
```
PS C:\>Set-AzDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

<span data-ttu-id="f561c-111">Ez a parancs a DAWikiAggregatedData nevű adatkészlet összes szeletének állapotát Várakozásra állítja a WikiADF nevű adathalmazban.</span><span class="sxs-lookup"><span data-stu-id="f561c-111">This command sets the status of all slices for the dataset named DAWikiAggregatedData to Waiting in the data factory named WikiADF.</span></span>
<span data-ttu-id="f561c-112">Az *UpdateType* paraméter értéke UpstreamInPipeline, ezért a parancs beállítja az egyes szeletek állapotát az adatkészlethez és az összes függő adatkészlethez.</span><span class="sxs-lookup"><span data-stu-id="f561c-112">The *UpdateType* parameter has a value of UpstreamInPipeline, and so the command sets the status of each slice for the dataset and all dependent datasets.</span></span>
<span data-ttu-id="f561c-113">A függő adatkészletek bemeneti adatkészletekként használatosak a folyamat tevékenységeihez.</span><span class="sxs-lookup"><span data-stu-id="f561c-113">Dependent datasets are used as input datasets for activities in the pipeline.</span></span>
<span data-ttu-id="f561c-114">Ez a parancs egy számértéket ad $True.</span><span class="sxs-lookup"><span data-stu-id="f561c-114">This command returns a value of $True.</span></span>

## <span data-ttu-id="f561c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f561c-115">PARAMETERS</span></span>

### <span data-ttu-id="f561c-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f561c-116">-DataFactory</span></span>
<span data-ttu-id="f561c-117">EGY **PSDataFactory-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="f561c-117">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="f561c-118">Ez a parancsmag módosítja a paraméter által megadott adat factoryhoz tartozó szeletek állapotát.</span><span class="sxs-lookup"><span data-stu-id="f561c-118">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f561c-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f561c-119">-DataFactoryName</span></span>
<span data-ttu-id="f561c-120">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f561c-120">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f561c-121">Ez a parancsmag módosítja a paraméter által megadott adat factoryhoz tartozó szeletek állapotát.</span><span class="sxs-lookup"><span data-stu-id="f561c-121">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f561c-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="f561c-122">-DatasetName</span></span>
<span data-ttu-id="f561c-123">Annak az adatkészletnek a nevét adja meg, amelynek a parancsmagja módosítja a szeleteket.</span><span class="sxs-lookup"><span data-stu-id="f561c-123">Specifies the name of the dataset for which this cmdlet modifies slices.</span></span>

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

### <span data-ttu-id="f561c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f561c-124">-DefaultProfile</span></span>
<span data-ttu-id="f561c-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f561c-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f561c-126">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="f561c-126">-EndDateTime</span></span>
<span data-ttu-id="f561c-127">Egy időtartomány végét adja meg **DateTime-objektumként.**</span><span class="sxs-lookup"><span data-stu-id="f561c-127">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="f561c-128">Ez az idő az adatszelet vége.</span><span class="sxs-lookup"><span data-stu-id="f561c-128">This time is the end of a data slice.</span></span>
<span data-ttu-id="f561c-129">A **DateTime-objektumokról** további információt ad `Get-Help Get-Date` meg.</span><span class="sxs-lookup"><span data-stu-id="f561c-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="f561c-130">Az *EndDateTime* értéket ISO8601 formátumban kell megadni, az alábbi példák szerint: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Csendes-óceáni téli idő) Az alapértelmezett időzóna-tervező az UTC.</span><span class="sxs-lookup"><span data-stu-id="f561c-130">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="f561c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f561c-131">-ResourceGroupName</span></span>
<span data-ttu-id="f561c-132">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f561c-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f561c-133">Ez a parancsmag módosítja a paraméter által megadott csoporthoz tartozó szeletek állapotát.</span><span class="sxs-lookup"><span data-stu-id="f561c-133">This cmdlet modifies the status of slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f561c-134">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="f561c-134">-StartDateTime</span></span>
<span data-ttu-id="f561c-135">Egy időtartomány kezdő időpontját adja meg **DateTime-objektumként.**</span><span class="sxs-lookup"><span data-stu-id="f561c-135">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="f561c-136">Ez az időpont egy adatszelet elején van.</span><span class="sxs-lookup"><span data-stu-id="f561c-136">This time is the beginning of a data slice.</span></span>

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

### <span data-ttu-id="f561c-137">-Állapot</span><span class="sxs-lookup"><span data-stu-id="f561c-137">-Status</span></span>
<span data-ttu-id="f561c-138">Megadja az adatszelethez hozzárendelni szükséges állapotot.</span><span class="sxs-lookup"><span data-stu-id="f561c-138">Specifies a status to assign to the data slice.</span></span>
<span data-ttu-id="f561c-139">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="f561c-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f561c-140">Várakozás.</span><span class="sxs-lookup"><span data-stu-id="f561c-140">Waiting.</span></span>
<span data-ttu-id="f561c-141">Az adatszelet a feldolgozás előtt érvényesítési házirendekre vár.</span><span class="sxs-lookup"><span data-stu-id="f561c-141">Data slice is waiting for validation against validation policies before being processed.</span></span> 
- <span data-ttu-id="f561c-142">Kész.</span><span class="sxs-lookup"><span data-stu-id="f561c-142">Ready.</span></span>
<span data-ttu-id="f561c-143">Az adatkezelés befejeződött, és az adatszelet készen áll.</span><span class="sxs-lookup"><span data-stu-id="f561c-143">Data processing has completed and the data slice is ready.</span></span>
- <span data-ttu-id="f561c-144">InProgress.</span><span class="sxs-lookup"><span data-stu-id="f561c-144">InProgress.</span></span>
<span data-ttu-id="f561c-145">Az adatok feldolgozása folyamatban van.</span><span class="sxs-lookup"><span data-stu-id="f561c-145">Data processing is in-progress.</span></span> 
- <span data-ttu-id="f561c-146">Sikertelen.</span><span class="sxs-lookup"><span data-stu-id="f561c-146">Failed.</span></span>
<span data-ttu-id="f561c-147">Az adatkezelés nem sikerült.</span><span class="sxs-lookup"><span data-stu-id="f561c-147">Data processing failed.</span></span>
- <span data-ttu-id="f561c-148">Kihagyva.</span><span class="sxs-lookup"><span data-stu-id="f561c-148">Skipped.</span></span>
<span data-ttu-id="f561c-149">Kihagyta az adatszelet feldolgozását.</span><span class="sxs-lookup"><span data-stu-id="f561c-149">Skipped processing the data slice.</span></span>

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

### <span data-ttu-id="f561c-150">-UpdateType</span><span class="sxs-lookup"><span data-stu-id="f561c-150">-UpdateType</span></span>
<span data-ttu-id="f561c-151">A szelet frissítésének típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="f561c-151">Specifies the type of update to the slice.</span></span>
<span data-ttu-id="f561c-152">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="f561c-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f561c-153">Egyéni.</span><span class="sxs-lookup"><span data-stu-id="f561c-153">Individual.</span></span>
<span data-ttu-id="f561c-154">Beállítja a megadott időtartományban az adatkészlet egyes szeletének állapotát.</span><span class="sxs-lookup"><span data-stu-id="f561c-154">Sets the status of each slice for the dataset in the specified time range.</span></span> 
- <span data-ttu-id="f561c-155">UpstreamInPipeline.</span><span class="sxs-lookup"><span data-stu-id="f561c-155">UpstreamInPipeline.</span></span>
<span data-ttu-id="f561c-156">Beállítja az adatkészlet egyes szeletei és a függő adatkészletek állapotát, amelyek a folyamat tevékenységeinek bemeneti adatkészleteiként használatosak.</span><span class="sxs-lookup"><span data-stu-id="f561c-156">Sets the status of each slice for the dataset and all the dependent datasets, which are used as input datasets for activities in the pipeline.</span></span>

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

### <span data-ttu-id="f561c-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f561c-157">CommonParameters</span></span>
<span data-ttu-id="f561c-158">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f561c-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f561c-159">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f561c-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f561c-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f561c-160">INPUTS</span></span>

### <span data-ttu-id="f561c-161">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f561c-161">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="f561c-162">System.String</span><span class="sxs-lookup"><span data-stu-id="f561c-162">System.String</span></span>

## <span data-ttu-id="f561c-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f561c-163">OUTPUTS</span></span>

### <span data-ttu-id="f561c-164">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f561c-164">System.Boolean</span></span>

## <span data-ttu-id="f561c-165">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f561c-165">NOTES</span></span>
* <span data-ttu-id="f561c-166">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="f561c-166">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f561c-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f561c-167">RELATED LINKS</span></span>

[<span data-ttu-id="f561c-168">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="f561c-168">Get-AzDataFactorySlice</span></span>](./Get-AzDataFactorySlice.md)


