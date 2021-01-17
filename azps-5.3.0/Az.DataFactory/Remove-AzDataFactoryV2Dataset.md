---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 7db88488ccf60865654169233bb19025eae080d4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480399"
---
# <span data-ttu-id="ed5c4-101">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="ed5c4-101">Remove-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="ed5c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed5c4-102">SYNOPSIS</span></span>
<span data-ttu-id="ed5c4-103">Eltávolít egy adatkészletet a Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="ed5c4-103">Removes a dataset from Data Factory.</span></span>

## <span data-ttu-id="ed5c4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ed5c4-104">SYNTAX</span></span>

### <span data-ttu-id="ed5c4-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ed5c4-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed5c4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ed5c4-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed5c4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ed5c4-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed5c4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ed5c4-108">DESCRIPTION</span></span>
<span data-ttu-id="ed5c4-109">A Remove-AzDataFactoryV2Dataset parancsmag eltávolít egy adatkészletet az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="ed5c4-109">The Remove-AzDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="ed5c4-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ed5c4-110">EXAMPLES</span></span>

### <span data-ttu-id="ed5c4-111">1. példa: Adatkészlet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ed5c4-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="ed5c4-112">Ez a parancs eltávolítja a DAWikiAggregatedData nevű adatkészletet a WikiADF nevű adatüzemből.</span><span class="sxs-lookup"><span data-stu-id="ed5c4-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="ed5c4-113">A parancs egy számértéket ad $True.</span><span class="sxs-lookup"><span data-stu-id="ed5c4-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="ed5c4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed5c4-114">PARAMETERS</span></span>

### <span data-ttu-id="ed5c4-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ed5c4-115">-DataFactoryName</span></span>
<span data-ttu-id="ed5c4-116">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ed5c4-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ed5c4-117">Ez a parancsmag eltávolít egy adatkészletet a paraméter által megadott adatüzemmódból.</span><span class="sxs-lookup"><span data-stu-id="ed5c4-117">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ed5c4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed5c4-118">-DefaultProfile</span></span>
<span data-ttu-id="ed5c4-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ed5c4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed5c4-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ed5c4-120">-Force</span></span>
<span data-ttu-id="ed5c4-121">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="ed5c4-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ed5c4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed5c4-122">-InputObject</span></span>
<span data-ttu-id="ed5c4-123">Eltávolítható Adatkészlet-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="ed5c4-123">Specifies a Dataset object to remove.</span></span>

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

### <span data-ttu-id="ed5c4-124">-Name</span><span class="sxs-lookup"><span data-stu-id="ed5c4-124">-Name</span></span>
<span data-ttu-id="ed5c4-125">Az eltávolítható adatkészlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ed5c4-125">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="ed5c4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed5c4-126">-ResourceGroupName</span></span>
<span data-ttu-id="ed5c4-127">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ed5c4-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ed5c4-128">Ez a parancsmag eltávolít egy adatkészletet a paraméter által megadott csoportból.</span><span class="sxs-lookup"><span data-stu-id="ed5c4-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ed5c4-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed5c4-129">-ResourceId</span></span>
<span data-ttu-id="ed5c4-130">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="ed5c4-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ed5c4-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed5c4-131">-Confirm</span></span>
<span data-ttu-id="ed5c4-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ed5c4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed5c4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed5c4-133">-WhatIf</span></span>
<span data-ttu-id="ed5c4-134">Azt mutatja, mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ed5c4-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="ed5c4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed5c4-135">CommonParameters</span></span>
<span data-ttu-id="ed5c4-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed5c4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed5c4-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed5c4-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed5c4-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed5c4-138">INPUTS</span></span>

### <span data-ttu-id="ed5c4-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="ed5c4-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="ed5c4-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ed5c4-140">System.String</span></span>

## <span data-ttu-id="ed5c4-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed5c4-141">OUTPUTS</span></span>

### <span data-ttu-id="ed5c4-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="ed5c4-142">System.Void</span></span>

## <span data-ttu-id="ed5c4-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ed5c4-143">NOTES</span></span>
<span data-ttu-id="ed5c4-144">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="ed5c4-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ed5c4-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed5c4-145">RELATED LINKS</span></span>

[<span data-ttu-id="ed5c4-146">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="ed5c4-146">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="ed5c4-147">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="ed5c4-147">Set-AzDataFactoryV2Dataset</span></span>]()
