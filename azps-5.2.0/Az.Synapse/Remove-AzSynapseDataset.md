---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
ms.openlocfilehash: 68da67d2a29b6f05ed50adc9eb8aef343a7e973b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368954"
---
# <span data-ttu-id="6b210-101">Remove-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="6b210-101">Remove-AzSynapseDataset</span></span>

## <span data-ttu-id="6b210-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b210-102">SYNOPSIS</span></span>
<span data-ttu-id="6b210-103">Eltávolít egy adatkészletet a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="6b210-103">Removes a dataset from workspace.</span></span>

## <span data-ttu-id="6b210-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6b210-104">SYNTAX</span></span>

### <span data-ttu-id="6b210-105">RemoveByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6b210-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataset -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b210-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="6b210-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b210-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="6b210-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataset -InputObject <PSDatasetResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b210-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6b210-108">DESCRIPTION</span></span>
<span data-ttu-id="6b210-109">A **Remove-AzSynapseDataset** parancsmag eltávolítja az adatkészletet a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="6b210-109">The **Remove-AzSynapseDataset** cmdlet removes a dataset from workspace.</span></span>

## <span data-ttu-id="6b210-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6b210-110">EXAMPLES</span></span>

### <span data-ttu-id="6b210-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="6b210-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="6b210-112">Ez a parancs eltávolítja a ContosoDataset nevű adatkészletet a ContosoWorkspace nevű munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="6b210-112">This command removes the dataset named ContosoDataset from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="6b210-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b210-113">PARAMETERS</span></span>

### <span data-ttu-id="6b210-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b210-114">-AsJob</span></span>
<span data-ttu-id="6b210-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6b210-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b210-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b210-116">-DefaultProfile</span></span>
<span data-ttu-id="6b210-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b210-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b210-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6b210-118">-Force</span></span>
<span data-ttu-id="6b210-119">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6b210-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6b210-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b210-120">-InputObject</span></span>
<span data-ttu-id="6b210-121">Az adatkészlet-objektum.</span><span class="sxs-lookup"><span data-stu-id="6b210-121">The dataset object.</span></span>

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

### <span data-ttu-id="6b210-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6b210-122">-Name</span></span>
<span data-ttu-id="6b210-123">Az adatkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="6b210-123">The dataset name.</span></span>

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

### <span data-ttu-id="6b210-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b210-124">-PassThru</span></span>
<span data-ttu-id="6b210-125">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="6b210-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="6b210-126">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="6b210-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="6b210-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6b210-127">-WorkspaceName</span></span>
<span data-ttu-id="6b210-128">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="6b210-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6b210-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6b210-129">-WorkspaceObject</span></span>
<span data-ttu-id="6b210-130">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="6b210-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6b210-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b210-131">-Confirm</span></span>
<span data-ttu-id="6b210-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6b210-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b210-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b210-133">-WhatIf</span></span>
<span data-ttu-id="6b210-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6b210-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b210-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6b210-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b210-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b210-136">CommonParameters</span></span>
<span data-ttu-id="6b210-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b210-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b210-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b210-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b210-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b210-139">INPUTS</span></span>

### <span data-ttu-id="6b210-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6b210-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6b210-141">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="6b210-141">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="6b210-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b210-142">OUTPUTS</span></span>

### <span data-ttu-id="6b210-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6b210-143">System.Boolean</span></span>

## <span data-ttu-id="6b210-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6b210-144">NOTES</span></span>

## <span data-ttu-id="6b210-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b210-145">RELATED LINKS</span></span>
