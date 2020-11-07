---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: F522841A-4246-4028-A754-393D8DADD924
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/resume-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Resume-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Resume-AzDataFactoryPipeline.md
ms.openlocfilehash: 221fb414464c062a2f1798223bfe68a09543d7c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666984"
---
# <span data-ttu-id="101b2-101">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="101b2-101">Resume-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="101b2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="101b2-102">SYNOPSIS</span></span>
<span data-ttu-id="101b2-103">Felfüggesztett csővezeték folytatása az adatfeldolgozóban.</span><span class="sxs-lookup"><span data-stu-id="101b2-103">Resumes a suspended pipeline in Data Factory.</span></span>

## <span data-ttu-id="101b2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="101b2-104">SYNTAX</span></span>

### <span data-ttu-id="101b2-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="101b2-105">ByFactoryName (Default)</span></span>
```
Resume-AzDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="101b2-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="101b2-106">ByFactoryObject</span></span>
```
Resume-AzDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="101b2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="101b2-107">DESCRIPTION</span></span>
<span data-ttu-id="101b2-108">A **resume-AzDataFactoryPipeline** parancsmag felfüggesztett csővezetéket folytat az Azure Data Factory-ban.</span><span class="sxs-lookup"><span data-stu-id="101b2-108">The **Resume-AzDataFactoryPipeline** cmdlet resumes a suspended pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="101b2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="101b2-109">EXAMPLES</span></span>

### <span data-ttu-id="101b2-110">Példa 1: csővezeték folytatása</span><span class="sxs-lookup"><span data-stu-id="101b2-110">Example 1: Resume a pipeline</span></span>
```
PS C:\>Resume-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to resume pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="101b2-111">Ez a parancs a DPWikisample nevű csővezetéket a WikiADF nevű adatgyárban folytatja.</span><span class="sxs-lookup"><span data-stu-id="101b2-111">This command resumes the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="101b2-112">A **felfüggesztés – AzDataFactoryPipeline** parancsmag használatával felfüggesztheti a csővezetéket.</span><span class="sxs-lookup"><span data-stu-id="101b2-112">Use the **Suspend-AzDataFactoryPipeline** cmdlet to suspend a pipeline.</span></span>
<span data-ttu-id="101b2-113">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="101b2-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="101b2-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="101b2-114">PARAMETERS</span></span>

### <span data-ttu-id="101b2-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="101b2-115">-DataFactory</span></span>
<span data-ttu-id="101b2-116">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="101b2-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="101b2-117">Ez a parancsmag egy olyan csővezetéket ad vissza, amely az adatfeldolgozóhoz tartozik, és ez a paraméter határozza meg.</span><span class="sxs-lookup"><span data-stu-id="101b2-117">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="101b2-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="101b2-118">-DataFactoryName</span></span>
<span data-ttu-id="101b2-119">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="101b2-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="101b2-120">Ez a parancsmag egy olyan csővezetéket ad vissza, amely az adatfeldolgozóhoz tartozik, és ez a paraméter határozza meg.</span><span class="sxs-lookup"><span data-stu-id="101b2-120">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="101b2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="101b2-121">-DefaultProfile</span></span>
<span data-ttu-id="101b2-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="101b2-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="101b2-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="101b2-123">-Name</span></span>
<span data-ttu-id="101b2-124">A folytatáshoz adja meg a csővezeték nevét.</span><span class="sxs-lookup"><span data-stu-id="101b2-124">Specifies the name of the pipeline to resume.</span></span>

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

### <span data-ttu-id="101b2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="101b2-125">-ResourceGroupName</span></span>
<span data-ttu-id="101b2-126">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="101b2-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="101b2-127">Ez a parancsmag egy olyan futószalagot ad vissza, amely a paraméter által megadott csoportba tartozik.</span><span class="sxs-lookup"><span data-stu-id="101b2-127">This cmdlet resumes a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="101b2-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="101b2-128">-Confirm</span></span>
<span data-ttu-id="101b2-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="101b2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="101b2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="101b2-130">-WhatIf</span></span>
<span data-ttu-id="101b2-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="101b2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="101b2-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="101b2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="101b2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="101b2-133">CommonParameters</span></span>
<span data-ttu-id="101b2-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="101b2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="101b2-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="101b2-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="101b2-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="101b2-136">INPUTS</span></span>

### <span data-ttu-id="101b2-137">System. String</span><span class="sxs-lookup"><span data-stu-id="101b2-137">System.String</span></span>

### <span data-ttu-id="101b2-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="101b2-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="101b2-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="101b2-139">OUTPUTS</span></span>

### <span data-ttu-id="101b2-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="101b2-140">System.Boolean</span></span>

## <span data-ttu-id="101b2-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="101b2-141">NOTES</span></span>
* <span data-ttu-id="101b2-142">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="101b2-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="101b2-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="101b2-143">RELATED LINKS</span></span>

[<span data-ttu-id="101b2-144">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="101b2-144">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="101b2-145">Új – AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="101b2-145">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="101b2-146">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="101b2-146">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="101b2-147">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="101b2-147">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="101b2-148">Felfüggesztés – AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="101b2-148">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


