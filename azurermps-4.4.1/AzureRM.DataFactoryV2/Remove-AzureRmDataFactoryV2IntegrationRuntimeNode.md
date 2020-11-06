---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: e5bf7ca6951a78fc631b5bc2ffa96a2042423d9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502747"
---
# <span data-ttu-id="f5795-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="f5795-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="f5795-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f5795-102">SYNOPSIS</span></span>
<span data-ttu-id="f5795-103">A megadott nevű csomópont eltávolítása az integrációs futtatókörnyezetben.</span><span class="sxs-lookup"><span data-stu-id="f5795-103">Remove a node with the given name on an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5795-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f5795-104">SYNTAX</span></span>

### <span data-ttu-id="f5795-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f5795-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String> [-WhatIf]
 [-Confirm]
```

### <span data-ttu-id="f5795-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f5795-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-ResourceId] <String> [-WhatIf]
 [-Confirm]
```

### <span data-ttu-id="f5795-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="f5795-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-InputObject] <PSIntegrationRuntime> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="f5795-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f5795-108">DESCRIPTION</span></span>
<span data-ttu-id="f5795-109">A Remove-AzureRmDataFactoryV2IntegrationRuntimeNode parancsmag eltávolítja a csomópontot egy integrációs futtatókörnyezetben.</span><span class="sxs-lookup"><span data-stu-id="f5795-109">The Remove-AzureRmDataFactoryV2IntegrationRuntimeNode cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="f5795-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f5795-110">EXAMPLES</span></span>

### <span data-ttu-id="f5795-111">1. példa: csomópont eltávolítása egy integrációs futtatókörnyezetből</span><span class="sxs-lookup"><span data-stu-id="f5795-111">Example 1: Remove a node from an integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="f5795-112">Ez a parancs eltávolítja az "Node_1" nevű csomópontot az "selfhost-IR" nevű, "RG-teszt-dfv2" nevű erőforráscsoport-előfizetésben, valamint a "teszt-DF-EU2" nevű adatkezelési futtatókörnyezetben.</span><span class="sxs-lookup"><span data-stu-id="f5795-112">This command removes an node named 'Node_1' in the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="f5795-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f5795-113">PARAMETERS</span></span>

### <span data-ttu-id="f5795-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f5795-114">-Confirm</span></span>
<span data-ttu-id="f5795-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f5795-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5795-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f5795-116">-DataFactoryName</span></span>
<span data-ttu-id="f5795-117">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="f5795-117">The data factory name.</span></span>

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

### <span data-ttu-id="f5795-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f5795-118">-Force</span></span>
<span data-ttu-id="f5795-119">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="f5795-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="f5795-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5795-120">-InputObject</span></span>
<span data-ttu-id="f5795-121">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="f5795-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="f5795-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="f5795-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="f5795-123">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="f5795-123">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5795-124">-Csomópontnév</span><span class="sxs-lookup"><span data-stu-id="f5795-124">-NodeName</span></span>
<span data-ttu-id="f5795-125">Az integráció futásidejű csomópontjának neve.</span><span class="sxs-lookup"><span data-stu-id="f5795-125">The integration runtime node name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5795-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5795-126">-ResourceGroupName</span></span>
<span data-ttu-id="f5795-127">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="f5795-127">The resource group name.</span></span>

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

### <span data-ttu-id="f5795-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5795-128">-ResourceId</span></span>
<span data-ttu-id="f5795-129">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="f5795-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="f5795-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5795-130">-WhatIf</span></span>
<span data-ttu-id="f5795-131">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f5795-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="f5795-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5795-132">INPUTS</span></span>

### <span data-ttu-id="f5795-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f5795-133">System.String</span></span>
<span data-ttu-id="f5795-134">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f5795-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="f5795-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5795-135">OUTPUTS</span></span>

### <span data-ttu-id="f5795-136">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="f5795-136">System.Object</span></span>

## <span data-ttu-id="f5795-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f5795-137">NOTES</span></span>

## <span data-ttu-id="f5795-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5795-138">RELATED LINKS</span></span>

