---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 31647da87319ca6be90962f34d128f5e2c922d47
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025048"
---
# <span data-ttu-id="a224b-101">Update-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a224b-101">Update-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="a224b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a224b-102">SYNOPSIS</span></span>
<span data-ttu-id="a224b-103">Az integrációs futtatókörnyezet frissítése</span><span class="sxs-lookup"><span data-stu-id="a224b-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="a224b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a224b-104">SYNTAX</span></span>

### <span data-ttu-id="a224b-105">UpdateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a224b-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a224b-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a224b-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a224b-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a224b-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -ResourceId <String> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a224b-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a224b-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a224b-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="a224b-109">DESCRIPTION</span></span>
<span data-ttu-id="a224b-110">Az **Update-AzSynapseIntegrationRuntime** parancsmag frissíti az integrációs futtatókörnyezet tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="a224b-110">The **Update-AzSynapseIntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="a224b-111">Jelenleg a parancsmag csak az "AutoUpdate" és a "AutoUpdateDelayOffset" frissítést támogatja az önálló integrációs futtatókörnyezethez.</span><span class="sxs-lookup"><span data-stu-id="a224b-111">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="a224b-112">Példák</span><span class="sxs-lookup"><span data-stu-id="a224b-112">EXAMPLES</span></span>

### <span data-ttu-id="a224b-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a224b-113">Example 1</span></span>
```powershell
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -AutoUpdate Off -AutoUpdateDelayOffset $ts
```

<span data-ttu-id="a224b-114">A parancsmag a "teszt-selfhost-IR" nevű önálló integrációs futtatókörnyezetet frissíti.</span><span class="sxs-lookup"><span data-stu-id="a224b-114">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="a224b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a224b-115">PARAMETERS</span></span>

### <span data-ttu-id="a224b-116">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="a224b-116">-AutoUpdate</span></span>
<span data-ttu-id="a224b-117">Engedélyezze vagy tiltsa le az önkiszolgáló integrációs futtatókörnyezet automatikus frissítését.</span><span class="sxs-lookup"><span data-stu-id="a224b-117">Enable or disable the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="a224b-118">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="a224b-118">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="a224b-119">Az önkiszolgáló integrációs futtatókörnyezet automatikus frissítése napjának időpontja.</span><span class="sxs-lookup"><span data-stu-id="a224b-119">The time of the day for the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="a224b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a224b-120">-DefaultProfile</span></span>
<span data-ttu-id="a224b-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a224b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a224b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a224b-122">-InputObject</span></span>
<span data-ttu-id="a224b-123">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="a224b-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="a224b-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="a224b-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="a224b-125">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="a224b-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="a224b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a224b-126">-ResourceGroupName</span></span>
<span data-ttu-id="a224b-127">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="a224b-127">Resource group name.</span></span>

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

### <span data-ttu-id="a224b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a224b-128">-ResourceId</span></span>
<span data-ttu-id="a224b-129">A szinapszis-integrációs futtatókörnyezet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a224b-129">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="a224b-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a224b-130">-WorkspaceName</span></span>
<span data-ttu-id="a224b-131">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="a224b-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a224b-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a224b-132">-WorkspaceObject</span></span>
<span data-ttu-id="a224b-133">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="a224b-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a224b-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a224b-134">-Confirm</span></span>
<span data-ttu-id="a224b-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a224b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a224b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a224b-136">-WhatIf</span></span>
<span data-ttu-id="a224b-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a224b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a224b-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a224b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a224b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a224b-139">CommonParameters</span></span>
<span data-ttu-id="a224b-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a224b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a224b-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a224b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a224b-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a224b-142">INPUTS</span></span>

### <span data-ttu-id="a224b-143">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a224b-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a224b-144">Microsoft. Azure. commands. szinapszis. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a224b-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="a224b-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a224b-145">OUTPUTS</span></span>

### <span data-ttu-id="a224b-146">Microsoft. Azure. commands. szinapszis. models. PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="a224b-146">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="a224b-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a224b-147">NOTES</span></span>

## <span data-ttu-id="a224b-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a224b-148">RELATED LINKS</span></span>
