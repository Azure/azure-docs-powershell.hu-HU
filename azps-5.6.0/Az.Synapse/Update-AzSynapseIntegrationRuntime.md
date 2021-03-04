---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 004cfc8e0bd22be1f57a320cf10aa7d7f53cbb0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938425"
---
# <span data-ttu-id="a214b-101">Update-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a214b-101">Update-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="a214b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a214b-102">SYNOPSIS</span></span>
<span data-ttu-id="a214b-103">Egy integrációs futási idő frissítése.</span><span class="sxs-lookup"><span data-stu-id="a214b-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="a214b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a214b-104">SYNTAX</span></span>

### <span data-ttu-id="a214b-105">UpdateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a214b-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a214b-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a214b-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a214b-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a214b-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -ResourceId <String> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a214b-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a214b-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a214b-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a214b-109">DESCRIPTION</span></span>
<span data-ttu-id="a214b-110">Az **Update-AzSynapseIntegrationRuntime parancsmag** frissíti az integráció futásidejű tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="a214b-110">The **Update-AzSynapseIntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="a214b-111">A parancsmag jelenleg csak az "AutoUpdate" és az "AutoUpdateDelayOffset" frissítését támogatja az önkiszolgáló integráció futásidejéhez.</span><span class="sxs-lookup"><span data-stu-id="a214b-111">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="a214b-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a214b-112">EXAMPLES</span></span>

### <span data-ttu-id="a214b-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="a214b-113">Example 1</span></span>
```powershell
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -AutoUpdate Off -AutoUpdateDelayOffset $ts
```

<span data-ttu-id="a214b-114">A parancsmag frissíti a "test-selfhost-ir" nevű önkiszolgáló integrációs futásiidőt.</span><span class="sxs-lookup"><span data-stu-id="a214b-114">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="a214b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a214b-115">PARAMETERS</span></span>

### <span data-ttu-id="a214b-116">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="a214b-116">-AutoUpdate</span></span>
<span data-ttu-id="a214b-117">Az önkiszolgáló integrációs futásidejű automatikus frissítés engedélyezése vagy letiltása.</span><span class="sxs-lookup"><span data-stu-id="a214b-117">Enable or disable the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: On, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a214b-118">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="a214b-118">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="a214b-119">Az önkiszolgáló integrációs futásidejű automatikus frissítés napának ideje.</span><span class="sxs-lookup"><span data-stu-id="a214b-119">The time of the day for the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a214b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a214b-120">-DefaultProfile</span></span>
<span data-ttu-id="a214b-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a214b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a214b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a214b-122">-InputObject</span></span>
<span data-ttu-id="a214b-123">Az integráció futásidejű objektuma.</span><span class="sxs-lookup"><span data-stu-id="a214b-123">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a214b-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="a214b-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="a214b-125">Az integráció futásidejű neve.</span><span class="sxs-lookup"><span data-stu-id="a214b-125">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a214b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a214b-126">-ResourceGroupName</span></span>
<span data-ttu-id="a214b-127">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a214b-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a214b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a214b-128">-ResourceId</span></span>
<span data-ttu-id="a214b-129">A Synapse-integráció futásideje erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a214b-129">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a214b-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a214b-130">-WorkspaceName</span></span>
<span data-ttu-id="a214b-131">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="a214b-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a214b-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a214b-132">-WorkspaceObject</span></span>
<span data-ttu-id="a214b-133">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="a214b-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a214b-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a214b-134">-Confirm</span></span>
<span data-ttu-id="a214b-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a214b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a214b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a214b-136">-WhatIf</span></span>
<span data-ttu-id="a214b-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a214b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a214b-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a214b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a214b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a214b-139">CommonParameters</span></span>
<span data-ttu-id="a214b-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a214b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a214b-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a214b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a214b-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a214b-142">INPUTS</span></span>

### <span data-ttu-id="a214b-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a214b-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a214b-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a214b-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="a214b-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a214b-145">OUTPUTS</span></span>

### <span data-ttu-id="a214b-146">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="a214b-146">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="a214b-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a214b-147">NOTES</span></span>

## <span data-ttu-id="a214b-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a214b-148">RELATED LINKS</span></span>
