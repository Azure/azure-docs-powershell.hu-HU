---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
ms.openlocfilehash: fbdca80b33dd15e34a958cb63a41377b400d03ce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476606"
---
# <span data-ttu-id="0a6b4-101">Remove-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0a6b4-101">Remove-AzSynapseWorkspace</span></span>

## <span data-ttu-id="0a6b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a6b4-102">SYNOPSIS</span></span>
<span data-ttu-id="0a6b4-103">A Synapse Analytics munkaterületének törlése.</span><span class="sxs-lookup"><span data-stu-id="0a6b4-103">Deletes a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="0a6b4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0a6b4-104">SYNTAX</span></span>

### <span data-ttu-id="0a6b4-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0a6b4-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseWorkspace [-ResourceGroupName <String>] -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a6b4-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a6b4-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a6b4-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a6b4-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseWorkspace -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a6b4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0a6b4-108">DESCRIPTION</span></span>
<span data-ttu-id="0a6b4-109">A **Remove-AzSynapseWorkspace** parancsmag véglegesen törli az Azure Synapse Analytics munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="0a6b4-109">The **Remove-AzSynapseWorkspace** cmdlet permanently deletes an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="0a6b4-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0a6b4-110">EXAMPLES</span></span>

### <span data-ttu-id="0a6b4-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="0a6b4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="0a6b4-112">Ez a parancs törli az Azure Synapse Analytics munkaterületét.</span><span class="sxs-lookup"><span data-stu-id="0a6b4-112">This command deletes an Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="0a6b4-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="0a6b4-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseWorkspace
```

<span data-ttu-id="0a6b4-114">Ez a parancs egy Azure Synapse Analytics-munkaterületet töröl folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="0a6b4-114">This command deletes an Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="0a6b4-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="0a6b4-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="0a6b4-116">Ez a parancs törli az Azure Synapse Analytics munkaterületet a megadott erőforrás-azonosítójú folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="0a6b4-116">This command deletes an Azure Synapse Analytics workspace through pipeline with the specified resource ID.</span></span>

## <span data-ttu-id="0a6b4-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a6b4-117">PARAMETERS</span></span>

### <span data-ttu-id="0a6b4-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a6b4-118">-AsJob</span></span>
<span data-ttu-id="0a6b4-119">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0a6b4-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a6b4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a6b4-120">-DefaultProfile</span></span>
<span data-ttu-id="0a6b4-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0a6b4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a6b4-122">-Force</span><span class="sxs-lookup"><span data-stu-id="0a6b4-122">-Force</span></span>
<span data-ttu-id="0a6b4-123">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0a6b4-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0a6b4-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a6b4-124">-InputObject</span></span>
<span data-ttu-id="0a6b4-125">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="0a6b4-125">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6b4-126">-Name</span><span class="sxs-lookup"><span data-stu-id="0a6b4-126">-Name</span></span>
<span data-ttu-id="0a6b4-127">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="0a6b4-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a6b4-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a6b4-128">-PassThru</span></span>
<span data-ttu-id="0a6b4-129">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="0a6b4-129">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="0a6b4-130">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="0a6b4-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="0a6b4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a6b4-131">-ResourceGroupName</span></span>
<span data-ttu-id="0a6b4-132">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0a6b4-132">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a6b4-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a6b4-133">-ResourceId</span></span>
<span data-ttu-id="0a6b4-134">A Synapse-munkaterület erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0a6b4-134">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a6b4-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a6b4-135">-Confirm</span></span>
<span data-ttu-id="0a6b4-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0a6b4-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a6b4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a6b4-137">-WhatIf</span></span>
<span data-ttu-id="0a6b4-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0a6b4-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a6b4-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0a6b4-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a6b4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a6b4-140">CommonParameters</span></span>
<span data-ttu-id="0a6b4-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a6b4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a6b4-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a6b4-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a6b4-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0a6b4-143">INPUTS</span></span>

### <span data-ttu-id="0a6b4-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0a6b4-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="0a6b4-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a6b4-145">OUTPUTS</span></span>

### <span data-ttu-id="0a6b4-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0a6b4-146">System.Boolean</span></span>

## <span data-ttu-id="0a6b4-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0a6b4-147">NOTES</span></span>

## <span data-ttu-id="0a6b4-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a6b4-148">RELATED LINKS</span></span>
