---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
ms.openlocfilehash: 1001aa2f282ab59e6ddc9e3e1ecc654950d8e30e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919098"
---
# <span data-ttu-id="84153-101">Set-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="84153-101">Set-AzSynapseDataset</span></span>

## <span data-ttu-id="84153-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84153-102">SYNOPSIS</span></span>
<span data-ttu-id="84153-103">Munkaterületen hoz létre vagy frissíti az adatkészletet.</span><span class="sxs-lookup"><span data-stu-id="84153-103">Creates or updates a dataset in workspace.</span></span>

## <span data-ttu-id="84153-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="84153-104">SYNTAX</span></span>

### <span data-ttu-id="84153-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="84153-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataset -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84153-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="84153-106">SetByObject</span></span>
```
Set-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84153-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="84153-107">DESCRIPTION</span></span>
<span data-ttu-id="84153-108">A **Set-AzSynapseDataset** parancsmag létrehoz egy adatkészletet, vagy frissíti a munkaterületen meglévő adatkészletet.</span><span class="sxs-lookup"><span data-stu-id="84153-108">The **Set-AzSynapseDataset** cmdlet creates a dataset or updates an existing dataset in workspace.</span></span>

## <span data-ttu-id="84153-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="84153-109">EXAMPLES</span></span>

### <span data-ttu-id="84153-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="84153-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset -DefinitionFile "C:\\samples\\Dataset.json"
```

<span data-ttu-id="84153-111">Ez a parancs létrehoz egy ContosoDataset nevű adatkészletet a ContosoWorkspace nevű munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="84153-111">This command creates a dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="84153-112">A parancs az adatkészletet a fájlon Dataset.jsalapján.</span><span class="sxs-lookup"><span data-stu-id="84153-112">The command bases the dataset on information in the Dataset.json file.</span></span>

## <span data-ttu-id="84153-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84153-113">PARAMETERS</span></span>

### <span data-ttu-id="84153-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84153-114">-AsJob</span></span>
<span data-ttu-id="84153-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="84153-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="84153-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84153-116">-DefaultProfile</span></span>
<span data-ttu-id="84153-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="84153-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84153-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="84153-118">-DefinitionFile</span></span>
<span data-ttu-id="84153-119">A JSON fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="84153-119">The JSON file path.</span></span>

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

### <span data-ttu-id="84153-120">-Name</span><span class="sxs-lookup"><span data-stu-id="84153-120">-Name</span></span>
<span data-ttu-id="84153-121">Az adatkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="84153-121">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84153-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="84153-122">-WorkspaceName</span></span>
<span data-ttu-id="84153-123">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="84153-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="84153-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="84153-124">-WorkspaceObject</span></span>
<span data-ttu-id="84153-125">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="84153-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="84153-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84153-126">-Confirm</span></span>
<span data-ttu-id="84153-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="84153-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84153-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84153-128">-WhatIf</span></span>
<span data-ttu-id="84153-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="84153-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84153-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="84153-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84153-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84153-131">CommonParameters</span></span>
<span data-ttu-id="84153-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84153-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84153-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84153-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84153-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="84153-134">INPUTS</span></span>

### <span data-ttu-id="84153-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="84153-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="84153-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84153-136">OUTPUTS</span></span>

### <span data-ttu-id="84153-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="84153-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="84153-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="84153-138">NOTES</span></span>

## <span data-ttu-id="84153-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84153-139">RELATED LINKS</span></span>
