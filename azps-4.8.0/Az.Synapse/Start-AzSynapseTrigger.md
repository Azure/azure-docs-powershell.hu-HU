---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/start-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
ms.openlocfilehash: d2488a99bba1813c192df5ef8561d83c06f2f6e7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182485"
---
# <span data-ttu-id="64299-101">Start-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="64299-101">Start-AzSynapseTrigger</span></span>

## <span data-ttu-id="64299-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="64299-102">SYNOPSIS</span></span>
<span data-ttu-id="64299-103">Elindítja az indítót egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="64299-103">Starts a trigger in a workspace.</span></span>

## <span data-ttu-id="64299-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="64299-104">SYNTAX</span></span>

### <span data-ttu-id="64299-105">StartByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="64299-105">StartByName (Default)</span></span>
```
Start-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64299-106">StartByObject</span><span class="sxs-lookup"><span data-stu-id="64299-106">StartByObject</span></span>
```
Start-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64299-107">StartByInputObject</span><span class="sxs-lookup"><span data-stu-id="64299-107">StartByInputObject</span></span>
```
Start-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64299-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="64299-108">DESCRIPTION</span></span>
<span data-ttu-id="64299-109">A **Start-AzSynapseTrigger** parancsmag egy munkaterületen indítja el az indítót.</span><span class="sxs-lookup"><span data-stu-id="64299-109">The **Start-AzSynapseTrigger** cmdlet starts a trigger in a workspace.</span></span> <span data-ttu-id="64299-110">Ha az indító a "leállt" állapotban van, a parancsmag elindítja az indítót, és az előbbi a futószalagokat a definíciója alapján hívja fel.</span><span class="sxs-lookup"><span data-stu-id="64299-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="64299-111">Ha az indító már a "Started" állapotban van, ez a parancsmag nincs befolyással.</span><span class="sxs-lookup"><span data-stu-id="64299-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="64299-112">Példák</span><span class="sxs-lookup"><span data-stu-id="64299-112">EXAMPLES</span></span>

### <span data-ttu-id="64299-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="64299-113">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="64299-114">Elindítja a ContosoTrigger nevű triggert a munkaterület ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="64299-114">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="64299-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="64299-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Start-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="64299-116">Elindítja a ContosoTrigger nevű triggert a munkaterület ContosoWorkspace a csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="64299-116">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="64299-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="64299-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Start-AzSynapseTrigger
```

<span data-ttu-id="64299-118">Elindítja a ContosoTrigger nevű triggert a munkaterület ContosoWorkspace a csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="64299-118">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="64299-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="64299-119">PARAMETERS</span></span>

### <span data-ttu-id="64299-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64299-120">-AsJob</span></span>
<span data-ttu-id="64299-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="64299-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="64299-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64299-122">-DefaultProfile</span></span>
<span data-ttu-id="64299-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64299-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64299-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64299-124">-InputObject</span></span>
<span data-ttu-id="64299-125">Az indító objektum.</span><span class="sxs-lookup"><span data-stu-id="64299-125">The trigger object.</span></span>

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

### <span data-ttu-id="64299-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="64299-126">-Name</span></span>
<span data-ttu-id="64299-127">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="64299-127">The trigger name.</span></span>

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

### <span data-ttu-id="64299-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64299-128">-PassThru</span></span>
<span data-ttu-id="64299-129">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="64299-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="64299-130">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="64299-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="64299-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="64299-131">-WorkspaceName</span></span>
<span data-ttu-id="64299-132">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="64299-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="64299-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="64299-133">-WorkspaceObject</span></span>
<span data-ttu-id="64299-134">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="64299-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="64299-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="64299-135">-Confirm</span></span>
<span data-ttu-id="64299-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="64299-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64299-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64299-137">-WhatIf</span></span>
<span data-ttu-id="64299-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="64299-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64299-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="64299-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64299-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64299-140">CommonParameters</span></span>
<span data-ttu-id="64299-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="64299-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64299-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="64299-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64299-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="64299-143">INPUTS</span></span>

### <span data-ttu-id="64299-144">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="64299-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="64299-145">Microsoft. Azure. commands. szinapszis. models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="64299-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="64299-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64299-146">OUTPUTS</span></span>

### <span data-ttu-id="64299-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="64299-147">System.Boolean</span></span>

## <span data-ttu-id="64299-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="64299-148">NOTES</span></span>

## <span data-ttu-id="64299-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64299-149">RELATED LINKS</span></span>
