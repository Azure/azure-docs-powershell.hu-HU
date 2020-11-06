---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 77cb56c08e29bd209ccf53fcdee42545b774c650
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502751"
---
# <span data-ttu-id="34e86-101">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="34e86-101">Remove-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="34e86-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="34e86-102">SYNOPSIS</span></span>
<span data-ttu-id="34e86-103">Adatkészlet eltávolítása az adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="34e86-103">Removes a dataset from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34e86-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="34e86-104">SYNTAX</span></span>

### <span data-ttu-id="34e86-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="34e86-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="34e86-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="34e86-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="34e86-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="34e86-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="34e86-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="34e86-108">DESCRIPTION</span></span>
<span data-ttu-id="34e86-109">Az Remove-AzureRmDataFactoryV2Dataset parancsmag eltávolítja az adatkészletet az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="34e86-109">The Remove-AzureRmDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="34e86-110">Példák</span><span class="sxs-lookup"><span data-stu-id="34e86-110">EXAMPLES</span></span>

### <span data-ttu-id="34e86-111">1. példa: adatkészlet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="34e86-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="34e86-112">Ez a parancs eltávolítja a DAWikiAggregatedData nevű adatkészletet az WikiADF nevű adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="34e86-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="34e86-113">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="34e86-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="34e86-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="34e86-114">PARAMETERS</span></span>

### <span data-ttu-id="34e86-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="34e86-115">-Confirm</span></span>
<span data-ttu-id="34e86-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="34e86-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34e86-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="34e86-117">-DataFactoryName</span></span>
<span data-ttu-id="34e86-118">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="34e86-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="34e86-119">Ez a parancsmag eltávolítja az adatgyárból az adatkészletet, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="34e86-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="34e86-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34e86-120">-InputObject</span></span>
<span data-ttu-id="34e86-121">Az eltávolítandó adatkészlet-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="34e86-121">Specifies a Dataset object to remove.</span></span>

```yaml
Type: PSDataset
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34e86-122">-Force</span><span class="sxs-lookup"><span data-stu-id="34e86-122">-Force</span></span>
<span data-ttu-id="34e86-123">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="34e86-123">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="34e86-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="34e86-124">-Name</span></span>
<span data-ttu-id="34e86-125">Az eltávolítandó adatkészlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="34e86-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34e86-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34e86-126">-ResourceGroupName</span></span>
<span data-ttu-id="34e86-127">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="34e86-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="34e86-128">Ez a parancsmag eltávolítja azt az adatkészletet, amely a paraméter által megadott csoportba kerül.</span><span class="sxs-lookup"><span data-stu-id="34e86-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="34e86-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34e86-129">-ResourceId</span></span>
<span data-ttu-id="34e86-130">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="34e86-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="34e86-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34e86-131">-WhatIf</span></span>
<span data-ttu-id="34e86-132">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="34e86-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="34e86-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="34e86-133">INPUTS</span></span>

### <span data-ttu-id="34e86-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="34e86-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>
<span data-ttu-id="34e86-135">System. String</span><span class="sxs-lookup"><span data-stu-id="34e86-135">System.String</span></span>


## <span data-ttu-id="34e86-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="34e86-136">OUTPUTS</span></span>

### <span data-ttu-id="34e86-137">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="34e86-137">System.Object</span></span>

## <span data-ttu-id="34e86-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="34e86-138">NOTES</span></span>
<span data-ttu-id="34e86-139">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="34e86-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="34e86-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="34e86-140">RELATED LINKS</span></span>
[<span data-ttu-id="34e86-141">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="34e86-141">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="34e86-142">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="34e86-142">Set-AzureRmDataFactoryV2Dataset</span></span>]()
