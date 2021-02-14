---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/restore-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
ms.openlocfilehash: fd83b97a7b95760d0ee2ce88295ed14c98a43ab3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149922"
---
# <span data-ttu-id="66ad5-101">Restore-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="66ad5-101">Restore-AzSynapseSqlPool</span></span>

## <span data-ttu-id="66ad5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66ad5-102">SYNOPSIS</span></span>
<span data-ttu-id="66ad5-103">A Synapse Analytics SQL-készlet visszaállítása.</span><span class="sxs-lookup"><span data-stu-id="66ad5-103">Restores a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="66ad5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="66ad5-104">SYNTAX</span></span>

### <span data-ttu-id="66ad5-105">RestoreFromBackupIdByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="66ad5-105">RestoreFromBackupIdByNameParameterSet (Default)</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66ad5-106">RestoreFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66ad5-106">RestoreFromBackupIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66ad5-107">RestoreFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="66ad5-107">RestoreFromRestorePointIdByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> -PerformanceLevel <String> -ResourceId <String> -RestorePoint <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66ad5-108">RestoreFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66ad5-108">RestoreFromRestorePointIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 -PerformanceLevel <String> -ResourceId <String> -RestorePoint <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66ad5-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="66ad5-109">DESCRIPTION</span></span>
<span data-ttu-id="66ad5-110">A **Restore-AzSynapseSqlPool** parancsmag visszaállítja az Azure Synapse Analytics SQL-készletet bármely SQL-készlet biztonsági másolatából vagy visszaállítási pontjából.</span><span class="sxs-lookup"><span data-stu-id="66ad5-110">The **Restore-AzSynapseSqlPool** cmdlet restores an Azure Synapse Analytics SQL pool from a backup or a restore point of any SQL pool.</span></span>
<span data-ttu-id="66ad5-111">A visszaállított SQL-készlet új SQL-készletként jön létre.</span><span class="sxs-lookup"><span data-stu-id="66ad5-111">The restored SQL pool is created as a new SQL pool.</span></span>

## <span data-ttu-id="66ad5-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="66ad5-112">EXAMPLES</span></span>

### <span data-ttu-id="66ad5-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="66ad5-113">Example 1</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="66ad5-114">Ez a parancs létrehoz egy Azure Synapse Analytics SQL-készletet úgy, hogy visszaállítja az előfizetés bármely SQL-készletének legutóbbi biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="66ad5-114">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="66ad5-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="66ad5-115">Example 2</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="66ad5-116">Ez a parancs egy Azure Synapse Analytics SQL-készletet hoz létre úgy, hogy az előfizetés bármely SQL-készletéből visszaállítási pontot használva helyreállít vagy másol egy korábbi állapotot.</span><span class="sxs-lookup"><span data-stu-id="66ad5-116">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="66ad5-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="66ad5-117">Example 3</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="66ad5-118">Ez a parancs egy Azure Synapse Analytics SQL-készletet hoz létre, amely az előfizetésben található bármely SQL-készlet legutóbbi biztonsági másolatából, erőforrás-azonosítóval való visszaállítással hoz létre.</span><span class="sxs-lookup"><span data-stu-id="66ad5-118">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="66ad5-119">4. példa</span><span class="sxs-lookup"><span data-stu-id="66ad5-119">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws | Restore-AzSynapseSqlPool -FromRestorePoint -Name ContosoSqlPool -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="66ad5-120">Ez a parancs egy Azure Synapse Analytics SQL-készletet hoz létre úgy, hogy az előfizetés bármely SQL-készletéből egy visszaállítási pontot használva helyreállítja vagy átmásolja az erőforrás-azonosítót egy korábbi állapotból.</span><span class="sxs-lookup"><span data-stu-id="66ad5-120">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="66ad5-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66ad5-121">PARAMETERS</span></span>

### <span data-ttu-id="66ad5-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66ad5-122">-AsJob</span></span>
<span data-ttu-id="66ad5-123">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="66ad5-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="66ad5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66ad5-124">-DefaultProfile</span></span>
<span data-ttu-id="66ad5-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="66ad5-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66ad5-126">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="66ad5-126">-FromBackup</span></span>
<span data-ttu-id="66ad5-127">Azt jelzi, hogy az előfizetésben az SQL-készlet legutóbbi biztonsági másolatából kell visszaállítani.</span><span class="sxs-lookup"><span data-stu-id="66ad5-127">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

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

### <span data-ttu-id="66ad5-128">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="66ad5-128">-FromRestorePoint</span></span>
<span data-ttu-id="66ad5-129">Azt jelzi, hogy az előfizetés bármely SQL-készletéből ki kell használnia egy visszaállítási pontot egy korábbi állapot helyreállításához vagy egy korábbi állapotból való másoláshoz.</span><span class="sxs-lookup"><span data-stu-id="66ad5-129">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

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

### <span data-ttu-id="66ad5-130">-Name</span><span class="sxs-lookup"><span data-stu-id="66ad5-130">-Name</span></span>
<span data-ttu-id="66ad5-131">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="66ad5-131">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="66ad5-132">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="66ad5-132">-PerformanceLevel</span></span>
<span data-ttu-id="66ad5-133">Az SQL-készlethez hozzárendelni szükséges SQL-szolgáltatásréteg és teljesítményszint.</span><span class="sxs-lookup"><span data-stu-id="66ad5-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="66ad5-134">Például DW2000c.</span><span class="sxs-lookup"><span data-stu-id="66ad5-134">For example, DW2000c.</span></span>

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

### <span data-ttu-id="66ad5-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66ad5-135">-ResourceGroupName</span></span>
<span data-ttu-id="66ad5-136">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="66ad5-136">Resource group name.</span></span>

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

### <span data-ttu-id="66ad5-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66ad5-137">-ResourceId</span></span>
<span data-ttu-id="66ad5-138">A visszaállítani szükséges adatbázis erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="66ad5-138">The resource ID of the database to restore.</span></span>

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

### <span data-ttu-id="66ad5-139">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="66ad5-139">-RestorePoint</span></span>
<span data-ttu-id="66ad5-140">A visszaállítás pillanatfelvételi ideje.</span><span class="sxs-lookup"><span data-stu-id="66ad5-140">Snapshot time to restore.</span></span>

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

### <span data-ttu-id="66ad5-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="66ad5-141">-WorkspaceName</span></span>
<span data-ttu-id="66ad5-142">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="66ad5-142">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="66ad5-143">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="66ad5-143">-WorkspaceObject</span></span>
<span data-ttu-id="66ad5-144">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="66ad5-144">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="66ad5-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66ad5-145">-Confirm</span></span>
<span data-ttu-id="66ad5-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="66ad5-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66ad5-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66ad5-147">-WhatIf</span></span>
<span data-ttu-id="66ad5-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="66ad5-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66ad5-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="66ad5-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66ad5-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66ad5-150">CommonParameters</span></span>
<span data-ttu-id="66ad5-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66ad5-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66ad5-152">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66ad5-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66ad5-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="66ad5-153">INPUTS</span></span>

### <span data-ttu-id="66ad5-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="66ad5-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="66ad5-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66ad5-155">OUTPUTS</span></span>

### <span data-ttu-id="66ad5-156">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="66ad5-156">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="66ad5-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="66ad5-157">NOTES</span></span>

## <span data-ttu-id="66ad5-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66ad5-158">RELATED LINKS</span></span>
