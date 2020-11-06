---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: a636dcfabe3f1736f9705724ed302ab40d3637a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492304"
---
# <span data-ttu-id="164ca-101">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="164ca-101">Remove-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="164ca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="164ca-102">SYNOPSIS</span></span>
<span data-ttu-id="164ca-103">Egy kapcsolt szolgáltatás eltávolítása az adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="164ca-103">Removes a linked service from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="164ca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="164ca-104">SYNTAX</span></span>

### <span data-ttu-id="164ca-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="164ca-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="164ca-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="164ca-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="164ca-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="164ca-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="164ca-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="164ca-108">DESCRIPTION</span></span>
<span data-ttu-id="164ca-109">A Remove-AzureRmDataFactoryV2LinkedService parancsmag az Azure Data Factory szolgáltatásból távolítja el az egyik kapcsolt szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="164ca-109">The Remove-AzureRmDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="164ca-110">Példák</span><span class="sxs-lookup"><span data-stu-id="164ca-110">EXAMPLES</span></span>

### <span data-ttu-id="164ca-111">1. példa: kapcsolt szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="164ca-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="164ca-112">Ez a parancs eltávolítja a LinkedServiceTest nevű kapcsolt szolgáltatást a WikiADF nevű adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="164ca-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="164ca-113">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="164ca-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="164ca-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="164ca-114">PARAMETERS</span></span>

### <span data-ttu-id="164ca-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="164ca-115">-DataFactoryName</span></span>
<span data-ttu-id="164ca-116">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="164ca-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="164ca-117">Ez a parancsmag eltávolítja a kapcsolt szolgáltatást az adatgyárból, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="164ca-117">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="164ca-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="164ca-118">-DefaultProfile</span></span>
<span data-ttu-id="164ca-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="164ca-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="164ca-120">-Force</span><span class="sxs-lookup"><span data-stu-id="164ca-120">-Force</span></span>
<span data-ttu-id="164ca-121">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="164ca-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="164ca-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="164ca-122">-InputObject</span></span>
<span data-ttu-id="164ca-123">Az eltávolítandó LinkedService-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="164ca-123">Specifies the LinkedService object to remove.</span></span>

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

### <span data-ttu-id="164ca-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="164ca-124">-Name</span></span>
<span data-ttu-id="164ca-125">Az eltávolítandó kapcsolt szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="164ca-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="164ca-126">A kapcsolt szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="164ca-126">Name of the linked service.</span></span>

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

### <span data-ttu-id="164ca-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="164ca-127">-ResourceGroupName</span></span>
<span data-ttu-id="164ca-128">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="164ca-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="164ca-129">Ez a parancsmag eltávolítja a kapcsolt szolgáltatást abból a csoportból, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="164ca-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>


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

### <span data-ttu-id="164ca-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="164ca-130">-ResourceId</span></span>
<span data-ttu-id="164ca-131">Az eltávolítandó kapcsolt szolgáltatás Azure Resource ID azonosítója.</span><span class="sxs-lookup"><span data-stu-id="164ca-131">The Azure resource ID of the linked service to remove.</span></span>

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

### <span data-ttu-id="164ca-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="164ca-132">-Confirm</span></span>
<span data-ttu-id="164ca-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="164ca-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="164ca-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="164ca-134">-WhatIf</span></span>
<span data-ttu-id="164ca-135">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="164ca-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="164ca-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="164ca-136">CommonParameters</span></span>
<span data-ttu-id="164ca-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="164ca-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="164ca-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="164ca-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="164ca-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="164ca-139">INPUTS</span></span>

### <span data-ttu-id="164ca-140">Microsoft. Azure. Command. DataFactoryV2. models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="164ca-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>
<span data-ttu-id="164ca-141">System. String</span><span class="sxs-lookup"><span data-stu-id="164ca-141">System.String</span></span>

## <span data-ttu-id="164ca-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="164ca-142">OUTPUTS</span></span>

### <span data-ttu-id="164ca-143">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="164ca-143">System.Object</span></span>

## <span data-ttu-id="164ca-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="164ca-144">NOTES</span></span>
<span data-ttu-id="164ca-145">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="164ca-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="164ca-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="164ca-146">RELATED LINKS</span></span>

[<span data-ttu-id="164ca-147">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="164ca-147">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="164ca-148">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="164ca-148">Set-AzureRmDataFactoryV2LinkedService</span></span>]()

