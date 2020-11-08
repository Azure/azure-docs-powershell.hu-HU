---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
ms.openlocfilehash: 2bce821f55b5f8ff39f56fa8a6960cb1f99b47d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187905"
---
# <span data-ttu-id="97227-101">Set-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="97227-101">Set-AzSynapsePipeline</span></span>

## <span data-ttu-id="97227-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="97227-102">SYNOPSIS</span></span>
<span data-ttu-id="97227-103">Futószalagot hoz létre a munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="97227-103">Creates a pipeline in workspace.</span></span>

## <span data-ttu-id="97227-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="97227-104">SYNTAX</span></span>

### <span data-ttu-id="97227-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="97227-105">SetByName (Default)</span></span>
```
Set-AzSynapsePipeline -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97227-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="97227-106">SetByObject</span></span>
```
Set-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97227-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="97227-107">DESCRIPTION</span></span>
<span data-ttu-id="97227-108">A **set-AzSynapsePipeline** parancsmag létrehoz egy csővezetéket a munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="97227-108">The **Set-AzSynapsePipeline** cmdlet creates a pipeline in workspace.</span></span>

## <span data-ttu-id="97227-109">Példák</span><span class="sxs-lookup"><span data-stu-id="97227-109">EXAMPLES</span></span>

### <span data-ttu-id="97227-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="97227-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="97227-111">Ez a parancs létrehoz egy ContosoPipeline nevű csővezetéket a ContosoWorkspace nevű munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="97227-111">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="97227-112">A parancs a munkafolyamatot a fájl pipeline.jsban lévő adatokra alapozja.</span><span class="sxs-lookup"><span data-stu-id="97227-112">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="97227-113">Ez a fájl a tevékenységekről tartalmaz információkat.</span><span class="sxs-lookup"><span data-stu-id="97227-113">This file includes information about activities.</span></span>

### <span data-ttu-id="97227-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="97227-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapsePipeline -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="97227-115">Ez a parancs létrehoz egy ContosoPipeline nevű csővezetéket a ContosoWorkspace – csővezeték nevű munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="97227-115">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>
<span data-ttu-id="97227-116">A parancs a munkafolyamatot a fájl pipeline.jsban lévő adatokra alapozja.</span><span class="sxs-lookup"><span data-stu-id="97227-116">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="97227-117">Ez a fájl a tevékenységekről tartalmaz információkat.</span><span class="sxs-lookup"><span data-stu-id="97227-117">This file includes information about activities.</span></span>

## <span data-ttu-id="97227-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="97227-118">PARAMETERS</span></span>

### <span data-ttu-id="97227-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97227-119">-AsJob</span></span>
<span data-ttu-id="97227-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="97227-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97227-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97227-121">-DefaultProfile</span></span>
<span data-ttu-id="97227-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="97227-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97227-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="97227-123">-DefinitionFile</span></span>
<span data-ttu-id="97227-124">A JSON-fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="97227-124">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97227-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="97227-125">-Name</span></span>
<span data-ttu-id="97227-126">A csővezeték neve.</span><span class="sxs-lookup"><span data-stu-id="97227-126">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97227-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="97227-127">-WorkspaceName</span></span>
<span data-ttu-id="97227-128">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="97227-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97227-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="97227-129">-WorkspaceObject</span></span>
<span data-ttu-id="97227-130">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="97227-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97227-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="97227-131">-Confirm</span></span>
<span data-ttu-id="97227-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="97227-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97227-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97227-133">-WhatIf</span></span>
<span data-ttu-id="97227-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="97227-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97227-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="97227-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97227-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97227-136">CommonParameters</span></span>
<span data-ttu-id="97227-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="97227-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97227-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="97227-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97227-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="97227-139">INPUTS</span></span>

### <span data-ttu-id="97227-140">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="97227-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="97227-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97227-141">OUTPUTS</span></span>

### <span data-ttu-id="97227-142">Microsoft. Azure. commands. szinapszis. models. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="97227-142">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="97227-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="97227-143">NOTES</span></span>

## <span data-ttu-id="97227-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97227-144">RELATED LINKS</span></span>
