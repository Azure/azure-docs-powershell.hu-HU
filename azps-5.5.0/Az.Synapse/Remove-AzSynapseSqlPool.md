---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
ms.openlocfilehash: 37ece1d86c4b41dbf8a185c0d4ed5d7117db8b2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165578"
---
# <span data-ttu-id="3e769-101">Remove-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="3e769-101">Remove-AzSynapseSqlPool</span></span>

## <span data-ttu-id="3e769-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e769-102">SYNOPSIS</span></span>
<span data-ttu-id="3e769-103">Töröl egy Synapse Analytics SQL-készletet.</span><span class="sxs-lookup"><span data-stu-id="3e769-103">Deletes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="3e769-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3e769-104">SYNTAX</span></span>

### <span data-ttu-id="3e769-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3e769-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e769-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e769-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e769-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e769-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e769-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e769-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e769-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3e769-109">DESCRIPTION</span></span>
<span data-ttu-id="3e769-110">A **Remove-AzSynapseSqlPool** parancsmag véglegesen töröl egy Azure Synapse Analytics SQL-készletet.</span><span class="sxs-lookup"><span data-stu-id="3e769-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="3e769-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3e769-111">EXAMPLES</span></span>

### <span data-ttu-id="3e769-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="3e769-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="3e769-113">Ez a parancs töröl egy Azure Synapse Analytics SQL-készletet.</span><span class="sxs-lookup"><span data-stu-id="3e769-113">This command deletes an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="3e769-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="3e769-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlPool -Name ContosoSqlPool
```

<span data-ttu-id="3e769-115">Ez a parancs egy Azure Synapse Analytics SQL-készletet töröl folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="3e769-115">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="3e769-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="3e769-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPool
```

<span data-ttu-id="3e769-117">Ez a parancs egy Azure Synapse Analytics SQL-készletet töröl folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="3e769-117">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="3e769-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="3e769-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool
```

<span data-ttu-id="3e769-119">Ez a parancs töröl egy Azure Synapse Analytics SQL-készletet a megadott erőforrás-azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="3e769-119">This command deletes an Azure Synapse Analytics SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="3e769-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e769-120">PARAMETERS</span></span>

### <span data-ttu-id="3e769-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e769-121">-AsJob</span></span>
<span data-ttu-id="3e769-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3e769-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e769-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e769-123">-DefaultProfile</span></span>
<span data-ttu-id="3e769-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3e769-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e769-125">-Force</span><span class="sxs-lookup"><span data-stu-id="3e769-125">-Force</span></span>
<span data-ttu-id="3e769-126">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3e769-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3e769-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e769-127">-InputObject</span></span>
<span data-ttu-id="3e769-128">SQL-készlet bemeneti objektuma, amely általában a folyamaton keresztül áthalad.</span><span class="sxs-lookup"><span data-stu-id="3e769-128">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3e769-129">-Name</span><span class="sxs-lookup"><span data-stu-id="3e769-129">-Name</span></span>
<span data-ttu-id="3e769-130">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="3e769-130">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="3e769-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e769-131">-PassThru</span></span>
<span data-ttu-id="3e769-132">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="3e769-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="3e769-133">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="3e769-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="3e769-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e769-134">-ResourceGroupName</span></span>
<span data-ttu-id="3e769-135">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3e769-135">Resource group name.</span></span>

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

### <span data-ttu-id="3e769-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e769-136">-ResourceId</span></span>
<span data-ttu-id="3e769-137">A Synapse SQL-készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3e769-137">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="3e769-138">-Verzió</span><span class="sxs-lookup"><span data-stu-id="3e769-138">-Version</span></span>
<span data-ttu-id="3e769-139">A Synapse SQL-készlet verziója.</span><span class="sxs-lookup"><span data-stu-id="3e769-139">Version of Synapse SQL pool.</span></span> <span data-ttu-id="3e769-140">Például 2 vagy 3.</span><span class="sxs-lookup"><span data-stu-id="3e769-140">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="3e769-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3e769-141">-WorkspaceName</span></span>
<span data-ttu-id="3e769-142">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="3e769-142">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3e769-143">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3e769-143">-WorkspaceObject</span></span>
<span data-ttu-id="3e769-144">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="3e769-144">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3e769-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e769-145">-Confirm</span></span>
<span data-ttu-id="3e769-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3e769-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e769-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e769-147">-WhatIf</span></span>
<span data-ttu-id="3e769-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3e769-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e769-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3e769-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e769-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e769-150">CommonParameters</span></span>
<span data-ttu-id="3e769-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e769-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e769-152">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e769-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e769-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3e769-153">INPUTS</span></span>

### <span data-ttu-id="3e769-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3e769-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="3e769-155">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="3e769-155">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="3e769-156">System.String</span><span class="sxs-lookup"><span data-stu-id="3e769-156">System.String</span></span>

## <span data-ttu-id="3e769-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e769-157">OUTPUTS</span></span>

### <span data-ttu-id="3e769-158">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3e769-158">System.Boolean</span></span>

## <span data-ttu-id="3e769-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3e769-159">NOTES</span></span>

## <span data-ttu-id="3e769-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e769-160">RELATED LINKS</span></span>
