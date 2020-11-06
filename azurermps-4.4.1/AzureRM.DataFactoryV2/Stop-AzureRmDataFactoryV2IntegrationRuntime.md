---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 181d63a41853105b21826353fabfca83cddf1bd4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505964"
---
# <span data-ttu-id="ea453-101">Stop-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ea453-101">Stop-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="ea453-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ea453-102">SYNOPSIS</span></span>
<span data-ttu-id="ea453-103">Felügyelt dedikált integrációs futtatókörnyezetet állít be.</span><span class="sxs-lookup"><span data-stu-id="ea453-103">Stops a managed dedicated integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea453-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ea453-104">SYNTAX</span></span>

### <span data-ttu-id="ea453-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ea453-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="ea453-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ea453-106">ByResourceId</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="ea453-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="ea453-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="ea453-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ea453-108">DESCRIPTION</span></span>
<span data-ttu-id="ea453-109">A **stop-AzureRmDataFactoryV2IntegrationRuntime** parancsmag a "Started" állapotú, felügyelt dedikált integrációs futtatókörnyezetet állítja le, amelyet az Start-AzureRmDataFactoryV2IntegrationRuntime parancsmag kezdeményezett.</span><span class="sxs-lookup"><span data-stu-id="ea453-109">The **Stop-AzureRmDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="ea453-110">A program felszabadítja az erőforrásokat, és az állam átviszi a "leállt" értékre.</span><span class="sxs-lookup"><span data-stu-id="ea453-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="ea453-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ea453-111">EXAMPLES</span></span>

### <span data-ttu-id="ea453-112">1. példa: a felügyelt integrációs futtatókörnyezet leállítása "Started" állapotban.</span><span class="sxs-lookup"><span data-stu-id="ea453-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="ea453-113">A felügyelt integrációs futásidejű ' teszt-reserlved-IR ' "Started" állapotban van.</span><span class="sxs-lookup"><span data-stu-id="ea453-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="ea453-114">Miután futtatta az Stop-AzureRmDataFactoryV2IntegrationRuntime parancsmagot, a program felszabadítja az erőforrásokat, és az állam átviszi a "leállt" értékre.</span><span class="sxs-lookup"><span data-stu-id="ea453-114">After running Stop-AzureRmDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="ea453-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ea453-115">PARAMETERS</span></span>

### <span data-ttu-id="ea453-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ea453-116">-Confirm</span></span>
<span data-ttu-id="ea453-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ea453-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea453-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ea453-118">-DataFactoryName</span></span>
<span data-ttu-id="ea453-119">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="ea453-119">The data factory name.</span></span>

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

### <span data-ttu-id="ea453-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ea453-120">-Force</span></span>
<span data-ttu-id="ea453-121">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="ea453-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ea453-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea453-122">-InputObject</span></span>
<span data-ttu-id="ea453-123">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="ea453-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="ea453-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ea453-124">-Name</span></span>
<span data-ttu-id="ea453-125">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="ea453-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="ea453-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea453-126">-ResourceGroupName</span></span>
<span data-ttu-id="ea453-127">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="ea453-127">The resource group name.</span></span>

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

### <span data-ttu-id="ea453-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea453-128">-ResourceId</span></span>
<span data-ttu-id="ea453-129">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="ea453-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ea453-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ea453-130">-Confirm</span></span>
<span data-ttu-id="ea453-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ea453-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea453-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea453-132">-WhatIf</span></span>
<span data-ttu-id="ea453-133">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ea453-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="ea453-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea453-134">CommonParameters</span></span>
<span data-ttu-id="ea453-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ea453-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea453-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea453-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea453-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea453-137">INPUTS</span></span>

### <span data-ttu-id="ea453-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ea453-138">System.String</span></span>
<span data-ttu-id="ea453-139">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ea453-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="ea453-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea453-140">OUTPUTS</span></span>

### <span data-ttu-id="ea453-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ea453-141">System.Boolean</span></span>

## <span data-ttu-id="ea453-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ea453-142">NOTES</span></span>
<span data-ttu-id="ea453-143">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak, másolás, tevékenységek, integrációs futtatókörnyezet</span><span class="sxs-lookup"><span data-stu-id="ea453-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="ea453-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ea453-144">RELATED LINKS</span></span>
[<span data-ttu-id="ea453-145">Start-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ea453-145">Start-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
