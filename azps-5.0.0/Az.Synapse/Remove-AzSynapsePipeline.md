---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
ms.openlocfilehash: f28abbca41c68ce08e516fb52f69b7de8c54e67a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187926"
---
# <span data-ttu-id="3c482-101">Remove-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="3c482-101">Remove-AzSynapsePipeline</span></span>

## <span data-ttu-id="3c482-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3c482-102">SYNOPSIS</span></span>
<span data-ttu-id="3c482-103">Csővezeték eltávolítása a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="3c482-103">Removes a pipeline from workspace.</span></span>

## <span data-ttu-id="3c482-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3c482-104">SYNTAX</span></span>

### <span data-ttu-id="3c482-105">RemoveByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3c482-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapsePipeline -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c482-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="3c482-106">RemoveByObject</span></span>
```
Remove-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c482-107">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="3c482-107">NewByInputObject</span></span>
```
Remove-AzSynapsePipeline -Name <String> -InputObject <PSPipelineResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c482-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3c482-108">DESCRIPTION</span></span>
<span data-ttu-id="3c482-109">A **Remove-AzSynapsePipeline** parancsmag eltávolítja a munkaterületről a csővezetéket.</span><span class="sxs-lookup"><span data-stu-id="3c482-109">The **Remove-AzSynapsePipeline** cmdlet removes a pipeline from workspace.</span></span>

## <span data-ttu-id="3c482-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3c482-110">EXAMPLES</span></span>

### <span data-ttu-id="3c482-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3c482-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="3c482-112">Ez a parancsmag eltávolítja a ContosoPipeline nevű csővezetéket a ContosoWorkspace nevű munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="3c482-112">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="3c482-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="3c482-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="3c482-114">Ez a parancsmag eltávolítja a ContosoPipeline nevű csővezetéket a ContosoWorkspace-től a csővezetéken keresztül nevű munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="3c482-114">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="3c482-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="3c482-115">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Remove-AzSynapsePipeline
```

<span data-ttu-id="3c482-116">Ez a parancsmag eltávolítja a ContosoPipeline nevű csővezetéket a ContosoWorkspace-től a csővezetéken keresztül nevű munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="3c482-116">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="3c482-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3c482-117">PARAMETERS</span></span>

### <span data-ttu-id="3c482-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c482-118">-AsJob</span></span>
<span data-ttu-id="3c482-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3c482-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c482-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c482-120">-DefaultProfile</span></span>
<span data-ttu-id="3c482-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3c482-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c482-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c482-122">-InputObject</span></span>
<span data-ttu-id="3c482-123">A csővezeték-objektum.</span><span class="sxs-lookup"><span data-stu-id="3c482-123">The pipeline object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource
Parameter Sets: NewByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c482-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3c482-124">-Name</span></span>
<span data-ttu-id="3c482-125">A csővezeték neve.</span><span class="sxs-lookup"><span data-stu-id="3c482-125">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c482-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c482-126">-PassThru</span></span>
<span data-ttu-id="3c482-127">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="3c482-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="3c482-128">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="3c482-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="3c482-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3c482-129">-WorkspaceName</span></span>
<span data-ttu-id="3c482-130">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="3c482-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c482-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3c482-131">-WorkspaceObject</span></span>
<span data-ttu-id="3c482-132">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="3c482-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c482-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3c482-133">-Confirm</span></span>
<span data-ttu-id="3c482-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3c482-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c482-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c482-135">-WhatIf</span></span>
<span data-ttu-id="3c482-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3c482-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c482-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3c482-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c482-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c482-138">CommonParameters</span></span>
<span data-ttu-id="3c482-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3c482-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c482-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3c482-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c482-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c482-141">INPUTS</span></span>

### <span data-ttu-id="3c482-142">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3c482-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="3c482-143">Microsoft. Azure. commands. szinapszis. models. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="3c482-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="3c482-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c482-144">OUTPUTS</span></span>

### <span data-ttu-id="3c482-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3c482-145">System.Boolean</span></span>

## <span data-ttu-id="3c482-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3c482-146">NOTES</span></span>

## <span data-ttu-id="3c482-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c482-147">RELATED LINKS</span></span>
