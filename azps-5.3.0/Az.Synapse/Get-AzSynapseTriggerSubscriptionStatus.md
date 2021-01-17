---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetriggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
ms.openlocfilehash: b18a308b94bdb486945186c67c3a905bcb0408d3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383710"
---
# <span data-ttu-id="7e7fb-101">Get-AzSynapseTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="7e7fb-101">Get-AzSynapseTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="7e7fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e7fb-102">SYNOPSIS</span></span>
<span data-ttu-id="7e7fb-103">Az eseményindító előfizetésének állapotának lekérte a megadott külső szolgáltatási eseményekre.</span><span class="sxs-lookup"><span data-stu-id="7e7fb-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="7e7fb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7e7fb-104">SYNTAX</span></span>

### <span data-ttu-id="7e7fb-105">GetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7e7fb-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e7fb-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="7e7fb-106">GetByObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e7fb-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="7e7fb-107">GetByInputObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -InputObject <PSTriggerResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e7fb-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7e7fb-108">DESCRIPTION</span></span>
<span data-ttu-id="7e7fb-109">A **Get-AzSynapseTriggerSubscriptionStatus** parancsmag megkapja az eseményindító előfizetésének állapotát a megadott külső szolgáltatási eseményekre.</span><span class="sxs-lookup"><span data-stu-id="7e7fb-109">The **Get-AzSynapseTriggerSubscriptionStatus** cmdlet gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="7e7fb-110">Az eseményindító csak akkor indítható el, ha a visszaadott állapot "Engedélyezve" állapotú.</span><span class="sxs-lookup"><span data-stu-id="7e7fb-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="7e7fb-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7e7fb-111">EXAMPLES</span></span>

### <span data-ttu-id="7e7fb-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="7e7fb-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="7e7fb-113">Ez a parancs a ContosoTrigger nevű eseményindító feliratkozási állapotát fogja megkapni a külső szolgáltatásesemények számára.</span><span class="sxs-lookup"><span data-stu-id="7e7fb-113">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events.</span></span>

### <span data-ttu-id="7e7fb-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="7e7fb-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerSubscriptionStatus -Name ContosoTrigger
```

<span data-ttu-id="7e7fb-115">Ez a parancs a ContosoTrigger nevű eseményindítóhoz a külső szolgáltatásesemények folyamaton keresztüli feliratkozási állapotát fogja megkapni.</span><span class="sxs-lookup"><span data-stu-id="7e7fb-115">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

### <span data-ttu-id="7e7fb-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="7e7fb-116">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Get-AzSynapseTriggerSubscriptionStatus
```

<span data-ttu-id="7e7fb-117">Ez a parancs a ContosoTrigger nevű eseményindítóhoz a külső szolgáltatásesemények folyamaton keresztüli feliratkozási állapotát fogja megkapni.</span><span class="sxs-lookup"><span data-stu-id="7e7fb-117">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

## <span data-ttu-id="7e7fb-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e7fb-118">PARAMETERS</span></span>

### <span data-ttu-id="7e7fb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e7fb-119">-DefaultProfile</span></span>
<span data-ttu-id="7e7fb-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7e7fb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e7fb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e7fb-121">-InputObject</span></span>
<span data-ttu-id="7e7fb-122">Az eseményindító objektum.</span><span class="sxs-lookup"><span data-stu-id="7e7fb-122">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: GetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e7fb-123">-Name</span><span class="sxs-lookup"><span data-stu-id="7e7fb-123">-Name</span></span>
<span data-ttu-id="7e7fb-124">Az eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="7e7fb-124">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName, GetByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e7fb-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7e7fb-125">-WorkspaceName</span></span>
<span data-ttu-id="7e7fb-126">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="7e7fb-126">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e7fb-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7e7fb-127">-WorkspaceObject</span></span>
<span data-ttu-id="7e7fb-128">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="7e7fb-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e7fb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e7fb-129">CommonParameters</span></span>
<span data-ttu-id="7e7fb-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e7fb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e7fb-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e7fb-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e7fb-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e7fb-132">INPUTS</span></span>

### <span data-ttu-id="7e7fb-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7e7fb-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="7e7fb-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="7e7fb-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="7e7fb-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e7fb-135">OUTPUTS</span></span>

### <span data-ttu-id="7e7fb-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span><span class="sxs-lookup"><span data-stu-id="7e7fb-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span></span>

## <span data-ttu-id="7e7fb-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7e7fb-137">NOTES</span></span>

## <span data-ttu-id="7e7fb-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e7fb-138">RELATED LINKS</span></span>
