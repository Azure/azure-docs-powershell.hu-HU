---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 57b6c6619a45e515c7aff2e30edc346ff39af9ac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025623"
---
# <span data-ttu-id="da8ca-101">Remove-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="da8ca-101">Remove-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="da8ca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="da8ca-102">SYNOPSIS</span></span>
<span data-ttu-id="da8ca-103">Az integrációs futtatókörnyezet eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="da8ca-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="da8ca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="da8ca-104">SYNTAX</span></span>

### <span data-ttu-id="da8ca-105">RemoveByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="da8ca-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da8ca-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="da8ca-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da8ca-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="da8ca-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -ResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da8ca-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="da8ca-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da8ca-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="da8ca-109">DESCRIPTION</span></span>
<span data-ttu-id="da8ca-110">A **Remove-AzSynapseIntegrationRuntime** parancsmag az integrációs futtatókörnyezetet távolítja el.</span><span class="sxs-lookup"><span data-stu-id="da8ca-110">The **Remove-AzSynapseIntegrationRuntime** cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="da8ca-111">Példák</span><span class="sxs-lookup"><span data-stu-id="da8ca-111">EXAMPLES</span></span>

### <span data-ttu-id="da8ca-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="da8ca-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="da8ca-113">Ez a parancs eltávolítja a ContosoWorkspace nevű munkaterületről a ' teszt-fenntartva-IR ' nevű integrációs futtatókörnyezetet.</span><span class="sxs-lookup"><span data-stu-id="da8ca-113">This command removes the integration runtime named 'test-reserved-ir' from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="da8ca-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="da8ca-114">PARAMETERS</span></span>

### <span data-ttu-id="da8ca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da8ca-115">-DefaultProfile</span></span>
<span data-ttu-id="da8ca-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da8ca-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da8ca-117">-Force</span><span class="sxs-lookup"><span data-stu-id="da8ca-117">-Force</span></span>
<span data-ttu-id="da8ca-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="da8ca-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="da8ca-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da8ca-119">-InputObject</span></span>
<span data-ttu-id="da8ca-120">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="da8ca-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="da8ca-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="da8ca-121">-Name</span></span>
<span data-ttu-id="da8ca-122">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="da8ca-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da8ca-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da8ca-123">-ResourceGroupName</span></span>
<span data-ttu-id="da8ca-124">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="da8ca-124">Resource group name.</span></span>

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

### <span data-ttu-id="da8ca-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da8ca-125">-ResourceId</span></span>
<span data-ttu-id="da8ca-126">A szinapszis-integrációs futtatókörnyezet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="da8ca-126">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="da8ca-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="da8ca-127">-WorkspaceName</span></span>
<span data-ttu-id="da8ca-128">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="da8ca-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="da8ca-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="da8ca-129">-WorkspaceObject</span></span>
<span data-ttu-id="da8ca-130">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="da8ca-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="da8ca-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="da8ca-131">-Confirm</span></span>
<span data-ttu-id="da8ca-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="da8ca-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da8ca-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da8ca-133">-WhatIf</span></span>
<span data-ttu-id="da8ca-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="da8ca-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da8ca-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="da8ca-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da8ca-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da8ca-136">CommonParameters</span></span>
<span data-ttu-id="da8ca-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="da8ca-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da8ca-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="da8ca-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da8ca-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="da8ca-139">INPUTS</span></span>

### <span data-ttu-id="da8ca-140">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="da8ca-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="da8ca-141">Microsoft. Azure. commands. szinapszis. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="da8ca-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="da8ca-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da8ca-142">OUTPUTS</span></span>

### <span data-ttu-id="da8ca-143">System. Void</span><span class="sxs-lookup"><span data-stu-id="da8ca-143">System.Void</span></span>

## <span data-ttu-id="da8ca-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="da8ca-144">NOTES</span></span>

## <span data-ttu-id="da8ca-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da8ca-145">RELATED LINKS</span></span>
