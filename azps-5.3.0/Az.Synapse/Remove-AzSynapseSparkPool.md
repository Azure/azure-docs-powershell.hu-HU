---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
ms.openlocfilehash: 1afa4776aa82dcfddab1709cf08dcfe8cd0ff71b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383416"
---
# <span data-ttu-id="65fa8-101">Remove-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="65fa8-101">Remove-AzSynapseSparkPool</span></span>

## <span data-ttu-id="65fa8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65fa8-102">SYNOPSIS</span></span>
<span data-ttu-id="65fa8-103">Töröl egy Synapse Analytics spark-készletet.</span><span class="sxs-lookup"><span data-stu-id="65fa8-103">Deletes a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="65fa8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="65fa8-104">SYNTAX</span></span>

### <span data-ttu-id="65fa8-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="65fa8-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65fa8-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65fa8-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65fa8-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65fa8-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65fa8-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65fa8-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSparkPool -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65fa8-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="65fa8-109">DESCRIPTION</span></span>
<span data-ttu-id="65fa8-110">A **Remove-AzSynapseSparkPool** parancsmag véglegesen töröl egy Azure Synapse Analytics Spark-készletet.</span><span class="sxs-lookup"><span data-stu-id="65fa8-110">The **Remove-AzSynapseSparkPool** cmdlet permanently deletes an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="65fa8-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="65fa8-111">EXAMPLES</span></span>

### <span data-ttu-id="65fa8-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="65fa8-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="65fa8-113">Ez a parancs töröl egy Azure Synapse Analytics spark-készletet.</span><span class="sxs-lookup"><span data-stu-id="65fa8-113">This command deletes an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="65fa8-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="65fa8-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Remove-AzSynapseSparkPool
```

<span data-ttu-id="65fa8-115">Ez a parancs törli az Azure Synapse Analytics spark-készletet a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="65fa8-115">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="65fa8-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="65fa8-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSparkPool -Name ContosoSparkPool
```

<span data-ttu-id="65fa8-117">Ez a parancs törli az Azure Synapse Analytics spark-készletet a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="65fa8-117">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="65fa8-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="65fa8-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool
```

<span data-ttu-id="65fa8-119">Ez a parancs törli az Erőforrásazonosítóval együtt az Azure Synapse Analytics spark-készletet.</span><span class="sxs-lookup"><span data-stu-id="65fa8-119">This command deletes an Azure Synapse Analytics Spark pool with a resource ID.</span></span>

## <span data-ttu-id="65fa8-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65fa8-120">PARAMETERS</span></span>

### <span data-ttu-id="65fa8-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65fa8-121">-AsJob</span></span>
<span data-ttu-id="65fa8-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="65fa8-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65fa8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65fa8-123">-DefaultProfile</span></span>
<span data-ttu-id="65fa8-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="65fa8-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65fa8-125">-Force</span><span class="sxs-lookup"><span data-stu-id="65fa8-125">-Force</span></span>
<span data-ttu-id="65fa8-126">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="65fa8-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="65fa8-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65fa8-127">-InputObject</span></span>
<span data-ttu-id="65fa8-128">Spark pool input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="65fa8-128">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65fa8-129">-Name</span><span class="sxs-lookup"><span data-stu-id="65fa8-129">-Name</span></span>
<span data-ttu-id="65fa8-130">A Synapse spark-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="65fa8-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases: SparkPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65fa8-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65fa8-131">-PassThru</span></span>
<span data-ttu-id="65fa8-132">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="65fa8-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="65fa8-133">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="65fa8-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="65fa8-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65fa8-134">-ResourceGroupName</span></span>
<span data-ttu-id="65fa8-135">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="65fa8-135">Resource group name.</span></span>

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

### <span data-ttu-id="65fa8-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65fa8-136">-ResourceId</span></span>
<span data-ttu-id="65fa8-137">A Synapse Spark készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="65fa8-137">Resource identifier of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="65fa8-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="65fa8-138">-WorkspaceName</span></span>
<span data-ttu-id="65fa8-139">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="65fa8-139">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65fa8-140">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="65fa8-140">-WorkspaceObject</span></span>
<span data-ttu-id="65fa8-141">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="65fa8-141">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65fa8-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65fa8-142">-Confirm</span></span>
<span data-ttu-id="65fa8-143">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="65fa8-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65fa8-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65fa8-144">-WhatIf</span></span>
<span data-ttu-id="65fa8-145">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="65fa8-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65fa8-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="65fa8-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65fa8-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65fa8-147">CommonParameters</span></span>
<span data-ttu-id="65fa8-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65fa8-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65fa8-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65fa8-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65fa8-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65fa8-150">INPUTS</span></span>

### <span data-ttu-id="65fa8-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="65fa8-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="65fa8-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="65fa8-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="65fa8-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65fa8-153">OUTPUTS</span></span>

### <span data-ttu-id="65fa8-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="65fa8-154">System.Boolean</span></span>

## <span data-ttu-id="65fa8-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="65fa8-155">NOTES</span></span>

## <span data-ttu-id="65fa8-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65fa8-156">RELATED LINKS</span></span>
