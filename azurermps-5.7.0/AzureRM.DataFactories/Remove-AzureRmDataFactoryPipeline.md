---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: dec686838bd7826b57e7b158f4ed741608eaf782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493163"
---
# <span data-ttu-id="98a52-101">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="98a52-101">Remove-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="98a52-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="98a52-102">SYNOPSIS</span></span>
<span data-ttu-id="98a52-103">Az Azure Data Factory futószalagjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="98a52-103">Removes a pipeline from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98a52-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="98a52-104">SYNTAX</span></span>

### <span data-ttu-id="98a52-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="98a52-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98a52-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="98a52-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98a52-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="98a52-107">DESCRIPTION</span></span>
<span data-ttu-id="98a52-108">A **Remove-AzureRmDataFactoryPipeline** parancsmag eltávolítja a csővezetéket az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="98a52-108">The **Remove-AzureRmDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="98a52-109">Példák</span><span class="sxs-lookup"><span data-stu-id="98a52-109">EXAMPLES</span></span>

### <span data-ttu-id="98a52-110">1. példa: a csővezeték eltávolítása</span><span class="sxs-lookup"><span data-stu-id="98a52-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="98a52-111">Ez a parancsmag eltávolítja a DPWikisample nevű csővezetéket az WikiADF nevű adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="98a52-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="98a52-112">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="98a52-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="98a52-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="98a52-113">PARAMETERS</span></span>

### <span data-ttu-id="98a52-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="98a52-114">-DataFactory</span></span>
<span data-ttu-id="98a52-115">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="98a52-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="98a52-116">Ez a parancsmag eltávolítja a csővezetéket az adatgyárból, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="98a52-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="98a52-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="98a52-117">-DataFactoryName</span></span>
<span data-ttu-id="98a52-118">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="98a52-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="98a52-119">Ez a parancsmag eltávolítja a csővezetéket az adatgyárból, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="98a52-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="98a52-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98a52-120">-DefaultProfile</span></span>
<span data-ttu-id="98a52-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="98a52-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98a52-122">-Force</span><span class="sxs-lookup"><span data-stu-id="98a52-122">-Force</span></span>
<span data-ttu-id="98a52-123">Jelzi, hogy ez a parancsmag eltávolítja a csővezetéket anélkül, hogy megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="98a52-123">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98a52-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="98a52-124">-Name</span></span>
<span data-ttu-id="98a52-125">Az eltávolítandó csővezeték nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="98a52-125">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="98a52-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98a52-126">-ResourceGroupName</span></span>
<span data-ttu-id="98a52-127">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="98a52-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="98a52-128">Ez a parancsmag eltávolítja azt a csoportot, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="98a52-128">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="98a52-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="98a52-129">-Confirm</span></span>
<span data-ttu-id="98a52-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="98a52-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98a52-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98a52-131">-WhatIf</span></span>
<span data-ttu-id="98a52-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="98a52-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98a52-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="98a52-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98a52-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98a52-134">CommonParameters</span></span>
<span data-ttu-id="98a52-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="98a52-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98a52-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98a52-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98a52-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="98a52-137">INPUTS</span></span>

### <span data-ttu-id="98a52-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="98a52-138">None</span></span>
<span data-ttu-id="98a52-139">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="98a52-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="98a52-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98a52-140">OUTPUTS</span></span>

### <span data-ttu-id="98a52-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="98a52-141">System.Boolean</span></span>

## <span data-ttu-id="98a52-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="98a52-142">NOTES</span></span>
* <span data-ttu-id="98a52-143">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="98a52-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="98a52-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98a52-144">RELATED LINKS</span></span>

[<span data-ttu-id="98a52-145">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="98a52-145">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="98a52-146">Új – AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="98a52-146">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="98a52-147">Önéletrajz – AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="98a52-147">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="98a52-148">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="98a52-148">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="98a52-149">Felfüggesztés – AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="98a52-149">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


