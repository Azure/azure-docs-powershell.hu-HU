---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
ms.openlocfilehash: 69e7c17d28c94ce00f054a0e5b71eadc4d8ade76
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182489"
---
# <span data-ttu-id="aab87-101">Remove-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="aab87-101">Remove-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="aab87-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aab87-102">SYNOPSIS</span></span>
<span data-ttu-id="aab87-103">Lemondhatja az eseményindítót külső szolgáltatási eseményekre.</span><span class="sxs-lookup"><span data-stu-id="aab87-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="aab87-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aab87-104">SYNTAX</span></span>

### <span data-ttu-id="aab87-105">RemoveByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aab87-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aab87-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="aab87-106">RemoveByObject</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aab87-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="aab87-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aab87-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="aab87-108">DESCRIPTION</span></span>
<span data-ttu-id="aab87-109">A **Remove-AzSynapseTriggerSubscription** parancsmag lemond az esemény eseményindítóról a megadott külső szolgáltatási eseményekre az eseményindító Defintion.</span><span class="sxs-lookup"><span data-stu-id="aab87-109">The **Remove-AzSynapseTriggerSubscription** cmdlet unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="aab87-110">Példák</span><span class="sxs-lookup"><span data-stu-id="aab87-110">EXAMPLES</span></span>

### <span data-ttu-id="aab87-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="aab87-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="aab87-112">Ez a parancs lemondja a ContosoTrigger az indító Defintion megadott eseményekre.</span><span class="sxs-lookup"><span data-stu-id="aab87-112">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="aab87-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="aab87-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="aab87-114">Ez a parancs lemondja a ContosoTrigger-hoz megadott eseményekre az indító Defintion a csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="aab87-114">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="aab87-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="aab87-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTriggerSubscription
```

<span data-ttu-id="aab87-116">Ez a parancs lemondja a ContosoTrigger-hoz megadott eseményekre az indító Defintion a csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="aab87-116">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="aab87-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aab87-117">PARAMETERS</span></span>

### <span data-ttu-id="aab87-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aab87-118">-AsJob</span></span>
<span data-ttu-id="aab87-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="aab87-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aab87-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aab87-120">-DefaultProfile</span></span>
<span data-ttu-id="aab87-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aab87-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aab87-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aab87-122">-InputObject</span></span>
<span data-ttu-id="aab87-123">Az indító objektum.</span><span class="sxs-lookup"><span data-stu-id="aab87-123">The trigger object.</span></span>

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

### <span data-ttu-id="aab87-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aab87-124">-Name</span></span>
<span data-ttu-id="aab87-125">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="aab87-125">The trigger name.</span></span>

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

### <span data-ttu-id="aab87-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aab87-126">-PassThru</span></span>
<span data-ttu-id="aab87-127">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="aab87-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="aab87-128">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="aab87-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="aab87-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="aab87-129">-WorkspaceName</span></span>
<span data-ttu-id="aab87-130">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="aab87-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="aab87-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="aab87-131">-WorkspaceObject</span></span>
<span data-ttu-id="aab87-132">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="aab87-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="aab87-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aab87-133">-Confirm</span></span>
<span data-ttu-id="aab87-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aab87-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aab87-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aab87-135">-WhatIf</span></span>
<span data-ttu-id="aab87-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aab87-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aab87-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aab87-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aab87-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aab87-138">CommonParameters</span></span>
<span data-ttu-id="aab87-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aab87-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aab87-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="aab87-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aab87-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aab87-141">INPUTS</span></span>

### <span data-ttu-id="aab87-142">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="aab87-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="aab87-143">Microsoft. Azure. commands. szinapszis. models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="aab87-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="aab87-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aab87-144">OUTPUTS</span></span>

### <span data-ttu-id="aab87-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aab87-145">System.Boolean</span></span>

## <span data-ttu-id="aab87-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aab87-146">NOTES</span></span>

## <span data-ttu-id="aab87-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aab87-147">RELATED LINKS</span></span>
