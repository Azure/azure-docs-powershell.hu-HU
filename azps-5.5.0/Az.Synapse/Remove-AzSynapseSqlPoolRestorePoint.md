---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: 63c0dbc30557230f67e419bcde482e445f3df758
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209022"
---
# <span data-ttu-id="eb826-101">Remove-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="eb826-101">Remove-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="eb826-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb826-102">SYNOPSIS</span></span>
<span data-ttu-id="eb826-103">A Synapse Analytics SQL-készlet visszaállítási pontjának törlése.</span><span class="sxs-lookup"><span data-stu-id="eb826-103">Deletes a Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="eb826-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="eb826-104">SYNTAX</span></span>

### <span data-ttu-id="eb826-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eb826-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -RestorePointCreationDate <DateTime> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb826-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb826-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -RestorePointCreationDate <DateTime> -SqlPoolObject <PSSynapseSqlPool>
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eb826-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb826-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -InputObject <PSRestorePoint> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb826-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb826-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb826-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="eb826-109">DESCRIPTION</span></span>
<span data-ttu-id="eb826-110">A **Remove-AzSynapseSqlPoolRestorePoint** parancsmag véglegesen törli az Azure Synapse Analytics SQL-készlet visszaállítási pontját.</span><span class="sxs-lookup"><span data-stu-id="eb826-110">The **Remove-AzSynapseSqlPoolRestorePoint** cmdlet permanently deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="eb826-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="eb826-111">EXAMPLES</span></span>

### <span data-ttu-id="eb826-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="eb826-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="eb826-113">Ez a parancs törli az Azure Synapse Analytics SQL-készlet visszaállítási pontját.</span><span class="sxs-lookup"><span data-stu-id="eb826-113">This command deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

### <span data-ttu-id="eb826-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="eb826-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPoolRestorePoint -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="eb826-115">Ez a parancs törli az Azure Synapse Analytics SQL-készlet visszaállítási pontját a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="eb826-115">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="eb826-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="eb826-116">Example 3</span></span>
```powershell
PS C:\> $points = Get-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $points[index] | Remove-AzSynapseSqlPoolRestorePoint
```

<span data-ttu-id="eb826-117">Ez a parancs törli az Azure Synapse Analytics SQL-készlet visszaállítási pontját a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="eb826-117">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="eb826-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="eb826-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool/SqlPoolRestorePoints/RestorePointCreationDate
```

<span data-ttu-id="eb826-119">Ez a parancs törli a megadott erőforrás-azonosítójú Azure Synapse Analytics SQL-készlet visszaállítási pontját.</span><span class="sxs-lookup"><span data-stu-id="eb826-119">This command deletes an Azure Synapse Analytics SQL pool restore point with the specified resource ID.</span></span>

## <span data-ttu-id="eb826-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb826-120">PARAMETERS</span></span>

### <span data-ttu-id="eb826-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb826-121">-AsJob</span></span>
<span data-ttu-id="eb826-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="eb826-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eb826-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb826-123">-DefaultProfile</span></span>
<span data-ttu-id="eb826-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eb826-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb826-125">-Force</span><span class="sxs-lookup"><span data-stu-id="eb826-125">-Force</span></span>
<span data-ttu-id="eb826-126">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eb826-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="eb826-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb826-127">-InputObject</span></span>
<span data-ttu-id="eb826-128">SQL-készlet-visszaállítási pont létrehozási idő beviteli objektuma, amely általában áthalad a folyamaton.</span><span class="sxs-lookup"><span data-stu-id="eb826-128">SQL pool restore point creation time input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="eb826-129">-Name</span><span class="sxs-lookup"><span data-stu-id="eb826-129">-Name</span></span>
<span data-ttu-id="eb826-130">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="eb826-130">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="eb826-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb826-131">-PassThru</span></span>
<span data-ttu-id="eb826-132">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="eb826-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="eb826-133">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="eb826-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="eb826-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb826-134">-ResourceGroupName</span></span>
<span data-ttu-id="eb826-135">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="eb826-135">Resource group name.</span></span>

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

### <span data-ttu-id="eb826-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb826-136">-ResourceId</span></span>
<span data-ttu-id="eb826-137">A Synapse SQL-készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="eb826-137">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="eb826-138">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="eb826-138">-RestorePointCreationDate</span></span>
<span data-ttu-id="eb826-139">A Synapse SQL visszaállítási pont létrehozási dátumának neve.</span><span class="sxs-lookup"><span data-stu-id="eb826-139">Name of Synapse SQL Restore Point Creation Date .</span></span>

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

### <span data-ttu-id="eb826-140">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="eb826-140">-SqlPoolObject</span></span>
<span data-ttu-id="eb826-141">Sql Pool bemeneti objektum, amely általában a folyamaton keresztül áthalad.</span><span class="sxs-lookup"><span data-stu-id="eb826-141">Sql Pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="eb826-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="eb826-142">-WorkspaceName</span></span>
<span data-ttu-id="eb826-143">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="eb826-143">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="eb826-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb826-144">-Confirm</span></span>
<span data-ttu-id="eb826-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="eb826-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb826-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb826-146">-WhatIf</span></span>
<span data-ttu-id="eb826-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="eb826-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb826-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eb826-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb826-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb826-149">CommonParameters</span></span>
<span data-ttu-id="eb826-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb826-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb826-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb826-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb826-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eb826-152">INPUTS</span></span>

### <span data-ttu-id="eb826-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="eb826-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="eb826-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="eb826-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="eb826-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="eb826-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

### <span data-ttu-id="eb826-156">System.String</span><span class="sxs-lookup"><span data-stu-id="eb826-156">System.String</span></span>

## <span data-ttu-id="eb826-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb826-157">OUTPUTS</span></span>

### <span data-ttu-id="eb826-158">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="eb826-158">System.Boolean</span></span>

## <span data-ttu-id="eb826-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="eb826-159">NOTES</span></span>

## <span data-ttu-id="eb826-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb826-160">RELATED LINKS</span></span>
