---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
ms.openlocfilehash: 6224a871aebff834693c8eed3026a75f22879ffa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339185"
---
# <span data-ttu-id="9b6c3-101">Get-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="9b6c3-101">Get-AzSynapsePipeline</span></span>

## <span data-ttu-id="9b6c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b6c3-102">SYNOPSIS</span></span>
<span data-ttu-id="9b6c3-103">Információkat kap a munkaterületen található prognózisról.</span><span class="sxs-lookup"><span data-stu-id="9b6c3-103">Gets information about pipelines in workspace.</span></span>

## <span data-ttu-id="9b6c3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9b6c3-104">SYNTAX</span></span>

### <span data-ttu-id="9b6c3-105">GetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9b6c3-105">GetByName (Default)</span></span>
```
Get-AzSynapsePipeline -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b6c3-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="9b6c3-106">GetByObject</span></span>
```
Get-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b6c3-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9b6c3-107">DESCRIPTION</span></span>
<span data-ttu-id="9b6c3-108">A **Get-AzSynapsePipeline** parancsmag információt kap a munkaterületen található prognózisról.</span><span class="sxs-lookup"><span data-stu-id="9b6c3-108">The **Get-AzSynapsePipeline** cmdlet gets information about pipelines in workspace.</span></span> <span data-ttu-id="9b6c3-109">Ha megadja egy folyamat nevét, ez a parancsmag információt kap a folyamatról.</span><span class="sxs-lookup"><span data-stu-id="9b6c3-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span> <span data-ttu-id="9b6c3-110">Ha nem ad meg nevet, ez a parancsmag információt kap a munkaterületen található összes folyamatról.</span><span class="sxs-lookup"><span data-stu-id="9b6c3-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the workspace.</span></span>

## <span data-ttu-id="9b6c3-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9b6c3-111">EXAMPLES</span></span>

### <span data-ttu-id="9b6c3-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="9b6c3-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="9b6c3-113">Ez a parancs információkat kap a ContosoWorkspace nevű munkaterületen található összes folyamatról.</span><span class="sxs-lookup"><span data-stu-id="9b6c3-113">This command gets information about all pipelines in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="9b6c3-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="9b6c3-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="9b6c3-115">Ez a parancs információkat kap a ContosoPipeline nevű folyamatról a ContosoWorkspace nevű munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="9b6c3-115">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="9b6c3-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="9b6c3-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="9b6c3-117">Ez a parancs információkat kap a ContosoPipeline nevű folyamatról a ContosoWorkspace nevű munkaterületen a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="9b6c3-117">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="9b6c3-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b6c3-118">PARAMETERS</span></span>

### <span data-ttu-id="9b6c3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b6c3-119">-DefaultProfile</span></span>
<span data-ttu-id="9b6c3-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9b6c3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b6c3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9b6c3-121">-Name</span></span>
<span data-ttu-id="9b6c3-122">A folyamat neve.</span><span class="sxs-lookup"><span data-stu-id="9b6c3-122">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b6c3-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9b6c3-123">-WorkspaceName</span></span>
<span data-ttu-id="9b6c3-124">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="9b6c3-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9b6c3-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9b6c3-125">-WorkspaceObject</span></span>
<span data-ttu-id="9b6c3-126">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="9b6c3-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9b6c3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b6c3-127">CommonParameters</span></span>
<span data-ttu-id="9b6c3-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b6c3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b6c3-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b6c3-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b6c3-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9b6c3-130">INPUTS</span></span>

### <span data-ttu-id="9b6c3-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9b6c3-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="9b6c3-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b6c3-132">OUTPUTS</span></span>

### <span data-ttu-id="9b6c3-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="9b6c3-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="9b6c3-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9b6c3-134">NOTES</span></span>

## <span data-ttu-id="9b6c3-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9b6c3-135">RELATED LINKS</span></span>
