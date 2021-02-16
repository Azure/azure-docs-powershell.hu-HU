---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: b1d39c3d60d043485cc4ec4dc0c4ba986a97e800
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153482"
---
# <span data-ttu-id="fa25e-101">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="fa25e-101">Remove-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="fa25e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa25e-102">SYNOPSIS</span></span>
<span data-ttu-id="fa25e-103">Eltávolít egy prognózist a Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="fa25e-103">Removes a pipeline from Data Factory.</span></span>

## <span data-ttu-id="fa25e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fa25e-104">SYNTAX</span></span>

### <span data-ttu-id="fa25e-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fa25e-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa25e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fa25e-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa25e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fa25e-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa25e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fa25e-108">DESCRIPTION</span></span>
<span data-ttu-id="fa25e-109">A Remove-AzDataFactoryV2Pipeline parancsmag eltávolítja a prognózist az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="fa25e-109">The Remove-AzDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="fa25e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fa25e-110">EXAMPLES</span></span>

### <span data-ttu-id="fa25e-111">1. példa: Folyamat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="fa25e-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="fa25e-112">Ez a parancsmag eltávolítja a DPWikisample nevű folyamatot a WikiADF nevű adatüzemből.</span><span class="sxs-lookup"><span data-stu-id="fa25e-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="fa25e-113">A parancs egy számértéket ad $True.</span><span class="sxs-lookup"><span data-stu-id="fa25e-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="fa25e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa25e-114">PARAMETERS</span></span>

### <span data-ttu-id="fa25e-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fa25e-115">-DataFactoryName</span></span>
<span data-ttu-id="fa25e-116">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fa25e-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="fa25e-117">Ez a parancsmag eltávolít egy prognózist a paraméter által megadott adatüzemből.</span><span class="sxs-lookup"><span data-stu-id="fa25e-117">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="fa25e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa25e-118">-DefaultProfile</span></span>
<span data-ttu-id="fa25e-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fa25e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa25e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="fa25e-120">-Force</span></span>
<span data-ttu-id="fa25e-121">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="fa25e-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="fa25e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa25e-122">-InputObject</span></span>
<span data-ttu-id="fa25e-123">Egy Pipeline objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="fa25e-123">Specifies a Pipeline object.</span></span>
<span data-ttu-id="fa25e-124">Ez a parancsmag eltávolítja a paraméter által megadott folyamatot.</span><span class="sxs-lookup"><span data-stu-id="fa25e-124">This cmdlet removes the pipeline that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa25e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="fa25e-125">-Name</span></span>
<span data-ttu-id="fa25e-126">Az eltávolítható folyamat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fa25e-126">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa25e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa25e-127">-ResourceGroupName</span></span>
<span data-ttu-id="fa25e-128">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fa25e-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="fa25e-129">Ez a parancsmag eltávolít egy folyamatot a paraméter által megadott csoportból.</span><span class="sxs-lookup"><span data-stu-id="fa25e-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="fa25e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa25e-130">-ResourceId</span></span>
<span data-ttu-id="fa25e-131">Az eltávolítható folyamat Azure-erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="fa25e-131">The Azure resource ID of the pipeline to remove.</span></span>

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

### <span data-ttu-id="fa25e-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa25e-132">-Confirm</span></span>
<span data-ttu-id="fa25e-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fa25e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa25e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa25e-134">-WhatIf</span></span>
<span data-ttu-id="fa25e-135">Azt mutatja, mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fa25e-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="fa25e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa25e-136">CommonParameters</span></span>
<span data-ttu-id="fa25e-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa25e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa25e-138">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa25e-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa25e-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fa25e-139">INPUTS</span></span>

### <span data-ttu-id="fa25e-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="fa25e-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="fa25e-141">System.String</span><span class="sxs-lookup"><span data-stu-id="fa25e-141">System.String</span></span>

## <span data-ttu-id="fa25e-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa25e-142">OUTPUTS</span></span>

### <span data-ttu-id="fa25e-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fa25e-143">System.Boolean</span></span>

## <span data-ttu-id="fa25e-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fa25e-144">NOTES</span></span>
<span data-ttu-id="fa25e-145">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="fa25e-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="fa25e-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fa25e-146">RELATED LINKS</span></span>

[<span data-ttu-id="fa25e-147">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="fa25e-147">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="fa25e-148">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="fa25e-148">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="fa25e-149">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="fa25e-149">Invoke-AzDataFactoryV2Pipeline</span></span>]()

