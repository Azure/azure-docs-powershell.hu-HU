---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
ms.openlocfilehash: b70c30b7652c331571030917057339a9d2d7de3e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924345"
---
# <span data-ttu-id="1e523-101">Remove-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="1e523-101">Remove-AzSynapseDataset</span></span>

## <span data-ttu-id="1e523-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e523-102">SYNOPSIS</span></span>
<span data-ttu-id="1e523-103">Eltávolít egy adatkészletet a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="1e523-103">Removes a dataset from workspace.</span></span>

## <span data-ttu-id="1e523-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1e523-104">SYNTAX</span></span>

### <span data-ttu-id="1e523-105">RemoveByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1e523-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataset -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e523-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="1e523-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e523-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="1e523-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataset -InputObject <PSDatasetResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e523-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1e523-108">DESCRIPTION</span></span>
<span data-ttu-id="1e523-109">A **Remove-AzSynapseDataset** parancsmag eltávolítja az adatkészletet a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="1e523-109">The **Remove-AzSynapseDataset** cmdlet removes a dataset from workspace.</span></span>

## <span data-ttu-id="1e523-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1e523-110">EXAMPLES</span></span>

### <span data-ttu-id="1e523-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="1e523-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="1e523-112">Ez a parancs eltávolítja a ContosoDataset nevű adatkészletet a ContosoWorkspace nevű munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="1e523-112">This command removes the dataset named ContosoDataset from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="1e523-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e523-113">PARAMETERS</span></span>

### <span data-ttu-id="1e523-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e523-114">-AsJob</span></span>
<span data-ttu-id="1e523-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1e523-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e523-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e523-116">-DefaultProfile</span></span>
<span data-ttu-id="1e523-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1e523-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e523-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1e523-118">-Force</span></span>
<span data-ttu-id="1e523-119">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1e523-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1e523-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e523-120">-InputObject</span></span>
<span data-ttu-id="1e523-121">Az adatkészlet-objektum.</span><span class="sxs-lookup"><span data-stu-id="1e523-121">The dataset object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e523-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1e523-122">-Name</span></span>
<span data-ttu-id="1e523-123">Az adatkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="1e523-123">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: DatasetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e523-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e523-124">-PassThru</span></span>
<span data-ttu-id="1e523-125">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="1e523-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="1e523-126">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="1e523-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="1e523-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1e523-127">-WorkspaceName</span></span>
<span data-ttu-id="1e523-128">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="1e523-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e523-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1e523-129">-WorkspaceObject</span></span>
<span data-ttu-id="1e523-130">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="1e523-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e523-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e523-131">-Confirm</span></span>
<span data-ttu-id="1e523-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1e523-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e523-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e523-133">-WhatIf</span></span>
<span data-ttu-id="1e523-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1e523-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e523-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1e523-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e523-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e523-136">CommonParameters</span></span>
<span data-ttu-id="1e523-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e523-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e523-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e523-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e523-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1e523-139">INPUTS</span></span>

### <span data-ttu-id="1e523-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1e523-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="1e523-141">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="1e523-141">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="1e523-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e523-142">OUTPUTS</span></span>

### <span data-ttu-id="1e523-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1e523-143">System.Boolean</span></span>

## <span data-ttu-id="1e523-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1e523-144">NOTES</span></span>

## <span data-ttu-id="1e523-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e523-145">RELATED LINKS</span></span>
