---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
ms.openlocfilehash: a5c7ca7a651510d8b417beedc28cbd5ba26e6fe1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919985"
---
# <span data-ttu-id="ee474-101">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="ee474-101">Remove-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="ee474-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee474-102">SYNOPSIS</span></span>
<span data-ttu-id="ee474-103">Eltávolít egy adatkészletet a Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="ee474-103">Removes a dataset from Data Factory.</span></span>

## <span data-ttu-id="ee474-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ee474-104">SYNTAX</span></span>

### <span data-ttu-id="ee474-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ee474-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee474-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ee474-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee474-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ee474-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee474-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ee474-108">DESCRIPTION</span></span>
<span data-ttu-id="ee474-109">A Remove-AzDataFactoryV2Dataset parancsmag eltávolít egy adatkészletet az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="ee474-109">The Remove-AzDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="ee474-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ee474-110">EXAMPLES</span></span>

### <span data-ttu-id="ee474-111">1. példa: Adatkészlet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ee474-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="ee474-112">Ez a parancs eltávolítja a DAWikiAggregatedData nevű adatkészletet a WikiADF nevű adatüzemből.</span><span class="sxs-lookup"><span data-stu-id="ee474-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="ee474-113">A parancs egy számértéket ad $True.</span><span class="sxs-lookup"><span data-stu-id="ee474-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="ee474-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee474-114">PARAMETERS</span></span>

### <span data-ttu-id="ee474-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ee474-115">-DataFactoryName</span></span>
<span data-ttu-id="ee474-116">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee474-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ee474-117">Ez a parancsmag eltávolít egy adatkészletet a paraméter által megadott adatüzemmódból.</span><span class="sxs-lookup"><span data-stu-id="ee474-117">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ee474-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee474-118">-DefaultProfile</span></span>
<span data-ttu-id="ee474-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ee474-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee474-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ee474-120">-Force</span></span>
<span data-ttu-id="ee474-121">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="ee474-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ee474-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee474-122">-InputObject</span></span>
<span data-ttu-id="ee474-123">Eltávolítható Adatkészlet-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="ee474-123">Specifies a Dataset object to remove.</span></span>

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

### <span data-ttu-id="ee474-124">-Name</span><span class="sxs-lookup"><span data-stu-id="ee474-124">-Name</span></span>
<span data-ttu-id="ee474-125">Az eltávolítható adatkészlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee474-125">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="ee474-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee474-126">-ResourceGroupName</span></span>
<span data-ttu-id="ee474-127">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee474-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ee474-128">Ez a parancsmag eltávolít egy adatkészletet a paraméter által megadott csoportból.</span><span class="sxs-lookup"><span data-stu-id="ee474-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ee474-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee474-129">-ResourceId</span></span>
<span data-ttu-id="ee474-130">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="ee474-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ee474-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee474-131">-Confirm</span></span>
<span data-ttu-id="ee474-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ee474-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee474-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee474-133">-WhatIf</span></span>
<span data-ttu-id="ee474-134">Azt mutatja, mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ee474-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="ee474-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee474-135">CommonParameters</span></span>
<span data-ttu-id="ee474-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee474-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee474-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee474-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee474-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ee474-138">INPUTS</span></span>

### <span data-ttu-id="ee474-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="ee474-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="ee474-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ee474-140">System.String</span></span>

## <span data-ttu-id="ee474-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee474-141">OUTPUTS</span></span>

### <span data-ttu-id="ee474-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="ee474-142">System.Void</span></span>

## <span data-ttu-id="ee474-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ee474-143">NOTES</span></span>
<span data-ttu-id="ee474-144">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="ee474-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ee474-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee474-145">RELATED LINKS</span></span>

[<span data-ttu-id="ee474-146">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="ee474-146">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="ee474-147">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="ee474-147">Set-AzDataFactoryV2Dataset</span></span>]()
