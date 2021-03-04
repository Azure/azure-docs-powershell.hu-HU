---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
ms.openlocfilehash: 6161a0ca463973fad1ac7bac5df6487cf23cd0e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926210"
---
# <span data-ttu-id="749c4-101">Get-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="749c4-101">Get-AzSynapsePipeline</span></span>

## <span data-ttu-id="749c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="749c4-102">SYNOPSIS</span></span>
<span data-ttu-id="749c4-103">Információkat kap a munkaterületen található prognózisról.</span><span class="sxs-lookup"><span data-stu-id="749c4-103">Gets information about pipelines in workspace.</span></span>

## <span data-ttu-id="749c4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="749c4-104">SYNTAX</span></span>

### <span data-ttu-id="749c4-105">GetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="749c4-105">GetByName (Default)</span></span>
```
Get-AzSynapsePipeline -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="749c4-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="749c4-106">GetByObject</span></span>
```
Get-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="749c4-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="749c4-107">DESCRIPTION</span></span>
<span data-ttu-id="749c4-108">A **Get-AzSynapsePipeline** parancsmag információt kap a munkaterületen található prognózisról.</span><span class="sxs-lookup"><span data-stu-id="749c4-108">The **Get-AzSynapsePipeline** cmdlet gets information about pipelines in workspace.</span></span> <span data-ttu-id="749c4-109">Ha megadja egy folyamat nevét, ez a parancsmag információt kap a folyamatról.</span><span class="sxs-lookup"><span data-stu-id="749c4-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span> <span data-ttu-id="749c4-110">Ha nem ad meg nevet, ez a parancsmag információt kap a munkaterületen található összes folyamatról.</span><span class="sxs-lookup"><span data-stu-id="749c4-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the workspace.</span></span>

## <span data-ttu-id="749c4-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="749c4-111">EXAMPLES</span></span>

### <span data-ttu-id="749c4-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="749c4-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="749c4-113">Ez a parancs információkat kap a ContosoWorkspace nevű munkaterületen található összes folyamatról.</span><span class="sxs-lookup"><span data-stu-id="749c4-113">This command gets information about all pipelines in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="749c4-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="749c4-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="749c4-115">Ez a parancs információkat kap a ContosoPipeline nevű folyamatról a ContosoWorkspace nevű munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="749c4-115">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="749c4-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="749c4-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="749c4-117">Ez a parancs információkat kap a ContosoPipeline nevű folyamatról a ContosoWorkspace nevű munkaterületen a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="749c4-117">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="749c4-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="749c4-118">PARAMETERS</span></span>

### <span data-ttu-id="749c4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="749c4-119">-DefaultProfile</span></span>
<span data-ttu-id="749c4-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="749c4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="749c4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="749c4-121">-Name</span></span>
<span data-ttu-id="749c4-122">A folyamat neve.</span><span class="sxs-lookup"><span data-stu-id="749c4-122">The pipeline name.</span></span>

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

### <span data-ttu-id="749c4-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="749c4-123">-WorkspaceName</span></span>
<span data-ttu-id="749c4-124">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="749c4-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="749c4-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="749c4-125">-WorkspaceObject</span></span>
<span data-ttu-id="749c4-126">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="749c4-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="749c4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="749c4-127">CommonParameters</span></span>
<span data-ttu-id="749c4-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="749c4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="749c4-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="749c4-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="749c4-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="749c4-130">INPUTS</span></span>

### <span data-ttu-id="749c4-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="749c4-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="749c4-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="749c4-132">OUTPUTS</span></span>

### <span data-ttu-id="749c4-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="749c4-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="749c4-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="749c4-134">NOTES</span></span>

## <span data-ttu-id="749c4-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="749c4-135">RELATED LINKS</span></span>
