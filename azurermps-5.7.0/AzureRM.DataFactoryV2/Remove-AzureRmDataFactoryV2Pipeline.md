---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: 9f5bac03f9c1d59e2d2fc271f462e1e08ca6349b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672020"
---
# <span data-ttu-id="8b8a2-101">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="8b8a2-101">Remove-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="8b8a2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8b8a2-102">SYNOPSIS</span></span>
<span data-ttu-id="8b8a2-103">Csővezeték eltávolítása az adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-103">Removes a pipeline from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b8a2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8b8a2-104">SYNTAX</span></span>

### <span data-ttu-id="8b8a2-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8b8a2-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b8a2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8b8a2-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b8a2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8b8a2-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b8a2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8b8a2-108">DESCRIPTION</span></span>
<span data-ttu-id="8b8a2-109">Az Remove-AzureRmDataFactoryV2Pipeline parancsmag eltávolítja a csővezetéket az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-109">The Remove-AzureRmDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="8b8a2-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8b8a2-110">EXAMPLES</span></span>

### <span data-ttu-id="8b8a2-111">1. példa: a csővezeték eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8b8a2-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="8b8a2-112">Ez a parancsmag eltávolítja a DPWikisample nevű csővezetéket az WikiADF nevű adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="8b8a2-113">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="8b8a2-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8b8a2-114">PARAMETERS</span></span>

### <span data-ttu-id="8b8a2-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8b8a2-115">-DataFactoryName</span></span>
<span data-ttu-id="8b8a2-116">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="8b8a2-117">Ez a parancsmag eltávolítja a csővezetéket az adatgyárból, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-117">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8b8a2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b8a2-118">-DefaultProfile</span></span>
<span data-ttu-id="8b8a2-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b8a2-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8b8a2-120">-Force</span></span>
<span data-ttu-id="8b8a2-121">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="8b8a2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b8a2-122">-InputObject</span></span>
<span data-ttu-id="8b8a2-123">A pipeline-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-123">Specifies a Pipeline object.</span></span>
<span data-ttu-id="8b8a2-124">Ez a parancsmag eltávolítja a paraméter által megadott futószalagot.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-124">This cmdlet removes the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="8b8a2-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8b8a2-125">-Name</span></span>
<span data-ttu-id="8b8a2-126">Az eltávolítandó csővezeték nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-126">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="8b8a2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b8a2-127">-ResourceGroupName</span></span>
<span data-ttu-id="8b8a2-128">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8b8a2-129">Ez a parancsmag eltávolítja azt a csoportot, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8b8a2-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b8a2-130">-ResourceId</span></span>
<span data-ttu-id="8b8a2-131">Az eltávolítandó csővezeték Azure Resource ID azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-131">The Azure resource ID of the pipeline to remove.</span></span>

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

### <span data-ttu-id="8b8a2-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8b8a2-132">-Confirm</span></span>
<span data-ttu-id="8b8a2-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b8a2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b8a2-134">-WhatIf</span></span>
<span data-ttu-id="8b8a2-135">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8b8a2-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="8b8a2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b8a2-136">CommonParameters</span></span>
<span data-ttu-id="8b8a2-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8b8a2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b8a2-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b8a2-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b8a2-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b8a2-139">INPUTS</span></span>

### <span data-ttu-id="8b8a2-140">Microsoft. Azure. Command. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="8b8a2-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="8b8a2-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8b8a2-141">System.String</span></span>

## <span data-ttu-id="8b8a2-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b8a2-142">OUTPUTS</span></span>

### <span data-ttu-id="8b8a2-143">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="8b8a2-143">System.Object</span></span>

## <span data-ttu-id="8b8a2-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8b8a2-144">NOTES</span></span>
<span data-ttu-id="8b8a2-145">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="8b8a2-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8b8a2-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8b8a2-146">RELATED LINKS</span></span>

[<span data-ttu-id="8b8a2-147">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="8b8a2-147">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="8b8a2-148">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="8b8a2-148">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="8b8a2-149">Meghívó-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="8b8a2-149">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

