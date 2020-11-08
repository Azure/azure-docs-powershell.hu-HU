---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
ms.openlocfilehash: 62b1e0ef03d52337c03506d3bddc8bbfd3d5512d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183457"
---
# <span data-ttu-id="9d9fb-101">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="9d9fb-101">Update-AzSynapseSqlPool</span></span>

## <span data-ttu-id="9d9fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9d9fb-102">SYNOPSIS</span></span>
<span data-ttu-id="9d9fb-103">A szinapszis Analytics SQL-készlet frissítése</span><span class="sxs-lookup"><span data-stu-id="9d9fb-103">Updates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="9d9fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9d9fb-104">SYNTAX</span></span>

### <span data-ttu-id="9d9fb-105">UpdateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9d9fb-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d9fb-106">PauseByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d9fb-106">PauseByNameParameterSet</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Suspend] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d9fb-107">ResumeByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d9fb-107">ResumeByNameParameterSet</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Resume] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d9fb-108">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d9fb-108">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d9fb-109">PauseByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d9fb-109">PauseByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] [-Suspend] -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d9fb-110">ResumeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d9fb-110">ResumeByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] [-Resume] -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d9fb-111">PauseByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d9fb-111">PauseByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Suspend] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d9fb-112">PauseByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d9fb-112">PauseByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Suspend] -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d9fb-113">ResumeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d9fb-113">ResumeByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Resume] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d9fb-114">ResumeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d9fb-114">ResumeByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Resume] -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d9fb-115">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d9fb-115">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-Tag <Hashtable>]
 [-PerformanceLevel <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d9fb-116">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d9fb-116">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-Tag <Hashtable>] [-PerformanceLevel <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d9fb-117">Leírás</span><span class="sxs-lookup"><span data-stu-id="9d9fb-117">DESCRIPTION</span></span>
<span data-ttu-id="9d9fb-118">Az **Update-AzSynapseSqlPool** parancsmag az Azure SZINAPSZIS Analytics SQL-készletet frissíti.</span><span class="sxs-lookup"><span data-stu-id="9d9fb-118">The **Update-AzSynapseSqlPool** cmdlet updates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="9d9fb-119">Példák</span><span class="sxs-lookup"><span data-stu-id="9d9fb-119">EXAMPLES</span></span>

### <span data-ttu-id="9d9fb-120">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9d9fb-120">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -Tag @{'key'='value'} -PerformanceLevel DW300c
```

<span data-ttu-id="9d9fb-121">Ez a parancs frissíti az Azure szinapszis Analytics SQL-készletét.</span><span class="sxs-lookup"><span data-stu-id="9d9fb-121">This command updates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="9d9fb-122">2. példa</span><span class="sxs-lookup"><span data-stu-id="9d9fb-122">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSqlPool -Name ContosoSqlPool -Tag @{'key'='value1'}
```

<span data-ttu-id="9d9fb-123">Ez a parancs frissíti az Azure szinapszis Analytics SQL-készletet csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="9d9fb-123">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="9d9fb-124">3. példa</span><span class="sxs-lookup"><span data-stu-id="9d9fb-124">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Update-AzSynapseSqlPool -Tag @{'key'='value2'}
```

<span data-ttu-id="9d9fb-125">Ez a parancs frissíti az Azure szinapszis Analytics SQL-készletet csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="9d9fb-125">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="9d9fb-126">4. példa</span><span class="sxs-lookup"><span data-stu-id="9d9fb-126">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd3/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool -Tag @{'key'='value3'}
```

<span data-ttu-id="9d9fb-127">Ez a parancs frissíti az Azure szinapszis Analytics SQL-készletet erőforrás-AZONOSÍTÓval.</span><span class="sxs-lookup"><span data-stu-id="9d9fb-127">This command updates an Azure Synapse Analytics SQL pool with resource ID.</span></span>

## <span data-ttu-id="9d9fb-128">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9d9fb-128">PARAMETERS</span></span>

### <span data-ttu-id="9d9fb-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d9fb-129">-AsJob</span></span>
<span data-ttu-id="9d9fb-130">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9d9fb-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9d9fb-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d9fb-131">-DefaultProfile</span></span>
<span data-ttu-id="9d9fb-132">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9d9fb-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d9fb-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d9fb-133">-InputObject</span></span>
<span data-ttu-id="9d9fb-134">Az SQL-készlet bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="9d9fb-134">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: PauseByInputObjectParameterSet, ResumeByInputObjectParameterSet, UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d9fb-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9d9fb-135">-Name</span></span>
<span data-ttu-id="9d9fb-136">A szinapszis SQL Pool neve.</span><span class="sxs-lookup"><span data-stu-id="9d9fb-136">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, PauseByNameParameterSet, ResumeByNameParameterSet, UpdateByParentObjectParameterSet, PauseByParentObjectParameterSet, ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d9fb-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d9fb-137">-PassThru</span></span>
<span data-ttu-id="9d9fb-138">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="9d9fb-138">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="9d9fb-139">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="9d9fb-139">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9d9fb-140">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="9d9fb-140">-PerformanceLevel</span></span>
<span data-ttu-id="9d9fb-141">Az SQL-szolgáltatási szint és a teljesítmény szint az SQL-készlethez való hozzárendeléshez</span><span class="sxs-lookup"><span data-stu-id="9d9fb-141">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="9d9fb-142">Például DW2000c.</span><span class="sxs-lookup"><span data-stu-id="9d9fb-142">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet, UpdateByInputObjectParameterSet, UpdateByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d9fb-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d9fb-143">-ResourceGroupName</span></span>
<span data-ttu-id="9d9fb-144">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="9d9fb-144">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, PauseByNameParameterSet, ResumeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d9fb-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d9fb-145">-ResourceId</span></span>
<span data-ttu-id="9d9fb-146">A szinapszis SQL Pool erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9d9fb-146">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: PauseByResourceIdParameterSet, ResumeByResourceIdParameterSet, UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d9fb-147">– Önéletrajz</span><span class="sxs-lookup"><span data-stu-id="9d9fb-147">-Resume</span></span>
<span data-ttu-id="9d9fb-148">Az SQL-készlet folytatását jelzi</span><span class="sxs-lookup"><span data-stu-id="9d9fb-148">Indicates to resume the SQL pool</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ResumeByNameParameterSet, ResumeByParentObjectParameterSet, ResumeByInputObjectParameterSet, ResumeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d9fb-149">-Felfüggesztés</span><span class="sxs-lookup"><span data-stu-id="9d9fb-149">-Suspend</span></span>
<span data-ttu-id="9d9fb-150">Az SQL-készlet szüneteltetésének jelzése</span><span class="sxs-lookup"><span data-stu-id="9d9fb-150">Indicates to pause the SQL pool</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PauseByNameParameterSet, PauseByParentObjectParameterSet, PauseByInputObjectParameterSet, PauseByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d9fb-151">-Címke</span><span class="sxs-lookup"><span data-stu-id="9d9fb-151">-Tag</span></span>
<span data-ttu-id="9d9fb-152">Az erőforráshoz társított címkék karakterlánca, karakterláncok szótára</span><span class="sxs-lookup"><span data-stu-id="9d9fb-152">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet, UpdateByInputObjectParameterSet, UpdateByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d9fb-153">-Verzió</span><span class="sxs-lookup"><span data-stu-id="9d9fb-153">-Version</span></span>
<span data-ttu-id="9d9fb-154">A szinapszis SQL Pool verziója.</span><span class="sxs-lookup"><span data-stu-id="9d9fb-154">Version of Synapse SQL pool.</span></span> <span data-ttu-id="9d9fb-155">Például 2 vagy 3.</span><span class="sxs-lookup"><span data-stu-id="9d9fb-155">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="9d9fb-156">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9d9fb-156">-WorkspaceName</span></span>
<span data-ttu-id="9d9fb-157">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="9d9fb-157">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, PauseByNameParameterSet, ResumeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d9fb-158">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9d9fb-158">-WorkspaceObject</span></span>
<span data-ttu-id="9d9fb-159">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="9d9fb-159">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet, PauseByParentObjectParameterSet, ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d9fb-160">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9d9fb-160">-Confirm</span></span>
<span data-ttu-id="9d9fb-161">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9d9fb-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d9fb-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d9fb-162">-WhatIf</span></span>
<span data-ttu-id="9d9fb-163">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9d9fb-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d9fb-164">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9d9fb-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d9fb-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d9fb-165">CommonParameters</span></span>
<span data-ttu-id="9d9fb-166">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9d9fb-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d9fb-167">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9d9fb-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d9fb-168">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d9fb-168">INPUTS</span></span>

### <span data-ttu-id="9d9fb-169">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9d9fb-169">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="9d9fb-170">Microsoft. Azure. commands. szinapszis. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="9d9fb-170">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="9d9fb-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d9fb-171">OUTPUTS</span></span>

### <span data-ttu-id="9d9fb-172">Microsoft. Azure. commands. szinapszis. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="9d9fb-172">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="9d9fb-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9d9fb-173">NOTES</span></span>

## <span data-ttu-id="9d9fb-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9d9fb-174">RELATED LINKS</span></span>
