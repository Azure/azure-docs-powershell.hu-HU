---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/sync-azsynapseintegrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
ms.openlocfilehash: d183506538bb2063a21eaf33df088ba613a2d3ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011269"
---
# <span data-ttu-id="e1173-101">Sync-AzSynapseIntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="e1173-101">Sync-AzSynapseIntegrationRuntimeCredential</span></span>

## <span data-ttu-id="e1173-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1173-102">SYNOPSIS</span></span>
<span data-ttu-id="e1173-103">Szinkronizálja a hitelesítő adatokat az integrációs futásidejű csomópontok között.</span><span class="sxs-lookup"><span data-stu-id="e1173-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="e1173-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e1173-104">SYNTAX</span></span>

### <span data-ttu-id="e1173-105">StopByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e1173-105">StopByNameParameterSet (Default)</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1173-106">StopByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1173-106">StopByParentObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -IntegrationRuntimeName <String>
 -WorkspaceObject <PSSynapseWorkspace> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1173-107">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1173-107">StopByResourceIdParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -ResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1173-108">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1173-108">StopByInputObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1173-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e1173-109">DESCRIPTION</span></span>
<span data-ttu-id="e1173-110">A **Sync-AzSynapseIntegrationRuntimeCredential** parancsmag szinkronizálja a helyszíni hitelesítő adatokat az integrációs futásidejű csomópontok között, így a hitelesítő adatoknak minden csomópontban azonosnak kell lenniük.</span><span class="sxs-lookup"><span data-stu-id="e1173-110">The **Sync-AzSynapseIntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="e1173-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e1173-111">EXAMPLES</span></span>

### <span data-ttu-id="e1173-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="e1173-112">Example 1</span></span>
```powershell
PS C:\> Sync-AzSynapseIntegrationRuntimeCredential -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir'
```

<span data-ttu-id="e1173-113">Szinkronizálja a hitelesítő adatokat az integrációs futásidejű csomópontok között.</span><span class="sxs-lookup"><span data-stu-id="e1173-113">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="e1173-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1173-114">PARAMETERS</span></span>

### <span data-ttu-id="e1173-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1173-115">-DefaultProfile</span></span>
<span data-ttu-id="e1173-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e1173-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1173-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e1173-117">-Force</span></span>
<span data-ttu-id="e1173-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e1173-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e1173-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1173-119">-InputObject</span></span>
<span data-ttu-id="e1173-120">Az integráció futásidejű objektuma.</span><span class="sxs-lookup"><span data-stu-id="e1173-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: StopByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1173-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="e1173-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="e1173-122">Az integráció futásidejű neve.</span><span class="sxs-lookup"><span data-stu-id="e1173-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet, StopByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1173-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1173-123">-ResourceGroupName</span></span>
<span data-ttu-id="e1173-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e1173-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1173-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1173-125">-ResourceId</span></span>
<span data-ttu-id="e1173-126">A Synapse-integráció futásideje erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e1173-126">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1173-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e1173-127">-WorkspaceName</span></span>
<span data-ttu-id="e1173-128">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="e1173-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1173-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e1173-129">-WorkspaceObject</span></span>
<span data-ttu-id="e1173-130">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="e1173-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StopByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1173-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1173-131">-Confirm</span></span>
<span data-ttu-id="e1173-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e1173-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1173-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1173-133">-WhatIf</span></span>
<span data-ttu-id="e1173-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e1173-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1173-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e1173-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1173-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1173-136">CommonParameters</span></span>
<span data-ttu-id="e1173-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1173-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1173-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1173-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1173-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e1173-139">INPUTS</span></span>

### <span data-ttu-id="e1173-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e1173-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e1173-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e1173-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="e1173-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1173-142">OUTPUTS</span></span>

### <span data-ttu-id="e1173-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="e1173-143">System.Void</span></span>

## <span data-ttu-id="e1173-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e1173-144">NOTES</span></span>

## <span data-ttu-id="e1173-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1173-145">RELATED LINKS</span></span>
