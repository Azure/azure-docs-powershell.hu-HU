---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapseintegrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
ms.openlocfilehash: 59630bd0ffcf5bebfc68f647cff444466727a990
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180723"
---
# <span data-ttu-id="d9fab-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="d9fab-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="d9fab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d9fab-102">SYNOPSIS</span></span>
<span data-ttu-id="d9fab-103">Önkiszolgáló integrációs futtatókörnyezet frissítése</span><span class="sxs-lookup"><span data-stu-id="d9fab-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="d9fab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d9fab-104">SYNTAX</span></span>

### <span data-ttu-id="d9fab-105">InvokeByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d9fab-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9fab-106">InvokeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9fab-106">InvokeByParentObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9fab-107">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9fab-107">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9fab-108">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9fab-108">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9fab-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="d9fab-109">DESCRIPTION</span></span>
<span data-ttu-id="d9fab-110">A **meghívó-AzSynapseIntegrationRuntimeUpgrade** parancsmag az önálló integrációs futtatókörnyezetet frissíti, ha az új verzió elérhető.</span><span class="sxs-lookup"><span data-stu-id="d9fab-110">The **Invoke-AzSynapseIntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="d9fab-111">Példák</span><span class="sxs-lookup"><span data-stu-id="d9fab-111">EXAMPLES</span></span>

### <span data-ttu-id="d9fab-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d9fab-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapseIntegrationRuntimeUpgrade -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="d9fab-113">A parancsmag a "teszt-selfhost-IR" nevű önálló integrációs futtatókörnyezetet frissíti a munkaterület-ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="d9fab-113">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="d9fab-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d9fab-114">PARAMETERS</span></span>

### <span data-ttu-id="d9fab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9fab-115">-DefaultProfile</span></span>
<span data-ttu-id="d9fab-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d9fab-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9fab-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9fab-117">-InputObject</span></span>
<span data-ttu-id="d9fab-118">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="d9fab-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="d9fab-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d9fab-119">-Name</span></span>
<span data-ttu-id="d9fab-120">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="d9fab-120">The integration runtime name.</span></span>

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

### <span data-ttu-id="d9fab-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9fab-121">-ResourceGroupName</span></span>
<span data-ttu-id="d9fab-122">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d9fab-122">Resource group name.</span></span>

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

### <span data-ttu-id="d9fab-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9fab-123">-ResourceId</span></span>
<span data-ttu-id="d9fab-124">A szinapszis-integrációs futtatókörnyezet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d9fab-124">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="d9fab-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d9fab-125">-WorkspaceName</span></span>
<span data-ttu-id="d9fab-126">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="d9fab-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d9fab-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d9fab-127">-WorkspaceObject</span></span>
<span data-ttu-id="d9fab-128">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="d9fab-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d9fab-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d9fab-129">-Confirm</span></span>
<span data-ttu-id="d9fab-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d9fab-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9fab-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9fab-131">-WhatIf</span></span>
<span data-ttu-id="d9fab-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d9fab-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9fab-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d9fab-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9fab-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9fab-134">CommonParameters</span></span>
<span data-ttu-id="d9fab-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d9fab-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9fab-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d9fab-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9fab-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9fab-137">INPUTS</span></span>

### <span data-ttu-id="d9fab-138">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d9fab-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d9fab-139">Microsoft. Azure. commands. szinapszis. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d9fab-139">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="d9fab-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9fab-140">OUTPUTS</span></span>

### <span data-ttu-id="d9fab-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="d9fab-141">System.Void</span></span>

## <span data-ttu-id="d9fab-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d9fab-142">NOTES</span></span>

## <span data-ttu-id="d9fab-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d9fab-143">RELATED LINKS</span></span>
