---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 8c7ec74e43586a951b3f8d2c4d8af0caa6e09a2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491961"
---
# <span data-ttu-id="ab2ea-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ab2ea-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="ab2ea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ab2ea-102">SYNOPSIS</span></span>
<span data-ttu-id="ab2ea-103">Az integrációs futtatókörnyezet eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="ab2ea-103">Removes an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab2ea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ab2ea-104">SYNTAX</span></span>

### <span data-ttu-id="ab2ea-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ab2ea-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab2ea-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ab2ea-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab2ea-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="ab2ea-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab2ea-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ab2ea-108">DESCRIPTION</span></span>
<span data-ttu-id="ab2ea-109">A Remove-AzureRmDataFactoryV2IntegrationRuntime parancsmag eltávolítja az integrációs futtatókörnyezetet.</span><span class="sxs-lookup"><span data-stu-id="ab2ea-109">The Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="ab2ea-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ab2ea-110">EXAMPLES</span></span>

### <span data-ttu-id="ab2ea-111">1. példa: az integrációs futtatókörnyezet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ab2ea-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="ab2ea-112">Ez a parancs eltávolítja a "teszt-foglalt-IR" nevű integrációs futtatókörnyezetet a ' teszt-DF ' nevű adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="ab2ea-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="ab2ea-113">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="ab2ea-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="ab2ea-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ab2ea-114">PARAMETERS</span></span>

### <span data-ttu-id="ab2ea-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ab2ea-115">-DataFactoryName</span></span>
<span data-ttu-id="ab2ea-116">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="ab2ea-116">The data factory name.</span></span>

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

### <span data-ttu-id="ab2ea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab2ea-117">-DefaultProfile</span></span>
<span data-ttu-id="ab2ea-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ab2ea-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab2ea-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ab2ea-119">-Force</span></span>
<span data-ttu-id="ab2ea-120">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="ab2ea-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ab2ea-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab2ea-121">-InputObject</span></span>
<span data-ttu-id="ab2ea-122">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="ab2ea-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="ab2ea-123">-LinkedDataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ab2ea-123">-LinkedDataFactoryName</span></span>
<span data-ttu-id="ab2ea-124">A kapcsolt Data Factory neve.</span><span class="sxs-lookup"><span data-stu-id="ab2ea-124">The linked data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab2ea-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ab2ea-125">-Name</span></span>
<span data-ttu-id="ab2ea-126">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="ab2ea-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="ab2ea-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab2ea-127">-ResourceGroupName</span></span>
<span data-ttu-id="ab2ea-128">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="ab2ea-128">The resource group name.</span></span>

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

### <span data-ttu-id="ab2ea-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab2ea-129">-ResourceId</span></span>
<span data-ttu-id="ab2ea-130">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="ab2ea-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ab2ea-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ab2ea-131">-Confirm</span></span>
<span data-ttu-id="ab2ea-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ab2ea-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab2ea-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab2ea-133">-WhatIf</span></span>
<span data-ttu-id="ab2ea-134">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ab2ea-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="ab2ea-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab2ea-135">CommonParameters</span></span>
<span data-ttu-id="ab2ea-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ab2ea-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab2ea-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab2ea-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab2ea-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab2ea-138">INPUTS</span></span>

### <span data-ttu-id="ab2ea-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ab2ea-139">System.String</span></span>

### <span data-ttu-id="ab2ea-140">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ab2ea-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="ab2ea-141">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ab2ea-141">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="ab2ea-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab2ea-142">OUTPUTS</span></span>

### <span data-ttu-id="ab2ea-143">System. Void</span><span class="sxs-lookup"><span data-stu-id="ab2ea-143">System.Void</span></span>

## <span data-ttu-id="ab2ea-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ab2ea-144">NOTES</span></span>
<span data-ttu-id="ab2ea-145">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak, másolás, tevékenységek, integrációs futtatókörnyezet</span><span class="sxs-lookup"><span data-stu-id="ab2ea-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="ab2ea-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab2ea-146">RELATED LINKS</span></span>

[<span data-ttu-id="ab2ea-147">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ab2ea-147">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="ab2ea-148">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ab2ea-148">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

