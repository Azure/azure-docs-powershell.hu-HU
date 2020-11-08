---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
ms.openlocfilehash: 6224a871aebff834693c8eed3026a75f22879ffa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194165"
---
# <span data-ttu-id="37cd0-101">Get-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="37cd0-101">Get-AzSynapsePipeline</span></span>

## <span data-ttu-id="37cd0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="37cd0-102">SYNOPSIS</span></span>
<span data-ttu-id="37cd0-103">Információt kap a munkaterületen lévő csővezetékekről.</span><span class="sxs-lookup"><span data-stu-id="37cd0-103">Gets information about pipelines in workspace.</span></span>

## <span data-ttu-id="37cd0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="37cd0-104">SYNTAX</span></span>

### <span data-ttu-id="37cd0-105">GetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="37cd0-105">GetByName (Default)</span></span>
```
Get-AzSynapsePipeline -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="37cd0-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="37cd0-106">GetByObject</span></span>
```
Get-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37cd0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="37cd0-107">DESCRIPTION</span></span>
<span data-ttu-id="37cd0-108">A **Get-AzSynapsePipeline** parancsmag információkat kap a munkaterület-munkafolyamatokról.</span><span class="sxs-lookup"><span data-stu-id="37cd0-108">The **Get-AzSynapsePipeline** cmdlet gets information about pipelines in workspace.</span></span> <span data-ttu-id="37cd0-109">Ha megad egy csővezeték nevét, ez a parancsmag információkat kap a csővezetékről.</span><span class="sxs-lookup"><span data-stu-id="37cd0-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span> <span data-ttu-id="37cd0-110">Ha nem ad meg nevet, ez a parancsmag információkat kap a munkaterület összes csővezetékéről.</span><span class="sxs-lookup"><span data-stu-id="37cd0-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the workspace.</span></span>

## <span data-ttu-id="37cd0-111">Példák</span><span class="sxs-lookup"><span data-stu-id="37cd0-111">EXAMPLES</span></span>

### <span data-ttu-id="37cd0-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="37cd0-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="37cd0-113">Ez a parancs a ContosoWorkspace nevű munkaterületen lévő összes csővezetékről információt kap.</span><span class="sxs-lookup"><span data-stu-id="37cd0-113">This command gets information about all pipelines in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="37cd0-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="37cd0-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="37cd0-115">Ez a parancs a ContosoWorkspace nevű munkaterületen a ContosoPipeline nevű csővezetékről kap információkat.</span><span class="sxs-lookup"><span data-stu-id="37cd0-115">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="37cd0-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="37cd0-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="37cd0-117">Ez a parancs információt kap a ContosoPipeline nevű pipeline-munkaterületről a ContosoWorkspace – csővezeték nevű munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="37cd0-117">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="37cd0-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="37cd0-118">PARAMETERS</span></span>

### <span data-ttu-id="37cd0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37cd0-119">-DefaultProfile</span></span>
<span data-ttu-id="37cd0-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="37cd0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37cd0-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="37cd0-121">-Name</span></span>
<span data-ttu-id="37cd0-122">A csővezeték neve.</span><span class="sxs-lookup"><span data-stu-id="37cd0-122">The pipeline name.</span></span>

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

### <span data-ttu-id="37cd0-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="37cd0-123">-WorkspaceName</span></span>
<span data-ttu-id="37cd0-124">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="37cd0-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="37cd0-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="37cd0-125">-WorkspaceObject</span></span>
<span data-ttu-id="37cd0-126">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="37cd0-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="37cd0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37cd0-127">CommonParameters</span></span>
<span data-ttu-id="37cd0-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="37cd0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37cd0-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="37cd0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37cd0-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="37cd0-130">INPUTS</span></span>

### <span data-ttu-id="37cd0-131">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="37cd0-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="37cd0-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="37cd0-132">OUTPUTS</span></span>

### <span data-ttu-id="37cd0-133">Microsoft. Azure. commands. szinapszis. models. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="37cd0-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="37cd0-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="37cd0-134">NOTES</span></span>

## <span data-ttu-id="37cd0-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="37cd0-135">RELATED LINKS</span></span>
