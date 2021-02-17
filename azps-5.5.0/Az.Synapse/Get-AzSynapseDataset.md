---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
ms.openlocfilehash: 8919c554fb32a102991b9c40236e897662709ccb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164626"
---
# <span data-ttu-id="077cf-101">Get-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="077cf-101">Get-AzSynapseDataset</span></span>

## <span data-ttu-id="077cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="077cf-102">SYNOPSIS</span></span>
<span data-ttu-id="077cf-103">Információkat kap a munkaterületen található adatkészletekkel kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="077cf-103">Gets information about datasets in workspace.</span></span>

## <span data-ttu-id="077cf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="077cf-104">SYNTAX</span></span>

### <span data-ttu-id="077cf-105">GetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="077cf-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataset -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="077cf-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="077cf-106">GetByObject</span></span>
```
Get-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="077cf-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="077cf-107">DESCRIPTION</span></span>
<span data-ttu-id="077cf-108">A **Get-AzSynapseDataset** parancsmag információt kap a munkaterületen található adatkészletekkel kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="077cf-108">The **Get-AzSynapseDataset** cmdlet gets information about datasets in workspace.</span></span>
<span data-ttu-id="077cf-109">Ha megadja egy adatkészlet nevét, ez a parancsmag információt kap az adatkészletről.</span><span class="sxs-lookup"><span data-stu-id="077cf-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="077cf-110">Ha nem ad meg nevet, ez a parancsmag információt kap a munkaterületen található összes adatkészletről.</span><span class="sxs-lookup"><span data-stu-id="077cf-110">If you do not specify a name, this cmdlet gets information about all the datasets in the workspace.</span></span>

## <span data-ttu-id="077cf-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="077cf-111">EXAMPLES</span></span>

### <span data-ttu-id="077cf-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="077cf-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="077cf-113">Ez a parancs információkat kap a ContosoWorkspace nevű munkaterületen található összes adatkészletről.</span><span class="sxs-lookup"><span data-stu-id="077cf-113">This command gets information about all datasets in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="077cf-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="077cf-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="077cf-115">Ez a parancs információkat kap a ContosoDataset nevű adatkészletről a ContosoWorkspace nevű munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="077cf-115">This command gets information about the dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="077cf-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="077cf-116">PARAMETERS</span></span>

### <span data-ttu-id="077cf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="077cf-117">-DefaultProfile</span></span>
<span data-ttu-id="077cf-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="077cf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="077cf-119">-Name</span><span class="sxs-lookup"><span data-stu-id="077cf-119">-Name</span></span>
<span data-ttu-id="077cf-120">Az adatkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="077cf-120">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="077cf-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="077cf-121">-WorkspaceName</span></span>
<span data-ttu-id="077cf-122">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="077cf-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="077cf-123">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="077cf-123">-WorkspaceObject</span></span>
<span data-ttu-id="077cf-124">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="077cf-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="077cf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="077cf-125">CommonParameters</span></span>
<span data-ttu-id="077cf-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="077cf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="077cf-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="077cf-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="077cf-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="077cf-128">INPUTS</span></span>

### <span data-ttu-id="077cf-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="077cf-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="077cf-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="077cf-130">OUTPUTS</span></span>

### <span data-ttu-id="077cf-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="077cf-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="077cf-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="077cf-132">NOTES</span></span>

## <span data-ttu-id="077cf-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="077cf-133">RELATED LINKS</span></span>
