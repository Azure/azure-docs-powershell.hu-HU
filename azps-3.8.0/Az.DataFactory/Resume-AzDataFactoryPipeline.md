---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: F522841A-4246-4028-A754-393D8DADD924
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/resume-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Resume-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Resume-AzDataFactoryPipeline.md
ms.openlocfilehash: 26b0073cafebbd3e24afae5e8265b4acc9f4b0a9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847149"
---
# <span data-ttu-id="3d6ba-101">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="3d6ba-101">Resume-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="3d6ba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3d6ba-102">SYNOPSIS</span></span>
<span data-ttu-id="3d6ba-103">Felfüggesztett csővezeték folytatása az adatfeldolgozóban.</span><span class="sxs-lookup"><span data-stu-id="3d6ba-103">Resumes a suspended pipeline in Data Factory.</span></span>

## <span data-ttu-id="3d6ba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3d6ba-104">SYNTAX</span></span>

### <span data-ttu-id="3d6ba-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3d6ba-105">ByFactoryName (Default)</span></span>
```
Resume-AzDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d6ba-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3d6ba-106">ByFactoryObject</span></span>
```
Resume-AzDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d6ba-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3d6ba-107">DESCRIPTION</span></span>
<span data-ttu-id="3d6ba-108">A **resume-AzDataFactoryPipeline** parancsmag felfüggesztett csővezetéket folytat az Azure Data Factory-ban.</span><span class="sxs-lookup"><span data-stu-id="3d6ba-108">The **Resume-AzDataFactoryPipeline** cmdlet resumes a suspended pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="3d6ba-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3d6ba-109">EXAMPLES</span></span>

### <span data-ttu-id="3d6ba-110">Példa 1: csővezeték folytatása</span><span class="sxs-lookup"><span data-stu-id="3d6ba-110">Example 1: Resume a pipeline</span></span>
```
PS C:\>Resume-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to resume pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="3d6ba-111">Ez a parancs a DPWikisample nevű csővezetéket a WikiADF nevű adatgyárban folytatja.</span><span class="sxs-lookup"><span data-stu-id="3d6ba-111">This command resumes the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="3d6ba-112">A **felfüggesztés – AzDataFactoryPipeline** parancsmag használatával felfüggesztheti a csővezetéket.</span><span class="sxs-lookup"><span data-stu-id="3d6ba-112">Use the **Suspend-AzDataFactoryPipeline** cmdlet to suspend a pipeline.</span></span>
<span data-ttu-id="3d6ba-113">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="3d6ba-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="3d6ba-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3d6ba-114">PARAMETERS</span></span>

### <span data-ttu-id="3d6ba-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="3d6ba-115">-DataFactory</span></span>
<span data-ttu-id="3d6ba-116">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="3d6ba-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="3d6ba-117">Ez a parancsmag egy olyan csővezetéket ad vissza, amely az adatfeldolgozóhoz tartozik, és ez a paraméter határozza meg.</span><span class="sxs-lookup"><span data-stu-id="3d6ba-117">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3d6ba-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3d6ba-118">-DataFactoryName</span></span>
<span data-ttu-id="3d6ba-119">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3d6ba-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="3d6ba-120">Ez a parancsmag egy olyan csővezetéket ad vissza, amely az adatfeldolgozóhoz tartozik, és ez a paraméter határozza meg.</span><span class="sxs-lookup"><span data-stu-id="3d6ba-120">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3d6ba-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d6ba-121">-DefaultProfile</span></span>
<span data-ttu-id="3d6ba-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3d6ba-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d6ba-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3d6ba-123">-Name</span></span>
<span data-ttu-id="3d6ba-124">A folytatáshoz adja meg a csővezeték nevét.</span><span class="sxs-lookup"><span data-stu-id="3d6ba-124">Specifies the name of the pipeline to resume.</span></span>

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

### <span data-ttu-id="3d6ba-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d6ba-125">-ResourceGroupName</span></span>
<span data-ttu-id="3d6ba-126">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3d6ba-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3d6ba-127">Ez a parancsmag egy olyan futószalagot ad vissza, amely a paraméter által megadott csoportba tartozik.</span><span class="sxs-lookup"><span data-stu-id="3d6ba-127">This cmdlet resumes a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3d6ba-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3d6ba-128">-Confirm</span></span>
<span data-ttu-id="3d6ba-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3d6ba-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d6ba-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d6ba-130">-WhatIf</span></span>
<span data-ttu-id="3d6ba-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3d6ba-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d6ba-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3d6ba-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d6ba-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d6ba-133">CommonParameters</span></span>
<span data-ttu-id="3d6ba-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3d6ba-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d6ba-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d6ba-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d6ba-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d6ba-136">INPUTS</span></span>

### <span data-ttu-id="3d6ba-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3d6ba-137">System.String</span></span>

### <span data-ttu-id="3d6ba-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3d6ba-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="3d6ba-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d6ba-139">OUTPUTS</span></span>

### <span data-ttu-id="3d6ba-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3d6ba-140">System.Boolean</span></span>

## <span data-ttu-id="3d6ba-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3d6ba-141">NOTES</span></span>
* <span data-ttu-id="3d6ba-142">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="3d6ba-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3d6ba-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3d6ba-143">RELATED LINKS</span></span>

[<span data-ttu-id="3d6ba-144">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="3d6ba-144">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="3d6ba-145">Új – AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="3d6ba-145">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="3d6ba-146">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="3d6ba-146">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="3d6ba-147">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="3d6ba-147">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="3d6ba-148">Felfüggesztés – AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="3d6ba-148">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


