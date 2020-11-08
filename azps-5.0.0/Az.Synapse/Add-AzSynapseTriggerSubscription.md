---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/add-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
ms.openlocfilehash: ca5501115b7c75b2e3c1baca368ebaac841e0ae1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187965"
---
# <span data-ttu-id="b4d0a-101">Add-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="b4d0a-101">Add-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="b4d0a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b4d0a-102">SYNOPSIS</span></span>
<span data-ttu-id="b4d0a-103">Iratkozzon fel az eseményindítót külső szolgáltatási eseményekre.</span><span class="sxs-lookup"><span data-stu-id="b4d0a-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="b4d0a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b4d0a-104">SYNTAX</span></span>

### <span data-ttu-id="b4d0a-105">AddByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b4d0a-105">AddByName (Default)</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4d0a-106">AddByObject</span><span class="sxs-lookup"><span data-stu-id="b4d0a-106">AddByObject</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4d0a-107">AddByInputObject</span><span class="sxs-lookup"><span data-stu-id="b4d0a-107">AddByInputObject</span></span>
```
Add-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4d0a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b4d0a-108">DESCRIPTION</span></span>
<span data-ttu-id="b4d0a-109">A **Add-AzSynapseTriggerSubscription** parancsmag az eseményindító Defintion a megadott külső szolgáltatási eseményekre fizeti az eseményindítót.</span><span class="sxs-lookup"><span data-stu-id="b4d0a-109">The **Add-AzSynapseTriggerSubscription** cmdlet subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="b4d0a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b4d0a-110">EXAMPLES</span></span>

### <span data-ttu-id="b4d0a-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b4d0a-111">Example 1</span></span>
```powershell
PS C:\> Add-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="b4d0a-112">Ez a parancs Előfizeti a trigger Defintion megadott eseményeknek nevezett ContosoTrigger.</span><span class="sxs-lookup"><span data-stu-id="b4d0a-112">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="b4d0a-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="b4d0a-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Add-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="b4d0a-114">Ez a parancs Előfizeti a trigger nevű ContosoTrigger a megadott eseményekre az Defintion és a csővezeték között.</span><span class="sxs-lookup"><span data-stu-id="b4d0a-114">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="b4d0a-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="b4d0a-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Add-AzSynapseTriggerSubscription
```

<span data-ttu-id="b4d0a-116">Ez a parancs Előfizeti a trigger nevű ContosoTrigger a megadott eseményekre az Defintion és a csővezeték között.</span><span class="sxs-lookup"><span data-stu-id="b4d0a-116">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="b4d0a-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b4d0a-117">PARAMETERS</span></span>

### <span data-ttu-id="b4d0a-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4d0a-118">-AsJob</span></span>
<span data-ttu-id="b4d0a-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b4d0a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4d0a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4d0a-120">-DefaultProfile</span></span>
<span data-ttu-id="b4d0a-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b4d0a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4d0a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4d0a-122">-InputObject</span></span>
<span data-ttu-id="b4d0a-123">Az indító objektum.</span><span class="sxs-lookup"><span data-stu-id="b4d0a-123">The trigger object.</span></span>

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

### <span data-ttu-id="b4d0a-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b4d0a-124">-Name</span></span>
<span data-ttu-id="b4d0a-125">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="b4d0a-125">The trigger name.</span></span>

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

### <span data-ttu-id="b4d0a-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b4d0a-126">-WorkspaceName</span></span>
<span data-ttu-id="b4d0a-127">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="b4d0a-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b4d0a-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b4d0a-128">-WorkspaceObject</span></span>
<span data-ttu-id="b4d0a-129">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="b4d0a-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b4d0a-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b4d0a-130">-Confirm</span></span>
<span data-ttu-id="b4d0a-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b4d0a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4d0a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4d0a-132">-WhatIf</span></span>
<span data-ttu-id="b4d0a-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b4d0a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4d0a-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b4d0a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4d0a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4d0a-135">CommonParameters</span></span>
<span data-ttu-id="b4d0a-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b4d0a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4d0a-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b4d0a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4d0a-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4d0a-138">INPUTS</span></span>

### <span data-ttu-id="b4d0a-139">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b4d0a-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="b4d0a-140">Microsoft. Azure. commands. szinapszis. models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="b4d0a-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="b4d0a-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4d0a-141">OUTPUTS</span></span>

### <span data-ttu-id="b4d0a-142">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="b4d0a-142">System.Object</span></span>
## <span data-ttu-id="b4d0a-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b4d0a-143">NOTES</span></span>

## <span data-ttu-id="b4d0a-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4d0a-144">RELATED LINKS</span></span>
