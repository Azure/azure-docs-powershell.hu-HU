---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1FF0B0F9-4B2C-46BC-8BED-12BE865E4480
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/suspend-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
ms.openlocfilehash: 2f3d48044b06292b18b1254adf1e2bc6d0698d4f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671108"
---
# <span data-ttu-id="3c33b-101">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="3c33b-101">Suspend-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="3c33b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3c33b-102">SYNOPSIS</span></span>
<span data-ttu-id="3c33b-103">Az Azure Data Factory csővezetékének felfüggesztése</span><span class="sxs-lookup"><span data-stu-id="3c33b-103">Suspends a pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="3c33b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3c33b-104">SYNTAX</span></span>

### <span data-ttu-id="3c33b-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3c33b-105">ByFactoryName (Default)</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c33b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3c33b-106">ByFactoryObject</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c33b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3c33b-107">DESCRIPTION</span></span>
<span data-ttu-id="3c33b-108">A **felfüggesztés – AzDataFactoryPipeline** parancsmag felfüggeszti a csővezetéket az Azure Data Factory-ban.</span><span class="sxs-lookup"><span data-stu-id="3c33b-108">The **Suspend-AzDataFactoryPipeline** cmdlet suspends a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="3c33b-109">A csővezetéket az Resume-AzDataFactoryPipeline parancsmag használatával folytathatja újra.</span><span class="sxs-lookup"><span data-stu-id="3c33b-109">You can resume the pipeline by using the Resume-AzDataFactoryPipeline cmdlet.</span></span>

## <span data-ttu-id="3c33b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3c33b-110">EXAMPLES</span></span>

### <span data-ttu-id="3c33b-111">1. példa: a csővezeték felfüggesztése</span><span class="sxs-lookup"><span data-stu-id="3c33b-111">Example 1: Suspend a pipeline</span></span>
```
PS C:\>Suspend-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikiSample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to suspend pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="3c33b-112">Ez a parancs felfüggeszti a DPWikiSample nevű csővezetéket az WikiADF nevű adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="3c33b-112">This command suspends the pipeline named DPWikiSample in the data factory named WikiADF.</span></span>
<span data-ttu-id="3c33b-113">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="3c33b-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="3c33b-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3c33b-114">PARAMETERS</span></span>

### <span data-ttu-id="3c33b-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="3c33b-115">-DataFactory</span></span>
<span data-ttu-id="3c33b-116">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="3c33b-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="3c33b-117">Ez a parancsmag felfüggeszti az adatfeldolgozóhoz tartozó csővezetéket, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="3c33b-117">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3c33b-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3c33b-118">-DataFactoryName</span></span>
<span data-ttu-id="3c33b-119">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3c33b-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="3c33b-120">Ez a parancsmag felfüggeszti az adatfeldolgozóhoz tartozó csővezetéket, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="3c33b-120">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3c33b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c33b-121">-DefaultProfile</span></span>
<span data-ttu-id="3c33b-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3c33b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c33b-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3c33b-123">-Name</span></span>
<span data-ttu-id="3c33b-124">A felfüggeszteni kívánt futószalag nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3c33b-124">Specifies the name of the pipeline to suspend.</span></span>

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

### <span data-ttu-id="3c33b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c33b-125">-ResourceGroupName</span></span>
<span data-ttu-id="3c33b-126">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3c33b-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3c33b-127">Ez a parancsmag felfüggeszti azt a munkafolyamatot, amely a paraméter által megadott csoportba tartozik.</span><span class="sxs-lookup"><span data-stu-id="3c33b-127">This cmdlet suspends a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3c33b-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3c33b-128">-Confirm</span></span>
<span data-ttu-id="3c33b-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3c33b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c33b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c33b-130">-WhatIf</span></span>
<span data-ttu-id="3c33b-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3c33b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c33b-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3c33b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c33b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c33b-133">CommonParameters</span></span>
<span data-ttu-id="3c33b-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3c33b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c33b-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c33b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c33b-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c33b-136">INPUTS</span></span>

### <span data-ttu-id="3c33b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3c33b-137">System.String</span></span>

### <span data-ttu-id="3c33b-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3c33b-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="3c33b-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c33b-139">OUTPUTS</span></span>

### <span data-ttu-id="3c33b-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3c33b-140">System.Boolean</span></span>

## <span data-ttu-id="3c33b-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3c33b-141">NOTES</span></span>
* <span data-ttu-id="3c33b-142">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="3c33b-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3c33b-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c33b-143">RELATED LINKS</span></span>

[<span data-ttu-id="3c33b-144">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="3c33b-144">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="3c33b-145">Új – AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="3c33b-145">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="3c33b-146">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="3c33b-146">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="3c33b-147">Önéletrajz – AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="3c33b-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="3c33b-148">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="3c33b-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


