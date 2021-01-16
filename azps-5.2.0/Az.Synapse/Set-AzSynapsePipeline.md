---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
ms.openlocfilehash: 2bce821f55b5f8ff39f56fa8a6960cb1f99b47d0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354233"
---
# <span data-ttu-id="dcf62-101">Set-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="dcf62-101">Set-AzSynapsePipeline</span></span>

## <span data-ttu-id="dcf62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcf62-102">SYNOPSIS</span></span>
<span data-ttu-id="dcf62-103">Létrehoz egy prognózist a munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="dcf62-103">Creates a pipeline in workspace.</span></span>

## <span data-ttu-id="dcf62-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dcf62-104">SYNTAX</span></span>

### <span data-ttu-id="dcf62-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dcf62-105">SetByName (Default)</span></span>
```
Set-AzSynapsePipeline -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcf62-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="dcf62-106">SetByObject</span></span>
```
Set-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcf62-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dcf62-107">DESCRIPTION</span></span>
<span data-ttu-id="dcf62-108">A **Set-AzSynapsePipeline** parancsmag létrehoz egy folyamatot a munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="dcf62-108">The **Set-AzSynapsePipeline** cmdlet creates a pipeline in workspace.</span></span>

## <span data-ttu-id="dcf62-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dcf62-109">EXAMPLES</span></span>

### <span data-ttu-id="dcf62-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="dcf62-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="dcf62-111">Ez a parancs létrehoz egy ContosoPipeline nevű prognózist a ContosoWorkspace nevű munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="dcf62-111">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="dcf62-112">A parancs a folyamat alapja a fájlon pipeline.jsadatok.</span><span class="sxs-lookup"><span data-stu-id="dcf62-112">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="dcf62-113">Ez a fájl információkat tartalmaz a tevékenységekről.</span><span class="sxs-lookup"><span data-stu-id="dcf62-113">This file includes information about activities.</span></span>

### <span data-ttu-id="dcf62-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="dcf62-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapsePipeline -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="dcf62-115">Ez a parancs létrehoz egy ContosoPipeline nevű prognózist a ContosoWorkspace nevű munkaterületen a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="dcf62-115">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>
<span data-ttu-id="dcf62-116">A parancs a folyamat alapja a fájlon pipeline.jsadatok.</span><span class="sxs-lookup"><span data-stu-id="dcf62-116">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="dcf62-117">Ez a fájl információkat tartalmaz a tevékenységekről.</span><span class="sxs-lookup"><span data-stu-id="dcf62-117">This file includes information about activities.</span></span>

## <span data-ttu-id="dcf62-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dcf62-118">PARAMETERS</span></span>

### <span data-ttu-id="dcf62-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dcf62-119">-AsJob</span></span>
<span data-ttu-id="dcf62-120">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="dcf62-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dcf62-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcf62-121">-DefaultProfile</span></span>
<span data-ttu-id="dcf62-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dcf62-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcf62-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="dcf62-123">-DefinitionFile</span></span>
<span data-ttu-id="dcf62-124">A JSON fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="dcf62-124">The JSON file path.</span></span>

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

### <span data-ttu-id="dcf62-125">-Name</span><span class="sxs-lookup"><span data-stu-id="dcf62-125">-Name</span></span>
<span data-ttu-id="dcf62-126">A folyamat neve.</span><span class="sxs-lookup"><span data-stu-id="dcf62-126">The pipeline name.</span></span>

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

### <span data-ttu-id="dcf62-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="dcf62-127">-WorkspaceName</span></span>
<span data-ttu-id="dcf62-128">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="dcf62-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="dcf62-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="dcf62-129">-WorkspaceObject</span></span>
<span data-ttu-id="dcf62-130">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="dcf62-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="dcf62-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dcf62-131">-Confirm</span></span>
<span data-ttu-id="dcf62-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="dcf62-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcf62-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcf62-133">-WhatIf</span></span>
<span data-ttu-id="dcf62-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="dcf62-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcf62-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dcf62-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcf62-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcf62-136">CommonParameters</span></span>
<span data-ttu-id="dcf62-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcf62-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcf62-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dcf62-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcf62-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dcf62-139">INPUTS</span></span>

### <span data-ttu-id="dcf62-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="dcf62-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="dcf62-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dcf62-141">OUTPUTS</span></span>

### <span data-ttu-id="dcf62-142">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="dcf62-142">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="dcf62-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dcf62-143">NOTES</span></span>

## <span data-ttu-id="dcf62-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dcf62-144">RELATED LINKS</span></span>
