---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: dbf5b4eba8c6fe2dc55e55a58df79ed9b7d08afb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666994"
---
# <span data-ttu-id="ad890-101">Remove-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="ad890-101">Remove-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="ad890-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ad890-102">SYNOPSIS</span></span>
<span data-ttu-id="ad890-103">A megadott nevű csomópont eltávolítása az integrációs futtatókörnyezetben.</span><span class="sxs-lookup"><span data-stu-id="ad890-103">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="ad890-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ad890-104">SYNTAX</span></span>

### <span data-ttu-id="ad890-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ad890-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad890-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ad890-106">ByResourceId</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad890-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="ad890-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad890-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ad890-108">DESCRIPTION</span></span>
<span data-ttu-id="ad890-109">A Remove-AzDataFactoryV2IntegrationRuntimeNode parancsmag eltávolítja a csomópontot egy integrációs futtatókörnyezetben.</span><span class="sxs-lookup"><span data-stu-id="ad890-109">The Remove-AzDataFactoryV2IntegrationRuntimeNode cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="ad890-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ad890-110">EXAMPLES</span></span>

### <span data-ttu-id="ad890-111">1. példa: csomópont eltávolítása egy integrációs futtatókörnyezetből</span><span class="sxs-lookup"><span data-stu-id="ad890-111">Example 1: Remove a node from an integration runtime</span></span>
```
PS C:\> Remove-AzDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="ad890-112">Ez a parancs eltávolítja az "Node_1" nevű csomópontot az "selfhost-IR" nevű, "RG-teszt-dfv2" nevű erőforráscsoport-előfizetésben, valamint a "teszt-DF-EU2" nevű adatkezelési futtatókörnyezetben.</span><span class="sxs-lookup"><span data-stu-id="ad890-112">This command removes an node named 'Node_1' in the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="ad890-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ad890-113">PARAMETERS</span></span>

### <span data-ttu-id="ad890-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ad890-114">-DataFactoryName</span></span>
<span data-ttu-id="ad890-115">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="ad890-115">The data factory name.</span></span>

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

### <span data-ttu-id="ad890-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad890-116">-DefaultProfile</span></span>
<span data-ttu-id="ad890-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad890-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad890-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ad890-118">-Force</span></span>
<span data-ttu-id="ad890-119">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="ad890-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ad890-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad890-120">-InputObject</span></span>
<span data-ttu-id="ad890-121">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="ad890-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="ad890-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="ad890-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="ad890-123">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="ad890-123">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad890-124">-Csomópontnév</span><span class="sxs-lookup"><span data-stu-id="ad890-124">-NodeName</span></span>
<span data-ttu-id="ad890-125">Az integráció futásidejű csomópontjának neve.</span><span class="sxs-lookup"><span data-stu-id="ad890-125">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad890-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad890-126">-ResourceGroupName</span></span>
<span data-ttu-id="ad890-127">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="ad890-127">The resource group name.</span></span>

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

### <span data-ttu-id="ad890-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad890-128">-ResourceId</span></span>
<span data-ttu-id="ad890-129">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="ad890-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ad890-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ad890-130">-Confirm</span></span>
<span data-ttu-id="ad890-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ad890-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad890-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad890-132">-WhatIf</span></span>
<span data-ttu-id="ad890-133">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ad890-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="ad890-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad890-134">CommonParameters</span></span>
<span data-ttu-id="ad890-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ad890-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad890-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad890-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad890-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad890-137">INPUTS</span></span>

### <span data-ttu-id="ad890-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ad890-138">System.String</span></span>

### <span data-ttu-id="ad890-139">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ad890-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="ad890-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad890-140">OUTPUTS</span></span>

### <span data-ttu-id="ad890-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="ad890-141">System.Void</span></span>

## <span data-ttu-id="ad890-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ad890-142">NOTES</span></span>

## <span data-ttu-id="ad890-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad890-143">RELATED LINKS</span></span>
