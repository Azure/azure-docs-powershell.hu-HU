---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTrigger.md
ms.openlocfilehash: 648d215066fb7bd827d43ec9d063a7994ada82f8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149931"
---
# <span data-ttu-id="5bd1f-101">Remove-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="5bd1f-101">Remove-AzSynapseTrigger</span></span>

## <span data-ttu-id="5bd1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bd1f-102">SYNOPSIS</span></span>
<span data-ttu-id="5bd1f-103">Eltávolít egy eseményindítót egy munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-103">Removes a trigger from a workspace.</span></span>

## <span data-ttu-id="5bd1f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5bd1f-104">SYNTAX</span></span>

### <span data-ttu-id="5bd1f-105">RemoveByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5bd1f-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bd1f-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="5bd1f-106">RemoveByObject</span></span>
```
Remove-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bd1f-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="5bd1f-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bd1f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5bd1f-108">DESCRIPTION</span></span>
<span data-ttu-id="5bd1f-109">A **Remove-AzSynapseTrigger** parancsmag eltávolít egy eseményindítót a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-109">The **Remove-AzSynapseTrigger** cmdlet removes a trigger from a workspace.</span></span>

## <span data-ttu-id="5bd1f-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5bd1f-110">EXAMPLES</span></span>

### <span data-ttu-id="5bd1f-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="5bd1f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="5bd1f-112">Távolítsa el a ContosoTrigger nevű eseményindítót a ContosoWorkspace munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-112">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="5bd1f-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="5bd1f-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="5bd1f-114">Távolítsa el a ContosoTrigger nevű eseményindítót a ContosoWorkspace-munkaterületről a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-114">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="5bd1f-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="5bd1f-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTrigger
```

<span data-ttu-id="5bd1f-116">Távolítsa el a ContosoTrigger nevű eseményindítót a ContosoWorkspace-munkaterületről a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-116">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="5bd1f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bd1f-117">PARAMETERS</span></span>

### <span data-ttu-id="5bd1f-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5bd1f-118">-AsJob</span></span>
<span data-ttu-id="5bd1f-119">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="5bd1f-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5bd1f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bd1f-120">-DefaultProfile</span></span>
<span data-ttu-id="5bd1f-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bd1f-122">-Force</span><span class="sxs-lookup"><span data-stu-id="5bd1f-122">-Force</span></span>
<span data-ttu-id="5bd1f-123">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5bd1f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5bd1f-124">-InputObject</span></span>
<span data-ttu-id="5bd1f-125">Az eseményindító objektum.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-125">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bd1f-126">-Name</span><span class="sxs-lookup"><span data-stu-id="5bd1f-126">-Name</span></span>
<span data-ttu-id="5bd1f-127">Az eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd1f-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5bd1f-128">-PassThru</span></span>
<span data-ttu-id="5bd1f-129">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="5bd1f-130">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="5bd1f-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5bd1f-131">-WorkspaceName</span></span>
<span data-ttu-id="5bd1f-132">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5bd1f-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5bd1f-133">-WorkspaceObject</span></span>
<span data-ttu-id="5bd1f-134">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5bd1f-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5bd1f-135">-Confirm</span></span>
<span data-ttu-id="5bd1f-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bd1f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bd1f-137">-WhatIf</span></span>
<span data-ttu-id="5bd1f-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5bd1f-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bd1f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bd1f-140">CommonParameters</span></span>
<span data-ttu-id="5bd1f-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bd1f-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5bd1f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bd1f-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5bd1f-143">INPUTS</span></span>

### <span data-ttu-id="5bd1f-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5bd1f-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="5bd1f-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="5bd1f-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="5bd1f-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5bd1f-146">OUTPUTS</span></span>

### <span data-ttu-id="5bd1f-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5bd1f-147">System.Boolean</span></span>

## <span data-ttu-id="5bd1f-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5bd1f-148">NOTES</span></span>

## <span data-ttu-id="5bd1f-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5bd1f-149">RELATED LINKS</span></span>
