---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
ms.openlocfilehash: 79bd39616f33a50684827276c6af919990b269ca
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186315"
---
# <span data-ttu-id="e4f02-101">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e4f02-101">Update-AzSynapseSqlPool</span></span>

## <span data-ttu-id="e4f02-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e4f02-102">SYNOPSIS</span></span>
<span data-ttu-id="e4f02-103">A szinapszis Analytics SQL-készlet frissítése</span><span class="sxs-lookup"><span data-stu-id="e4f02-103">Updates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e4f02-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e4f02-104">SYNTAX</span></span>

### <span data-ttu-id="e4f02-105">UpdateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e4f02-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4f02-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4f02-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4f02-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4f02-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-Tag <Hashtable>]
 [-PerformanceLevel <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4f02-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4f02-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-Tag <Hashtable>] [-PerformanceLevel <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4f02-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="e4f02-109">DESCRIPTION</span></span>
<span data-ttu-id="e4f02-110">Az **Update-AzSynapseSqlPool** parancsmag az Azure SZINAPSZIS Analytics SQL-készletet frissíti.</span><span class="sxs-lookup"><span data-stu-id="e4f02-110">The **Update-AzSynapseSqlPool** cmdlet updates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e4f02-111">Példák</span><span class="sxs-lookup"><span data-stu-id="e4f02-111">EXAMPLES</span></span>

### <span data-ttu-id="e4f02-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e4f02-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -Tag @{'key'='value'} -PerformanceLevel DW300c
```

<span data-ttu-id="e4f02-113">Ez a parancs frissíti az Azure szinapszis Analytics SQL-készletét.</span><span class="sxs-lookup"><span data-stu-id="e4f02-113">This command updates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="e4f02-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="e4f02-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSqlPool -Name ContosoSqlPool -Tag @{'key'='value1'}
```

<span data-ttu-id="e4f02-115">Ez a parancs frissíti az Azure szinapszis Analytics SQL-készletet csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="e4f02-115">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="e4f02-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="e4f02-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Update-AzSynapseSqlPool -Tag @{'key'='value2'}
```

<span data-ttu-id="e4f02-117">Ez a parancs frissíti az Azure szinapszis Analytics SQL-készletet csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="e4f02-117">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="e4f02-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="e4f02-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd3/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool -Tag @{'key'='value3'}
```

<span data-ttu-id="e4f02-119">Ez a parancs frissíti az Azure szinapszis Analytics SQL-készletet erőforrás-AZONOSÍTÓval.</span><span class="sxs-lookup"><span data-stu-id="e4f02-119">This command updates an Azure Synapse Analytics SQL pool with resource ID.</span></span>

## <span data-ttu-id="e4f02-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e4f02-120">PARAMETERS</span></span>

### <span data-ttu-id="e4f02-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4f02-121">-AsJob</span></span>
<span data-ttu-id="e4f02-122">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e4f02-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e4f02-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4f02-123">-DefaultProfile</span></span>
<span data-ttu-id="e4f02-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e4f02-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4f02-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4f02-125">-InputObject</span></span>
<span data-ttu-id="e4f02-126">Az SQL-készlet bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="e4f02-126">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e4f02-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e4f02-127">-Name</span></span>
<span data-ttu-id="e4f02-128">A szinapszis SQL Pool neve.</span><span class="sxs-lookup"><span data-stu-id="e4f02-128">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4f02-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4f02-129">-PassThru</span></span>
<span data-ttu-id="e4f02-130">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="e4f02-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="e4f02-131">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="e4f02-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e4f02-132">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="e4f02-132">-PerformanceLevel</span></span>
<span data-ttu-id="e4f02-133">Az SQL-szolgáltatási szint és a teljesítmény szint az SQL-készlethez való hozzárendeléshez</span><span class="sxs-lookup"><span data-stu-id="e4f02-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="e4f02-134">Például DW2000c.</span><span class="sxs-lookup"><span data-stu-id="e4f02-134">For example, DW2000c.</span></span>

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

### <span data-ttu-id="e4f02-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4f02-135">-ResourceGroupName</span></span>
<span data-ttu-id="e4f02-136">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="e4f02-136">Resource group name.</span></span>

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

### <span data-ttu-id="e4f02-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4f02-137">-ResourceId</span></span>
<span data-ttu-id="e4f02-138">A szinapszis SQL Pool erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e4f02-138">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="e4f02-139">-Címke</span><span class="sxs-lookup"><span data-stu-id="e4f02-139">-Tag</span></span>
<span data-ttu-id="e4f02-140">Az erőforráshoz társított címkék karakterlánca, karakterláncok szótára</span><span class="sxs-lookup"><span data-stu-id="e4f02-140">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="e4f02-141">-Verzió</span><span class="sxs-lookup"><span data-stu-id="e4f02-141">-Version</span></span>
<span data-ttu-id="e4f02-142">A szinapszis SQL Pool verziója.</span><span class="sxs-lookup"><span data-stu-id="e4f02-142">Version of Synapse SQL pool.</span></span> <span data-ttu-id="e4f02-143">Például 2 vagy 3.</span><span class="sxs-lookup"><span data-stu-id="e4f02-143">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="e4f02-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e4f02-144">-WorkspaceName</span></span>
<span data-ttu-id="e4f02-145">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="e4f02-145">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e4f02-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e4f02-146">-WorkspaceObject</span></span>
<span data-ttu-id="e4f02-147">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="e4f02-147">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e4f02-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e4f02-148">-Confirm</span></span>
<span data-ttu-id="e4f02-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e4f02-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4f02-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4f02-150">-WhatIf</span></span>
<span data-ttu-id="e4f02-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e4f02-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4f02-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e4f02-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4f02-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4f02-153">CommonParameters</span></span>
<span data-ttu-id="e4f02-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e4f02-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4f02-155">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e4f02-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4f02-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4f02-156">INPUTS</span></span>

### <span data-ttu-id="e4f02-157">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e4f02-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e4f02-158">Microsoft. Azure. commands. szinapszis. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e4f02-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="e4f02-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4f02-159">OUTPUTS</span></span>

### <span data-ttu-id="e4f02-160">Microsoft. Azure. commands. szinapszis. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e4f02-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="e4f02-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e4f02-161">NOTES</span></span>

## <span data-ttu-id="e4f02-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4f02-162">RELATED LINKS</span></span>
