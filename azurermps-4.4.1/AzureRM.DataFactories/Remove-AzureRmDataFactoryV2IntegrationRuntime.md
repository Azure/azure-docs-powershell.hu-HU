---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: bf29e12292fba12cc6a5b4f99cef1e13f9d9fd8c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499148"
---
# <span data-ttu-id="2f97c-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2f97c-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="2f97c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f97c-102">SYNOPSIS</span></span>
<span data-ttu-id="2f97c-103">Az integrációs futtatókörnyezet eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="2f97c-103">Removes an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f97c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f97c-104">SYNTAX</span></span>

### <span data-ttu-id="2f97c-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2f97c-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f97c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2f97c-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f97c-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="2f97c-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f97c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f97c-108">DESCRIPTION</span></span>
<span data-ttu-id="2f97c-109">A Remove-AzureRmDataFactoryV2IntegrationRuntime parancsmag eltávolítja az integrációs futtatókörnyezetet.</span><span class="sxs-lookup"><span data-stu-id="2f97c-109">The Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="2f97c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2f97c-110">EXAMPLES</span></span>

### <span data-ttu-id="2f97c-111">1. példa: az integrációs futtatókörnyezet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2f97c-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="2f97c-112">Ez a parancs eltávolítja a "teszt-foglalt-IR" nevű integrációs futtatókörnyezetet a ' teszt-DF ' nevű adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="2f97c-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="2f97c-113">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="2f97c-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="2f97c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f97c-114">PARAMETERS</span></span>

### <span data-ttu-id="2f97c-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2f97c-115">-DataFactoryName</span></span>
<span data-ttu-id="2f97c-116">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="2f97c-116">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f97c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2f97c-117">-Force</span></span>
<span data-ttu-id="2f97c-118">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="2f97c-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="2f97c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f97c-119">-InputObject</span></span>
<span data-ttu-id="2f97c-120">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="2f97c-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f97c-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2f97c-121">-Name</span></span>
<span data-ttu-id="2f97c-122">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="2f97c-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f97c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f97c-123">-ResourceGroupName</span></span>
<span data-ttu-id="2f97c-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="2f97c-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f97c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f97c-125">-ResourceId</span></span>
<span data-ttu-id="2f97c-126">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="2f97c-126">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f97c-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2f97c-127">-Confirm</span></span>
<span data-ttu-id="2f97c-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2f97c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f97c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f97c-129">-WhatIf</span></span>
<span data-ttu-id="2f97c-130">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2f97c-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="2f97c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f97c-131">-DefaultProfile</span></span>
<span data-ttu-id="2f97c-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2f97c-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f97c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f97c-133">CommonParameters</span></span>
<span data-ttu-id="2f97c-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2f97c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f97c-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f97c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f97c-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f97c-136">INPUTS</span></span>

### <span data-ttu-id="2f97c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2f97c-137">System.String</span></span>
<span data-ttu-id="2f97c-138">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2f97c-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="2f97c-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f97c-139">OUTPUTS</span></span>

### <span data-ttu-id="2f97c-140">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="2f97c-140">System.Object</span></span>

## <span data-ttu-id="2f97c-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f97c-141">NOTES</span></span>
<span data-ttu-id="2f97c-142">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak, másolás, tevékenységek, integrációs futtatókörnyezet</span><span class="sxs-lookup"><span data-stu-id="2f97c-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="2f97c-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f97c-143">RELATED LINKS</span></span>

[<span data-ttu-id="2f97c-144">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2f97c-144">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="2f97c-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2f97c-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

