---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: 6105b043ee1e21ddbf2f29ce6bf0819639a133d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928418"
---
# <span data-ttu-id="cbd11-101">Remove-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="cbd11-101">Remove-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="cbd11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbd11-102">SYNOPSIS</span></span>
<span data-ttu-id="cbd11-103">A Synapse Analytics SQL-készlet visszaállítási pontjának törlése.</span><span class="sxs-lookup"><span data-stu-id="cbd11-103">Deletes a Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="cbd11-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cbd11-104">SYNTAX</span></span>

### <span data-ttu-id="cbd11-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cbd11-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -RestorePointCreationDate <DateTime> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbd11-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbd11-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -RestorePointCreationDate <DateTime> -SqlPoolObject <PSSynapseSqlPool>
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cbd11-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbd11-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -InputObject <PSRestorePoint> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbd11-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbd11-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbd11-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cbd11-109">DESCRIPTION</span></span>
<span data-ttu-id="cbd11-110">A **Remove-AzSynapseSqlPoolRestorePoint** parancsmag véglegesen törli az Azure Synapse Analytics SQL-készlet visszaállítási pontját.</span><span class="sxs-lookup"><span data-stu-id="cbd11-110">The **Remove-AzSynapseSqlPoolRestorePoint** cmdlet permanently deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="cbd11-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cbd11-111">EXAMPLES</span></span>

### <span data-ttu-id="cbd11-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="cbd11-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="cbd11-113">Ez a parancs törli az Azure Synapse Analytics SQL-készlet visszaállítási pontját.</span><span class="sxs-lookup"><span data-stu-id="cbd11-113">This command deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

### <span data-ttu-id="cbd11-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="cbd11-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPoolRestorePoint -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="cbd11-115">Ez a parancs törli az Azure Synapse Analytics SQL-készlet visszaállítási pontját a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="cbd11-115">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="cbd11-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="cbd11-116">Example 3</span></span>
```powershell
PS C:\> $points = Get-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $points[index] | Remove-AzSynapseSqlPoolRestorePoint
```

<span data-ttu-id="cbd11-117">Ez a parancs törli az Azure Synapse Analytics SQL-készlet visszaállítási pontját a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="cbd11-117">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="cbd11-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="cbd11-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool/SqlPoolRestorePoints/RestorePointCreationDate
```

<span data-ttu-id="cbd11-119">Ez a parancs törli a megadott erőforrás-azonosítójú Azure Synapse Analytics SQL-készlet visszaállítási pontját.</span><span class="sxs-lookup"><span data-stu-id="cbd11-119">This command deletes an Azure Synapse Analytics SQL pool restore point with the specified resource ID.</span></span>

## <span data-ttu-id="cbd11-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cbd11-120">PARAMETERS</span></span>

### <span data-ttu-id="cbd11-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cbd11-121">-AsJob</span></span>
<span data-ttu-id="cbd11-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="cbd11-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cbd11-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbd11-123">-DefaultProfile</span></span>
<span data-ttu-id="cbd11-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cbd11-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbd11-125">-Force</span><span class="sxs-lookup"><span data-stu-id="cbd11-125">-Force</span></span>
<span data-ttu-id="cbd11-126">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cbd11-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cbd11-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbd11-127">-InputObject</span></span>
<span data-ttu-id="cbd11-128">SQL-készlet-visszaállítási pont létrehozási idő beviteli objektuma, amely általában áthalad a folyamaton.</span><span class="sxs-lookup"><span data-stu-id="cbd11-128">SQL pool restore point creation time input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbd11-129">-Name</span><span class="sxs-lookup"><span data-stu-id="cbd11-129">-Name</span></span>
<span data-ttu-id="cbd11-130">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="cbd11-130">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbd11-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cbd11-131">-PassThru</span></span>
<span data-ttu-id="cbd11-132">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="cbd11-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="cbd11-133">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="cbd11-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="cbd11-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbd11-134">-ResourceGroupName</span></span>
<span data-ttu-id="cbd11-135">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cbd11-135">Resource group name.</span></span>

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

### <span data-ttu-id="cbd11-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cbd11-136">-ResourceId</span></span>
<span data-ttu-id="cbd11-137">A Synapse SQL-készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cbd11-137">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="cbd11-138">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="cbd11-138">-RestorePointCreationDate</span></span>
<span data-ttu-id="cbd11-139">A Synapse SQL visszaállítási pont létrehozási dátumának neve.</span><span class="sxs-lookup"><span data-stu-id="cbd11-139">Name of Synapse SQL Restore Point Creation Date .</span></span>

```yaml
Type: System.DateTime
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbd11-140">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="cbd11-140">-SqlPoolObject</span></span>
<span data-ttu-id="cbd11-141">Sql Pool bemeneti objektum, amely általában a folyamaton keresztül áthalad.</span><span class="sxs-lookup"><span data-stu-id="cbd11-141">Sql Pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbd11-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cbd11-142">-WorkspaceName</span></span>
<span data-ttu-id="cbd11-143">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="cbd11-143">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="cbd11-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cbd11-144">-Confirm</span></span>
<span data-ttu-id="cbd11-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cbd11-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbd11-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbd11-146">-WhatIf</span></span>
<span data-ttu-id="cbd11-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cbd11-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbd11-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cbd11-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbd11-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbd11-149">CommonParameters</span></span>
<span data-ttu-id="cbd11-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbd11-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbd11-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbd11-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbd11-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cbd11-152">INPUTS</span></span>

### <span data-ttu-id="cbd11-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cbd11-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="cbd11-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="cbd11-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="cbd11-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="cbd11-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

### <span data-ttu-id="cbd11-156">System.String</span><span class="sxs-lookup"><span data-stu-id="cbd11-156">System.String</span></span>

## <span data-ttu-id="cbd11-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbd11-157">OUTPUTS</span></span>

### <span data-ttu-id="cbd11-158">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cbd11-158">System.Boolean</span></span>

## <span data-ttu-id="cbd11-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cbd11-159">NOTES</span></span>

## <span data-ttu-id="cbd11-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cbd11-160">RELATED LINKS</span></span>
