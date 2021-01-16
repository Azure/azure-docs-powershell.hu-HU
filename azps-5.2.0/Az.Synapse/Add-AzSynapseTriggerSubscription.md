---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/add-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
ms.openlocfilehash: ca5501115b7c75b2e3c1baca368ebaac841e0ae1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341514"
---
# <span data-ttu-id="65ca1-101">Add-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="65ca1-101">Add-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="65ca1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65ca1-102">SYNOPSIS</span></span>
<span data-ttu-id="65ca1-103">Előfizeti az eseményindítót a külső szolgáltatás eseményeire.</span><span class="sxs-lookup"><span data-stu-id="65ca1-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="65ca1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="65ca1-104">SYNTAX</span></span>

### <span data-ttu-id="65ca1-105">AddByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="65ca1-105">AddByName (Default)</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65ca1-106">AddByObject</span><span class="sxs-lookup"><span data-stu-id="65ca1-106">AddByObject</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65ca1-107">AddByInputObject</span><span class="sxs-lookup"><span data-stu-id="65ca1-107">AddByInputObject</span></span>
```
Add-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65ca1-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="65ca1-108">DESCRIPTION</span></span>
<span data-ttu-id="65ca1-109">Az **Add-AzSynapseTriggerSubscription** parancsmag előfizeti az eseményindítót a megadott külső szolgáltatáseseményre az eseményindító definiálásból.</span><span class="sxs-lookup"><span data-stu-id="65ca1-109">The **Add-AzSynapseTriggerSubscription** cmdlet subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="65ca1-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="65ca1-110">EXAMPLES</span></span>

### <span data-ttu-id="65ca1-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="65ca1-111">Example 1</span></span>
```powershell
PS C:\> Add-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="65ca1-112">Ez a parancs a ContosoTrigger nevű eseményindítót fogja előfizetni a megadott eseményekre az eseményindító definiálásból.</span><span class="sxs-lookup"><span data-stu-id="65ca1-112">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="65ca1-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="65ca1-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Add-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="65ca1-114">Ez a parancs a ContosoTrigger nevű eseményindítót fogja előfizetni a megadott eseményekre az eseményindító definiálásból a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="65ca1-114">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="65ca1-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="65ca1-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Add-AzSynapseTriggerSubscription
```

<span data-ttu-id="65ca1-116">Ez a parancs a ContosoTrigger nevű eseményindítót fogja előfizetni a megadott eseményekre az eseményindító definiálásból a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="65ca1-116">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="65ca1-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65ca1-117">PARAMETERS</span></span>

### <span data-ttu-id="65ca1-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65ca1-118">-AsJob</span></span>
<span data-ttu-id="65ca1-119">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="65ca1-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65ca1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65ca1-120">-DefaultProfile</span></span>
<span data-ttu-id="65ca1-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="65ca1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65ca1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65ca1-122">-InputObject</span></span>
<span data-ttu-id="65ca1-123">Az eseményindító objektum.</span><span class="sxs-lookup"><span data-stu-id="65ca1-123">The trigger object.</span></span>

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

### <span data-ttu-id="65ca1-124">-Name</span><span class="sxs-lookup"><span data-stu-id="65ca1-124">-Name</span></span>
<span data-ttu-id="65ca1-125">Az eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="65ca1-125">The trigger name.</span></span>

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

### <span data-ttu-id="65ca1-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="65ca1-126">-WorkspaceName</span></span>
<span data-ttu-id="65ca1-127">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="65ca1-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="65ca1-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="65ca1-128">-WorkspaceObject</span></span>
<span data-ttu-id="65ca1-129">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="65ca1-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="65ca1-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65ca1-130">-Confirm</span></span>
<span data-ttu-id="65ca1-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="65ca1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65ca1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65ca1-132">-WhatIf</span></span>
<span data-ttu-id="65ca1-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="65ca1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65ca1-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="65ca1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65ca1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65ca1-135">CommonParameters</span></span>
<span data-ttu-id="65ca1-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65ca1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65ca1-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65ca1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65ca1-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65ca1-138">INPUTS</span></span>

### <span data-ttu-id="65ca1-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="65ca1-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="65ca1-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="65ca1-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="65ca1-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65ca1-141">OUTPUTS</span></span>

### <span data-ttu-id="65ca1-142">System.Object</span><span class="sxs-lookup"><span data-stu-id="65ca1-142">System.Object</span></span>
## <span data-ttu-id="65ca1-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="65ca1-143">NOTES</span></span>

## <span data-ttu-id="65ca1-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65ca1-144">RELATED LINKS</span></span>
