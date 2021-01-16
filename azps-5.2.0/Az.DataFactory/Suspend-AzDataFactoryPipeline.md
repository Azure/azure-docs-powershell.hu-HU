---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1FF0B0F9-4B2C-46BC-8BED-12BE865E4480
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/suspend-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
ms.openlocfilehash: f2538ecf8d4f6f962be85196ca49b8a0958f69e6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356409"
---
# <span data-ttu-id="2f357-101">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="2f357-101">Suspend-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="2f357-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f357-102">SYNOPSIS</span></span>
<span data-ttu-id="2f357-103">Felfüggeszti a folyamatot az Azure Data Factoryban.</span><span class="sxs-lookup"><span data-stu-id="2f357-103">Suspends a pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="2f357-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2f357-104">SYNTAX</span></span>

### <span data-ttu-id="2f357-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2f357-105">ByFactoryName (Default)</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f357-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="2f357-106">ByFactoryObject</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f357-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2f357-107">DESCRIPTION</span></span>
<span data-ttu-id="2f357-108">A **Suspend-AzDataFactoryPipeline** parancsmag felfüggeszti a folyamatot az Azure Data Factoryban.</span><span class="sxs-lookup"><span data-stu-id="2f357-108">The **Suspend-AzDataFactoryPipeline** cmdlet suspends a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="2f357-109">A folyamat folytatásához használja a Resume-AzDataFactoryPipeline parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2f357-109">You can resume the pipeline by using the Resume-AzDataFactoryPipeline cmdlet.</span></span>

## <span data-ttu-id="2f357-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2f357-110">EXAMPLES</span></span>

### <span data-ttu-id="2f357-111">1. példa: Folyamat felfüggesztése</span><span class="sxs-lookup"><span data-stu-id="2f357-111">Example 1: Suspend a pipeline</span></span>
```
PS C:\>Suspend-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikiSample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to suspend pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="2f357-112">Ez a parancs felfüggeszti a DPWikiSample nevű folyamatot a WikiADF nevű adatüzemben.</span><span class="sxs-lookup"><span data-stu-id="2f357-112">This command suspends the pipeline named DPWikiSample in the data factory named WikiADF.</span></span>
<span data-ttu-id="2f357-113">A parancs egy számértéket ad $True.</span><span class="sxs-lookup"><span data-stu-id="2f357-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="2f357-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f357-114">PARAMETERS</span></span>

### <span data-ttu-id="2f357-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="2f357-115">-DataFactory</span></span>
<span data-ttu-id="2f357-116">EGY **PSDataFactory-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="2f357-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="2f357-117">Ez a parancsmag felfüggeszti a paraméter által megadott adat factoryhoz tartozó folyamatot.</span><span class="sxs-lookup"><span data-stu-id="2f357-117">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="2f357-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2f357-118">-DataFactoryName</span></span>
<span data-ttu-id="2f357-119">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f357-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="2f357-120">Ez a parancsmag felfüggeszti a paraméter által megadott adat factoryhoz tartozó folyamatot.</span><span class="sxs-lookup"><span data-stu-id="2f357-120">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="2f357-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f357-121">-DefaultProfile</span></span>
<span data-ttu-id="2f357-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2f357-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f357-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2f357-123">-Name</span></span>
<span data-ttu-id="2f357-124">A felfüggesztenie kell a folyamat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f357-124">Specifies the name of the pipeline to suspend.</span></span>

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

### <span data-ttu-id="2f357-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f357-125">-ResourceGroupName</span></span>
<span data-ttu-id="2f357-126">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f357-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="2f357-127">Ez a parancsmag felfüggeszti a paraméter által megadott csoporthoz tartozó folyamatot.</span><span class="sxs-lookup"><span data-stu-id="2f357-127">This cmdlet suspends a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2f357-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f357-128">-Confirm</span></span>
<span data-ttu-id="2f357-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2f357-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f357-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f357-130">-WhatIf</span></span>
<span data-ttu-id="2f357-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2f357-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f357-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2f357-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f357-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f357-133">CommonParameters</span></span>
<span data-ttu-id="2f357-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f357-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f357-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f357-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f357-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2f357-136">INPUTS</span></span>

### <span data-ttu-id="2f357-137">System.String</span><span class="sxs-lookup"><span data-stu-id="2f357-137">System.String</span></span>

### <span data-ttu-id="2f357-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="2f357-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="2f357-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f357-139">OUTPUTS</span></span>

### <span data-ttu-id="2f357-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2f357-140">System.Boolean</span></span>

## <span data-ttu-id="2f357-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2f357-141">NOTES</span></span>
* <span data-ttu-id="2f357-142">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="2f357-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="2f357-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f357-143">RELATED LINKS</span></span>

[<span data-ttu-id="2f357-144">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="2f357-144">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="2f357-145">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="2f357-145">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="2f357-146">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="2f357-146">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="2f357-147">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="2f357-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="2f357-148">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="2f357-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


