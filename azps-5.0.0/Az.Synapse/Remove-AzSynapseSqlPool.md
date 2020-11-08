---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
ms.openlocfilehash: cd715bed20477fae4cbb17d033fd67fefa4e1cdc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187137"
---
# <span data-ttu-id="2229b-101">Remove-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="2229b-101">Remove-AzSynapseSqlPool</span></span>

## <span data-ttu-id="2229b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2229b-102">SYNOPSIS</span></span>
<span data-ttu-id="2229b-103">Egy szinapszis-Analytics SQL-készlet törlése</span><span class="sxs-lookup"><span data-stu-id="2229b-103">Deletes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="2229b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2229b-104">SYNTAX</span></span>

### <span data-ttu-id="2229b-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2229b-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2229b-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2229b-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2229b-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2229b-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2229b-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2229b-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2229b-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="2229b-109">DESCRIPTION</span></span>
<span data-ttu-id="2229b-110">A **Remove-AzSynapseSqlPool** parancsmag véglegesen törli az Azure szinapszis-Analytics SQL-készletét.</span><span class="sxs-lookup"><span data-stu-id="2229b-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="2229b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="2229b-111">EXAMPLES</span></span>

### <span data-ttu-id="2229b-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2229b-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="2229b-113">Ez a parancs törli az Azure szinapszis-Analytics SQL-készletét.</span><span class="sxs-lookup"><span data-stu-id="2229b-113">This command deletes an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="2229b-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="2229b-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlPool -Name ContosoSqlPool
```

<span data-ttu-id="2229b-115">Ez a parancs törli az Azure szinapszis Analytics SQL-készletet csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="2229b-115">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="2229b-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="2229b-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPool
```

<span data-ttu-id="2229b-117">Ez a parancs törli az Azure szinapszis Analytics SQL-készletet csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="2229b-117">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="2229b-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="2229b-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool
```

<span data-ttu-id="2229b-119">Ez a parancs törli az Azure szinapszis Analytics SQL-készletet a megadott erőforrás-AZONOSÍTÓval.</span><span class="sxs-lookup"><span data-stu-id="2229b-119">This command deletes an Azure Synapse Analytics SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="2229b-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2229b-120">PARAMETERS</span></span>

### <span data-ttu-id="2229b-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2229b-121">-AsJob</span></span>
<span data-ttu-id="2229b-122">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2229b-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2229b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2229b-123">-DefaultProfile</span></span>
<span data-ttu-id="2229b-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2229b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2229b-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2229b-125">-InputObject</span></span>
<span data-ttu-id="2229b-126">Az SQL-készlet bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="2229b-126">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2229b-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2229b-127">-Name</span></span>
<span data-ttu-id="2229b-128">A szinapszis SQL Pool neve.</span><span class="sxs-lookup"><span data-stu-id="2229b-128">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2229b-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2229b-129">-PassThru</span></span>
<span data-ttu-id="2229b-130">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="2229b-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="2229b-131">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="2229b-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="2229b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2229b-132">-ResourceGroupName</span></span>
<span data-ttu-id="2229b-133">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="2229b-133">Resource group name.</span></span>

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

### <span data-ttu-id="2229b-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2229b-134">-ResourceId</span></span>
<span data-ttu-id="2229b-135">A szinapszis SQL Pool erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2229b-135">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="2229b-136">-Verzió</span><span class="sxs-lookup"><span data-stu-id="2229b-136">-Version</span></span>
<span data-ttu-id="2229b-137">A szinapszis SQL Pool verziója.</span><span class="sxs-lookup"><span data-stu-id="2229b-137">Version of Synapse SQL pool.</span></span> <span data-ttu-id="2229b-138">Például 2 vagy 3.</span><span class="sxs-lookup"><span data-stu-id="2229b-138">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="2229b-139">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2229b-139">-WorkspaceName</span></span>
<span data-ttu-id="2229b-140">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="2229b-140">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="2229b-141">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2229b-141">-WorkspaceObject</span></span>
<span data-ttu-id="2229b-142">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="2229b-142">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2229b-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2229b-143">-Confirm</span></span>
<span data-ttu-id="2229b-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2229b-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2229b-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2229b-145">-WhatIf</span></span>
<span data-ttu-id="2229b-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2229b-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2229b-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2229b-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2229b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2229b-148">CommonParameters</span></span>
<span data-ttu-id="2229b-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2229b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2229b-150">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2229b-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2229b-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2229b-151">INPUTS</span></span>

### <span data-ttu-id="2229b-152">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2229b-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="2229b-153">Microsoft. Azure. commands. szinapszis. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="2229b-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="2229b-154">System. String</span><span class="sxs-lookup"><span data-stu-id="2229b-154">System.String</span></span>

## <span data-ttu-id="2229b-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2229b-155">OUTPUTS</span></span>

### <span data-ttu-id="2229b-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2229b-156">System.Boolean</span></span>

## <span data-ttu-id="2229b-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2229b-157">NOTES</span></span>

## <span data-ttu-id="2229b-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2229b-158">RELATED LINKS</span></span>
