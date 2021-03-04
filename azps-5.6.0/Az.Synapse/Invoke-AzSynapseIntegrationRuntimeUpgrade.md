---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/invoke-azsynapseintegrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
ms.openlocfilehash: ad5b23e29eb2d13fcad6aaf2659940dace83f4eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934634"
---
# <span data-ttu-id="7cfae-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="7cfae-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="7cfae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cfae-102">SYNOPSIS</span></span>
<span data-ttu-id="7cfae-103">Frissíti az önkiszolgáló integrációs futásiidőt.</span><span class="sxs-lookup"><span data-stu-id="7cfae-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="7cfae-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7cfae-104">SYNTAX</span></span>

### <span data-ttu-id="7cfae-105">InvokeByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7cfae-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cfae-106">InvokeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cfae-106">InvokeByParentObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cfae-107">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cfae-107">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cfae-108">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cfae-108">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cfae-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7cfae-109">DESCRIPTION</span></span>
<span data-ttu-id="7cfae-110">Az **Invoke-AzSynapseIntegrationRuntimeUpgrade** parancsmag frissíti az önkiszolgáló integrációs futásiidőt, ha az új verzió elérhető.</span><span class="sxs-lookup"><span data-stu-id="7cfae-110">The **Invoke-AzSynapseIntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="7cfae-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7cfae-111">EXAMPLES</span></span>

### <span data-ttu-id="7cfae-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="7cfae-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapseIntegrationRuntimeUpgrade -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="7cfae-113">A parancsmag frissíti a "test-selfhost-ir" nevű önkiszolgáló integrációs futásiidőt a ContosoWorkspace munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="7cfae-113">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="7cfae-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7cfae-114">PARAMETERS</span></span>

### <span data-ttu-id="7cfae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cfae-115">-DefaultProfile</span></span>
<span data-ttu-id="7cfae-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7cfae-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cfae-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cfae-117">-InputObject</span></span>
<span data-ttu-id="7cfae-118">Az integráció futásidejű objektuma.</span><span class="sxs-lookup"><span data-stu-id="7cfae-118">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: InvokeByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cfae-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7cfae-119">-Name</span></span>
<span data-ttu-id="7cfae-120">Az integráció futásidejű neve.</span><span class="sxs-lookup"><span data-stu-id="7cfae-120">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet, InvokeByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cfae-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cfae-121">-ResourceGroupName</span></span>
<span data-ttu-id="7cfae-122">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7cfae-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cfae-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7cfae-123">-ResourceId</span></span>
<span data-ttu-id="7cfae-124">A Synapse-integráció futásideje erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7cfae-124">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cfae-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7cfae-125">-WorkspaceName</span></span>
<span data-ttu-id="7cfae-126">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="7cfae-126">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cfae-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7cfae-127">-WorkspaceObject</span></span>
<span data-ttu-id="7cfae-128">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="7cfae-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: InvokeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cfae-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7cfae-129">-Confirm</span></span>
<span data-ttu-id="7cfae-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7cfae-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cfae-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cfae-131">-WhatIf</span></span>
<span data-ttu-id="7cfae-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7cfae-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cfae-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7cfae-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cfae-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cfae-134">CommonParameters</span></span>
<span data-ttu-id="7cfae-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cfae-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cfae-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7cfae-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cfae-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7cfae-137">INPUTS</span></span>

### <span data-ttu-id="7cfae-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7cfae-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="7cfae-139">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="7cfae-139">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="7cfae-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cfae-140">OUTPUTS</span></span>

### <span data-ttu-id="7cfae-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="7cfae-141">System.Void</span></span>

## <span data-ttu-id="7cfae-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7cfae-142">NOTES</span></span>

## <span data-ttu-id="7cfae-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7cfae-143">RELATED LINKS</span></span>
