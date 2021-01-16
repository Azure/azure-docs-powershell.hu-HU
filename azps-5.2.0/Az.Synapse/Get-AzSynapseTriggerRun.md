---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetriggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
ms.openlocfilehash: 0d6d3bb99062177e1d75c4ab496562782cf142c1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334049"
---
# <span data-ttu-id="73c46-101">Get-AzSynapseTriggerRun</span><span class="sxs-lookup"><span data-stu-id="73c46-101">Get-AzSynapseTriggerRun</span></span>

## <span data-ttu-id="73c46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73c46-102">SYNOPSIS</span></span>
<span data-ttu-id="73c46-103">Információkat ad vissza az eseményindítók futásról.</span><span class="sxs-lookup"><span data-stu-id="73c46-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="73c46-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="73c46-104">SYNTAX</span></span>

### <span data-ttu-id="73c46-105">GetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="73c46-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceName <String> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73c46-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="73c46-106">GetByObject</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceObject <PSSynapseWorkspace> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73c46-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="73c46-107">DESCRIPTION</span></span>
<span data-ttu-id="73c46-108">A **Get-AzSynapseTriggerRun parancs** részletes információkat ad vissza a megadott eseményindítónak az adott időkeretben való futtatásról.</span><span class="sxs-lookup"><span data-stu-id="73c46-108">The **Get-AzSynapseTriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="73c46-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="73c46-109">EXAMPLES</span></span>

### <span data-ttu-id="73c46-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="73c46-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerRun -WorkspaceName ContosoWorkspace -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="73c46-111">Ez a parancs a "2018-09-01T21:00" és a "2019-09-09-01T21:00" és a "2019-09-01T21:00" közötti munkaterületen futó ContosoTriggerre vonatkozó információkat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="73c46-111">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00".</span></span>

### <span data-ttu-id="73c46-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="73c46-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerRun -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="73c46-113">Ez a parancs a ContosoTrigger munkaterületen a "2018-09-01T21:00" és a "2019-09-09-01T21:00" közötti folyamatra vonatkozó információkat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="73c46-113">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00" through pipeline.</span></span>

## <span data-ttu-id="73c46-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73c46-114">PARAMETERS</span></span>

### <span data-ttu-id="73c46-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73c46-115">-DefaultProfile</span></span>
<span data-ttu-id="73c46-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="73c46-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73c46-117">-Name</span><span class="sxs-lookup"><span data-stu-id="73c46-117">-Name</span></span>
<span data-ttu-id="73c46-118">Az eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="73c46-118">The trigger name.</span></span>

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

### <span data-ttu-id="73c46-119">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="73c46-119">-RunStartedAfter</span></span>
<span data-ttu-id="73c46-120">Az az időpont, amikor vagy amely után a futtatás eseménye "ISO 8601" formátumban frissült.</span><span class="sxs-lookup"><span data-stu-id="73c46-120">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="73c46-121">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="73c46-121">-RunStartedBefore</span></span>
<span data-ttu-id="73c46-122">Az az időpont, amikor vagy amely előtt a futtatás eseménye "ISO 8601" formátumban frissült.</span><span class="sxs-lookup"><span data-stu-id="73c46-122">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="73c46-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="73c46-123">-WorkspaceName</span></span>
<span data-ttu-id="73c46-124">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="73c46-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="73c46-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="73c46-125">-WorkspaceObject</span></span>
<span data-ttu-id="73c46-126">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="73c46-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="73c46-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73c46-127">CommonParameters</span></span>
<span data-ttu-id="73c46-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73c46-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73c46-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73c46-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73c46-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73c46-130">INPUTS</span></span>

### <span data-ttu-id="73c46-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="73c46-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="73c46-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="73c46-132">OUTPUTS</span></span>

### <span data-ttu-id="73c46-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="73c46-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerRun</span></span>

## <span data-ttu-id="73c46-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="73c46-134">NOTES</span></span>

## <span data-ttu-id="73c46-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="73c46-135">RELATED LINKS</span></span>
