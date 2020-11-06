---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 1FF0B0F9-4B2C-46BC-8BED-12BE865E4480
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/suspend-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Suspend-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Suspend-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: ecbf1a97ebaa7f4d008b63f9b7d4c49c49a09956
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502971"
---
# <span data-ttu-id="4ef0d-101">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="4ef0d-101">Suspend-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="4ef0d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4ef0d-102">SYNOPSIS</span></span>
<span data-ttu-id="4ef0d-103">Az Azure Data Factory csővezetékének felfüggesztése</span><span class="sxs-lookup"><span data-stu-id="4ef0d-103">Suspends a pipeline in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ef0d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4ef0d-104">SYNTAX</span></span>

### <span data-ttu-id="4ef0d-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4ef0d-105">ByFactoryName (Default)</span></span>
```
Suspend-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ef0d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4ef0d-106">ByFactoryObject</span></span>
```
Suspend-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ef0d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4ef0d-107">DESCRIPTION</span></span>
<span data-ttu-id="4ef0d-108">A **felfüggesztés – AzureRmDataFactoryPipeline** parancsmag felfüggeszti a csővezetéket az Azure Data Factory-ban.</span><span class="sxs-lookup"><span data-stu-id="4ef0d-108">The **Suspend-AzureRmDataFactoryPipeline** cmdlet suspends a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="4ef0d-109">A csővezetéket az Resume-AzureRmDataFactoryPipeline parancsmag használatával folytathatja újra.</span><span class="sxs-lookup"><span data-stu-id="4ef0d-109">You can resume the pipeline by using the Resume-AzureRmDataFactoryPipeline cmdlet.</span></span>

## <span data-ttu-id="4ef0d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4ef0d-110">EXAMPLES</span></span>

### <span data-ttu-id="4ef0d-111">1. példa: a csővezeték felfüggesztése</span><span class="sxs-lookup"><span data-stu-id="4ef0d-111">Example 1: Suspend a pipeline</span></span>
```
PS C:\>Suspend-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikiSample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to suspend pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="4ef0d-112">Ez a parancs felfüggeszti a DPWikiSample nevű csővezetéket az WikiADF nevű adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="4ef0d-112">This command suspends the pipeline named DPWikiSample in the data factory named WikiADF.</span></span>
<span data-ttu-id="4ef0d-113">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="4ef0d-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="4ef0d-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4ef0d-114">PARAMETERS</span></span>

### <span data-ttu-id="4ef0d-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="4ef0d-115">-DataFactory</span></span>
<span data-ttu-id="4ef0d-116">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="4ef0d-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="4ef0d-117">Ez a parancsmag felfüggeszti az adatfeldolgozóhoz tartozó csővezetéket, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ef0d-117">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4ef0d-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4ef0d-118">-DataFactoryName</span></span>
<span data-ttu-id="4ef0d-119">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ef0d-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="4ef0d-120">Ez a parancsmag felfüggeszti az adatfeldolgozóhoz tartozó csővezetéket, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ef0d-120">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4ef0d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ef0d-121">-DefaultProfile</span></span>
<span data-ttu-id="4ef0d-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4ef0d-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ef0d-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4ef0d-123">-Name</span></span>
<span data-ttu-id="4ef0d-124">A felfüggeszteni kívánt futószalag nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ef0d-124">Specifies the name of the pipeline to suspend.</span></span>

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

### <span data-ttu-id="4ef0d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ef0d-125">-ResourceGroupName</span></span>
<span data-ttu-id="4ef0d-126">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ef0d-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4ef0d-127">Ez a parancsmag felfüggeszti azt a munkafolyamatot, amely a paraméter által megadott csoportba tartozik.</span><span class="sxs-lookup"><span data-stu-id="4ef0d-127">This cmdlet suspends a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4ef0d-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4ef0d-128">-Confirm</span></span>
<span data-ttu-id="4ef0d-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4ef0d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ef0d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ef0d-130">-WhatIf</span></span>
<span data-ttu-id="4ef0d-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4ef0d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ef0d-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4ef0d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ef0d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ef0d-133">CommonParameters</span></span>
<span data-ttu-id="4ef0d-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4ef0d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ef0d-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ef0d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ef0d-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ef0d-136">INPUTS</span></span>

### <span data-ttu-id="4ef0d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4ef0d-137">System.String</span></span>

### <span data-ttu-id="4ef0d-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="4ef0d-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="4ef0d-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ef0d-139">OUTPUTS</span></span>

### <span data-ttu-id="4ef0d-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4ef0d-140">System.Boolean</span></span>

## <span data-ttu-id="4ef0d-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4ef0d-141">NOTES</span></span>
* <span data-ttu-id="4ef0d-142">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="4ef0d-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4ef0d-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ef0d-143">RELATED LINKS</span></span>

[<span data-ttu-id="4ef0d-144">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="4ef0d-144">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="4ef0d-145">Új – AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="4ef0d-145">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="4ef0d-146">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="4ef0d-146">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="4ef0d-147">Önéletrajz – AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="4ef0d-147">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="4ef0d-148">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="4ef0d-148">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)


