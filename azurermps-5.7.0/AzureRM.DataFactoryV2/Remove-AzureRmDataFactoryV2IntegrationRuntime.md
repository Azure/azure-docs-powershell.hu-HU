---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: a2515b3713f449d25963af5952e233117e078ba9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492306"
---
# <span data-ttu-id="deec3-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="deec3-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="deec3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="deec3-102">SYNOPSIS</span></span>
<span data-ttu-id="deec3-103">Az integrációs futtatókörnyezet eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="deec3-103">Removes an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="deec3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="deec3-104">SYNTAX</span></span>

### <span data-ttu-id="deec3-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="deec3-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="deec3-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="deec3-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="deec3-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="deec3-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="deec3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="deec3-108">DESCRIPTION</span></span>
<span data-ttu-id="deec3-109">A Remove-AzureRmDataFactoryV2IntegrationRuntime parancsmag eltávolítja az integrációs futtatókörnyezetet.</span><span class="sxs-lookup"><span data-stu-id="deec3-109">The Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="deec3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="deec3-110">EXAMPLES</span></span>

### <span data-ttu-id="deec3-111">1. példa: az integrációs futtatókörnyezet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="deec3-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="deec3-112">Ez a parancs eltávolítja a "teszt-foglalt-IR" nevű integrációs futtatókörnyezetet a ' teszt-DF ' nevű adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="deec3-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="deec3-113">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="deec3-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="deec3-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="deec3-114">PARAMETERS</span></span>

### <span data-ttu-id="deec3-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="deec3-115">-DataFactoryName</span></span>
<span data-ttu-id="deec3-116">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="deec3-116">The data factory name.</span></span>

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

### <span data-ttu-id="deec3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deec3-117">-DefaultProfile</span></span>
<span data-ttu-id="deec3-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="deec3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="deec3-119">-Force</span><span class="sxs-lookup"><span data-stu-id="deec3-119">-Force</span></span>
<span data-ttu-id="deec3-120">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="deec3-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="deec3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="deec3-121">-InputObject</span></span>
<span data-ttu-id="deec3-122">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="deec3-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="deec3-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="deec3-123">-Name</span></span>
<span data-ttu-id="deec3-124">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="deec3-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="deec3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="deec3-125">-ResourceGroupName</span></span>
<span data-ttu-id="deec3-126">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="deec3-126">The resource group name.</span></span>

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

### <span data-ttu-id="deec3-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="deec3-127">-ResourceId</span></span>
<span data-ttu-id="deec3-128">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="deec3-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="deec3-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="deec3-129">-Confirm</span></span>
<span data-ttu-id="deec3-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="deec3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="deec3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="deec3-131">-WhatIf</span></span>
<span data-ttu-id="deec3-132">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="deec3-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="deec3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deec3-133">CommonParameters</span></span>
<span data-ttu-id="deec3-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="deec3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deec3-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="deec3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deec3-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="deec3-136">INPUTS</span></span>

### <span data-ttu-id="deec3-137">System. String</span><span class="sxs-lookup"><span data-stu-id="deec3-137">System.String</span></span>
<span data-ttu-id="deec3-138">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="deec3-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="deec3-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="deec3-139">OUTPUTS</span></span>

### <span data-ttu-id="deec3-140">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="deec3-140">System.Object</span></span>

## <span data-ttu-id="deec3-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="deec3-141">NOTES</span></span>
<span data-ttu-id="deec3-142">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak, másolás, tevékenységek, integrációs futtatókörnyezet</span><span class="sxs-lookup"><span data-stu-id="deec3-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="deec3-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="deec3-143">RELATED LINKS</span></span>

[<span data-ttu-id="deec3-144">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="deec3-144">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="deec3-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="deec3-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

