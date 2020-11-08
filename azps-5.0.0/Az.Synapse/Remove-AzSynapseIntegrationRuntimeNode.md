---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: cb2c632b47e512d31a5349be9b6091a9981f5459
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187143"
---
# <span data-ttu-id="b81f4-101">Remove-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="b81f4-101">Remove-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="b81f4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b81f4-102">SYNOPSIS</span></span>
<span data-ttu-id="b81f4-103">A megadott nevű csomópont eltávolítása az integrációs futtatókörnyezetben.</span><span class="sxs-lookup"><span data-stu-id="b81f4-103">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="b81f4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b81f4-104">SYNTAX</span></span>

### <span data-ttu-id="b81f4-105">RemoveByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b81f4-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b81f4-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b81f4-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b81f4-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b81f4-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -ResourceId <String> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b81f4-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b81f4-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b81f4-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="b81f4-109">DESCRIPTION</span></span>
<span data-ttu-id="b81f4-110">A **Remove-AzSynapseIntegrationRuntimeNode** parancsmag egy csomópontot távolít el egy integrációs futtatókörnyezetben.</span><span class="sxs-lookup"><span data-stu-id="b81f4-110">The **Remove-AzSynapseIntegrationRuntimeNode** cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="b81f4-111">Példák</span><span class="sxs-lookup"><span data-stu-id="b81f4-111">EXAMPLES</span></span>

### <span data-ttu-id="b81f4-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b81f4-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="b81f4-113">A megadott nevű csomópont eltávolítása az integrációs futtatókörnyezetben.</span><span class="sxs-lookup"><span data-stu-id="b81f4-113">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="b81f4-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b81f4-114">PARAMETERS</span></span>

### <span data-ttu-id="b81f4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b81f4-115">-DefaultProfile</span></span>
<span data-ttu-id="b81f4-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b81f4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b81f4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b81f4-117">-Force</span></span>
<span data-ttu-id="b81f4-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b81f4-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="b81f4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b81f4-119">-InputObject</span></span>
<span data-ttu-id="b81f4-120">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="b81f4-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b81f4-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="b81f4-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="b81f4-122">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="b81f4-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b81f4-123">-Csomópontnév</span><span class="sxs-lookup"><span data-stu-id="b81f4-123">-NodeName</span></span>
<span data-ttu-id="b81f4-124">Az integráció futásidejű csomópontjának neve.</span><span class="sxs-lookup"><span data-stu-id="b81f4-124">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b81f4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b81f4-125">-ResourceGroupName</span></span>
<span data-ttu-id="b81f4-126">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="b81f4-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b81f4-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b81f4-127">-ResourceId</span></span>
<span data-ttu-id="b81f4-128">A szinapszis-integrációs futtatókörnyezet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b81f4-128">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b81f4-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b81f4-129">-WorkspaceName</span></span>
<span data-ttu-id="b81f4-130">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="b81f4-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b81f4-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b81f4-131">-WorkspaceObject</span></span>
<span data-ttu-id="b81f4-132">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="b81f4-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b81f4-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b81f4-133">-Confirm</span></span>
<span data-ttu-id="b81f4-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b81f4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b81f4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b81f4-135">-WhatIf</span></span>
<span data-ttu-id="b81f4-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b81f4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b81f4-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b81f4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b81f4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b81f4-138">CommonParameters</span></span>
<span data-ttu-id="b81f4-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b81f4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b81f4-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b81f4-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b81f4-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b81f4-141">INPUTS</span></span>

### <span data-ttu-id="b81f4-142">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b81f4-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="b81f4-143">Microsoft. Azure. commands. szinapszis. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b81f4-143">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="b81f4-144">System. String</span><span class="sxs-lookup"><span data-stu-id="b81f4-144">System.String</span></span>

## <span data-ttu-id="b81f4-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b81f4-145">OUTPUTS</span></span>

### <span data-ttu-id="b81f4-146">System. Void</span><span class="sxs-lookup"><span data-stu-id="b81f4-146">System.Void</span></span>

## <span data-ttu-id="b81f4-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b81f4-147">NOTES</span></span>

## <span data-ttu-id="b81f4-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b81f4-148">RELATED LINKS</span></span>
