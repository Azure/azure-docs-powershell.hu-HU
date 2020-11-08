---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetriggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
ms.openlocfilehash: b18a308b94bdb486945186c67c3a905bcb0408d3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017477"
---
# <span data-ttu-id="89682-101">Get-AzSynapseTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="89682-101">Get-AzSynapseTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="89682-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="89682-102">SYNOPSIS</span></span>
<span data-ttu-id="89682-103">Az esemény eseményindítójának állapotát a megadott külső szolgáltatási eseményekre vonatkozóan szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="89682-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="89682-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="89682-104">SYNTAX</span></span>

### <span data-ttu-id="89682-105">GetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="89682-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89682-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="89682-106">GetByObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89682-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="89682-107">GetByInputObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -InputObject <PSTriggerResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89682-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="89682-108">DESCRIPTION</span></span>
<span data-ttu-id="89682-109">A **Get-AzSynapseTriggerSubscriptionStatus** parancsmag az esemény eseményindítójának állapotát a megadott külső szolgáltatási eseményekre kapja.</span><span class="sxs-lookup"><span data-stu-id="89682-109">The **Get-AzSynapseTriggerSubscriptionStatus** cmdlet gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="89682-110">Az indító nem indítható el, amíg a visszaadott állapot "engedélyezve" nem van.</span><span class="sxs-lookup"><span data-stu-id="89682-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="89682-111">Példák</span><span class="sxs-lookup"><span data-stu-id="89682-111">EXAMPLES</span></span>

### <span data-ttu-id="89682-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="89682-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="89682-113">Ez a parancs a külső szolgáltatási eseményekhez az ContosoTrigger nevű Subscribtion állapotát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="89682-113">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events.</span></span>

### <span data-ttu-id="89682-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="89682-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerSubscriptionStatus -Name ContosoTrigger
```

<span data-ttu-id="89682-115">Ez a parancs a ContosoTrigger a külső szolgáltatási eseményekre csővezetéken keresztüli Subscribtion állapotát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="89682-115">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

### <span data-ttu-id="89682-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="89682-116">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Get-AzSynapseTriggerSubscriptionStatus
```

<span data-ttu-id="89682-117">Ez a parancs a ContosoTrigger a külső szolgáltatási eseményekre csővezetéken keresztüli Subscribtion állapotát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="89682-117">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

## <span data-ttu-id="89682-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="89682-118">PARAMETERS</span></span>

### <span data-ttu-id="89682-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89682-119">-DefaultProfile</span></span>
<span data-ttu-id="89682-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="89682-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89682-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89682-121">-InputObject</span></span>
<span data-ttu-id="89682-122">Az indító objektum.</span><span class="sxs-lookup"><span data-stu-id="89682-122">The trigger object.</span></span>

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

### <span data-ttu-id="89682-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="89682-123">-Name</span></span>
<span data-ttu-id="89682-124">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="89682-124">The trigger name.</span></span>

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

### <span data-ttu-id="89682-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="89682-125">-WorkspaceName</span></span>
<span data-ttu-id="89682-126">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="89682-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="89682-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="89682-127">-WorkspaceObject</span></span>
<span data-ttu-id="89682-128">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="89682-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="89682-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89682-129">CommonParameters</span></span>
<span data-ttu-id="89682-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="89682-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89682-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="89682-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89682-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="89682-132">INPUTS</span></span>

### <span data-ttu-id="89682-133">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="89682-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="89682-134">Microsoft. Azure. commands. szinapszis. models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="89682-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="89682-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89682-135">OUTPUTS</span></span>

### <span data-ttu-id="89682-136">Microsoft. Azure. commands. szinapszis. models. PSTriggerSubscriptionOperationStatus</span><span class="sxs-lookup"><span data-stu-id="89682-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span></span>

## <span data-ttu-id="89682-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="89682-137">NOTES</span></span>

## <span data-ttu-id="89682-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89682-138">RELATED LINKS</span></span>
