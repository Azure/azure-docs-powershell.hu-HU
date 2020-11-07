---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 04e93db967a589c9dbcca4a88ed29d75f742ba7a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836438"
---
# <span data-ttu-id="4e3be-101">Stop-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4e3be-101">Stop-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="4e3be-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4e3be-102">SYNOPSIS</span></span>
<span data-ttu-id="4e3be-103">Felügyelt dedikált integrációs futtatókörnyezetet állít be.</span><span class="sxs-lookup"><span data-stu-id="4e3be-103">Stops a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="4e3be-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4e3be-104">SYNTAX</span></span>

### <span data-ttu-id="4e3be-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4e3be-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4e3be-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4e3be-106">ByResourceId</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e3be-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="4e3be-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e3be-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4e3be-108">DESCRIPTION</span></span>
<span data-ttu-id="4e3be-109">A **stop-AzDataFactoryV2IntegrationRuntime** parancsmag a "Started" állapotú, felügyelt dedikált integrációs futtatókörnyezetet állítja le, amelyet az Start-AzDataFactoryV2IntegrationRuntime parancsmag kezdeményezett.</span><span class="sxs-lookup"><span data-stu-id="4e3be-109">The **Stop-AzDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="4e3be-110">A program felszabadítja az erőforrásokat, és az állam átviszi a "leállt" értékre.</span><span class="sxs-lookup"><span data-stu-id="4e3be-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="4e3be-111">Példák</span><span class="sxs-lookup"><span data-stu-id="4e3be-111">EXAMPLES</span></span>

### <span data-ttu-id="4e3be-112">1. példa: a felügyelt integrációs futtatókörnyezet leállítása "Started" állapotban.</span><span class="sxs-lookup"><span data-stu-id="4e3be-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="4e3be-113">A felügyelt integrációs futásidejű ' teszt-reserlved-IR ' "Started" állapotban van.</span><span class="sxs-lookup"><span data-stu-id="4e3be-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="4e3be-114">Miután futtatta az Stop-AzDataFactoryV2IntegrationRuntime parancsmagot, a program felszabadítja az erőforrásokat, és az állam átviszi a "leállt" értékre.</span><span class="sxs-lookup"><span data-stu-id="4e3be-114">After running Stop-AzDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="4e3be-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4e3be-115">PARAMETERS</span></span>

### <span data-ttu-id="4e3be-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4e3be-116">-DataFactoryName</span></span>
<span data-ttu-id="4e3be-117">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="4e3be-117">The data factory name.</span></span>

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

### <span data-ttu-id="4e3be-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e3be-118">-DefaultProfile</span></span>
<span data-ttu-id="4e3be-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4e3be-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e3be-120">-Force</span><span class="sxs-lookup"><span data-stu-id="4e3be-120">-Force</span></span>
<span data-ttu-id="4e3be-121">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="4e3be-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="4e3be-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e3be-122">-InputObject</span></span>
<span data-ttu-id="4e3be-123">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="4e3be-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="4e3be-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4e3be-124">-Name</span></span>
<span data-ttu-id="4e3be-125">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="4e3be-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="4e3be-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e3be-126">-ResourceGroupName</span></span>
<span data-ttu-id="4e3be-127">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="4e3be-127">The resource group name.</span></span>

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

### <span data-ttu-id="4e3be-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e3be-128">-ResourceId</span></span>
<span data-ttu-id="4e3be-129">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="4e3be-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="4e3be-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4e3be-130">-Confirm</span></span>
<span data-ttu-id="4e3be-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4e3be-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e3be-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e3be-132">-WhatIf</span></span>
<span data-ttu-id="4e3be-133">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4e3be-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="4e3be-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e3be-134">CommonParameters</span></span>
<span data-ttu-id="4e3be-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4e3be-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e3be-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e3be-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e3be-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e3be-137">INPUTS</span></span>

### <span data-ttu-id="4e3be-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4e3be-138">System.String</span></span>

### <span data-ttu-id="4e3be-139">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4e3be-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="4e3be-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e3be-140">OUTPUTS</span></span>

### <span data-ttu-id="4e3be-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="4e3be-141">System.Void</span></span>

## <span data-ttu-id="4e3be-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4e3be-142">NOTES</span></span>
<span data-ttu-id="4e3be-143">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak, másolás, tevékenységek, integrációs futtatókörnyezet</span><span class="sxs-lookup"><span data-stu-id="4e3be-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="4e3be-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e3be-144">RELATED LINKS</span></span>

[<span data-ttu-id="4e3be-145">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4e3be-145">Start-AzDataFactoryV2IntegrationRuntime</span></span>]()
