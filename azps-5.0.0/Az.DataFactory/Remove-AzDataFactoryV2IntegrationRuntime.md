---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 0c24f77b51bcfc50ec11e211fc7f11b60e348221
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298337"
---
# <span data-ttu-id="c2570-101">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c2570-101">Remove-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="c2570-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c2570-102">SYNOPSIS</span></span>
<span data-ttu-id="c2570-103">Az integrációs futtatókörnyezet eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="c2570-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="c2570-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c2570-104">SYNTAX</span></span>

### <span data-ttu-id="c2570-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c2570-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2570-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c2570-106">ByResourceId</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2570-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="c2570-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c2570-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c2570-108">DESCRIPTION</span></span>
<span data-ttu-id="c2570-109">A Remove-AzDataFactoryV2IntegrationRuntime parancsmag eltávolítja az integrációs futtatókörnyezetet.</span><span class="sxs-lookup"><span data-stu-id="c2570-109">The Remove-AzDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="c2570-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c2570-110">EXAMPLES</span></span>

### <span data-ttu-id="c2570-111">1. példa: az integrációs futtatókörnyezet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c2570-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="c2570-112">Ez a parancs eltávolítja a "teszt-foglalt-IR" nevű integrációs futtatókörnyezetet a ' teszt-DF ' nevű adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="c2570-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="c2570-113">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="c2570-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="c2570-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c2570-114">PARAMETERS</span></span>

### <span data-ttu-id="c2570-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c2570-115">-DataFactoryName</span></span>
<span data-ttu-id="c2570-116">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="c2570-116">The data factory name.</span></span>

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

### <span data-ttu-id="c2570-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2570-117">-DefaultProfile</span></span>
<span data-ttu-id="c2570-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c2570-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2570-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c2570-119">-Force</span></span>
<span data-ttu-id="c2570-120">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="c2570-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="c2570-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2570-121">-InputObject</span></span>
<span data-ttu-id="c2570-122">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="c2570-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="c2570-123">-LinkedDataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c2570-123">-LinkedDataFactoryName</span></span>
<span data-ttu-id="c2570-124">A kapcsolt Data Factory neve.</span><span class="sxs-lookup"><span data-stu-id="c2570-124">The linked data factory name.</span></span>

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

### <span data-ttu-id="c2570-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c2570-125">-Name</span></span>
<span data-ttu-id="c2570-126">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="c2570-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="c2570-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2570-127">-ResourceGroupName</span></span>
<span data-ttu-id="c2570-128">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="c2570-128">The resource group name.</span></span>

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

### <span data-ttu-id="c2570-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2570-129">-ResourceId</span></span>
<span data-ttu-id="c2570-130">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="c2570-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="c2570-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c2570-131">-Confirm</span></span>
<span data-ttu-id="c2570-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c2570-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2570-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2570-133">-WhatIf</span></span>
<span data-ttu-id="c2570-134">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c2570-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="c2570-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2570-135">CommonParameters</span></span>
<span data-ttu-id="c2570-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c2570-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2570-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2570-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2570-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2570-138">INPUTS</span></span>

### <span data-ttu-id="c2570-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c2570-139">System.String</span></span>

### <span data-ttu-id="c2570-140">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c2570-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="c2570-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2570-141">OUTPUTS</span></span>

### <span data-ttu-id="c2570-142">System. Void</span><span class="sxs-lookup"><span data-stu-id="c2570-142">System.Void</span></span>

## <span data-ttu-id="c2570-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c2570-143">NOTES</span></span>
<span data-ttu-id="c2570-144">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak, másolás, tevékenységek, integrációs futtatókörnyezet</span><span class="sxs-lookup"><span data-stu-id="c2570-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="c2570-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c2570-145">RELATED LINKS</span></span>

[<span data-ttu-id="c2570-146">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c2570-146">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="c2570-147">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c2570-147">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

