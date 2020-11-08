---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
ms.openlocfilehash: 4e35814be14c2be3b5ba0fd1ca5960d297590dca
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186599"
---
# <span data-ttu-id="c0456-101">Stop-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="c0456-101">Stop-AzSynapseTrigger</span></span>

## <span data-ttu-id="c0456-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c0456-102">SYNOPSIS</span></span>
<span data-ttu-id="c0456-103">A munkaterületen leállít egy triggert.</span><span class="sxs-lookup"><span data-stu-id="c0456-103">Stops a trigger in a workspace.</span></span>

## <span data-ttu-id="c0456-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c0456-104">SYNTAX</span></span>

### <span data-ttu-id="c0456-105">StopByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c0456-105">StopByName (Default)</span></span>
```
Stop-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0456-106">StopByObject</span><span class="sxs-lookup"><span data-stu-id="c0456-106">StopByObject</span></span>
```
Stop-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0456-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="c0456-107">StopByInputObject</span></span>
```
Stop-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0456-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c0456-108">DESCRIPTION</span></span>
<span data-ttu-id="c0456-109">A **stop-AzSynapseTrigger** parancsmag leállítja a munkaterületen az indítót.</span><span class="sxs-lookup"><span data-stu-id="c0456-109">The **Stop-AzSynapseTrigger** cmdlet stops a trigger in a workspace.</span></span> <span data-ttu-id="c0456-110">Ha az indító az "Elindítva" állapotban van, a parancsmag leállítja az indítási fázist, és már nem indítja el a csővezetékeket.</span><span class="sxs-lookup"><span data-stu-id="c0456-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="c0456-111">Ha az indító már a "leállt" állapotban van, ez a parancsmag nincs befolyással.</span><span class="sxs-lookup"><span data-stu-id="c0456-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="c0456-112">Példák</span><span class="sxs-lookup"><span data-stu-id="c0456-112">EXAMPLES</span></span>

### <span data-ttu-id="c0456-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c0456-113">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="c0456-114">Leállít egy ContosoTrigger nevű triggert a munkaterület ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="c0456-114">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="c0456-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="c0456-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="c0456-116">Egy ContosoTrigger nevű triggert állít le a munkaterület ContosoWorkspace a csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="c0456-116">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="c0456-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="c0456-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Stop-AzSynapseTrigger
```

<span data-ttu-id="c0456-118">Állítsa le a ContosoTrigger nevű triggert a munkaterület ContosoWorkspace a csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="c0456-118">Stop a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="c0456-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c0456-119">PARAMETERS</span></span>

### <span data-ttu-id="c0456-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0456-120">-AsJob</span></span>
<span data-ttu-id="c0456-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c0456-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c0456-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0456-122">-DefaultProfile</span></span>
<span data-ttu-id="c0456-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c0456-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0456-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0456-124">-InputObject</span></span>
<span data-ttu-id="c0456-125">Az indító objektum.</span><span class="sxs-lookup"><span data-stu-id="c0456-125">The trigger object.</span></span>

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

### <span data-ttu-id="c0456-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c0456-126">-Name</span></span>
<span data-ttu-id="c0456-127">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="c0456-127">The trigger name.</span></span>

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

### <span data-ttu-id="c0456-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0456-128">-PassThru</span></span>
<span data-ttu-id="c0456-129">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="c0456-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="c0456-130">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="c0456-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="c0456-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c0456-131">-WorkspaceName</span></span>
<span data-ttu-id="c0456-132">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="c0456-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c0456-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c0456-133">-WorkspaceObject</span></span>
<span data-ttu-id="c0456-134">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="c0456-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c0456-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c0456-135">-Confirm</span></span>
<span data-ttu-id="c0456-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c0456-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0456-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0456-137">-WhatIf</span></span>
<span data-ttu-id="c0456-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c0456-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0456-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c0456-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0456-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0456-140">CommonParameters</span></span>
<span data-ttu-id="c0456-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c0456-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0456-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c0456-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0456-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0456-143">INPUTS</span></span>

### <span data-ttu-id="c0456-144">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c0456-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="c0456-145">Microsoft. Azure. commands. szinapszis. models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="c0456-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="c0456-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0456-146">OUTPUTS</span></span>

### <span data-ttu-id="c0456-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c0456-147">System.Boolean</span></span>

## <span data-ttu-id="c0456-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c0456-148">NOTES</span></span>

## <span data-ttu-id="c0456-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0456-149">RELATED LINKS</span></span>
