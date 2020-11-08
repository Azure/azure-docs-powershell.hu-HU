---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetriggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
ms.openlocfilehash: 0d6d3bb99062177e1d75c4ab496562782cf142c1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187148"
---
# <span data-ttu-id="659ab-101">Get-AzSynapseTriggerRun</span><span class="sxs-lookup"><span data-stu-id="659ab-101">Get-AzSynapseTriggerRun</span></span>

## <span data-ttu-id="659ab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="659ab-102">SYNOPSIS</span></span>
<span data-ttu-id="659ab-103">Információt ad az indításról.</span><span class="sxs-lookup"><span data-stu-id="659ab-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="659ab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="659ab-104">SYNTAX</span></span>

### <span data-ttu-id="659ab-105">GetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="659ab-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceName <String> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="659ab-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="659ab-106">GetByObject</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceObject <PSSynapseWorkspace> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="659ab-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="659ab-107">DESCRIPTION</span></span>
<span data-ttu-id="659ab-108">A **Get-AzSynapseTriggerRun** parancs részletes információt ad az adott időkeretben megadott triggerről.</span><span class="sxs-lookup"><span data-stu-id="659ab-108">The **Get-AzSynapseTriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="659ab-109">Példák</span><span class="sxs-lookup"><span data-stu-id="659ab-109">EXAMPLES</span></span>

### <span data-ttu-id="659ab-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="659ab-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerRun -WorkspaceName ContosoWorkspace -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="659ab-111">Ebben a parancsban a "2018-09-01T21:00" és a "2019-09-01T21:00" között kezdődő ContosoTrigger-ContosoWorkspace futtathatók.</span><span class="sxs-lookup"><span data-stu-id="659ab-111">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00".</span></span>

### <span data-ttu-id="659ab-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="659ab-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerRun -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="659ab-113">Ebben a parancsban a ContosoTrigger-ban futó ContosoWorkspace a "2018-09-01T21:00" és a "2019-09-01T21:00" közötti kapcsolatra vonatkozó információkat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="659ab-113">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00" through pipeline.</span></span>

## <span data-ttu-id="659ab-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="659ab-114">PARAMETERS</span></span>

### <span data-ttu-id="659ab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="659ab-115">-DefaultProfile</span></span>
<span data-ttu-id="659ab-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="659ab-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="659ab-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="659ab-117">-Name</span></span>
<span data-ttu-id="659ab-118">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="659ab-118">The trigger name.</span></span>

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

### <span data-ttu-id="659ab-119">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="659ab-119">-RunStartedAfter</span></span>
<span data-ttu-id="659ab-120">A futási esemény "ISO 8601" formátumban való frissítésének időpontja.</span><span class="sxs-lookup"><span data-stu-id="659ab-120">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="659ab-121">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="659ab-121">-RunStartedBefore</span></span>
<span data-ttu-id="659ab-122">A futási esemény "ISO 8601" formátumban való frissítésének időpontja.</span><span class="sxs-lookup"><span data-stu-id="659ab-122">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="659ab-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="659ab-123">-WorkspaceName</span></span>
<span data-ttu-id="659ab-124">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="659ab-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="659ab-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="659ab-125">-WorkspaceObject</span></span>
<span data-ttu-id="659ab-126">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="659ab-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="659ab-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="659ab-127">CommonParameters</span></span>
<span data-ttu-id="659ab-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="659ab-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="659ab-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="659ab-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="659ab-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="659ab-130">INPUTS</span></span>

### <span data-ttu-id="659ab-131">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="659ab-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="659ab-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="659ab-132">OUTPUTS</span></span>

### <span data-ttu-id="659ab-133">Microsoft. Azure. commands. szinapszis. models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="659ab-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerRun</span></span>

## <span data-ttu-id="659ab-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="659ab-134">NOTES</span></span>

## <span data-ttu-id="659ab-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="659ab-135">RELATED LINKS</span></span>
