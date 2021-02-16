---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: cb2c632b47e512d31a5349be9b6091a9981f5459
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165586"
---
# <span data-ttu-id="5d1c1-101">Remove-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="5d1c1-101">Remove-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="5d1c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d1c1-102">SYNOPSIS</span></span>
<span data-ttu-id="5d1c1-103">Eltávolíthat egy adott nevű csomópontot egy integrációs futási időben.</span><span class="sxs-lookup"><span data-stu-id="5d1c1-103">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="5d1c1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5d1c1-104">SYNTAX</span></span>

### <span data-ttu-id="5d1c1-105">RemoveByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5d1c1-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d1c1-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d1c1-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5d1c1-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d1c1-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -ResourceId <String> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d1c1-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d1c1-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d1c1-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5d1c1-109">DESCRIPTION</span></span>
<span data-ttu-id="5d1c1-110">A **Remove-AzSynapseIntegrationRuntimeNode** parancsmag eltávolít egy csomópontot egy integrációs futási időben.</span><span class="sxs-lookup"><span data-stu-id="5d1c1-110">The **Remove-AzSynapseIntegrationRuntimeNode** cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="5d1c1-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5d1c1-111">EXAMPLES</span></span>

### <span data-ttu-id="5d1c1-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="5d1c1-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="5d1c1-113">Eltávolíthat egy adott nevű csomópontot egy integrációs futási időben.</span><span class="sxs-lookup"><span data-stu-id="5d1c1-113">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="5d1c1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d1c1-114">PARAMETERS</span></span>

### <span data-ttu-id="5d1c1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d1c1-115">-DefaultProfile</span></span>
<span data-ttu-id="5d1c1-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5d1c1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d1c1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5d1c1-117">-Force</span></span>
<span data-ttu-id="5d1c1-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5d1c1-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="5d1c1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d1c1-119">-InputObject</span></span>
<span data-ttu-id="5d1c1-120">Az integráció futásidejű objektuma.</span><span class="sxs-lookup"><span data-stu-id="5d1c1-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="5d1c1-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="5d1c1-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="5d1c1-122">Az integráció futásidejű neve.</span><span class="sxs-lookup"><span data-stu-id="5d1c1-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="5d1c1-123">-NodeName</span><span class="sxs-lookup"><span data-stu-id="5d1c1-123">-NodeName</span></span>
<span data-ttu-id="5d1c1-124">Az integráció futásidejű csomópontjának neve.</span><span class="sxs-lookup"><span data-stu-id="5d1c1-124">The integration runtime node name.</span></span>

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

### <span data-ttu-id="5d1c1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d1c1-125">-ResourceGroupName</span></span>
<span data-ttu-id="5d1c1-126">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5d1c1-126">Resource group name.</span></span>

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

### <span data-ttu-id="5d1c1-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d1c1-127">-ResourceId</span></span>
<span data-ttu-id="5d1c1-128">A Synapse-integráció futásideje erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5d1c1-128">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="5d1c1-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5d1c1-129">-WorkspaceName</span></span>
<span data-ttu-id="5d1c1-130">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="5d1c1-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5d1c1-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5d1c1-131">-WorkspaceObject</span></span>
<span data-ttu-id="5d1c1-132">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="5d1c1-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5d1c1-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d1c1-133">-Confirm</span></span>
<span data-ttu-id="5d1c1-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5d1c1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d1c1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d1c1-135">-WhatIf</span></span>
<span data-ttu-id="5d1c1-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5d1c1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d1c1-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5d1c1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d1c1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d1c1-138">CommonParameters</span></span>
<span data-ttu-id="5d1c1-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d1c1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d1c1-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d1c1-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d1c1-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5d1c1-141">INPUTS</span></span>

### <span data-ttu-id="5d1c1-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5d1c1-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="5d1c1-143">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5d1c1-143">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="5d1c1-144">System.String</span><span class="sxs-lookup"><span data-stu-id="5d1c1-144">System.String</span></span>

## <span data-ttu-id="5d1c1-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d1c1-145">OUTPUTS</span></span>

### <span data-ttu-id="5d1c1-146">System.Void</span><span class="sxs-lookup"><span data-stu-id="5d1c1-146">System.Void</span></span>

## <span data-ttu-id="5d1c1-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5d1c1-147">NOTES</span></span>

## <span data-ttu-id="5d1c1-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d1c1-148">RELATED LINKS</span></span>
