---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/start-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
ms.openlocfilehash: 39801db0d1cd400fa88868b87098260c9148daa3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939162"
---
# <span data-ttu-id="5bd1e-101">Start-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="5bd1e-101">Start-AzSynapseTrigger</span></span>

## <span data-ttu-id="5bd1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bd1e-102">SYNOPSIS</span></span>
<span data-ttu-id="5bd1e-103">Elindít egy eseményindítót egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="5bd1e-103">Starts a trigger in a workspace.</span></span>

## <span data-ttu-id="5bd1e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5bd1e-104">SYNTAX</span></span>

### <span data-ttu-id="5bd1e-105">StartByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5bd1e-105">StartByName (Default)</span></span>
```
Start-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bd1e-106">StartByObject</span><span class="sxs-lookup"><span data-stu-id="5bd1e-106">StartByObject</span></span>
```
Start-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bd1e-107">StartByInputObject</span><span class="sxs-lookup"><span data-stu-id="5bd1e-107">StartByInputObject</span></span>
```
Start-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bd1e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5bd1e-108">DESCRIPTION</span></span>
<span data-ttu-id="5bd1e-109">A **Start-AzSynapseTrigger** parancsmag elindít egy eseményindítót egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="5bd1e-109">The **Start-AzSynapseTrigger** cmdlet starts a trigger in a workspace.</span></span> <span data-ttu-id="5bd1e-110">Ha az eseményindító "Leállítva" állapotban van, a parancsmag elindítja az eseményindítót, és végül a definíciója alapján meghívja a prognózisokat.</span><span class="sxs-lookup"><span data-stu-id="5bd1e-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="5bd1e-111">Ha az eseményindító már "Elindítva" állapotban van, ennek a parancsmagnak nincs hatása.</span><span class="sxs-lookup"><span data-stu-id="5bd1e-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="5bd1e-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5bd1e-112">EXAMPLES</span></span>

### <span data-ttu-id="5bd1e-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="5bd1e-113">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="5bd1e-114">Elindít egy ContosoTrigger nevű eseményindítót a ContosoWorkspace munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="5bd1e-114">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="5bd1e-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="5bd1e-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Start-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="5bd1e-116">Elindít egy ContosoTrigger nevű eseményindítót a contosoworkspace-munkaterületen egy folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="5bd1e-116">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="5bd1e-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="5bd1e-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Start-AzSynapseTrigger
```

<span data-ttu-id="5bd1e-118">Elindít egy ContosoTrigger nevű eseményindítót a contosoworkspace-munkaterületen egy folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="5bd1e-118">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="5bd1e-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bd1e-119">PARAMETERS</span></span>

### <span data-ttu-id="5bd1e-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5bd1e-120">-AsJob</span></span>
<span data-ttu-id="5bd1e-121">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="5bd1e-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5bd1e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bd1e-122">-DefaultProfile</span></span>
<span data-ttu-id="5bd1e-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5bd1e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bd1e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5bd1e-124">-InputObject</span></span>
<span data-ttu-id="5bd1e-125">Az eseményindító objektum.</span><span class="sxs-lookup"><span data-stu-id="5bd1e-125">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: StartByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bd1e-126">-Name</span><span class="sxs-lookup"><span data-stu-id="5bd1e-126">-Name</span></span>
<span data-ttu-id="5bd1e-127">Az eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="5bd1e-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: StartByName, StartByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd1e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5bd1e-128">-PassThru</span></span>
<span data-ttu-id="5bd1e-129">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="5bd1e-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="5bd1e-130">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="5bd1e-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="5bd1e-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5bd1e-131">-WorkspaceName</span></span>
<span data-ttu-id="5bd1e-132">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="5bd1e-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd1e-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5bd1e-133">-WorkspaceObject</span></span>
<span data-ttu-id="5bd1e-134">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="5bd1e-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StartByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bd1e-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5bd1e-135">-Confirm</span></span>
<span data-ttu-id="5bd1e-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5bd1e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bd1e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bd1e-137">-WhatIf</span></span>
<span data-ttu-id="5bd1e-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5bd1e-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5bd1e-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5bd1e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bd1e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bd1e-140">CommonParameters</span></span>
<span data-ttu-id="5bd1e-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bd1e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bd1e-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5bd1e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bd1e-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5bd1e-143">INPUTS</span></span>

### <span data-ttu-id="5bd1e-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5bd1e-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="5bd1e-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="5bd1e-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="5bd1e-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5bd1e-146">OUTPUTS</span></span>

### <span data-ttu-id="5bd1e-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5bd1e-147">System.Boolean</span></span>

## <span data-ttu-id="5bd1e-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5bd1e-148">NOTES</span></span>

## <span data-ttu-id="5bd1e-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5bd1e-149">RELATED LINKS</span></span>
