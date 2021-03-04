---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
ms.openlocfilehash: 0852cbbce26e1f95bfb75975418fae30038316ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939186"
---
# <span data-ttu-id="4dc72-101">Set-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="4dc72-101">Set-AzSynapseTrigger</span></span>

## <span data-ttu-id="4dc72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dc72-102">SYNOPSIS</span></span>
<span data-ttu-id="4dc72-103">Létrehoz egy eseményindítót egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="4dc72-103">Creates a trigger in a workspace.</span></span>

## <span data-ttu-id="4dc72-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4dc72-104">SYNTAX</span></span>

### <span data-ttu-id="4dc72-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4dc72-105">SetByName (Default)</span></span>
```
Set-AzSynapseTrigger -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dc72-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="4dc72-106">SetByObject</span></span>
```
Set-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dc72-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4dc72-107">DESCRIPTION</span></span>
<span data-ttu-id="4dc72-108">A **Set-AzSynapseTrigger** parancsmag létrehoz egy eseményindítót egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="4dc72-108">The **Set-AzSynapseTrigger** cmdlet creates a trigger in a workspace.</span></span> <span data-ttu-id="4dc72-109">Az eseményindítók "Leállítva" állapotban jön létre, ami azt jelenti, hogy nem kezdődnek azonnal a hivatkozott prognózisok.</span><span class="sxs-lookup"><span data-stu-id="4dc72-109">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="4dc72-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4dc72-110">EXAMPLES</span></span>

### <span data-ttu-id="4dc72-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="4dc72-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="4dc72-112">Hozzon létre egy ContosoTrigger nevű új eseményindítót a ContosoWorkspace munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="4dc72-112">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span> <span data-ttu-id="4dc72-113">Az eseményindító "Leállítva" állapotban jön létre, ami azt jelenti, hogy nem indul el azonnal.</span><span class="sxs-lookup"><span data-stu-id="4dc72-113">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="4dc72-114">A parancsmag használatával elindítható egy `Start-AzDataFactoryV2Trigger` eseményindító.</span><span class="sxs-lookup"><span data-stu-id="4dc72-114">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

### <span data-ttu-id="4dc72-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="4dc72-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseTrigger -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="4dc72-116">Hozzon létre egy Új Eseményindítót a ContosoTrigger nevű munkaterületen a ContosoWorkspace folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="4dc72-116">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span> <span data-ttu-id="4dc72-117">Az eseményindító "Leállítva" állapotban jön létre, ami azt jelenti, hogy nem indul el azonnal.</span><span class="sxs-lookup"><span data-stu-id="4dc72-117">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="4dc72-118">A parancsmag használatával elindítható egy `Start-AzDataFactoryV2Trigger` eseményindító.</span><span class="sxs-lookup"><span data-stu-id="4dc72-118">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="4dc72-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4dc72-119">PARAMETERS</span></span>

### <span data-ttu-id="4dc72-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4dc72-120">-AsJob</span></span>
<span data-ttu-id="4dc72-121">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4dc72-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4dc72-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dc72-122">-DefaultProfile</span></span>
<span data-ttu-id="4dc72-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4dc72-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dc72-124">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="4dc72-124">-DefinitionFile</span></span>
<span data-ttu-id="4dc72-125">A JSON fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="4dc72-125">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dc72-126">-Name</span><span class="sxs-lookup"><span data-stu-id="4dc72-126">-Name</span></span>
<span data-ttu-id="4dc72-127">Az eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="4dc72-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dc72-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4dc72-128">-WorkspaceName</span></span>
<span data-ttu-id="4dc72-129">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="4dc72-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dc72-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4dc72-130">-WorkspaceObject</span></span>
<span data-ttu-id="4dc72-131">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="4dc72-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc72-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4dc72-132">-Confirm</span></span>
<span data-ttu-id="4dc72-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4dc72-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dc72-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dc72-134">-WhatIf</span></span>
<span data-ttu-id="4dc72-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4dc72-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dc72-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4dc72-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dc72-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dc72-137">CommonParameters</span></span>
<span data-ttu-id="4dc72-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dc72-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dc72-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4dc72-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dc72-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4dc72-140">INPUTS</span></span>

### <span data-ttu-id="4dc72-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4dc72-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="4dc72-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4dc72-142">OUTPUTS</span></span>

### <span data-ttu-id="4dc72-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="4dc72-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="4dc72-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4dc72-144">NOTES</span></span>

## <span data-ttu-id="4dc72-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4dc72-145">RELATED LINKS</span></span>
