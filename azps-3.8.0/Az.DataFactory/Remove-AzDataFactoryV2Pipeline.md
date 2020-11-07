---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: b1d39c3d60d043485cc4ec4dc0c4ba986a97e800
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847186"
---
# <span data-ttu-id="a3811-101">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="a3811-101">Remove-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="a3811-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a3811-102">SYNOPSIS</span></span>
<span data-ttu-id="a3811-103">Csővezeték eltávolítása az adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="a3811-103">Removes a pipeline from Data Factory.</span></span>

## <span data-ttu-id="a3811-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a3811-104">SYNTAX</span></span>

### <span data-ttu-id="a3811-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a3811-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3811-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a3811-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3811-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a3811-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3811-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a3811-108">DESCRIPTION</span></span>
<span data-ttu-id="a3811-109">Az Remove-AzDataFactoryV2Pipeline parancsmag eltávolítja a csővezetéket az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="a3811-109">The Remove-AzDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="a3811-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a3811-110">EXAMPLES</span></span>

### <span data-ttu-id="a3811-111">1. példa: a csővezeték eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a3811-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="a3811-112">Ez a parancsmag eltávolítja a DPWikisample nevű csővezetéket az WikiADF nevű adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="a3811-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="a3811-113">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="a3811-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="a3811-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a3811-114">PARAMETERS</span></span>

### <span data-ttu-id="a3811-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a3811-115">-DataFactoryName</span></span>
<span data-ttu-id="a3811-116">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3811-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a3811-117">Ez a parancsmag eltávolítja a csővezetéket az adatgyárból, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3811-117">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a3811-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3811-118">-DefaultProfile</span></span>
<span data-ttu-id="a3811-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a3811-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3811-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a3811-120">-Force</span></span>
<span data-ttu-id="a3811-121">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="a3811-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="a3811-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3811-122">-InputObject</span></span>
<span data-ttu-id="a3811-123">A pipeline-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3811-123">Specifies a Pipeline object.</span></span>
<span data-ttu-id="a3811-124">Ez a parancsmag eltávolítja a paraméter által megadott futószalagot.</span><span class="sxs-lookup"><span data-stu-id="a3811-124">This cmdlet removes the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="a3811-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a3811-125">-Name</span></span>
<span data-ttu-id="a3811-126">Az eltávolítandó csővezeték nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3811-126">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="a3811-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3811-127">-ResourceGroupName</span></span>
<span data-ttu-id="a3811-128">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3811-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a3811-129">Ez a parancsmag eltávolítja azt a csoportot, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="a3811-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a3811-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3811-130">-ResourceId</span></span>
<span data-ttu-id="a3811-131">Az eltávolítandó csővezeték Azure Resource ID azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a3811-131">The Azure resource ID of the pipeline to remove.</span></span>

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

### <span data-ttu-id="a3811-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a3811-132">-Confirm</span></span>
<span data-ttu-id="a3811-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a3811-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3811-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3811-134">-WhatIf</span></span>
<span data-ttu-id="a3811-135">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a3811-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="a3811-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3811-136">CommonParameters</span></span>
<span data-ttu-id="a3811-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a3811-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3811-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3811-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3811-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3811-139">INPUTS</span></span>

### <span data-ttu-id="a3811-140">Microsoft. Azure. Command. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="a3811-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="a3811-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a3811-141">System.String</span></span>

## <span data-ttu-id="a3811-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3811-142">OUTPUTS</span></span>

### <span data-ttu-id="a3811-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a3811-143">System.Boolean</span></span>

## <span data-ttu-id="a3811-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a3811-144">NOTES</span></span>
<span data-ttu-id="a3811-145">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="a3811-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a3811-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3811-146">RELATED LINKS</span></span>

[<span data-ttu-id="a3811-147">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="a3811-147">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="a3811-148">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="a3811-148">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="a3811-149">Meghívó-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="a3811-149">Invoke-AzDataFactoryV2Pipeline</span></span>]()
