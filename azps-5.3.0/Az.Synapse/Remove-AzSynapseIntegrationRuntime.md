---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 57b6c6619a45e515c7aff2e30edc346ff39af9ac
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383486"
---
# <span data-ttu-id="d26cd-101">Remove-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d26cd-101">Remove-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="d26cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d26cd-102">SYNOPSIS</span></span>
<span data-ttu-id="d26cd-103">Eltávolítja az integrációs futásiidőt.</span><span class="sxs-lookup"><span data-stu-id="d26cd-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="d26cd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d26cd-104">SYNTAX</span></span>

### <span data-ttu-id="d26cd-105">RemoveByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d26cd-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d26cd-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d26cd-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d26cd-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d26cd-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -ResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d26cd-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d26cd-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d26cd-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d26cd-109">DESCRIPTION</span></span>
<span data-ttu-id="d26cd-110">A **Remove-AzSynapseIntegrationRuntime parancsmag** eltávolítja az integrációs futásiidőt.</span><span class="sxs-lookup"><span data-stu-id="d26cd-110">The **Remove-AzSynapseIntegrationRuntime** cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="d26cd-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d26cd-111">EXAMPLES</span></span>

### <span data-ttu-id="d26cd-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="d26cd-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="d26cd-113">Ez a parancs eltávolítja a "test-reserved-ir" nevű integrációs futásiidőt a ContosoWorkspace nevű munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="d26cd-113">This command removes the integration runtime named 'test-reserved-ir' from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="d26cd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d26cd-114">PARAMETERS</span></span>

### <span data-ttu-id="d26cd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d26cd-115">-DefaultProfile</span></span>
<span data-ttu-id="d26cd-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d26cd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d26cd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d26cd-117">-Force</span></span>
<span data-ttu-id="d26cd-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d26cd-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="d26cd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d26cd-119">-InputObject</span></span>
<span data-ttu-id="d26cd-120">Az integráció futásidejű objektuma.</span><span class="sxs-lookup"><span data-stu-id="d26cd-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="d26cd-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d26cd-121">-Name</span></span>
<span data-ttu-id="d26cd-122">Az integráció futásidejű neve.</span><span class="sxs-lookup"><span data-stu-id="d26cd-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="d26cd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d26cd-123">-ResourceGroupName</span></span>
<span data-ttu-id="d26cd-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d26cd-124">Resource group name.</span></span>

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

### <span data-ttu-id="d26cd-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d26cd-125">-ResourceId</span></span>
<span data-ttu-id="d26cd-126">A Synapse-integráció futásideje erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d26cd-126">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="d26cd-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d26cd-127">-WorkspaceName</span></span>
<span data-ttu-id="d26cd-128">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="d26cd-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d26cd-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d26cd-129">-WorkspaceObject</span></span>
<span data-ttu-id="d26cd-130">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="d26cd-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d26cd-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d26cd-131">-Confirm</span></span>
<span data-ttu-id="d26cd-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d26cd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d26cd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d26cd-133">-WhatIf</span></span>
<span data-ttu-id="d26cd-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d26cd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d26cd-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d26cd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d26cd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d26cd-136">CommonParameters</span></span>
<span data-ttu-id="d26cd-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d26cd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d26cd-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d26cd-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d26cd-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d26cd-139">INPUTS</span></span>

### <span data-ttu-id="d26cd-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d26cd-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d26cd-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d26cd-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="d26cd-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d26cd-142">OUTPUTS</span></span>

### <span data-ttu-id="d26cd-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="d26cd-143">System.Void</span></span>

## <span data-ttu-id="d26cd-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d26cd-144">NOTES</span></span>

## <span data-ttu-id="d26cd-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d26cd-145">RELATED LINKS</span></span>
