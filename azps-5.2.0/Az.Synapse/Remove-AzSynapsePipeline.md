---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
ms.openlocfilehash: 747658224703a09f98f232deb865adf4bb084682
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365005"
---
# <span data-ttu-id="3a85e-101">Remove-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="3a85e-101">Remove-AzSynapsePipeline</span></span>

## <span data-ttu-id="3a85e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a85e-102">SYNOPSIS</span></span>
<span data-ttu-id="3a85e-103">Eltávolít egy prognózist a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="3a85e-103">Removes a pipeline from workspace.</span></span>

## <span data-ttu-id="3a85e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3a85e-104">SYNTAX</span></span>

### <span data-ttu-id="3a85e-105">RemoveByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3a85e-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapsePipeline -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a85e-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="3a85e-106">RemoveByObject</span></span>
```
Remove-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a85e-107">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="3a85e-107">NewByInputObject</span></span>
```
Remove-AzSynapsePipeline -Name <String> -InputObject <PSPipelineResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a85e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3a85e-108">DESCRIPTION</span></span>
<span data-ttu-id="3a85e-109">A **Remove-AzSynapsePipeline** parancsmag eltávolít egy folyamatot a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="3a85e-109">The **Remove-AzSynapsePipeline** cmdlet removes a pipeline from workspace.</span></span>

## <span data-ttu-id="3a85e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3a85e-110">EXAMPLES</span></span>

### <span data-ttu-id="3a85e-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="3a85e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="3a85e-112">Ez a parancsmag eltávolítja a ContosoPipeline nevű folyamatot a ContosoWorkspace nevű munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="3a85e-112">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="3a85e-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="3a85e-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="3a85e-114">Ez a parancsmag eltávolítja a ContosoPipeline nevű folyamatot a ContosoWorkspace nevű munkaterületről a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="3a85e-114">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="3a85e-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="3a85e-115">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Remove-AzSynapsePipeline
```

<span data-ttu-id="3a85e-116">Ez a parancsmag eltávolítja a ContosoPipeline nevű folyamatot a ContosoWorkspace nevű munkaterületről a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="3a85e-116">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="3a85e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a85e-117">PARAMETERS</span></span>

### <span data-ttu-id="3a85e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a85e-118">-AsJob</span></span>
<span data-ttu-id="3a85e-119">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3a85e-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a85e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a85e-120">-DefaultProfile</span></span>
<span data-ttu-id="3a85e-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3a85e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a85e-122">-Force</span><span class="sxs-lookup"><span data-stu-id="3a85e-122">-Force</span></span>
<span data-ttu-id="3a85e-123">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3a85e-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3a85e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a85e-124">-InputObject</span></span>
<span data-ttu-id="3a85e-125">A folyamatobjektum.</span><span class="sxs-lookup"><span data-stu-id="3a85e-125">The pipeline object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource
Parameter Sets: NewByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a85e-126">-Name</span><span class="sxs-lookup"><span data-stu-id="3a85e-126">-Name</span></span>
<span data-ttu-id="3a85e-127">A folyamat neve.</span><span class="sxs-lookup"><span data-stu-id="3a85e-127">The pipeline name.</span></span>

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

### <span data-ttu-id="3a85e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a85e-128">-PassThru</span></span>
<span data-ttu-id="3a85e-129">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="3a85e-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="3a85e-130">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="3a85e-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="3a85e-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3a85e-131">-WorkspaceName</span></span>
<span data-ttu-id="3a85e-132">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="3a85e-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3a85e-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3a85e-133">-WorkspaceObject</span></span>
<span data-ttu-id="3a85e-134">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="3a85e-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3a85e-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a85e-135">-Confirm</span></span>
<span data-ttu-id="3a85e-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3a85e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a85e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a85e-137">-WhatIf</span></span>
<span data-ttu-id="3a85e-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3a85e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a85e-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3a85e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a85e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a85e-140">CommonParameters</span></span>
<span data-ttu-id="3a85e-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a85e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a85e-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a85e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a85e-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3a85e-143">INPUTS</span></span>

### <span data-ttu-id="3a85e-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3a85e-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="3a85e-145">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="3a85e-145">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="3a85e-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a85e-146">OUTPUTS</span></span>

### <span data-ttu-id="3a85e-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3a85e-147">System.Boolean</span></span>

## <span data-ttu-id="3a85e-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3a85e-148">NOTES</span></span>

## <span data-ttu-id="3a85e-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3a85e-149">RELATED LINKS</span></span>
