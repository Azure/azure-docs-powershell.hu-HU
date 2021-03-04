---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/add-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
ms.openlocfilehash: d9ff2e46b7b4ccf7b3d2fafd1aa8142efd0675b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933305"
---
# <span data-ttu-id="7261f-101">Add-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="7261f-101">Add-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="7261f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7261f-102">SYNOPSIS</span></span>
<span data-ttu-id="7261f-103">Előfizeti az eseményindítót a külső szolgáltatás eseményeire.</span><span class="sxs-lookup"><span data-stu-id="7261f-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="7261f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7261f-104">SYNTAX</span></span>

### <span data-ttu-id="7261f-105">AddByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7261f-105">AddByName (Default)</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7261f-106">AddByObject</span><span class="sxs-lookup"><span data-stu-id="7261f-106">AddByObject</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7261f-107">AddByInputObject</span><span class="sxs-lookup"><span data-stu-id="7261f-107">AddByInputObject</span></span>
```
Add-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7261f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7261f-108">DESCRIPTION</span></span>
<span data-ttu-id="7261f-109">Az **Add-AzSynapseTriggerSubscription** parancsmag előfizeti az eseményindítót a megadott külső szolgáltatáseseményre az eseményindító definiálásból.</span><span class="sxs-lookup"><span data-stu-id="7261f-109">The **Add-AzSynapseTriggerSubscription** cmdlet subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="7261f-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7261f-110">EXAMPLES</span></span>

### <span data-ttu-id="7261f-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="7261f-111">Example 1</span></span>
```powershell
PS C:\> Add-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="7261f-112">Ez a parancs a ContosoTrigger nevű eseményindítót fogja előfizetni a megadott eseményre az eseményindító definiálásból.</span><span class="sxs-lookup"><span data-stu-id="7261f-112">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="7261f-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="7261f-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Add-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="7261f-114">Ez a parancs a ContosoTrigger nevű eseményindítót fogja előfizetni a megadott eseményekre az eseményindító definiálásból a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="7261f-114">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="7261f-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="7261f-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Add-AzSynapseTriggerSubscription
```

<span data-ttu-id="7261f-116">Ez a parancs a ContosoTrigger nevű eseményindítót fogja előfizetni a megadott eseményekre az eseményindító definiálásból a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="7261f-116">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="7261f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7261f-117">PARAMETERS</span></span>

### <span data-ttu-id="7261f-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7261f-118">-AsJob</span></span>
<span data-ttu-id="7261f-119">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7261f-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7261f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7261f-120">-DefaultProfile</span></span>
<span data-ttu-id="7261f-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7261f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7261f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7261f-122">-InputObject</span></span>
<span data-ttu-id="7261f-123">Az eseményindító objektum.</span><span class="sxs-lookup"><span data-stu-id="7261f-123">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: AddByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7261f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="7261f-124">-Name</span></span>
<span data-ttu-id="7261f-125">Az eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="7261f-125">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: AddByName, AddByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7261f-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7261f-126">-WorkspaceName</span></span>
<span data-ttu-id="7261f-127">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="7261f-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: AddByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7261f-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7261f-128">-WorkspaceObject</span></span>
<span data-ttu-id="7261f-129">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="7261f-129">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: AddByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7261f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7261f-130">-Confirm</span></span>
<span data-ttu-id="7261f-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7261f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7261f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7261f-132">-WhatIf</span></span>
<span data-ttu-id="7261f-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7261f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7261f-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7261f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7261f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7261f-135">CommonParameters</span></span>
<span data-ttu-id="7261f-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7261f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7261f-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7261f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7261f-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7261f-138">INPUTS</span></span>

### <span data-ttu-id="7261f-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7261f-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="7261f-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="7261f-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="7261f-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7261f-141">OUTPUTS</span></span>

### <span data-ttu-id="7261f-142">System.Object</span><span class="sxs-lookup"><span data-stu-id="7261f-142">System.Object</span></span>
## <span data-ttu-id="7261f-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7261f-143">NOTES</span></span>

## <span data-ttu-id="7261f-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7261f-144">RELATED LINKS</span></span>
