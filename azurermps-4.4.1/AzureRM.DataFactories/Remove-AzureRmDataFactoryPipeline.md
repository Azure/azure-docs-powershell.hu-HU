---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 48638f53f58fd420e9a7b3dfe2e50a3e61d2314f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493548"
---
# <span data-ttu-id="c6bf0-101">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="c6bf0-101">Remove-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="c6bf0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c6bf0-102">SYNOPSIS</span></span>
<span data-ttu-id="c6bf0-103">Az Azure Data Factory futószalagjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="c6bf0-103">Removes a pipeline from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6bf0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c6bf0-104">SYNTAX</span></span>

### <span data-ttu-id="c6bf0-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c6bf0-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6bf0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c6bf0-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6bf0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c6bf0-107">DESCRIPTION</span></span>
<span data-ttu-id="c6bf0-108">A **Remove-AzureRmDataFactoryPipeline** parancsmag eltávolítja a csővezetéket az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="c6bf0-108">The **Remove-AzureRmDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="c6bf0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c6bf0-109">EXAMPLES</span></span>

### <span data-ttu-id="c6bf0-110">1. példa: a csővezeték eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c6bf0-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="c6bf0-111">Ez a parancsmag eltávolítja a DPWikisample nevű csővezetéket az WikiADF nevű adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="c6bf0-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="c6bf0-112">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="c6bf0-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="c6bf0-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c6bf0-113">PARAMETERS</span></span>

### <span data-ttu-id="c6bf0-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="c6bf0-114">-DataFactory</span></span>
<span data-ttu-id="c6bf0-115">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="c6bf0-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="c6bf0-116">Ez a parancsmag eltávolítja a csővezetéket az adatgyárból, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="c6bf0-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c6bf0-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c6bf0-117">-DataFactoryName</span></span>
<span data-ttu-id="c6bf0-118">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c6bf0-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="c6bf0-119">Ez a parancsmag eltávolítja a csővezetéket az adatgyárból, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="c6bf0-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c6bf0-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c6bf0-120">-Force</span></span>
<span data-ttu-id="c6bf0-121">Jelzi, hogy ez a parancsmag eltávolítja a csővezetéket anélkül, hogy megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c6bf0-121">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="c6bf0-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c6bf0-122">-Name</span></span>
<span data-ttu-id="c6bf0-123">Az eltávolítandó csővezeték nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c6bf0-123">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="c6bf0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6bf0-124">-ResourceGroupName</span></span>
<span data-ttu-id="c6bf0-125">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c6bf0-125">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c6bf0-126">Ez a parancsmag eltávolítja azt a csoportot, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="c6bf0-126">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c6bf0-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c6bf0-127">-Confirm</span></span>
<span data-ttu-id="c6bf0-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c6bf0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6bf0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6bf0-129">-WhatIf</span></span>
<span data-ttu-id="c6bf0-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c6bf0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6bf0-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c6bf0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6bf0-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6bf0-132">-DefaultProfile</span></span>
<span data-ttu-id="c6bf0-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c6bf0-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6bf0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6bf0-134">CommonParameters</span></span>
<span data-ttu-id="c6bf0-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c6bf0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6bf0-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6bf0-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6bf0-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6bf0-137">INPUTS</span></span>

## <span data-ttu-id="c6bf0-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6bf0-138">OUTPUTS</span></span>

### <span data-ttu-id="c6bf0-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c6bf0-139">System.Boolean</span></span>

## <span data-ttu-id="c6bf0-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c6bf0-140">NOTES</span></span>
* <span data-ttu-id="c6bf0-141">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="c6bf0-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c6bf0-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6bf0-142">RELATED LINKS</span></span>

[<span data-ttu-id="c6bf0-143">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="c6bf0-143">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="c6bf0-144">Új – AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="c6bf0-144">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="c6bf0-145">Önéletrajz – AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="c6bf0-145">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="c6bf0-146">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="c6bf0-146">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="c6bf0-147">Felfüggesztés – AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="c6bf0-147">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


