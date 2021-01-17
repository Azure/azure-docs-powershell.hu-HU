---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
ms.openlocfilehash: 4e35814be14c2be3b5ba0fd1ca5960d297590dca
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327413"
---
# <span data-ttu-id="6d9e9-101">Stop-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="6d9e9-101">Stop-AzSynapseTrigger</span></span>

## <span data-ttu-id="6d9e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d9e9-102">SYNOPSIS</span></span>
<span data-ttu-id="6d9e9-103">Leállít egy eseményindítót egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="6d9e9-103">Stops a trigger in a workspace.</span></span>

## <span data-ttu-id="6d9e9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6d9e9-104">SYNTAX</span></span>

### <span data-ttu-id="6d9e9-105">StopByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6d9e9-105">StopByName (Default)</span></span>
```
Stop-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d9e9-106">StopByObject</span><span class="sxs-lookup"><span data-stu-id="6d9e9-106">StopByObject</span></span>
```
Stop-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d9e9-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="6d9e9-107">StopByInputObject</span></span>
```
Stop-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d9e9-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6d9e9-108">DESCRIPTION</span></span>
<span data-ttu-id="6d9e9-109">A **Stop-AzSynapseTrigger** parancsmag leállít egy eseményindítót egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="6d9e9-109">The **Stop-AzSynapseTrigger** cmdlet stops a trigger in a workspace.</span></span> <span data-ttu-id="6d9e9-110">Ha az eseményindító "Elindítva" állapotban van, a parancsmag leállítja az eseményindítót, és a továbbiakban nem indítja el a folyamatokat.</span><span class="sxs-lookup"><span data-stu-id="6d9e9-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="6d9e9-111">Ha az eseményindító már "Leállítva" állapotban van, ennek a parancsmagnak nincs hatása.</span><span class="sxs-lookup"><span data-stu-id="6d9e9-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="6d9e9-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6d9e9-112">EXAMPLES</span></span>

### <span data-ttu-id="6d9e9-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="6d9e9-113">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="6d9e9-114">Leállítja a ContosoTrigger nevű eseményindítót a ContosoWorkspace munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="6d9e9-114">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="6d9e9-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="6d9e9-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="6d9e9-116">A ContosoTrigger nevű eseményindítót leállítja a munkaterületEn a ContosoWorkspace folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="6d9e9-116">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="6d9e9-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="6d9e9-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Stop-AzSynapseTrigger
```

<span data-ttu-id="6d9e9-118">Állítsa le a ContosoTrigger nevű eseményindítót a Munkaterület ContosoWorkspace-folyamatán keresztül.</span><span class="sxs-lookup"><span data-stu-id="6d9e9-118">Stop a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="6d9e9-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d9e9-119">PARAMETERS</span></span>

### <span data-ttu-id="6d9e9-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d9e9-120">-AsJob</span></span>
<span data-ttu-id="6d9e9-121">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6d9e9-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d9e9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d9e9-122">-DefaultProfile</span></span>
<span data-ttu-id="6d9e9-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6d9e9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d9e9-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d9e9-124">-InputObject</span></span>
<span data-ttu-id="6d9e9-125">Az eseményindító objektum.</span><span class="sxs-lookup"><span data-stu-id="6d9e9-125">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d9e9-126">-Name</span><span class="sxs-lookup"><span data-stu-id="6d9e9-126">-Name</span></span>
<span data-ttu-id="6d9e9-127">Az eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="6d9e9-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByName, StopByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d9e9-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d9e9-128">-PassThru</span></span>
<span data-ttu-id="6d9e9-129">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="6d9e9-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="6d9e9-130">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="6d9e9-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="6d9e9-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6d9e9-131">-WorkspaceName</span></span>
<span data-ttu-id="6d9e9-132">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="6d9e9-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d9e9-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6d9e9-133">-WorkspaceObject</span></span>
<span data-ttu-id="6d9e9-134">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="6d9e9-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StopByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d9e9-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d9e9-135">-Confirm</span></span>
<span data-ttu-id="6d9e9-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6d9e9-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d9e9-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d9e9-137">-WhatIf</span></span>
<span data-ttu-id="6d9e9-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6d9e9-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6d9e9-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6d9e9-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d9e9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d9e9-140">CommonParameters</span></span>
<span data-ttu-id="6d9e9-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d9e9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d9e9-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d9e9-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d9e9-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6d9e9-143">INPUTS</span></span>

### <span data-ttu-id="6d9e9-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6d9e9-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6d9e9-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="6d9e9-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="6d9e9-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d9e9-146">OUTPUTS</span></span>

### <span data-ttu-id="6d9e9-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6d9e9-147">System.Boolean</span></span>

## <span data-ttu-id="6d9e9-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6d9e9-148">NOTES</span></span>

## <span data-ttu-id="6d9e9-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6d9e9-149">RELATED LINKS</span></span>
