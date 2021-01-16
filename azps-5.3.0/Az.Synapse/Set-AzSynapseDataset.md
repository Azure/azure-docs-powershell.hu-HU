---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
ms.openlocfilehash: d2471320a27b1af96dba6b5e2b552a01ff5b50e3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383233"
---
# <span data-ttu-id="9a8bd-101">Set-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="9a8bd-101">Set-AzSynapseDataset</span></span>

## <span data-ttu-id="9a8bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a8bd-102">SYNOPSIS</span></span>
<span data-ttu-id="9a8bd-103">Munkaterületen hoz létre vagy frissíti az adatkészletet.</span><span class="sxs-lookup"><span data-stu-id="9a8bd-103">Creates or updates a dataset in workspace.</span></span>

## <span data-ttu-id="9a8bd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9a8bd-104">SYNTAX</span></span>

### <span data-ttu-id="9a8bd-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9a8bd-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataset -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a8bd-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="9a8bd-106">SetByObject</span></span>
```
Set-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a8bd-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9a8bd-107">DESCRIPTION</span></span>
<span data-ttu-id="9a8bd-108">A **Set-AzSynapseDataset** parancsmag létrehoz egy adatkészletet, vagy frissíti a munkaterületen meglévő adatkészletet.</span><span class="sxs-lookup"><span data-stu-id="9a8bd-108">The **Set-AzSynapseDataset** cmdlet creates a dataset or updates an existing dataset in workspace.</span></span>

## <span data-ttu-id="9a8bd-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9a8bd-109">EXAMPLES</span></span>

### <span data-ttu-id="9a8bd-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="9a8bd-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset -DefinitionFile "C:\\samples\\Dataset.json"
```

<span data-ttu-id="9a8bd-111">Ez a parancs létrehoz egy ContosoDataset nevű adatkészletet a ContosoWorkspace nevű munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="9a8bd-111">This command creates a dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="9a8bd-112">A parancs az adatkészletet a fájlon Dataset.jsalapján.</span><span class="sxs-lookup"><span data-stu-id="9a8bd-112">The command bases the dataset on information in the Dataset.json file.</span></span>

## <span data-ttu-id="9a8bd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a8bd-113">PARAMETERS</span></span>

### <span data-ttu-id="9a8bd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a8bd-114">-AsJob</span></span>
<span data-ttu-id="9a8bd-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9a8bd-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a8bd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a8bd-116">-DefaultProfile</span></span>
<span data-ttu-id="9a8bd-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9a8bd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a8bd-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="9a8bd-118">-DefinitionFile</span></span>
<span data-ttu-id="9a8bd-119">A JSON fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="9a8bd-119">The JSON file path.</span></span>

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

### <span data-ttu-id="9a8bd-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9a8bd-120">-Name</span></span>
<span data-ttu-id="9a8bd-121">Az adatkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="9a8bd-121">The dataset name.</span></span>

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

### <span data-ttu-id="9a8bd-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9a8bd-122">-WorkspaceName</span></span>
<span data-ttu-id="9a8bd-123">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="9a8bd-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9a8bd-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9a8bd-124">-WorkspaceObject</span></span>
<span data-ttu-id="9a8bd-125">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="9a8bd-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9a8bd-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a8bd-126">-Confirm</span></span>
<span data-ttu-id="9a8bd-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9a8bd-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a8bd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a8bd-128">-WhatIf</span></span>
<span data-ttu-id="9a8bd-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9a8bd-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a8bd-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9a8bd-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a8bd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a8bd-131">CommonParameters</span></span>
<span data-ttu-id="9a8bd-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a8bd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a8bd-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a8bd-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a8bd-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9a8bd-134">INPUTS</span></span>

### <span data-ttu-id="9a8bd-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9a8bd-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="9a8bd-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a8bd-136">OUTPUTS</span></span>

### <span data-ttu-id="9a8bd-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="9a8bd-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="9a8bd-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9a8bd-138">NOTES</span></span>

## <span data-ttu-id="9a8bd-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a8bd-139">RELATED LINKS</span></span>
