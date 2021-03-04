---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1FF0B0F9-4B2C-46BC-8BED-12BE865E4480
online version: https://docs.microsoft.com/powershell/module/az.datafactory/suspend-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
ms.openlocfilehash: 7b909669ecec054ac4cbef13c5babf7e5cdcdb08
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942842"
---
# <span data-ttu-id="0160a-101">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0160a-101">Suspend-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="0160a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0160a-102">SYNOPSIS</span></span>
<span data-ttu-id="0160a-103">Felfüggeszti a folyamatot az Azure Data Factoryban.</span><span class="sxs-lookup"><span data-stu-id="0160a-103">Suspends a pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="0160a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0160a-104">SYNTAX</span></span>

### <span data-ttu-id="0160a-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0160a-105">ByFactoryName (Default)</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0160a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0160a-106">ByFactoryObject</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0160a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0160a-107">DESCRIPTION</span></span>
<span data-ttu-id="0160a-108">A **Suspend-AzDataFactoryPipeline** parancsmag felfüggeszti a folyamatot az Azure Data Factoryban.</span><span class="sxs-lookup"><span data-stu-id="0160a-108">The **Suspend-AzDataFactoryPipeline** cmdlet suspends a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="0160a-109">A folyamat folytatásához használja a Resume-AzDataFactoryPipeline parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0160a-109">You can resume the pipeline by using the Resume-AzDataFactoryPipeline cmdlet.</span></span>

## <span data-ttu-id="0160a-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0160a-110">EXAMPLES</span></span>

### <span data-ttu-id="0160a-111">1. példa: Folyamat felfüggesztése</span><span class="sxs-lookup"><span data-stu-id="0160a-111">Example 1: Suspend a pipeline</span></span>
```
PS C:\>Suspend-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikiSample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to suspend pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="0160a-112">Ez a parancs felfüggeszti a DPWikiSample nevű folyamatot a WikiADF nevű adatüzemben.</span><span class="sxs-lookup"><span data-stu-id="0160a-112">This command suspends the pipeline named DPWikiSample in the data factory named WikiADF.</span></span>
<span data-ttu-id="0160a-113">A parancs egy számértéket ad $True.</span><span class="sxs-lookup"><span data-stu-id="0160a-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="0160a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0160a-114">PARAMETERS</span></span>

### <span data-ttu-id="0160a-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="0160a-115">-DataFactory</span></span>
<span data-ttu-id="0160a-116">EGY **PSDataFactory-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="0160a-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="0160a-117">Ez a parancsmag felfüggeszti a paraméter által megadott adat factoryhoz tartozó folyamatot.</span><span class="sxs-lookup"><span data-stu-id="0160a-117">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0160a-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0160a-118">-DataFactoryName</span></span>
<span data-ttu-id="0160a-119">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0160a-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="0160a-120">Ez a parancsmag felfüggeszti a paraméter által megadott adat factoryhoz tartozó folyamatot.</span><span class="sxs-lookup"><span data-stu-id="0160a-120">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0160a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0160a-121">-DefaultProfile</span></span>
<span data-ttu-id="0160a-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0160a-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0160a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0160a-123">-Name</span></span>
<span data-ttu-id="0160a-124">A felfüggesztenie kell a folyamat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0160a-124">Specifies the name of the pipeline to suspend.</span></span>

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

### <span data-ttu-id="0160a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0160a-125">-ResourceGroupName</span></span>
<span data-ttu-id="0160a-126">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0160a-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0160a-127">Ez a parancsmag felfüggeszti a paraméter által megadott csoporthoz tartozó folyamatot.</span><span class="sxs-lookup"><span data-stu-id="0160a-127">This cmdlet suspends a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0160a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0160a-128">-Confirm</span></span>
<span data-ttu-id="0160a-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0160a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0160a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0160a-130">-WhatIf</span></span>
<span data-ttu-id="0160a-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0160a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0160a-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0160a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0160a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0160a-133">CommonParameters</span></span>
<span data-ttu-id="0160a-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0160a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0160a-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0160a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0160a-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0160a-136">INPUTS</span></span>

### <span data-ttu-id="0160a-137">System.String</span><span class="sxs-lookup"><span data-stu-id="0160a-137">System.String</span></span>

### <span data-ttu-id="0160a-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0160a-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="0160a-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0160a-139">OUTPUTS</span></span>

### <span data-ttu-id="0160a-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0160a-140">System.Boolean</span></span>

## <span data-ttu-id="0160a-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0160a-141">NOTES</span></span>
* <span data-ttu-id="0160a-142">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="0160a-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0160a-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0160a-143">RELATED LINKS</span></span>

[<span data-ttu-id="0160a-144">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0160a-144">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="0160a-145">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0160a-145">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="0160a-146">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0160a-146">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="0160a-147">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0160a-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="0160a-148">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="0160a-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


