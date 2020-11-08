---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
ms.openlocfilehash: 365311b156b8bd6f2c61da760c6b82a3b2d5dfb4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181223"
---
# <span data-ttu-id="0a3ce-101">Get-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="0a3ce-101">Get-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="0a3ce-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0a3ce-102">SYNOPSIS</span></span>
<span data-ttu-id="0a3ce-103">Információt kap a csővezetékről.</span><span class="sxs-lookup"><span data-stu-id="0a3ce-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="0a3ce-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0a3ce-104">SYNTAX</span></span>

### <span data-ttu-id="0a3ce-105">GetByNameAndId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0a3ce-105">GetByNameAndId (Default)</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a3ce-106">GetByNameAndTime</span><span class="sxs-lookup"><span data-stu-id="0a3ce-106">GetByNameAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0a3ce-107">GetByObjectAndId</span><span class="sxs-lookup"><span data-stu-id="0a3ce-107">GetByObjectAndId</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a3ce-108">GetByObjectAndTime</span><span class="sxs-lookup"><span data-stu-id="0a3ce-108">GetByObjectAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0a3ce-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="0a3ce-109">DESCRIPTION</span></span>
<span data-ttu-id="0a3ce-110">A **Get-AzSynapsePipelineRun** parancs a megadott csővezetéken futó futásokra vonatkozó információkat adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="0a3ce-110">The **Get-AzSynapsePipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="0a3ce-111">Ha a PipelineRunId meg van adva, az adott AZONOSÍTÓval végzett Futtatás részleteit jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="0a3ce-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="0a3ce-112">Ha a PipelineRunId nem adja meg, akkor a RunStartedAfter és a RunStartedBefore értékek közötti csővezetékek esetén az összes futóról szóló információt jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="0a3ce-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of RunStartedAfter and RunStartedBefore.</span></span>

## <span data-ttu-id="0a3ce-113">Példák</span><span class="sxs-lookup"><span data-stu-id="0a3ce-113">EXAMPLES</span></span>

### <span data-ttu-id="0a3ce-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0a3ce-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"
```

<span data-ttu-id="0a3ce-115">Ez a parancs részletesen ismerteti az "61eb095a-FE23-4591-8a97-fade6c65ca72" AZONOSÍTÓJÚ pipeline-kapcsolat adatait.</span><span class="sxs-lookup"><span data-stu-id="0a3ce-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="0a3ce-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0a3ce-116">PARAMETERS</span></span>

### <span data-ttu-id="0a3ce-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a3ce-117">-DefaultProfile</span></span>
<span data-ttu-id="0a3ce-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0a3ce-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a3ce-119">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="0a3ce-119">-PipelineName</span></span>
<span data-ttu-id="0a3ce-120">A csővezeték neve.</span><span class="sxs-lookup"><span data-stu-id="0a3ce-120">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a3ce-121">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="0a3ce-121">-PipelineRunId</span></span>
<span data-ttu-id="0a3ce-122">A pipeline-Run azonosító.</span><span class="sxs-lookup"><span data-stu-id="0a3ce-122">The pipeline run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndId, GetByObjectAndId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a3ce-123">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="0a3ce-123">-RunStartedAfter</span></span>
<span data-ttu-id="0a3ce-124">A futási esemény "ISO 8601" formátumban való frissítésének időpontja.</span><span class="sxs-lookup"><span data-stu-id="0a3ce-124">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a3ce-125">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="0a3ce-125">-RunStartedBefore</span></span>
<span data-ttu-id="0a3ce-126">A futási esemény "ISO 8601" formátumban való frissítésének időpontja.</span><span class="sxs-lookup"><span data-stu-id="0a3ce-126">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a3ce-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0a3ce-127">-WorkspaceName</span></span>
<span data-ttu-id="0a3ce-128">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="0a3ce-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndId, GetByNameAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a3ce-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0a3ce-129">-WorkspaceObject</span></span>
<span data-ttu-id="0a3ce-130">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="0a3ce-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObjectAndId, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a3ce-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a3ce-131">CommonParameters</span></span>
<span data-ttu-id="0a3ce-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0a3ce-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a3ce-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0a3ce-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a3ce-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a3ce-134">INPUTS</span></span>

### <span data-ttu-id="0a3ce-135">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0a3ce-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="0a3ce-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a3ce-136">OUTPUTS</span></span>

### <span data-ttu-id="0a3ce-137">Microsoft. Azure. commands. szinapszis. models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="0a3ce-137">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="0a3ce-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0a3ce-138">NOTES</span></span>

## <span data-ttu-id="0a3ce-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a3ce-139">RELATED LINKS</span></span>
