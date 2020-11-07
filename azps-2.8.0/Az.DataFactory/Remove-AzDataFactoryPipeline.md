---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
ms.openlocfilehash: 6d3353e9f2daead1135b3da4ebde530137d8ae1e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667004"
---
# <span data-ttu-id="a0cbd-101">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a0cbd-101">Remove-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="a0cbd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a0cbd-102">SYNOPSIS</span></span>
<span data-ttu-id="a0cbd-103">Az Azure Data Factory futószalagjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="a0cbd-103">Removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="a0cbd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a0cbd-104">SYNTAX</span></span>

### <span data-ttu-id="a0cbd-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a0cbd-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a0cbd-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a0cbd-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0cbd-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a0cbd-107">DESCRIPTION</span></span>
<span data-ttu-id="a0cbd-108">A **Remove-AzDataFactoryPipeline** parancsmag eltávolítja a csővezetéket az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="a0cbd-108">The **Remove-AzDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="a0cbd-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a0cbd-109">EXAMPLES</span></span>

### <span data-ttu-id="a0cbd-110">1. példa: a csővezeték eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a0cbd-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="a0cbd-111">Ez a parancsmag eltávolítja a DPWikisample nevű csővezetéket az WikiADF nevű adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="a0cbd-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="a0cbd-112">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="a0cbd-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="a0cbd-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a0cbd-113">PARAMETERS</span></span>

### <span data-ttu-id="a0cbd-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a0cbd-114">-DataFactory</span></span>
<span data-ttu-id="a0cbd-115">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="a0cbd-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="a0cbd-116">Ez a parancsmag eltávolítja a csővezetéket az adatgyárból, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0cbd-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0cbd-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a0cbd-117">-DataFactoryName</span></span>
<span data-ttu-id="a0cbd-118">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0cbd-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a0cbd-119">Ez a parancsmag eltávolítja a csővezetéket az adatgyárból, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0cbd-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a0cbd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0cbd-120">-DefaultProfile</span></span>
<span data-ttu-id="a0cbd-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a0cbd-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0cbd-122">-Force</span><span class="sxs-lookup"><span data-stu-id="a0cbd-122">-Force</span></span>
<span data-ttu-id="a0cbd-123">Jelzi, hogy ez a parancsmag eltávolítja a csővezetéket anélkül, hogy megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a0cbd-123">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="a0cbd-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a0cbd-124">-Name</span></span>
<span data-ttu-id="a0cbd-125">Az eltávolítandó csővezeték nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0cbd-125">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0cbd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0cbd-126">-ResourceGroupName</span></span>
<span data-ttu-id="a0cbd-127">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0cbd-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a0cbd-128">Ez a parancsmag eltávolítja azt a csoportot, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="a0cbd-128">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a0cbd-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a0cbd-129">-Confirm</span></span>
<span data-ttu-id="a0cbd-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a0cbd-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0cbd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0cbd-131">-WhatIf</span></span>
<span data-ttu-id="a0cbd-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a0cbd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0cbd-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a0cbd-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0cbd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0cbd-134">CommonParameters</span></span>
<span data-ttu-id="a0cbd-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a0cbd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0cbd-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0cbd-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0cbd-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0cbd-137">INPUTS</span></span>

### <span data-ttu-id="a0cbd-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a0cbd-138">System.String</span></span>

### <span data-ttu-id="a0cbd-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a0cbd-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="a0cbd-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0cbd-140">OUTPUTS</span></span>

### <span data-ttu-id="a0cbd-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="a0cbd-141">System.Void</span></span>

## <span data-ttu-id="a0cbd-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a0cbd-142">NOTES</span></span>
* <span data-ttu-id="a0cbd-143">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="a0cbd-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a0cbd-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0cbd-144">RELATED LINKS</span></span>

[<span data-ttu-id="a0cbd-145">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a0cbd-145">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="a0cbd-146">Új – AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a0cbd-146">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="a0cbd-147">Önéletrajz – AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a0cbd-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="a0cbd-148">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="a0cbd-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="a0cbd-149">Felfüggesztés – AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a0cbd-149">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


