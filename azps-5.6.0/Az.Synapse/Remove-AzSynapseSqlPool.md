---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
ms.openlocfilehash: 298077ced1b7cb308bae4a8a5d27e13893c4b4e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943257"
---
# <span data-ttu-id="598d1-101">Remove-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="598d1-101">Remove-AzSynapseSqlPool</span></span>

## <span data-ttu-id="598d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="598d1-102">SYNOPSIS</span></span>
<span data-ttu-id="598d1-103">Töröl egy Synapse Analytics SQL-készletet.</span><span class="sxs-lookup"><span data-stu-id="598d1-103">Deletes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="598d1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="598d1-104">SYNTAX</span></span>

### <span data-ttu-id="598d1-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="598d1-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="598d1-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="598d1-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="598d1-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="598d1-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="598d1-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="598d1-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="598d1-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="598d1-109">DESCRIPTION</span></span>
<span data-ttu-id="598d1-110">A **Remove-AzSynapseSqlPool** parancsmag véglegesen töröl egy Azure Synapse Analytics SQL-készletet.</span><span class="sxs-lookup"><span data-stu-id="598d1-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="598d1-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="598d1-111">EXAMPLES</span></span>

### <span data-ttu-id="598d1-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="598d1-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="598d1-113">Ez a parancs töröl egy Azure Synapse Analytics SQL-készletet.</span><span class="sxs-lookup"><span data-stu-id="598d1-113">This command deletes an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="598d1-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="598d1-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlPool -Name ContosoSqlPool
```

<span data-ttu-id="598d1-115">Ez a parancs egy Azure Synapse Analytics SQL-készletet töröl folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="598d1-115">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="598d1-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="598d1-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPool
```

<span data-ttu-id="598d1-117">Ez a parancs egy Azure Synapse Analytics SQL-készletet töröl folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="598d1-117">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="598d1-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="598d1-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool
```

<span data-ttu-id="598d1-119">Ez a parancs töröl egy Azure Synapse Analytics SQL-készletet a megadott erőforrás-azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="598d1-119">This command deletes an Azure Synapse Analytics SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="598d1-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="598d1-120">PARAMETERS</span></span>

### <span data-ttu-id="598d1-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="598d1-121">-AsJob</span></span>
<span data-ttu-id="598d1-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="598d1-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="598d1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="598d1-123">-DefaultProfile</span></span>
<span data-ttu-id="598d1-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="598d1-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="598d1-125">-Force</span><span class="sxs-lookup"><span data-stu-id="598d1-125">-Force</span></span>
<span data-ttu-id="598d1-126">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="598d1-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="598d1-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="598d1-127">-InputObject</span></span>
<span data-ttu-id="598d1-128">SQL-készlet bemeneti objektuma, amely általában a folyamaton keresztül áthalad.</span><span class="sxs-lookup"><span data-stu-id="598d1-128">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="598d1-129">-Name</span><span class="sxs-lookup"><span data-stu-id="598d1-129">-Name</span></span>
<span data-ttu-id="598d1-130">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="598d1-130">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="598d1-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="598d1-131">-PassThru</span></span>
<span data-ttu-id="598d1-132">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="598d1-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="598d1-133">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="598d1-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="598d1-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="598d1-134">-ResourceGroupName</span></span>
<span data-ttu-id="598d1-135">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="598d1-135">Resource group name.</span></span>

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

### <span data-ttu-id="598d1-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="598d1-136">-ResourceId</span></span>
<span data-ttu-id="598d1-137">A Synapse SQL-készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="598d1-137">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="598d1-138">-Version</span><span class="sxs-lookup"><span data-stu-id="598d1-138">-Version</span></span>
<span data-ttu-id="598d1-139">A Synapse SQL-készlet verziója.</span><span class="sxs-lookup"><span data-stu-id="598d1-139">Version of Synapse SQL pool.</span></span> <span data-ttu-id="598d1-140">Például 2 vagy 3.</span><span class="sxs-lookup"><span data-stu-id="598d1-140">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="598d1-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="598d1-141">-WorkspaceName</span></span>
<span data-ttu-id="598d1-142">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="598d1-142">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="598d1-143">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="598d1-143">-WorkspaceObject</span></span>
<span data-ttu-id="598d1-144">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="598d1-144">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="598d1-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="598d1-145">-Confirm</span></span>
<span data-ttu-id="598d1-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="598d1-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="598d1-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="598d1-147">-WhatIf</span></span>
<span data-ttu-id="598d1-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="598d1-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="598d1-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="598d1-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="598d1-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="598d1-150">CommonParameters</span></span>
<span data-ttu-id="598d1-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="598d1-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="598d1-152">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="598d1-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="598d1-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="598d1-153">INPUTS</span></span>

### <span data-ttu-id="598d1-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="598d1-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="598d1-155">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="598d1-155">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="598d1-156">System.String</span><span class="sxs-lookup"><span data-stu-id="598d1-156">System.String</span></span>

## <span data-ttu-id="598d1-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="598d1-157">OUTPUTS</span></span>

### <span data-ttu-id="598d1-158">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="598d1-158">System.Boolean</span></span>

## <span data-ttu-id="598d1-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="598d1-159">NOTES</span></span>

## <span data-ttu-id="598d1-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="598d1-160">RELATED LINKS</span></span>
