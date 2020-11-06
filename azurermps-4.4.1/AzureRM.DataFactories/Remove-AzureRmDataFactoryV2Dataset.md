---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 36ee24fea327828247336d7f9c983515ced9deb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499155"
---
# <span data-ttu-id="aa455-101">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="aa455-101">Remove-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="aa455-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aa455-102">SYNOPSIS</span></span>
<span data-ttu-id="aa455-103">Adatkészlet eltávolítása az adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="aa455-103">Removes a dataset from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa455-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aa455-104">SYNTAX</span></span>

### <span data-ttu-id="aa455-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aa455-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa455-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="aa455-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa455-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="aa455-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa455-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="aa455-108">DESCRIPTION</span></span>
<span data-ttu-id="aa455-109">Az Remove-AzureRmDataFactoryV2Dataset parancsmag eltávolítja az adatkészletet az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="aa455-109">The Remove-AzureRmDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="aa455-110">Példák</span><span class="sxs-lookup"><span data-stu-id="aa455-110">EXAMPLES</span></span>

### <span data-ttu-id="aa455-111">1. példa: adatkészlet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="aa455-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="aa455-112">Ez a parancs eltávolítja a DAWikiAggregatedData nevű adatkészletet az WikiADF nevű adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="aa455-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="aa455-113">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="aa455-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="aa455-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aa455-114">PARAMETERS</span></span>

### <span data-ttu-id="aa455-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aa455-115">-Confirm</span></span>
<span data-ttu-id="aa455-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aa455-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa455-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="aa455-117">-DataFactoryName</span></span>
<span data-ttu-id="aa455-118">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa455-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="aa455-119">Ez a parancsmag eltávolítja az adatgyárból az adatkészletet, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa455-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="aa455-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa455-120">-InputObject</span></span>
<span data-ttu-id="aa455-121">Az eltávolítandó adatkészlet-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa455-121">Specifies a Dataset object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa455-122">-Force</span><span class="sxs-lookup"><span data-stu-id="aa455-122">-Force</span></span>
<span data-ttu-id="aa455-123">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="aa455-123">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="aa455-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aa455-124">-Name</span></span>
<span data-ttu-id="aa455-125">Az eltávolítandó adatkészlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa455-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa455-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa455-126">-ResourceGroupName</span></span>
<span data-ttu-id="aa455-127">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa455-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="aa455-128">Ez a parancsmag eltávolítja azt az adatkészletet, amely a paraméter által megadott csoportba kerül.</span><span class="sxs-lookup"><span data-stu-id="aa455-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="aa455-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa455-129">-ResourceId</span></span>
<span data-ttu-id="aa455-130">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="aa455-130">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa455-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa455-131">-WhatIf</span></span>
<span data-ttu-id="aa455-132">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="aa455-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa455-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa455-133">-DefaultProfile</span></span>
<span data-ttu-id="aa455-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aa455-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa455-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa455-135">CommonParameters</span></span>
<span data-ttu-id="aa455-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aa455-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa455-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa455-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa455-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa455-138">INPUTS</span></span>

### <span data-ttu-id="aa455-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="aa455-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>
<span data-ttu-id="aa455-140">System. String</span><span class="sxs-lookup"><span data-stu-id="aa455-140">System.String</span></span>

## <span data-ttu-id="aa455-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa455-141">OUTPUTS</span></span>

### <span data-ttu-id="aa455-142">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="aa455-142">System.Object</span></span>

## <span data-ttu-id="aa455-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aa455-143">NOTES</span></span>
<span data-ttu-id="aa455-144">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="aa455-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="aa455-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa455-145">RELATED LINKS</span></span>

[<span data-ttu-id="aa455-146">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="aa455-146">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="aa455-147">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="aa455-147">Set-AzureRmDataFactoryV2Dataset</span></span>]()
