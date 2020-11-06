---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: F522841A-4246-4028-A754-393D8DADD924
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/resume-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Resume-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Resume-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 5cf769a02b6a02f0fba9b26df48554d80a406140
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493164"
---
# <span data-ttu-id="cee53-101">Resume-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="cee53-101">Resume-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="cee53-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cee53-102">SYNOPSIS</span></span>
<span data-ttu-id="cee53-103">Felfüggesztett csővezeték folytatása az adatfeldolgozóban.</span><span class="sxs-lookup"><span data-stu-id="cee53-103">Resumes a suspended pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cee53-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cee53-104">SYNTAX</span></span>

### <span data-ttu-id="cee53-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cee53-105">ByFactoryName (Default)</span></span>
```
Resume-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cee53-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="cee53-106">ByFactoryObject</span></span>
```
Resume-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cee53-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cee53-107">DESCRIPTION</span></span>
<span data-ttu-id="cee53-108">A **resume-AzureRmDataFactoryPipeline** parancsmag felfüggesztett csővezetéket folytat az Azure Data Factory-ban.</span><span class="sxs-lookup"><span data-stu-id="cee53-108">The **Resume-AzureRmDataFactoryPipeline** cmdlet resumes a suspended pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="cee53-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cee53-109">EXAMPLES</span></span>

### <span data-ttu-id="cee53-110">Példa 1: csővezeték folytatása</span><span class="sxs-lookup"><span data-stu-id="cee53-110">Example 1: Resume a pipeline</span></span>
```
PS C:\>Resume-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to resume pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="cee53-111">Ez a parancs a DPWikisample nevű csővezetéket a WikiADF nevű adatgyárban folytatja.</span><span class="sxs-lookup"><span data-stu-id="cee53-111">This command resumes the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="cee53-112">A **felfüggesztés – AzureRmDataFactoryPipeline** parancsmag használatával felfüggesztheti a csővezetéket.</span><span class="sxs-lookup"><span data-stu-id="cee53-112">Use the **Suspend-AzureRmDataFactoryPipeline** cmdlet to suspend a pipeline.</span></span>
<span data-ttu-id="cee53-113">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="cee53-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="cee53-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cee53-114">PARAMETERS</span></span>

### <span data-ttu-id="cee53-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="cee53-115">-DataFactory</span></span>
<span data-ttu-id="cee53-116">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="cee53-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="cee53-117">Ez a parancsmag egy olyan csővezetéket ad vissza, amely az adatfeldolgozóhoz tartozik, és ez a paraméter határozza meg.</span><span class="sxs-lookup"><span data-stu-id="cee53-117">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cee53-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cee53-118">-DataFactoryName</span></span>
<span data-ttu-id="cee53-119">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cee53-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="cee53-120">Ez a parancsmag egy olyan csővezetéket ad vissza, amely az adatfeldolgozóhoz tartozik, és ez a paraméter határozza meg.</span><span class="sxs-lookup"><span data-stu-id="cee53-120">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="cee53-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cee53-121">-DefaultProfile</span></span>
<span data-ttu-id="cee53-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cee53-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cee53-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cee53-123">-Name</span></span>
<span data-ttu-id="cee53-124">A folytatáshoz adja meg a csővezeték nevét.</span><span class="sxs-lookup"><span data-stu-id="cee53-124">Specifies the name of the pipeline to resume.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cee53-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cee53-125">-ResourceGroupName</span></span>
<span data-ttu-id="cee53-126">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cee53-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="cee53-127">Ez a parancsmag egy olyan futószalagot ad vissza, amely a paraméter által megadott csoportba tartozik.</span><span class="sxs-lookup"><span data-stu-id="cee53-127">This cmdlet resumes a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="cee53-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cee53-128">-Confirm</span></span>
<span data-ttu-id="cee53-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cee53-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cee53-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cee53-130">-WhatIf</span></span>
<span data-ttu-id="cee53-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cee53-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cee53-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cee53-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cee53-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cee53-133">CommonParameters</span></span>
<span data-ttu-id="cee53-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cee53-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cee53-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cee53-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cee53-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cee53-136">INPUTS</span></span>

### <span data-ttu-id="cee53-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="cee53-137">None</span></span>
<span data-ttu-id="cee53-138">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="cee53-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cee53-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cee53-139">OUTPUTS</span></span>

### <span data-ttu-id="cee53-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cee53-140">System.Boolean</span></span>

## <span data-ttu-id="cee53-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cee53-141">NOTES</span></span>
* <span data-ttu-id="cee53-142">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="cee53-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="cee53-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cee53-143">RELATED LINKS</span></span>

[<span data-ttu-id="cee53-144">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="cee53-144">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="cee53-145">Új – AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="cee53-145">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="cee53-146">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="cee53-146">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="cee53-147">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="cee53-147">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="cee53-148">Felfüggesztés – AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="cee53-148">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


