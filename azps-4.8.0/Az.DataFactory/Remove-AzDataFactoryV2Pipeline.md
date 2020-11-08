---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: b1d39c3d60d043485cc4ec4dc0c4ba986a97e800
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182840"
---
# <span data-ttu-id="df4ba-101">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="df4ba-101">Remove-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="df4ba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="df4ba-102">SYNOPSIS</span></span>
<span data-ttu-id="df4ba-103">Csővezeték eltávolítása az adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="df4ba-103">Removes a pipeline from Data Factory.</span></span>

## <span data-ttu-id="df4ba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="df4ba-104">SYNTAX</span></span>

### <span data-ttu-id="df4ba-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="df4ba-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df4ba-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="df4ba-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df4ba-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="df4ba-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df4ba-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="df4ba-108">DESCRIPTION</span></span>
<span data-ttu-id="df4ba-109">Az Remove-AzDataFactoryV2Pipeline parancsmag eltávolítja a csővezetéket az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="df4ba-109">The Remove-AzDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="df4ba-110">Példák</span><span class="sxs-lookup"><span data-stu-id="df4ba-110">EXAMPLES</span></span>

### <span data-ttu-id="df4ba-111">1. példa: a csővezeték eltávolítása</span><span class="sxs-lookup"><span data-stu-id="df4ba-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="df4ba-112">Ez a parancsmag eltávolítja a DPWikisample nevű csővezetéket az WikiADF nevű adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="df4ba-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="df4ba-113">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="df4ba-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="df4ba-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="df4ba-114">PARAMETERS</span></span>

### <span data-ttu-id="df4ba-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="df4ba-115">-DataFactoryName</span></span>
<span data-ttu-id="df4ba-116">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="df4ba-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="df4ba-117">Ez a parancsmag eltávolítja a csővezetéket az adatgyárból, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="df4ba-117">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="df4ba-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df4ba-118">-DefaultProfile</span></span>
<span data-ttu-id="df4ba-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="df4ba-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df4ba-120">-Force</span><span class="sxs-lookup"><span data-stu-id="df4ba-120">-Force</span></span>
<span data-ttu-id="df4ba-121">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="df4ba-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="df4ba-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df4ba-122">-InputObject</span></span>
<span data-ttu-id="df4ba-123">A pipeline-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="df4ba-123">Specifies a Pipeline object.</span></span>
<span data-ttu-id="df4ba-124">Ez a parancsmag eltávolítja a paraméter által megadott futószalagot.</span><span class="sxs-lookup"><span data-stu-id="df4ba-124">This cmdlet removes the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="df4ba-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="df4ba-125">-Name</span></span>
<span data-ttu-id="df4ba-126">Az eltávolítandó csővezeték nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="df4ba-126">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="df4ba-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df4ba-127">-ResourceGroupName</span></span>
<span data-ttu-id="df4ba-128">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="df4ba-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="df4ba-129">Ez a parancsmag eltávolítja azt a csoportot, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="df4ba-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="df4ba-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df4ba-130">-ResourceId</span></span>
<span data-ttu-id="df4ba-131">Az eltávolítandó csővezeték Azure Resource ID azonosítója.</span><span class="sxs-lookup"><span data-stu-id="df4ba-131">The Azure resource ID of the pipeline to remove.</span></span>

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

### <span data-ttu-id="df4ba-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="df4ba-132">-Confirm</span></span>
<span data-ttu-id="df4ba-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="df4ba-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df4ba-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df4ba-134">-WhatIf</span></span>
<span data-ttu-id="df4ba-135">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="df4ba-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="df4ba-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df4ba-136">CommonParameters</span></span>
<span data-ttu-id="df4ba-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="df4ba-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df4ba-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df4ba-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df4ba-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="df4ba-139">INPUTS</span></span>

### <span data-ttu-id="df4ba-140">Microsoft. Azure. Command. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="df4ba-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="df4ba-141">System. String</span><span class="sxs-lookup"><span data-stu-id="df4ba-141">System.String</span></span>

## <span data-ttu-id="df4ba-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df4ba-142">OUTPUTS</span></span>

### <span data-ttu-id="df4ba-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="df4ba-143">System.Boolean</span></span>

## <span data-ttu-id="df4ba-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="df4ba-144">NOTES</span></span>
<span data-ttu-id="df4ba-145">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="df4ba-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="df4ba-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df4ba-146">RELATED LINKS</span></span>

[<span data-ttu-id="df4ba-147">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="df4ba-147">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="df4ba-148">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="df4ba-148">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="df4ba-149">Meghívó-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="df4ba-149">Invoke-AzDataFactoryV2Pipeline</span></span>]()

