---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/start-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
ms.openlocfilehash: d2488a99bba1813c192df5ef8561d83c06f2f6e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164546"
---
# <span data-ttu-id="483a8-101">Start-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="483a8-101">Start-AzSynapseTrigger</span></span>

## <span data-ttu-id="483a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="483a8-102">SYNOPSIS</span></span>
<span data-ttu-id="483a8-103">Elindít egy eseményindítót egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="483a8-103">Starts a trigger in a workspace.</span></span>

## <span data-ttu-id="483a8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="483a8-104">SYNTAX</span></span>

### <span data-ttu-id="483a8-105">StartByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="483a8-105">StartByName (Default)</span></span>
```
Start-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="483a8-106">StartByObject</span><span class="sxs-lookup"><span data-stu-id="483a8-106">StartByObject</span></span>
```
Start-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="483a8-107">StartByInputObject</span><span class="sxs-lookup"><span data-stu-id="483a8-107">StartByInputObject</span></span>
```
Start-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="483a8-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="483a8-108">DESCRIPTION</span></span>
<span data-ttu-id="483a8-109">A **Start-AzSynapseTrigger** parancsmag elindít egy eseményindítót egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="483a8-109">The **Start-AzSynapseTrigger** cmdlet starts a trigger in a workspace.</span></span> <span data-ttu-id="483a8-110">Ha az eseményindító "Leállítva" állapotban van, a parancsmag elindítja az eseményindítót, és végül a definíciója alapján meghívja a prognózisokat.</span><span class="sxs-lookup"><span data-stu-id="483a8-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="483a8-111">Ha az eseményindító már "Elindítva" állapotban van, ennek a parancsmagnak nincs hatása.</span><span class="sxs-lookup"><span data-stu-id="483a8-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="483a8-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="483a8-112">EXAMPLES</span></span>

### <span data-ttu-id="483a8-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="483a8-113">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="483a8-114">Elindít egy ContosoTrigger nevű eseményindítót a ContosoWorkspace munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="483a8-114">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="483a8-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="483a8-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Start-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="483a8-116">Elindít egy ContosoTrigger nevű eseményindítót a ContosoWorkspace munkaterületen egy folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="483a8-116">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="483a8-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="483a8-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Start-AzSynapseTrigger
```

<span data-ttu-id="483a8-118">Elindít egy ContosoTrigger nevű eseményindítót a ContosoWorkspace munkaterületen egy folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="483a8-118">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="483a8-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="483a8-119">PARAMETERS</span></span>

### <span data-ttu-id="483a8-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="483a8-120">-AsJob</span></span>
<span data-ttu-id="483a8-121">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="483a8-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="483a8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="483a8-122">-DefaultProfile</span></span>
<span data-ttu-id="483a8-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="483a8-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="483a8-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="483a8-124">-InputObject</span></span>
<span data-ttu-id="483a8-125">Az eseményindító objektum.</span><span class="sxs-lookup"><span data-stu-id="483a8-125">The trigger object.</span></span>

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

### <span data-ttu-id="483a8-126">-Name</span><span class="sxs-lookup"><span data-stu-id="483a8-126">-Name</span></span>
<span data-ttu-id="483a8-127">Az eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="483a8-127">The trigger name.</span></span>

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

### <span data-ttu-id="483a8-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="483a8-128">-PassThru</span></span>
<span data-ttu-id="483a8-129">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="483a8-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="483a8-130">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="483a8-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="483a8-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="483a8-131">-WorkspaceName</span></span>
<span data-ttu-id="483a8-132">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="483a8-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="483a8-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="483a8-133">-WorkspaceObject</span></span>
<span data-ttu-id="483a8-134">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="483a8-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="483a8-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="483a8-135">-Confirm</span></span>
<span data-ttu-id="483a8-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="483a8-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="483a8-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="483a8-137">-WhatIf</span></span>
<span data-ttu-id="483a8-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="483a8-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="483a8-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="483a8-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="483a8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="483a8-140">CommonParameters</span></span>
<span data-ttu-id="483a8-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="483a8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="483a8-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="483a8-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="483a8-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="483a8-143">INPUTS</span></span>

### <span data-ttu-id="483a8-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="483a8-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="483a8-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="483a8-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="483a8-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="483a8-146">OUTPUTS</span></span>

### <span data-ttu-id="483a8-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="483a8-147">System.Boolean</span></span>

## <span data-ttu-id="483a8-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="483a8-148">NOTES</span></span>

## <span data-ttu-id="483a8-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="483a8-149">RELATED LINKS</span></span>
