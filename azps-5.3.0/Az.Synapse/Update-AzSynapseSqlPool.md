---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
ms.openlocfilehash: 25f9c829bd0f2557f4419bcc0c3b95c71a2e4b9b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375841"
---
# <span data-ttu-id="5badf-101">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="5badf-101">Update-AzSynapseSqlPool</span></span>

## <span data-ttu-id="5badf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5badf-102">SYNOPSIS</span></span>
<span data-ttu-id="5badf-103">Frissíti a Synapse Analytics SQL-készletet.</span><span class="sxs-lookup"><span data-stu-id="5badf-103">Updates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="5badf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5badf-104">SYNTAX</span></span>

### <span data-ttu-id="5badf-105">UpdateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5badf-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5badf-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5badf-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5badf-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5badf-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-Tag <Hashtable>]
 [-PerformanceLevel <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5badf-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5badf-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-Tag <Hashtable>] [-PerformanceLevel <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5badf-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5badf-109">DESCRIPTION</span></span>
<span data-ttu-id="5badf-110">Az **Update-AzSynapseSqlPool** parancsmag frissíti az Azure Synapse Analytics SQL-készletet.</span><span class="sxs-lookup"><span data-stu-id="5badf-110">The **Update-AzSynapseSqlPool** cmdlet updates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="5badf-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5badf-111">EXAMPLES</span></span>

### <span data-ttu-id="5badf-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="5badf-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -Tag @{'key'='value'} -PerformanceLevel DW300c
```

<span data-ttu-id="5badf-113">Ez a parancs frissíti az Azure Synapse Analytics SQL-készletet.</span><span class="sxs-lookup"><span data-stu-id="5badf-113">This command updates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="5badf-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="5badf-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSqlPool -Name ContosoSqlPool -Tag @{'key'='value1'}
```

<span data-ttu-id="5badf-115">Ez a parancs egy Azure Synapse Analytics SQL-készletet frissíti folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="5badf-115">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="5badf-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="5badf-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Update-AzSynapseSqlPool -Tag @{'key'='value2'}
```

<span data-ttu-id="5badf-117">Ez a parancs egy Azure Synapse Analytics SQL-készletet frissíti folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="5badf-117">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="5badf-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="5badf-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd3/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool -Tag @{'key'='value3'}
```

<span data-ttu-id="5badf-119">Ez a parancs frissíti az Azure Synapse Analytics SQL-készletet erőforrás-azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="5badf-119">This command updates an Azure Synapse Analytics SQL pool with resource ID.</span></span>

## <span data-ttu-id="5badf-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5badf-120">PARAMETERS</span></span>

### <span data-ttu-id="5badf-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5badf-121">-AsJob</span></span>
<span data-ttu-id="5badf-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="5badf-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5badf-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5badf-123">-DefaultProfile</span></span>
<span data-ttu-id="5badf-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5badf-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5badf-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5badf-125">-InputObject</span></span>
<span data-ttu-id="5badf-126">SQL-készlet bemeneti objektuma, amely általában a folyamaton keresztül áthalad.</span><span class="sxs-lookup"><span data-stu-id="5badf-126">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5badf-127">-Name</span><span class="sxs-lookup"><span data-stu-id="5badf-127">-Name</span></span>
<span data-ttu-id="5badf-128">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="5badf-128">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="5badf-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5badf-129">-PassThru</span></span>
<span data-ttu-id="5badf-130">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="5badf-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="5badf-131">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="5badf-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="5badf-132">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="5badf-132">-PerformanceLevel</span></span>
<span data-ttu-id="5badf-133">Az SQL-készlethez hozzárendelni szükséges SQL-szolgáltatásréteg és teljesítményszint.</span><span class="sxs-lookup"><span data-stu-id="5badf-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="5badf-134">Például DW2000c.</span><span class="sxs-lookup"><span data-stu-id="5badf-134">For example, DW2000c.</span></span>

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

### <span data-ttu-id="5badf-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5badf-135">-ResourceGroupName</span></span>
<span data-ttu-id="5badf-136">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5badf-136">Resource group name.</span></span>

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

### <span data-ttu-id="5badf-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5badf-137">-ResourceId</span></span>
<span data-ttu-id="5badf-138">A Synapse SQL-készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5badf-138">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="5badf-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="5badf-139">-Tag</span></span>
<span data-ttu-id="5badf-140">Az erőforráshoz társított címkék karakterlánc-karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="5badf-140">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="5badf-141">-Version</span><span class="sxs-lookup"><span data-stu-id="5badf-141">-Version</span></span>
<span data-ttu-id="5badf-142">A Synapse SQL-készlet verziója.</span><span class="sxs-lookup"><span data-stu-id="5badf-142">Version of Synapse SQL pool.</span></span> <span data-ttu-id="5badf-143">Például 2 vagy 3.</span><span class="sxs-lookup"><span data-stu-id="5badf-143">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="5badf-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5badf-144">-WorkspaceName</span></span>
<span data-ttu-id="5badf-145">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="5badf-145">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5badf-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5badf-146">-WorkspaceObject</span></span>
<span data-ttu-id="5badf-147">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="5badf-147">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5badf-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5badf-148">-Confirm</span></span>
<span data-ttu-id="5badf-149">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5badf-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5badf-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5badf-150">-WhatIf</span></span>
<span data-ttu-id="5badf-151">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5badf-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5badf-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5badf-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5badf-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5badf-153">CommonParameters</span></span>
<span data-ttu-id="5badf-154">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5badf-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5badf-155">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5badf-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5badf-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5badf-156">INPUTS</span></span>

### <span data-ttu-id="5badf-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5badf-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="5badf-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="5badf-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="5badf-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5badf-159">OUTPUTS</span></span>

### <span data-ttu-id="5badf-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="5badf-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="5badf-161">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5badf-161">NOTES</span></span>

## <span data-ttu-id="5badf-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5badf-162">RELATED LINKS</span></span>
