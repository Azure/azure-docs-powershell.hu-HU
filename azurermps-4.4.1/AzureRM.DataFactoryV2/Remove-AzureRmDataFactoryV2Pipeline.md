---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: cc43b2982ff2269a1e0e72da065a806895cc798e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505987"
---
# <span data-ttu-id="cb278-101">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="cb278-101">Remove-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="cb278-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cb278-102">SYNOPSIS</span></span>
<span data-ttu-id="cb278-103">Csővezeték eltávolítása az adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="cb278-103">Removes a pipeline from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb278-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cb278-104">SYNTAX</span></span>

### <span data-ttu-id="cb278-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cb278-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="cb278-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cb278-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="cb278-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cb278-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="cb278-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="cb278-108">DESCRIPTION</span></span>
<span data-ttu-id="cb278-109">Az Remove-AzureRmDataFactoryV2Pipeline parancsmag eltávolítja a csővezetéket az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="cb278-109">The Remove-AzureRmDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="cb278-110">Példák</span><span class="sxs-lookup"><span data-stu-id="cb278-110">EXAMPLES</span></span>

### <span data-ttu-id="cb278-111">1. példa: a csővezeték eltávolítása</span><span class="sxs-lookup"><span data-stu-id="cb278-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="cb278-112">Ez a parancsmag eltávolítja a DPWikisample nevű csővezetéket az WikiADF nevű adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="cb278-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="cb278-113">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="cb278-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="cb278-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cb278-114">PARAMETERS</span></span>

### <span data-ttu-id="cb278-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cb278-115">-Confirm</span></span>
<span data-ttu-id="cb278-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cb278-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb278-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cb278-117">-DataFactoryName</span></span>
<span data-ttu-id="cb278-118">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb278-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="cb278-119">Ez a parancsmag eltávolítja a csővezetéket az adatgyárból, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb278-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="cb278-120">-Force</span><span class="sxs-lookup"><span data-stu-id="cb278-120">-Force</span></span>
<span data-ttu-id="cb278-121">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="cb278-121">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb278-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cb278-122">-Name</span></span>
<span data-ttu-id="cb278-123">Az eltávolítandó csővezeték nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb278-123">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb278-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb278-124">-InputObject</span></span>
<span data-ttu-id="cb278-125">A pipeline-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb278-125">Specifies a Pipeline object.</span></span>
<span data-ttu-id="cb278-126">Ez a parancsmag eltávolítja a paraméter által megadott futószalagot.</span><span class="sxs-lookup"><span data-stu-id="cb278-126">This cmdlet removes the pipeline that this parameter specifies.</span></span>

```yaml
Type: PSPipeline
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb278-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb278-127">-ResourceGroupName</span></span>
<span data-ttu-id="cb278-128">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb278-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="cb278-129">Ez a parancsmag eltávolítja azt a csoportot, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="cb278-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="cb278-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb278-130">-ResourceId</span></span>
<span data-ttu-id="cb278-131">Az eltávolítandó csővezeték Azure Resource ID azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cb278-131">The Azure resource ID of the pipeline to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb278-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb278-132">-WhatIf</span></span>
<span data-ttu-id="cb278-133">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cb278-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="cb278-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb278-134">INPUTS</span></span>

### <span data-ttu-id="cb278-135">Microsoft. Azure. Command. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="cb278-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="cb278-136">System. String</span><span class="sxs-lookup"><span data-stu-id="cb278-136">System.String</span></span>


## <span data-ttu-id="cb278-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb278-137">OUTPUTS</span></span>

### <span data-ttu-id="cb278-138">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="cb278-138">System.Object</span></span>

## <span data-ttu-id="cb278-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cb278-139">NOTES</span></span>
<span data-ttu-id="cb278-140">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="cb278-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="cb278-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb278-141">RELATED LINKS</span></span>
[<span data-ttu-id="cb278-142">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="cb278-142">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="cb278-143">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="cb278-143">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="cb278-144">Meghívó-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="cb278-144">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

