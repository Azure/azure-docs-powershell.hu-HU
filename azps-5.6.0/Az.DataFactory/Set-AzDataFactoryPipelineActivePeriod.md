---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D853A91F-95E7-4C36-AC0F-2C10DFCF68F8
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactorypipelineactiveperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
ms.openlocfilehash: 5cbb353a0a6349842878ef787b75c1ce34b1cfd3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925081"
---
# <span data-ttu-id="43847-101">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="43847-101">Set-AzDataFactoryPipelineActivePeriod</span></span>

## <span data-ttu-id="43847-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43847-102">SYNOPSIS</span></span>
<span data-ttu-id="43847-103">Az adatszeletek aktív időszakának beállítása.</span><span class="sxs-lookup"><span data-stu-id="43847-103">Configures the active period for data slices.</span></span>

## <span data-ttu-id="43847-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="43847-104">SYNTAX</span></span>

### <span data-ttu-id="43847-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="43847-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactoryName] <String>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43847-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="43847-106">ByFactoryObject</span></span>
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactory] <PSDataFactory>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43847-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="43847-107">DESCRIPTION</span></span>
<span data-ttu-id="43847-108">A **Set-AzDataFactoryPipelineActivePeriod** parancsmag konfigurálja az Azure Data Factory-folyamat által feldolgozott adatszeletek aktív időszakát.</span><span class="sxs-lookup"><span data-stu-id="43847-108">The **Set-AzDataFactoryPipelineActivePeriod** cmdlet configures the active period for the data slices that are processed by a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="43847-109">Ha a Set-AzDataFactorySliceStatus-parancsmag használatával módosítja egy adatkészlet szeletének állapotát, ellenőrizze, hogy a szelet kezdési és záró ideje a folyamat aktív időszakában van-e.</span><span class="sxs-lookup"><span data-stu-id="43847-109">If you use the Set-AzDataFactorySliceStatus cmdlet to modify the status of slices for a dataset, make sure that the start time and end time for a slice are in the active period of the pipeline.</span></span>
<span data-ttu-id="43847-110">A folyamat létrehozása után megadhatja az adatok feldolgozásának időszakát.</span><span class="sxs-lookup"><span data-stu-id="43847-110">After you create a pipeline, you can specify the period in which data processing occurs.</span></span>
<span data-ttu-id="43847-111">Egy folyamat aktív időszakának megadása meghatározza az adatszeletek feldolgozásának időtartamát  az egyes Data Factory-adatkészletek elérhetőségi tulajdonságai alapján.</span><span class="sxs-lookup"><span data-stu-id="43847-111">Specifying the active period for a pipeline defines the time duration in which the data slices are processed based on the **Availability** properties that were defined for each Data Factory dataset.</span></span>

## <span data-ttu-id="43847-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="43847-112">EXAMPLES</span></span>

### <span data-ttu-id="43847-113">1. példa: Az aktív időszak konfigurálása</span><span class="sxs-lookup"><span data-stu-id="43847-113">Example 1: Configure the active period</span></span>
```
PS C:\>Set-AzDataFactoryPipelineActivePeriod -ResourceGroupName "ADF" -PipelineName "DPWikisample" -DataFactoryName "WikiADF" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-22T16:00:00Z
Confirm
Are you sure you want to set pipeline 'DPWikisample' active period from '05/21/2014 16:00:00' to
'05/22/2014 16:00:00'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="43847-114">Ez a parancs beállítja a DPWikisample nevű folyamat adatszeletei aktív időszakát.</span><span class="sxs-lookup"><span data-stu-id="43847-114">This command configures the active period for the data slices that the pipeline named DPWikisample processes.</span></span>
<span data-ttu-id="43847-115">A parancs értékként biztosítja az adatszeletek kezdő és záró pontjait.</span><span class="sxs-lookup"><span data-stu-id="43847-115">The command provides beginning and end points for the data slices as values.</span></span>
<span data-ttu-id="43847-116">A parancs egy számértéket ad $True.</span><span class="sxs-lookup"><span data-stu-id="43847-116">The command returns a value of $True.</span></span>

## <span data-ttu-id="43847-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43847-117">PARAMETERS</span></span>

### <span data-ttu-id="43847-118">-AutoResolve</span><span class="sxs-lookup"><span data-stu-id="43847-118">-AutoResolve</span></span>
<span data-ttu-id="43847-119">Azt jelzi, hogy ez a parancsmag automatikusan feloldja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="43847-119">Indicates that this cmdlet uses auto resolve.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43847-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="43847-120">-DataFactory</span></span>
<span data-ttu-id="43847-121">EGY **PSDataFactory-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="43847-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="43847-122">Ez a parancsmag módosítja egy olyan folyamat aktív időszakát, amely a paraméter által megadott adatüzemhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="43847-122">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="43847-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="43847-123">-DataFactoryName</span></span>
<span data-ttu-id="43847-124">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="43847-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="43847-125">Ez a parancsmag módosítja egy olyan folyamat aktív időszakát, amely a paraméter által megadott adatüzemhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="43847-125">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="43847-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43847-126">-DefaultProfile</span></span>
<span data-ttu-id="43847-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="43847-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43847-128">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="43847-128">-EndDateTime</span></span>
<span data-ttu-id="43847-129">Egy időtartomány végét adja meg **DateTime-objektumként.**</span><span class="sxs-lookup"><span data-stu-id="43847-129">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="43847-130">Az adatok feldolgozása vagy az adatszeletek feldolgozása ezen az időszakon belül történik.</span><span class="sxs-lookup"><span data-stu-id="43847-130">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="43847-131">A **DateTime-objektumokról** további információt ad `Get-Help Get-Date` meg.</span><span class="sxs-lookup"><span data-stu-id="43847-131">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="43847-132">Az *EndDateTime* értéket ISO8601 formátumban kell megadni, az alábbi példák szerint: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Csendes-óceáni téli idő) Az alapértelmezett időzóna-tervező az UTC.</span><span class="sxs-lookup"><span data-stu-id="43847-132">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="43847-133">-ForceRecalculate</span><span class="sxs-lookup"><span data-stu-id="43847-133">-ForceRecalculate</span></span>
<span data-ttu-id="43847-134">Azt jelzi, hogy a parancsmag kényszerített újraszámítást használ.</span><span class="sxs-lookup"><span data-stu-id="43847-134">Indicates that this cmdlet uses force recalculate.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43847-135">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="43847-135">-PipelineName</span></span>
<span data-ttu-id="43847-136">A folyamat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="43847-136">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="43847-137">Ez a parancsmag beállítja a paraméter által megadott folyamat aktív időszakát.</span><span class="sxs-lookup"><span data-stu-id="43847-137">This cmdlet sets the active period for the pipeline that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43847-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43847-138">-ResourceGroupName</span></span>
<span data-ttu-id="43847-139">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="43847-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="43847-140">Ez a parancsmag módosítja egy olyan folyamat aktív időszakát, amely a paraméter által megadott csoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="43847-140">This cmdlet modifies the active period for a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="43847-141">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="43847-141">-StartDateTime</span></span>
<span data-ttu-id="43847-142">Egy időtartomány kezdő időpontját adja meg **DateTime-objektumként.**</span><span class="sxs-lookup"><span data-stu-id="43847-142">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="43847-143">Az adatok feldolgozása vagy az adatszeletek feldolgozása ezen az időszakon belül történik.</span><span class="sxs-lookup"><span data-stu-id="43847-143">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="43847-144">*A StartDateTime* értéket ISO8601 formátumban kell megadni.</span><span class="sxs-lookup"><span data-stu-id="43847-144">*StartDateTime* must be specified in the ISO8601 format.</span></span>

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

### <span data-ttu-id="43847-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43847-145">-Confirm</span></span>
<span data-ttu-id="43847-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="43847-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43847-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43847-147">-WhatIf</span></span>
<span data-ttu-id="43847-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="43847-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43847-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="43847-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43847-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43847-150">CommonParameters</span></span>
<span data-ttu-id="43847-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43847-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43847-152">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43847-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43847-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="43847-153">INPUTS</span></span>

### <span data-ttu-id="43847-154">System.String</span><span class="sxs-lookup"><span data-stu-id="43847-154">System.String</span></span>

### <span data-ttu-id="43847-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="43847-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="43847-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43847-156">OUTPUTS</span></span>

### <span data-ttu-id="43847-157">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="43847-157">System.Boolean</span></span>

## <span data-ttu-id="43847-158">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="43847-158">NOTES</span></span>
* <span data-ttu-id="43847-159">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="43847-159">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="43847-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43847-160">RELATED LINKS</span></span>

[<span data-ttu-id="43847-161">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="43847-161">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="43847-162">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="43847-162">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)


