---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: ceeb33615748b7cf11c13441399bbae6a934a56f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383360"
---
# <span data-ttu-id="02b48-101">Remove-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="02b48-101">Remove-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="02b48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02b48-102">SYNOPSIS</span></span>
<span data-ttu-id="02b48-103">A Synapse Analytics SQL-készlet visszaállítási pontjának törlése.</span><span class="sxs-lookup"><span data-stu-id="02b48-103">Deletes a Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="02b48-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="02b48-104">SYNTAX</span></span>

### <span data-ttu-id="02b48-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="02b48-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -SqlPoolName <String>
 -RestorePointCreationDate <DateTime> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02b48-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02b48-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -RestorePointCreationDate <DateTime> -SqlPoolObject <PSSynapseSqlPool>
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02b48-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02b48-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -InputObject <PSRestorePoint> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02b48-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="02b48-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02b48-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="02b48-109">DESCRIPTION</span></span>
<span data-ttu-id="02b48-110">A **Remove-AzSynapseSqlPoolRestorePoint** parancsmag véglegesen törli az Azure Synapse Analytics SQL-készlet visszaállítási pontját.</span><span class="sxs-lookup"><span data-stu-id="02b48-110">The **Remove-AzSynapseSqlPoolRestorePoint** cmdlet permanently deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="02b48-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="02b48-111">EXAMPLES</span></span>

### <span data-ttu-id="02b48-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="02b48-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="02b48-113">Ez a parancs törli az Azure Synapse Analytics SQL-készlet visszaállítási pontját.</span><span class="sxs-lookup"><span data-stu-id="02b48-113">This command deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

### <span data-ttu-id="02b48-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="02b48-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPoolRestorePoint -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="02b48-115">Ez a parancs törli az Azure Synapse Analytics SQL-készlet visszaállítási pontját a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="02b48-115">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="02b48-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="02b48-116">Example 3</span></span>
```powershell
PS C:\> $points = Get-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $points[index] | Remove-AzSynapseSqlPoolRestorePoint
```

<span data-ttu-id="02b48-117">Ez a parancs törli az Azure Synapse Analytics SQL-készlet visszaállítási pontját a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="02b48-117">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="02b48-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="02b48-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool/SqlPoolRestorePoints/RestorePointCreationDate
```

<span data-ttu-id="02b48-119">Ez a parancs törli a megadott erőforrás-azonosítójú Azure Synapse Analytics SQL-készlet visszaállítási pontját.</span><span class="sxs-lookup"><span data-stu-id="02b48-119">This command deletes an Azure Synapse Analytics SQL pool restore point with the specified resource ID.</span></span>

## <span data-ttu-id="02b48-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02b48-120">PARAMETERS</span></span>

### <span data-ttu-id="02b48-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02b48-121">-AsJob</span></span>
<span data-ttu-id="02b48-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="02b48-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02b48-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02b48-123">-DefaultProfile</span></span>
<span data-ttu-id="02b48-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="02b48-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02b48-125">-Force</span><span class="sxs-lookup"><span data-stu-id="02b48-125">-Force</span></span>
<span data-ttu-id="02b48-126">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="02b48-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="02b48-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02b48-127">-InputObject</span></span>
<span data-ttu-id="02b48-128">SQL-készlet-visszaállítási pont létrehozási idő beviteli objektuma, amely általában a folyamaton keresztül megy keresztül.</span><span class="sxs-lookup"><span data-stu-id="02b48-128">SQL pool restore point creation time input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="02b48-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02b48-129">-PassThru</span></span>
<span data-ttu-id="02b48-130">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="02b48-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="02b48-131">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="02b48-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="02b48-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02b48-132">-ResourceGroupName</span></span>
<span data-ttu-id="02b48-133">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="02b48-133">Resource group name.</span></span>

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

### <span data-ttu-id="02b48-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02b48-134">-ResourceId</span></span>
<span data-ttu-id="02b48-135">A Synapse SQL-készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="02b48-135">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="02b48-136">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="02b48-136">-RestorePointCreationDate</span></span>
<span data-ttu-id="02b48-137">A Synapse SQL visszaállítási pont létrehozási dátumának neve.</span><span class="sxs-lookup"><span data-stu-id="02b48-137">Name of Synapse SQL Restore Point Creation Date .</span></span>

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

### <span data-ttu-id="02b48-138">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="02b48-138">-SqlPoolName</span></span>
<span data-ttu-id="02b48-139">A Synapse Sql-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="02b48-139">Name of Synapse Sql pool.</span></span>

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

### <span data-ttu-id="02b48-140">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="02b48-140">-SqlPoolObject</span></span>
<span data-ttu-id="02b48-141">Sql Pool bemeneti objektum, amely általában a folyamaton keresztül áthalad.</span><span class="sxs-lookup"><span data-stu-id="02b48-141">Sql Pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="02b48-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="02b48-142">-WorkspaceName</span></span>
<span data-ttu-id="02b48-143">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="02b48-143">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="02b48-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02b48-144">-Confirm</span></span>
<span data-ttu-id="02b48-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="02b48-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02b48-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02b48-146">-WhatIf</span></span>
<span data-ttu-id="02b48-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="02b48-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02b48-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="02b48-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02b48-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02b48-149">CommonParameters</span></span>
<span data-ttu-id="02b48-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02b48-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02b48-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02b48-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02b48-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="02b48-152">INPUTS</span></span>

### <span data-ttu-id="02b48-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="02b48-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="02b48-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="02b48-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="02b48-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="02b48-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

### <span data-ttu-id="02b48-156">System.String</span><span class="sxs-lookup"><span data-stu-id="02b48-156">System.String</span></span>

## <span data-ttu-id="02b48-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02b48-157">OUTPUTS</span></span>

### <span data-ttu-id="02b48-158">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="02b48-158">System.Boolean</span></span>

## <span data-ttu-id="02b48-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="02b48-159">NOTES</span></span>

## <span data-ttu-id="02b48-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02b48-160">RELATED LINKS</span></span>
