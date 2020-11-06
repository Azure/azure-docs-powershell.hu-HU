---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: F522841A-4246-4028-A754-393D8DADD924
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Resume-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Resume-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 63bb7337e7473d27838b08763ebe2a7de14514a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493551"
---
# <span data-ttu-id="982ab-101">Resume-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="982ab-101">Resume-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="982ab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="982ab-102">SYNOPSIS</span></span>
<span data-ttu-id="982ab-103">Felfüggesztett csővezeték folytatása az adatfeldolgozóban.</span><span class="sxs-lookup"><span data-stu-id="982ab-103">Resumes a suspended pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="982ab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="982ab-104">SYNTAX</span></span>

### <span data-ttu-id="982ab-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="982ab-105">ByFactoryName (Default)</span></span>
```
Resume-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="982ab-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="982ab-106">ByFactoryObject</span></span>
```
Resume-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="982ab-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="982ab-107">DESCRIPTION</span></span>
<span data-ttu-id="982ab-108">A **resume-AzureRmDataFactoryPipeline** parancsmag felfüggesztett csővezetéket folytat az Azure Data Factory-ban.</span><span class="sxs-lookup"><span data-stu-id="982ab-108">The **Resume-AzureRmDataFactoryPipeline** cmdlet resumes a suspended pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="982ab-109">Példák</span><span class="sxs-lookup"><span data-stu-id="982ab-109">EXAMPLES</span></span>

### <span data-ttu-id="982ab-110">Példa 1: csővezeték folytatása</span><span class="sxs-lookup"><span data-stu-id="982ab-110">Example 1: Resume a pipeline</span></span>
```
PS C:\>Resume-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to resume pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="982ab-111">Ez a parancs a DPWikisample nevű csővezetéket a WikiADF nevű adatgyárban folytatja.</span><span class="sxs-lookup"><span data-stu-id="982ab-111">This command resumes the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="982ab-112">A **felfüggesztés – AzureRmDataFactoryPipeline** parancsmag használatával felfüggesztheti a csővezetéket.</span><span class="sxs-lookup"><span data-stu-id="982ab-112">Use the **Suspend-AzureRmDataFactoryPipeline** cmdlet to suspend a pipeline.</span></span>
<span data-ttu-id="982ab-113">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="982ab-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="982ab-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="982ab-114">PARAMETERS</span></span>

### <span data-ttu-id="982ab-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="982ab-115">-DataFactory</span></span>
<span data-ttu-id="982ab-116">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="982ab-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="982ab-117">Ez a parancsmag egy olyan csővezetéket ad vissza, amely az adatfeldolgozóhoz tartozik, és ez a paraméter határozza meg.</span><span class="sxs-lookup"><span data-stu-id="982ab-117">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="982ab-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="982ab-118">-DataFactoryName</span></span>
<span data-ttu-id="982ab-119">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="982ab-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="982ab-120">Ez a parancsmag egy olyan csővezetéket ad vissza, amely az adatfeldolgozóhoz tartozik, és ez a paraméter határozza meg.</span><span class="sxs-lookup"><span data-stu-id="982ab-120">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="982ab-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="982ab-121">-Name</span></span>
<span data-ttu-id="982ab-122">A folytatáshoz adja meg a csővezeték nevét.</span><span class="sxs-lookup"><span data-stu-id="982ab-122">Specifies the name of the pipeline to resume.</span></span>

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

### <span data-ttu-id="982ab-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="982ab-123">-ResourceGroupName</span></span>
<span data-ttu-id="982ab-124">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="982ab-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="982ab-125">Ez a parancsmag egy olyan futószalagot ad vissza, amely a paraméter által megadott csoportba tartozik.</span><span class="sxs-lookup"><span data-stu-id="982ab-125">This cmdlet resumes a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="982ab-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="982ab-126">-Confirm</span></span>
<span data-ttu-id="982ab-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="982ab-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="982ab-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="982ab-128">-WhatIf</span></span>
<span data-ttu-id="982ab-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="982ab-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="982ab-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="982ab-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="982ab-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="982ab-131">-DefaultProfile</span></span>
<span data-ttu-id="982ab-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="982ab-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="982ab-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="982ab-133">CommonParameters</span></span>
<span data-ttu-id="982ab-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="982ab-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="982ab-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="982ab-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="982ab-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="982ab-136">INPUTS</span></span>

## <span data-ttu-id="982ab-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="982ab-137">OUTPUTS</span></span>

### <span data-ttu-id="982ab-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="982ab-138">System.Boolean</span></span>

## <span data-ttu-id="982ab-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="982ab-139">NOTES</span></span>
* <span data-ttu-id="982ab-140">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="982ab-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="982ab-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="982ab-141">RELATED LINKS</span></span>

[<span data-ttu-id="982ab-142">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="982ab-142">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="982ab-143">Új – AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="982ab-143">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="982ab-144">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="982ab-144">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="982ab-145">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="982ab-145">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="982ab-146">Felfüggesztés – AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="982ab-146">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


