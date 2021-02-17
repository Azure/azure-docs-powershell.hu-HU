---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
ms.openlocfilehash: 289e601ab80e4842b493cd6852839bec544bcc36
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207599"
---
# <span data-ttu-id="ac891-101">Set-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="ac891-101">Set-AzSynapseTrigger</span></span>

## <span data-ttu-id="ac891-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac891-102">SYNOPSIS</span></span>
<span data-ttu-id="ac891-103">Létrehoz egy eseményindítót egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="ac891-103">Creates a trigger in a workspace.</span></span>

## <span data-ttu-id="ac891-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ac891-104">SYNTAX</span></span>

### <span data-ttu-id="ac891-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ac891-105">SetByName (Default)</span></span>
```
Set-AzSynapseTrigger -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac891-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="ac891-106">SetByObject</span></span>
```
Set-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac891-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ac891-107">DESCRIPTION</span></span>
<span data-ttu-id="ac891-108">A **Set-AzSynapseTrigger** parancsmag létrehoz egy eseményindítót egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="ac891-108">The **Set-AzSynapseTrigger** cmdlet creates a trigger in a workspace.</span></span> <span data-ttu-id="ac891-109">Az eseményindítók a "Leállítva" állapotban jön létre, ami azt jelenti, hogy nem kezdődnek azonnal a hivatkozott prognózisok megindítói.</span><span class="sxs-lookup"><span data-stu-id="ac891-109">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="ac891-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ac891-110">EXAMPLES</span></span>

### <span data-ttu-id="ac891-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="ac891-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="ac891-112">Hozzon létre egy ContosoTrigger nevű új eseményindítót a ContosoWorkspace munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="ac891-112">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span> <span data-ttu-id="ac891-113">Az eseményindító "Leállítva" állapotban jön létre, ami azt jelenti, hogy nem indul el azonnal.</span><span class="sxs-lookup"><span data-stu-id="ac891-113">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="ac891-114">A parancsmag használatával elindítható egy `Start-AzDataFactoryV2Trigger` eseményindító.</span><span class="sxs-lookup"><span data-stu-id="ac891-114">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

### <span data-ttu-id="ac891-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="ac891-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseTrigger -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="ac891-116">Hozzon létre egy Új Eseményindítót a ContosoTrigger nevű munkaterületen a ContosoWorkspace folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="ac891-116">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span> <span data-ttu-id="ac891-117">Az eseményindító "Leállítva" állapotban jön létre, ami azt jelenti, hogy nem indul el azonnal.</span><span class="sxs-lookup"><span data-stu-id="ac891-117">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="ac891-118">A parancsmag használatával elindítható egy `Start-AzDataFactoryV2Trigger` eseményindító.</span><span class="sxs-lookup"><span data-stu-id="ac891-118">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="ac891-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac891-119">PARAMETERS</span></span>

### <span data-ttu-id="ac891-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac891-120">-AsJob</span></span>
<span data-ttu-id="ac891-121">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ac891-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ac891-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac891-122">-DefaultProfile</span></span>
<span data-ttu-id="ac891-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ac891-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac891-124">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="ac891-124">-DefinitionFile</span></span>
<span data-ttu-id="ac891-125">A JSON fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="ac891-125">The JSON file path.</span></span>

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

### <span data-ttu-id="ac891-126">-Name</span><span class="sxs-lookup"><span data-stu-id="ac891-126">-Name</span></span>
<span data-ttu-id="ac891-127">Az eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="ac891-127">The trigger name.</span></span>

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

### <span data-ttu-id="ac891-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ac891-128">-WorkspaceName</span></span>
<span data-ttu-id="ac891-129">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="ac891-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ac891-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ac891-130">-WorkspaceObject</span></span>
<span data-ttu-id="ac891-131">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="ac891-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ac891-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac891-132">-Confirm</span></span>
<span data-ttu-id="ac891-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ac891-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac891-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac891-134">-WhatIf</span></span>
<span data-ttu-id="ac891-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ac891-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac891-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ac891-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac891-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac891-137">CommonParameters</span></span>
<span data-ttu-id="ac891-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac891-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac891-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ac891-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac891-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ac891-140">INPUTS</span></span>

### <span data-ttu-id="ac891-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ac891-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ac891-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac891-142">OUTPUTS</span></span>

### <span data-ttu-id="ac891-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="ac891-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="ac891-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ac891-144">NOTES</span></span>

## <span data-ttu-id="ac891-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ac891-145">RELATED LINKS</span></span>
