---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/restore-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
ms.openlocfilehash: 3a9620a6b5fa68fc2d4e5baf647d8dc720d787a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941362"
---
# <span data-ttu-id="81716-101">Restore-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="81716-101">Restore-AzSynapseSqlPool</span></span>

## <span data-ttu-id="81716-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81716-102">SYNOPSIS</span></span>
<span data-ttu-id="81716-103">A Synapse Analytics SQL-készlet visszaállítása.</span><span class="sxs-lookup"><span data-stu-id="81716-103">Restores a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="81716-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="81716-104">SYNTAX</span></span>

### <span data-ttu-id="81716-105">RestoreFromBackupIdByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="81716-105">RestoreFromBackupIdByNameParameterSet (Default)</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="81716-106">RestoreFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81716-106">RestoreFromBackupIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="81716-107">RestoreFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="81716-107">RestoreFromRestorePointIdByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> -PerformanceLevel <String> -ResourceId <String> -RestorePoint <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81716-108">RestoreFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81716-108">RestoreFromRestorePointIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 -PerformanceLevel <String> -ResourceId <String> -RestorePoint <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81716-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="81716-109">DESCRIPTION</span></span>
<span data-ttu-id="81716-110">A **Restore-AzSynapseSqlPool** parancsmag visszaállítja az Azure Synapse Analytics SQL-készletet bármely SQL-készlet biztonsági másolatából vagy visszaállítási pontjából.</span><span class="sxs-lookup"><span data-stu-id="81716-110">The **Restore-AzSynapseSqlPool** cmdlet restores an Azure Synapse Analytics SQL pool from a backup or a restore point of any SQL pool.</span></span>
<span data-ttu-id="81716-111">A visszaállított SQL-készlet új SQL-készletként jön létre.</span><span class="sxs-lookup"><span data-stu-id="81716-111">The restored SQL pool is created as a new SQL pool.</span></span>

## <span data-ttu-id="81716-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="81716-112">EXAMPLES</span></span>

### <span data-ttu-id="81716-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="81716-113">Example 1</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="81716-114">Ez a parancs egy Azure Synapse Analytics SQL-készletet hoz létre úgy, hogy visszaállítja az előfizetés bármely SQL-készletének legutóbbi biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="81716-114">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="81716-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="81716-115">Example 2</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="81716-116">Ez a parancs egy Azure Synapse Analytics SQL-készletet hoz létre úgy, hogy az előfizetés bármely SQL-készletéből visszaállítási pontot használva helyreállít vagy másol egy korábbi állapotot.</span><span class="sxs-lookup"><span data-stu-id="81716-116">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="81716-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="81716-117">Example 3</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="81716-118">Ez a parancs létrehoz egy Azure Synapse Analytics SQL-készletet úgy, hogy visszaállítja az előfizetés bármely SQL-készletének legutóbbi biztonsági másolatát erőforrás-azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="81716-118">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="81716-119">4. példa</span><span class="sxs-lookup"><span data-stu-id="81716-119">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws | Restore-AzSynapseSqlPool -FromRestorePoint -Name ContosoSqlPool -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="81716-120">Ez a parancs egy Azure Synapse Analytics SQL-készletet hoz létre úgy, hogy az előfizetés bármely SQL-készletéből egy visszaállítási pontot használva helyreállít vagy másol egy erőforrás-azonosítóval egy korábbi állapotot.</span><span class="sxs-lookup"><span data-stu-id="81716-120">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="81716-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81716-121">PARAMETERS</span></span>

### <span data-ttu-id="81716-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81716-122">-AsJob</span></span>
<span data-ttu-id="81716-123">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="81716-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="81716-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81716-124">-DefaultProfile</span></span>
<span data-ttu-id="81716-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="81716-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81716-126">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="81716-126">-FromBackup</span></span>
<span data-ttu-id="81716-127">Azt jelzi, hogy az előfizetésben az SQL-készlet legutóbbi biztonsági másolatából kell visszaállítani.</span><span class="sxs-lookup"><span data-stu-id="81716-127">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81716-128">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="81716-128">-FromRestorePoint</span></span>
<span data-ttu-id="81716-129">Azt jelzi, hogy az előfizetés bármely SQL-készletéből ki kell használnia egy visszaállítási pontot egy korábbi állapot helyreállításához vagy egy korábbi állapotból való másoláshoz.</span><span class="sxs-lookup"><span data-stu-id="81716-129">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81716-130">-Name</span><span class="sxs-lookup"><span data-stu-id="81716-130">-Name</span></span>
<span data-ttu-id="81716-131">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="81716-131">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetSqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81716-132">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="81716-132">-PerformanceLevel</span></span>
<span data-ttu-id="81716-133">Az SQL-készlethez hozzárendelni szükséges SQL-szolgáltatásréteg és teljesítményszint.</span><span class="sxs-lookup"><span data-stu-id="81716-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="81716-134">Például DW2000c.</span><span class="sxs-lookup"><span data-stu-id="81716-134">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81716-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81716-135">-ResourceGroupName</span></span>
<span data-ttu-id="81716-136">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="81716-136">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81716-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81716-137">-ResourceId</span></span>
<span data-ttu-id="81716-138">A visszaállítani szükséges adatbázis erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="81716-138">The resource ID of the database to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81716-139">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="81716-139">-RestorePoint</span></span>
<span data-ttu-id="81716-140">A visszaállítás pillanatfelvételi ideje.</span><span class="sxs-lookup"><span data-stu-id="81716-140">Snapshot time to restore.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases: PointInTime

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81716-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="81716-141">-WorkspaceName</span></span>
<span data-ttu-id="81716-142">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="81716-142">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81716-143">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="81716-143">-WorkspaceObject</span></span>
<span data-ttu-id="81716-144">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="81716-144">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RestoreFromBackupIdByParentObjectParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81716-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81716-145">-Confirm</span></span>
<span data-ttu-id="81716-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="81716-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81716-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81716-147">-WhatIf</span></span>
<span data-ttu-id="81716-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="81716-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81716-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="81716-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81716-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81716-150">CommonParameters</span></span>
<span data-ttu-id="81716-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81716-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81716-152">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81716-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81716-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="81716-153">INPUTS</span></span>

### <span data-ttu-id="81716-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="81716-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="81716-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81716-155">OUTPUTS</span></span>

### <span data-ttu-id="81716-156">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="81716-156">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="81716-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="81716-157">NOTES</span></span>

## <span data-ttu-id="81716-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81716-158">RELATED LINKS</span></span>
