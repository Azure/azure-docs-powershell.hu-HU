---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: f84973c29d83e8c7c01c3505d17166275a833460
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836470"
---
# <span data-ttu-id="ce198-101">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="ce198-101">Remove-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="ce198-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ce198-102">SYNOPSIS</span></span>
<span data-ttu-id="ce198-103">Egy kapcsolt szolgáltatás eltávolítása az adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="ce198-103">Removes a linked service from Data Factory.</span></span>

## <span data-ttu-id="ce198-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ce198-104">SYNTAX</span></span>

### <span data-ttu-id="ce198-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ce198-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce198-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ce198-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce198-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ce198-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2LinkedService [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce198-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ce198-108">DESCRIPTION</span></span>
<span data-ttu-id="ce198-109">A Remove-AzDataFactoryV2LinkedService parancsmag az Azure Data Factory szolgáltatásból távolítja el az egyik kapcsolt szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="ce198-109">The Remove-AzDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="ce198-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ce198-110">EXAMPLES</span></span>

### <span data-ttu-id="ce198-111">1. példa: kapcsolt szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ce198-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="ce198-112">Ez a parancs eltávolítja a LinkedServiceTest nevű kapcsolt szolgáltatást a WikiADF nevű adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="ce198-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="ce198-113">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="ce198-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="ce198-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ce198-114">PARAMETERS</span></span>

### <span data-ttu-id="ce198-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ce198-115">-DataFactoryName</span></span>
<span data-ttu-id="ce198-116">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ce198-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ce198-117">Ez a parancsmag eltávolítja a kapcsolt szolgáltatást az adatgyárból, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="ce198-117">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ce198-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce198-118">-DefaultProfile</span></span>
<span data-ttu-id="ce198-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ce198-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce198-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ce198-120">-Force</span></span>
<span data-ttu-id="ce198-121">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="ce198-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ce198-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce198-122">-InputObject</span></span>
<span data-ttu-id="ce198-123">Az eltávolítandó LinkedService-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="ce198-123">Specifies the LinkedService object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce198-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ce198-124">-Name</span></span>
<span data-ttu-id="ce198-125">Az eltávolítandó kapcsolt szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ce198-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="ce198-126">A kapcsolt szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="ce198-126">Name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce198-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce198-127">-ResourceGroupName</span></span>
<span data-ttu-id="ce198-128">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ce198-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ce198-129">Ez a parancsmag eltávolítja a kapcsolt szolgáltatást abból a csoportból, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="ce198-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ce198-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce198-130">-ResourceId</span></span>
<span data-ttu-id="ce198-131">Az eltávolítandó kapcsolt szolgáltatás Azure Resource ID azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ce198-131">The Azure resource ID of the linked service to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce198-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ce198-132">-Confirm</span></span>
<span data-ttu-id="ce198-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ce198-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce198-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce198-134">-WhatIf</span></span>
<span data-ttu-id="ce198-135">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ce198-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce198-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce198-136">CommonParameters</span></span>
<span data-ttu-id="ce198-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ce198-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce198-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce198-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce198-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce198-139">INPUTS</span></span>

### <span data-ttu-id="ce198-140">Microsoft. Azure. Command. DataFactoryV2. models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="ce198-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

### <span data-ttu-id="ce198-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ce198-141">System.String</span></span>

## <span data-ttu-id="ce198-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce198-142">OUTPUTS</span></span>

### <span data-ttu-id="ce198-143">System. Void</span><span class="sxs-lookup"><span data-stu-id="ce198-143">System.Void</span></span>

## <span data-ttu-id="ce198-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ce198-144">NOTES</span></span>
<span data-ttu-id="ce198-145">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="ce198-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ce198-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ce198-146">RELATED LINKS</span></span>

[<span data-ttu-id="ce198-147">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="ce198-147">Get-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="ce198-148">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="ce198-148">Set-AzDataFactoryV2LinkedService</span></span>]()

