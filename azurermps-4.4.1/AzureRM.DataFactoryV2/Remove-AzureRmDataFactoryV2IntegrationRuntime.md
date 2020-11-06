---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 81b05b8229530a8975be023a3b4a5e8c93d93c80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505084"
---
# <span data-ttu-id="1e06e-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1e06e-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="1e06e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1e06e-102">SYNOPSIS</span></span>
<span data-ttu-id="1e06e-103">Az integrációs futtatókörnyezet eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="1e06e-103">Removes an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e06e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1e06e-104">SYNTAX</span></span>

### <span data-ttu-id="1e06e-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1e06e-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="1e06e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1e06e-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="1e06e-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="1e06e-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="1e06e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1e06e-108">DESCRIPTION</span></span>
<span data-ttu-id="1e06e-109">A Remove-AzureRmDataFactoryV2IntegrationRuntime parancsmag eltávolítja az integrációs futtatókörnyezetet.</span><span class="sxs-lookup"><span data-stu-id="1e06e-109">The Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="1e06e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1e06e-110">EXAMPLES</span></span>

### <span data-ttu-id="1e06e-111">1. példa: az integrációs futtatókörnyezet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="1e06e-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="1e06e-112">Ez a parancs eltávolítja a "teszt-foglalt-IR" nevű integrációs futtatókörnyezetet a ' teszt-DF ' nevű adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="1e06e-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="1e06e-113">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="1e06e-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="1e06e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1e06e-114">PARAMETERS</span></span>

### <span data-ttu-id="1e06e-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1e06e-115">-DataFactoryName</span></span>
<span data-ttu-id="1e06e-116">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="1e06e-116">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e06e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1e06e-117">-Force</span></span>
<span data-ttu-id="1e06e-118">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="1e06e-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="1e06e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e06e-119">-InputObject</span></span>
<span data-ttu-id="1e06e-120">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="1e06e-120">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e06e-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1e06e-121">-Name</span></span>
<span data-ttu-id="1e06e-122">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="1e06e-122">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e06e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e06e-123">-ResourceGroupName</span></span>
<span data-ttu-id="1e06e-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="1e06e-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e06e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e06e-125">-ResourceId</span></span>
<span data-ttu-id="1e06e-126">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="1e06e-126">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e06e-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1e06e-127">-Confirm</span></span>
<span data-ttu-id="1e06e-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1e06e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e06e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e06e-129">-WhatIf</span></span>
<span data-ttu-id="1e06e-130">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1e06e-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="1e06e-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e06e-131">INPUTS</span></span>

### <span data-ttu-id="1e06e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1e06e-132">System.String</span></span>
<span data-ttu-id="1e06e-133">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1e06e-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="1e06e-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e06e-134">OUTPUTS</span></span>

### <span data-ttu-id="1e06e-135">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="1e06e-135">System.Object</span></span>

## <span data-ttu-id="1e06e-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1e06e-136">NOTES</span></span>
<span data-ttu-id="1e06e-137">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak, másolás, tevékenységek, integrációs futtatókörnyezet</span><span class="sxs-lookup"><span data-stu-id="1e06e-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="1e06e-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e06e-138">RELATED LINKS</span></span>
[<span data-ttu-id="1e06e-139">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1e06e-139">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="1e06e-140">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1e06e-140">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

