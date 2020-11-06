---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 24c84657dd33c5ea313f1d6d2c0710b6a3801afd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505988"
---
# <span data-ttu-id="29fcf-101">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="29fcf-101">Remove-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="29fcf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29fcf-102">SYNOPSIS</span></span>
<span data-ttu-id="29fcf-103">Egy kapcsolt szolgáltatás eltávolítása az adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="29fcf-103">Removes a linked service from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29fcf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29fcf-104">SYNTAX</span></span>

### <span data-ttu-id="29fcf-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="29fcf-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="29fcf-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="29fcf-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="29fcf-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="29fcf-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="29fcf-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="29fcf-108">DESCRIPTION</span></span>
<span data-ttu-id="29fcf-109">A Remove-AzureRmDataFactoryV2LinkedService parancsmag az Azure Data Factory szolgáltatásból távolítja el az egyik kapcsolt szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="29fcf-109">The Remove-AzureRmDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="29fcf-110">Példák</span><span class="sxs-lookup"><span data-stu-id="29fcf-110">EXAMPLES</span></span>

### <span data-ttu-id="29fcf-111">1. példa: kapcsolt szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="29fcf-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="29fcf-112">Ez a parancs eltávolítja a LinkedServiceTest nevű kapcsolt szolgáltatást a WikiADF nevű adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="29fcf-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="29fcf-113">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="29fcf-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="29fcf-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29fcf-114">PARAMETERS</span></span>

### <span data-ttu-id="29fcf-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="29fcf-115">-Confirm</span></span>
<span data-ttu-id="29fcf-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="29fcf-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29fcf-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="29fcf-117">-DataFactoryName</span></span>
<span data-ttu-id="29fcf-118">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="29fcf-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="29fcf-119">Ez a parancsmag eltávolítja a kapcsolt szolgáltatást az adatgyárból, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="29fcf-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="29fcf-120">-Force</span><span class="sxs-lookup"><span data-stu-id="29fcf-120">-Force</span></span>
<span data-ttu-id="29fcf-121">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="29fcf-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="29fcf-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29fcf-122">-InputObject</span></span>
<span data-ttu-id="29fcf-123">Az eltávolítandó LinkedService-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="29fcf-123">Specifies the LinkedService object to remove.</span></span>

```yaml
Type: PSLinkedService
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29fcf-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="29fcf-124">-Name</span></span>
<span data-ttu-id="29fcf-125">Az eltávolítandó kapcsolt szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="29fcf-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="29fcf-126">A kapcsolt szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="29fcf-126">Name of the linked service.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29fcf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29fcf-127">-ResourceGroupName</span></span>
<span data-ttu-id="29fcf-128">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="29fcf-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="29fcf-129">Ez a parancsmag eltávolítja a kapcsolt szolgáltatást abból a csoportból, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="29fcf-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>


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

### <span data-ttu-id="29fcf-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29fcf-130">-ResourceId</span></span>
<span data-ttu-id="29fcf-131">Az eltávolítandó kapcsolt szolgáltatás Azure Resource ID azonosítója.</span><span class="sxs-lookup"><span data-stu-id="29fcf-131">The Azure resource ID of the linked service to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29fcf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29fcf-132">-WhatIf</span></span>
<span data-ttu-id="29fcf-133">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="29fcf-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="29fcf-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29fcf-134">INPUTS</span></span>

### <span data-ttu-id="29fcf-135">Microsoft. Azure. Command. DataFactoryV2. models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="29fcf-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>
<span data-ttu-id="29fcf-136">System. String</span><span class="sxs-lookup"><span data-stu-id="29fcf-136">System.String</span></span>


## <span data-ttu-id="29fcf-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29fcf-137">OUTPUTS</span></span>

### <span data-ttu-id="29fcf-138">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="29fcf-138">System.Object</span></span>

## <span data-ttu-id="29fcf-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29fcf-139">NOTES</span></span>
<span data-ttu-id="29fcf-140">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="29fcf-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="29fcf-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29fcf-141">RELATED LINKS</span></span>
[<span data-ttu-id="29fcf-142">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="29fcf-142">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="29fcf-143">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="29fcf-143">Set-AzureRmDataFactoryV2LinkedService</span></span>]()

