---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
ms.openlocfilehash: 2bae0bd597cbd97a81efeaecb07e052457b88438
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372355"
---
# <span data-ttu-id="870ea-101">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="870ea-101">Remove-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="870ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="870ea-102">SYNOPSIS</span></span>
<span data-ttu-id="870ea-103">Eltávolít egy prognózist az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="870ea-103">Removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="870ea-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="870ea-104">SYNTAX</span></span>

### <span data-ttu-id="870ea-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="870ea-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="870ea-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="870ea-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="870ea-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="870ea-107">DESCRIPTION</span></span>
<span data-ttu-id="870ea-108">A **Remove-AzDataFactoryPipeline** parancsmag eltávolít egy folyamatot az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="870ea-108">The **Remove-AzDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="870ea-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="870ea-109">EXAMPLES</span></span>

### <span data-ttu-id="870ea-110">1. példa: Folyamat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="870ea-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="870ea-111">Ez a parancsmag eltávolítja a DPWikisample nevű folyamatot a WikiADF nevű adatüzemből.</span><span class="sxs-lookup"><span data-stu-id="870ea-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="870ea-112">A parancs egy számértéket ad $True.</span><span class="sxs-lookup"><span data-stu-id="870ea-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="870ea-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="870ea-113">PARAMETERS</span></span>

### <span data-ttu-id="870ea-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="870ea-114">-DataFactory</span></span>
<span data-ttu-id="870ea-115">EGY **PSDataFactory-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="870ea-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="870ea-116">Ez a parancsmag eltávolít egy prognózist a paraméter által megadott adatüzemből.</span><span class="sxs-lookup"><span data-stu-id="870ea-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="870ea-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="870ea-117">-DataFactoryName</span></span>
<span data-ttu-id="870ea-118">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="870ea-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="870ea-119">Ez a parancsmag eltávolít egy prognózist a paraméter által megadott adatüzemből.</span><span class="sxs-lookup"><span data-stu-id="870ea-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="870ea-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="870ea-120">-DefaultProfile</span></span>
<span data-ttu-id="870ea-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="870ea-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="870ea-122">-Force</span><span class="sxs-lookup"><span data-stu-id="870ea-122">-Force</span></span>
<span data-ttu-id="870ea-123">Azt jelzi, hogy ez a parancsmag anélkül távolítja el a folyamatot, hogy megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="870ea-123">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="870ea-124">-Name</span><span class="sxs-lookup"><span data-stu-id="870ea-124">-Name</span></span>
<span data-ttu-id="870ea-125">Az eltávolítható folyamat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="870ea-125">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="870ea-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="870ea-126">-ResourceGroupName</span></span>
<span data-ttu-id="870ea-127">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="870ea-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="870ea-128">Ez a parancsmag eltávolít egy prognózist a paraméter által megadott csoportból.</span><span class="sxs-lookup"><span data-stu-id="870ea-128">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="870ea-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="870ea-129">-Confirm</span></span>
<span data-ttu-id="870ea-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="870ea-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="870ea-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="870ea-131">-WhatIf</span></span>
<span data-ttu-id="870ea-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="870ea-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="870ea-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="870ea-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="870ea-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="870ea-134">CommonParameters</span></span>
<span data-ttu-id="870ea-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="870ea-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="870ea-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="870ea-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="870ea-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="870ea-137">INPUTS</span></span>

### <span data-ttu-id="870ea-138">System.String</span><span class="sxs-lookup"><span data-stu-id="870ea-138">System.String</span></span>

### <span data-ttu-id="870ea-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="870ea-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="870ea-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="870ea-140">OUTPUTS</span></span>

### <span data-ttu-id="870ea-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="870ea-141">System.Void</span></span>

## <span data-ttu-id="870ea-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="870ea-142">NOTES</span></span>
* <span data-ttu-id="870ea-143">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="870ea-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="870ea-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="870ea-144">RELATED LINKS</span></span>

[<span data-ttu-id="870ea-145">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="870ea-145">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="870ea-146">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="870ea-146">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="870ea-147">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="870ea-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="870ea-148">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="870ea-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="870ea-149">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="870ea-149">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


