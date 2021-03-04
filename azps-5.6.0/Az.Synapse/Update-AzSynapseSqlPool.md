---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
ms.openlocfilehash: fe13a82a6662b0f8e9578f4f0fd5143b350538c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922593"
---
# <span data-ttu-id="db807-101">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="db807-101">Update-AzSynapseSqlPool</span></span>

## <span data-ttu-id="db807-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db807-102">SYNOPSIS</span></span>
<span data-ttu-id="db807-103">Frissíti a Synapse Analytics SQL-készletet.</span><span class="sxs-lookup"><span data-stu-id="db807-103">Updates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="db807-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="db807-104">SYNTAX</span></span>

### <span data-ttu-id="db807-105">UpdateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="db807-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db807-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db807-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db807-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db807-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-Tag <Hashtable>]
 [-PerformanceLevel <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db807-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db807-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-Tag <Hashtable>] [-PerformanceLevel <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db807-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="db807-109">DESCRIPTION</span></span>
<span data-ttu-id="db807-110">Az **Update-AzSynapseSqlPool** parancsmag frissíti az Azure Synapse Analytics SQL-készletet.</span><span class="sxs-lookup"><span data-stu-id="db807-110">The **Update-AzSynapseSqlPool** cmdlet updates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="db807-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="db807-111">EXAMPLES</span></span>

### <span data-ttu-id="db807-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="db807-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -Tag @{'key'='value'} -PerformanceLevel DW300c
```

<span data-ttu-id="db807-113">Ez a parancs frissíti az Azure Synapse Analytics SQL-készletet.</span><span class="sxs-lookup"><span data-stu-id="db807-113">This command updates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="db807-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="db807-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSqlPool -Name ContosoSqlPool -Tag @{'key'='value1'}
```

<span data-ttu-id="db807-115">Ez a parancs egy Azure Synapse Analytics SQL-készletet frissíti folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="db807-115">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="db807-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="db807-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Update-AzSynapseSqlPool -Tag @{'key'='value2'}
```

<span data-ttu-id="db807-117">Ez a parancs egy Azure Synapse Analytics SQL-készletet frissíti folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="db807-117">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="db807-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="db807-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd3/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool -Tag @{'key'='value3'}
```

<span data-ttu-id="db807-119">Ez a parancs frissíti az Azure Synapse Analytics SQL-készletet erőforrás-azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="db807-119">This command updates an Azure Synapse Analytics SQL pool with resource ID.</span></span>

## <span data-ttu-id="db807-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db807-120">PARAMETERS</span></span>

### <span data-ttu-id="db807-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db807-121">-AsJob</span></span>
<span data-ttu-id="db807-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="db807-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db807-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db807-123">-DefaultProfile</span></span>
<span data-ttu-id="db807-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db807-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db807-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db807-125">-InputObject</span></span>
<span data-ttu-id="db807-126">SQL-készlet bemeneti objektuma, amely általában a folyamaton keresztül áthalad.</span><span class="sxs-lookup"><span data-stu-id="db807-126">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db807-127">-Name</span><span class="sxs-lookup"><span data-stu-id="db807-127">-Name</span></span>
<span data-ttu-id="db807-128">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="db807-128">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db807-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db807-129">-PassThru</span></span>
<span data-ttu-id="db807-130">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="db807-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="db807-131">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="db807-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="db807-132">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="db807-132">-PerformanceLevel</span></span>
<span data-ttu-id="db807-133">Az SQL-készlethez hozzárendelni szükséges SQL-szolgáltatásréteg és teljesítményszint.</span><span class="sxs-lookup"><span data-stu-id="db807-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="db807-134">Például DW2000c.</span><span class="sxs-lookup"><span data-stu-id="db807-134">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db807-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db807-135">-ResourceGroupName</span></span>
<span data-ttu-id="db807-136">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="db807-136">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db807-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db807-137">-ResourceId</span></span>
<span data-ttu-id="db807-138">A Synapse SQL-készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="db807-138">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db807-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="db807-139">-Tag</span></span>
<span data-ttu-id="db807-140">Az erőforráshoz társított címkék karakterlánc-karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="db807-140">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db807-141">-Version</span><span class="sxs-lookup"><span data-stu-id="db807-141">-Version</span></span>
<span data-ttu-id="db807-142">A Synapse SQL-készlet verziója.</span><span class="sxs-lookup"><span data-stu-id="db807-142">Version of Synapse SQL pool.</span></span> <span data-ttu-id="db807-143">Például 2 vagy 3.</span><span class="sxs-lookup"><span data-stu-id="db807-143">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="db807-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="db807-144">-WorkspaceName</span></span>
<span data-ttu-id="db807-145">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="db807-145">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db807-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="db807-146">-WorkspaceObject</span></span>
<span data-ttu-id="db807-147">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="db807-147">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db807-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db807-148">-Confirm</span></span>
<span data-ttu-id="db807-149">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="db807-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db807-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db807-150">-WhatIf</span></span>
<span data-ttu-id="db807-151">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="db807-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db807-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="db807-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db807-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db807-153">CommonParameters</span></span>
<span data-ttu-id="db807-154">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db807-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db807-155">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db807-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db807-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db807-156">INPUTS</span></span>

### <span data-ttu-id="db807-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="db807-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="db807-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="db807-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="db807-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db807-159">OUTPUTS</span></span>

### <span data-ttu-id="db807-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="db807-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="db807-161">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="db807-161">NOTES</span></span>

## <span data-ttu-id="db807-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db807-162">RELATED LINKS</span></span>
