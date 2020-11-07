---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D853A91F-95E7-4C36-AC0F-2C10DFCF68F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactorypipelineactiveperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
ms.openlocfilehash: edb2e94900d383675bd183c09df16e295828aae1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666980"
---
# <span data-ttu-id="a7df9-101">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="a7df9-101">Set-AzDataFactoryPipelineActivePeriod</span></span>

## <span data-ttu-id="a7df9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a7df9-102">SYNOPSIS</span></span>
<span data-ttu-id="a7df9-103">Az adatszeletek aktív időszakának beállítása.</span><span class="sxs-lookup"><span data-stu-id="a7df9-103">Configures the active period for data slices.</span></span>

## <span data-ttu-id="a7df9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a7df9-104">SYNTAX</span></span>

### <span data-ttu-id="a7df9-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a7df9-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactoryName] <String>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a7df9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a7df9-106">ByFactoryObject</span></span>
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactory] <PSDataFactory>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7df9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a7df9-107">DESCRIPTION</span></span>
<span data-ttu-id="a7df9-108">A **set-AzDataFactoryPipelineActivePeriod** parancsmag beállítja az adatszeletek aktív időszakát az Azure Data Factory által feldolgozott csővezetékekkel.</span><span class="sxs-lookup"><span data-stu-id="a7df9-108">The **Set-AzDataFactoryPipelineActivePeriod** cmdlet configures the active period for the data slices that are processed by a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="a7df9-109">Ha az Set-AzDataFactorySliceStatus parancsmagot használja az adatkészlet szeletei állapotának módosításához, győződjön meg arról, hogy a szelet kezdési és befejezési időpontja a csővezeték aktív időszakában van.</span><span class="sxs-lookup"><span data-stu-id="a7df9-109">If you use the Set-AzDataFactorySliceStatus cmdlet to modify the status of slices for a dataset, make sure that the start time and end time for a slice are in the active period of the pipeline.</span></span>
<span data-ttu-id="a7df9-110">Miután létrehozta a csővezetéket, megadhatja, hogy milyen időszakon belül történjen az adatfeldolgozás.</span><span class="sxs-lookup"><span data-stu-id="a7df9-110">After you create a pipeline, you can specify the period in which data processing occurs.</span></span>
<span data-ttu-id="a7df9-111">A csővezetékek aktív időszakának meghatározása: azt az időtartamot adja meg, amelyben az adatszeletek feldolgozása az egyes adatfeldolgozó-adatkészletekhez meghatározott **elérhetőségi** tulajdonságok alapján történik.</span><span class="sxs-lookup"><span data-stu-id="a7df9-111">Specifying the active period for a pipeline defines the time duration in which the data slices are processed based on the **Availability** properties that were defined for each Data Factory dataset.</span></span>

## <span data-ttu-id="a7df9-112">Példák</span><span class="sxs-lookup"><span data-stu-id="a7df9-112">EXAMPLES</span></span>

### <span data-ttu-id="a7df9-113">1. példa: az aktív időszak beállítása</span><span class="sxs-lookup"><span data-stu-id="a7df9-113">Example 1: Configure the active period</span></span>
```
PS C:\>Set-AzDataFactoryPipelineActivePeriod -ResourceGroupName "ADF" -PipelineName "DPWikisample" -DataFactoryName "WikiADF" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-22T16:00:00Z
Confirm
Are you sure you want to set pipeline 'DPWikisample' active period from '05/21/2014 16:00:00' to
'05/22/2014 16:00:00'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="a7df9-114">Ez a parancs beállítja az adatszeletek aktív időszakát a DPWikisample folyamatok nevű csővezetékhez.</span><span class="sxs-lookup"><span data-stu-id="a7df9-114">This command configures the active period for the data slices that the pipeline named DPWikisample processes.</span></span>
<span data-ttu-id="a7df9-115">A parancs az adatszeletek kezdő és záró pontját adja meg értékként.</span><span class="sxs-lookup"><span data-stu-id="a7df9-115">The command provides beginning and end points for the data slices as values.</span></span>
<span data-ttu-id="a7df9-116">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="a7df9-116">The command returns a value of $True.</span></span>

## <span data-ttu-id="a7df9-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a7df9-117">PARAMETERS</span></span>

### <span data-ttu-id="a7df9-118">-Autofeloldás</span><span class="sxs-lookup"><span data-stu-id="a7df9-118">-AutoResolve</span></span>
<span data-ttu-id="a7df9-119">Azt jelzi, hogy ez a parancsmag az automatikus feloldást használja.</span><span class="sxs-lookup"><span data-stu-id="a7df9-119">Indicates that this cmdlet uses auto resolve.</span></span>

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

### <span data-ttu-id="a7df9-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a7df9-120">-DataFactory</span></span>
<span data-ttu-id="a7df9-121">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="a7df9-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="a7df9-122">Ez a parancsmag módosította az adatfeldolgozóhoz tartozó csővezeték aktív időszakát, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="a7df9-122">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a7df9-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a7df9-123">-DataFactoryName</span></span>
<span data-ttu-id="a7df9-124">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a7df9-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a7df9-125">Ez a parancsmag módosította az adatfeldolgozóhoz tartozó csővezeték aktív időszakát, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="a7df9-125">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a7df9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7df9-126">-DefaultProfile</span></span>
<span data-ttu-id="a7df9-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a7df9-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7df9-128">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="a7df9-128">-EndDateTime</span></span>
<span data-ttu-id="a7df9-129">Az időszak végét **datetime** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="a7df9-129">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="a7df9-130">Ebben az időszakban dolgozzák fel az adatfeldolgozást vagy az adatszeleteket.</span><span class="sxs-lookup"><span data-stu-id="a7df9-130">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="a7df9-131">A **datetime** -objektumokkal kapcsolatos további tudnivalókért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="a7df9-131">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="a7df9-132">A *EndDateTime* a ISO8601 formátumban kell megadni: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (Pacific standard Time) az alapértelmezett időzóna-megjelölést az UTC adja meg.</span><span class="sxs-lookup"><span data-stu-id="a7df9-132">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="a7df9-133">-ForceRecalculate</span><span class="sxs-lookup"><span data-stu-id="a7df9-133">-ForceRecalculate</span></span>
<span data-ttu-id="a7df9-134">Azt jelzi, hogy ez a parancsmag a kényszerített újraszámítást használja.</span><span class="sxs-lookup"><span data-stu-id="a7df9-134">Indicates that this cmdlet uses force recalculate.</span></span>

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

### <span data-ttu-id="a7df9-135">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="a7df9-135">-PipelineName</span></span>
<span data-ttu-id="a7df9-136">A csővezeték nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a7df9-136">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="a7df9-137">Ez a parancsmag az aktív időszakot adja meg ahhoz a csővezetékhez, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="a7df9-137">This cmdlet sets the active period for the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="a7df9-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7df9-138">-ResourceGroupName</span></span>
<span data-ttu-id="a7df9-139">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a7df9-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a7df9-140">Ez a parancsmag módosítja egy olyan csővezeték aktív időszakát, amely a paraméter által meghatározott csoportba tartozik.</span><span class="sxs-lookup"><span data-stu-id="a7df9-140">This cmdlet modifies the active period for a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a7df9-141">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="a7df9-141">-StartDateTime</span></span>
<span data-ttu-id="a7df9-142">Az időszak kezdését **datetime** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="a7df9-142">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="a7df9-143">Ebben az időszakban dolgozzák fel az adatfeldolgozást vagy az adatszeleteket.</span><span class="sxs-lookup"><span data-stu-id="a7df9-143">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="a7df9-144">A *StartDateTime* a ISO8601 formátumban kell megadni.</span><span class="sxs-lookup"><span data-stu-id="a7df9-144">*StartDateTime* must be specified in the ISO8601 format.</span></span>

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

### <span data-ttu-id="a7df9-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a7df9-145">-Confirm</span></span>
<span data-ttu-id="a7df9-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a7df9-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7df9-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7df9-147">-WhatIf</span></span>
<span data-ttu-id="a7df9-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a7df9-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7df9-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a7df9-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7df9-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7df9-150">CommonParameters</span></span>
<span data-ttu-id="a7df9-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a7df9-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7df9-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7df9-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7df9-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7df9-153">INPUTS</span></span>

### <span data-ttu-id="a7df9-154">System. String</span><span class="sxs-lookup"><span data-stu-id="a7df9-154">System.String</span></span>

### <span data-ttu-id="a7df9-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a7df9-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="a7df9-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7df9-156">OUTPUTS</span></span>

### <span data-ttu-id="a7df9-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a7df9-157">System.Boolean</span></span>

## <span data-ttu-id="a7df9-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a7df9-158">NOTES</span></span>
* <span data-ttu-id="a7df9-159">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="a7df9-159">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a7df9-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a7df9-160">RELATED LINKS</span></span>

[<span data-ttu-id="a7df9-161">Új – AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a7df9-161">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="a7df9-162">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="a7df9-162">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)


