---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
ms.openlocfilehash: 69e7c17d28c94ce00f054a0e5b71eadc4d8ade76
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187134"
---
# <span data-ttu-id="ed27e-101">Remove-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="ed27e-101">Remove-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="ed27e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ed27e-102">SYNOPSIS</span></span>
<span data-ttu-id="ed27e-103">Lemondhatja az eseményindítót külső szolgáltatási eseményekre.</span><span class="sxs-lookup"><span data-stu-id="ed27e-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="ed27e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ed27e-104">SYNTAX</span></span>

### <span data-ttu-id="ed27e-105">RemoveByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ed27e-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed27e-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="ed27e-106">RemoveByObject</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed27e-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="ed27e-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed27e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ed27e-108">DESCRIPTION</span></span>
<span data-ttu-id="ed27e-109">A **Remove-AzSynapseTriggerSubscription** parancsmag lemond az esemény eseményindítóról a megadott külső szolgáltatási eseményekre az eseményindító Defintion.</span><span class="sxs-lookup"><span data-stu-id="ed27e-109">The **Remove-AzSynapseTriggerSubscription** cmdlet unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="ed27e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ed27e-110">EXAMPLES</span></span>

### <span data-ttu-id="ed27e-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ed27e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="ed27e-112">Ez a parancs lemondja a ContosoTrigger az indító Defintion megadott eseményekre.</span><span class="sxs-lookup"><span data-stu-id="ed27e-112">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="ed27e-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="ed27e-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="ed27e-114">Ez a parancs lemondja a ContosoTrigger-hoz megadott eseményekre az indító Defintion a csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="ed27e-114">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="ed27e-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="ed27e-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTriggerSubscription
```

<span data-ttu-id="ed27e-116">Ez a parancs lemondja a ContosoTrigger-hoz megadott eseményekre az indító Defintion a csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="ed27e-116">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="ed27e-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ed27e-117">PARAMETERS</span></span>

### <span data-ttu-id="ed27e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed27e-118">-AsJob</span></span>
<span data-ttu-id="ed27e-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ed27e-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ed27e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed27e-120">-DefaultProfile</span></span>
<span data-ttu-id="ed27e-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ed27e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed27e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed27e-122">-InputObject</span></span>
<span data-ttu-id="ed27e-123">Az indító objektum.</span><span class="sxs-lookup"><span data-stu-id="ed27e-123">The trigger object.</span></span>

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

### <span data-ttu-id="ed27e-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ed27e-124">-Name</span></span>
<span data-ttu-id="ed27e-125">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="ed27e-125">The trigger name.</span></span>

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

### <span data-ttu-id="ed27e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed27e-126">-PassThru</span></span>
<span data-ttu-id="ed27e-127">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="ed27e-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="ed27e-128">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="ed27e-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="ed27e-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ed27e-129">-WorkspaceName</span></span>
<span data-ttu-id="ed27e-130">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="ed27e-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ed27e-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ed27e-131">-WorkspaceObject</span></span>
<span data-ttu-id="ed27e-132">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="ed27e-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ed27e-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ed27e-133">-Confirm</span></span>
<span data-ttu-id="ed27e-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ed27e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed27e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed27e-135">-WhatIf</span></span>
<span data-ttu-id="ed27e-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ed27e-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed27e-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ed27e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed27e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed27e-138">CommonParameters</span></span>
<span data-ttu-id="ed27e-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ed27e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed27e-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ed27e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed27e-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed27e-141">INPUTS</span></span>

### <span data-ttu-id="ed27e-142">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ed27e-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ed27e-143">Microsoft. Azure. commands. szinapszis. models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="ed27e-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="ed27e-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed27e-144">OUTPUTS</span></span>

### <span data-ttu-id="ed27e-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ed27e-145">System.Boolean</span></span>

## <span data-ttu-id="ed27e-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ed27e-146">NOTES</span></span>

## <span data-ttu-id="ed27e-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed27e-147">RELATED LINKS</span></span>
