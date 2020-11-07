---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: faf5d80b231b93124279f3c9bb6a347f89d988d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672021"
---
# <span data-ttu-id="69859-101">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="69859-101">Remove-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="69859-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="69859-102">SYNOPSIS</span></span>
<span data-ttu-id="69859-103">Adatkészlet eltávolítása az adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="69859-103">Removes a dataset from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69859-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="69859-104">SYNTAX</span></span>

### <span data-ttu-id="69859-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="69859-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69859-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="69859-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69859-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="69859-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69859-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="69859-108">DESCRIPTION</span></span>
<span data-ttu-id="69859-109">Az Remove-AzureRmDataFactoryV2Dataset parancsmag eltávolítja az adatkészletet az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="69859-109">The Remove-AzureRmDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="69859-110">Példák</span><span class="sxs-lookup"><span data-stu-id="69859-110">EXAMPLES</span></span>

### <span data-ttu-id="69859-111">1. példa: adatkészlet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="69859-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="69859-112">Ez a parancs eltávolítja a DAWikiAggregatedData nevű adatkészletet az WikiADF nevű adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="69859-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="69859-113">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="69859-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="69859-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="69859-114">PARAMETERS</span></span>

### <span data-ttu-id="69859-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="69859-115">-DataFactoryName</span></span>
<span data-ttu-id="69859-116">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="69859-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="69859-117">Ez a parancsmag eltávolítja az adatgyárból az adatkészletet, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="69859-117">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="69859-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69859-118">-DefaultProfile</span></span>
<span data-ttu-id="69859-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69859-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69859-120">-Force</span><span class="sxs-lookup"><span data-stu-id="69859-120">-Force</span></span>
<span data-ttu-id="69859-121">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="69859-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="69859-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69859-122">-InputObject</span></span>
<span data-ttu-id="69859-123">Az eltávolítandó adatkészlet-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="69859-123">Specifies a Dataset object to remove.</span></span>

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

### <span data-ttu-id="69859-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="69859-124">-Name</span></span>
<span data-ttu-id="69859-125">Az eltávolítandó adatkészlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="69859-125">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="69859-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69859-126">-ResourceGroupName</span></span>
<span data-ttu-id="69859-127">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="69859-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="69859-128">Ez a parancsmag eltávolítja azt az adatkészletet, amely a paraméter által megadott csoportba kerül.</span><span class="sxs-lookup"><span data-stu-id="69859-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="69859-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69859-129">-ResourceId</span></span>
<span data-ttu-id="69859-130">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="69859-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="69859-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="69859-131">-Confirm</span></span>
<span data-ttu-id="69859-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="69859-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69859-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69859-133">-WhatIf</span></span>
<span data-ttu-id="69859-134">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="69859-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="69859-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69859-135">CommonParameters</span></span>
<span data-ttu-id="69859-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="69859-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69859-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69859-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69859-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="69859-138">INPUTS</span></span>

### <span data-ttu-id="69859-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="69859-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>
<span data-ttu-id="69859-140">System. String</span><span class="sxs-lookup"><span data-stu-id="69859-140">System.String</span></span>

## <span data-ttu-id="69859-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69859-141">OUTPUTS</span></span>

### <span data-ttu-id="69859-142">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="69859-142">System.Object</span></span>

## <span data-ttu-id="69859-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="69859-143">NOTES</span></span>
<span data-ttu-id="69859-144">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="69859-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="69859-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69859-145">RELATED LINKS</span></span>

[<span data-ttu-id="69859-146">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="69859-146">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="69859-147">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="69859-147">Set-AzureRmDataFactoryV2Dataset</span></span>]()
