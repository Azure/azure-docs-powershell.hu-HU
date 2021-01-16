---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/sync-azsynapseintegrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
ms.openlocfilehash: feb9d74cf49dfa8ae5455b303ee78f443a08e942
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357110"
---
# <span data-ttu-id="b9852-101">Sync-AzSynapseIntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="b9852-101">Sync-AzSynapseIntegrationRuntimeCredential</span></span>

## <span data-ttu-id="b9852-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9852-102">SYNOPSIS</span></span>
<span data-ttu-id="b9852-103">Szinkronizálja a hitelesítő adatokat az integrációs futásidejű csomópontok között.</span><span class="sxs-lookup"><span data-stu-id="b9852-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="b9852-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b9852-104">SYNTAX</span></span>

### <span data-ttu-id="b9852-105">StopByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b9852-105">StopByNameParameterSet (Default)</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b9852-106">StopByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9852-106">StopByParentObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -IntegrationRuntimeName <String>
 -WorkspaceObject <PSSynapseWorkspace> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b9852-107">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9852-107">StopByResourceIdParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -ResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9852-108">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9852-108">StopByInputObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9852-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b9852-109">DESCRIPTION</span></span>
<span data-ttu-id="b9852-110">A **Sync-AzSynapseIntegrationRuntimeCredential** parancsmag szinkronizálja a helyszíni hitelesítő adatokat az integrációs futásidejű csomópontok között, így a hitelesítő adatoknak minden csomópontban azonosnak kell lenniük.</span><span class="sxs-lookup"><span data-stu-id="b9852-110">The **Sync-AzSynapseIntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="b9852-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b9852-111">EXAMPLES</span></span>

### <span data-ttu-id="b9852-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="b9852-112">Example 1</span></span>
```powershell
PS C:\> Sync-AzSynapseIntegrationRuntimeCredential -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir'
```

<span data-ttu-id="b9852-113">Szinkronizálja a hitelesítő adatokat az integrációs futásidejű csomópontok között.</span><span class="sxs-lookup"><span data-stu-id="b9852-113">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="b9852-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9852-114">PARAMETERS</span></span>

### <span data-ttu-id="b9852-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9852-115">-DefaultProfile</span></span>
<span data-ttu-id="b9852-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b9852-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9852-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b9852-117">-Force</span></span>
<span data-ttu-id="b9852-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b9852-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="b9852-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9852-119">-InputObject</span></span>
<span data-ttu-id="b9852-120">Az integráció futásidejű objektuma.</span><span class="sxs-lookup"><span data-stu-id="b9852-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="b9852-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="b9852-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="b9852-122">Az integráció futásidejű neve.</span><span class="sxs-lookup"><span data-stu-id="b9852-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="b9852-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9852-123">-ResourceGroupName</span></span>
<span data-ttu-id="b9852-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b9852-124">Resource group name.</span></span>

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

### <span data-ttu-id="b9852-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9852-125">-ResourceId</span></span>
<span data-ttu-id="b9852-126">A Synapse-integráció futásideje erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b9852-126">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="b9852-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b9852-127">-WorkspaceName</span></span>
<span data-ttu-id="b9852-128">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="b9852-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b9852-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b9852-129">-WorkspaceObject</span></span>
<span data-ttu-id="b9852-130">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="b9852-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b9852-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9852-131">-Confirm</span></span>
<span data-ttu-id="b9852-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b9852-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9852-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9852-133">-WhatIf</span></span>
<span data-ttu-id="b9852-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b9852-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9852-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b9852-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9852-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9852-136">CommonParameters</span></span>
<span data-ttu-id="b9852-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9852-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9852-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9852-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9852-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b9852-139">INPUTS</span></span>

### <span data-ttu-id="b9852-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b9852-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="b9852-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b9852-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="b9852-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9852-142">OUTPUTS</span></span>

### <span data-ttu-id="b9852-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="b9852-143">System.Void</span></span>

## <span data-ttu-id="b9852-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b9852-144">NOTES</span></span>

## <span data-ttu-id="b9852-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9852-145">RELATED LINKS</span></span>
