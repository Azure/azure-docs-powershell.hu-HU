---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/restore-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
ms.openlocfilehash: 7fbc6cedf039cca33d0a30b39a21f9cdcb350b61
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476586"
---
# <span data-ttu-id="1cb3e-101">Restore-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="1cb3e-101">Restore-AzSynapseSqlPool</span></span>

## <span data-ttu-id="1cb3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cb3e-102">SYNOPSIS</span></span>
<span data-ttu-id="1cb3e-103">A Synapse Analytics SQL-készlet visszaállítása.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-103">Restores a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="1cb3e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1cb3e-104">SYNTAX</span></span>

### <span data-ttu-id="1cb3e-105">RestoreFromBackupIdByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1cb3e-105">RestoreFromBackupIdByNameParameterSet (Default)</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cb3e-106">RestoreFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cb3e-106">RestoreFromBackupIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1cb3e-107">RestoreFromBackupNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cb3e-107">RestoreFromBackupNameByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1cb3e-108">RestoreFromBackupNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cb3e-108">RestoreFromBackupNameByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-BackupResourceGroupName <String>] -BackupWorkspaceName <String> -BackupSqlPoolName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cb3e-109">RestoreFromBackupInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cb3e-109">RestoreFromBackupInputObjectByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] -BackupSqlPoolObject <PSSynapseSqlPool> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cb3e-110">RestoreFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cb3e-110">RestoreFromRestorePointIdByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1cb3e-111">RestoreFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cb3e-111">RestoreFromRestorePointIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String> [-RestorePoint <DateTime>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cb3e-112">RestoreFromRestorePointNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cb3e-112">RestoreFromRestorePointNameByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] -PerformanceLevel <String> [-SourceResourceGroupName <String>]
 -SourceWorkspaceName <String> -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cb3e-113">RestoreFromRestorePointNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cb3e-113">RestoreFromRestorePointNameByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Tag <Hashtable>] [-SourceResourceGroupName <String>] -SourceWorkspaceName <String>
 -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1cb3e-114">RestoreFromRestorePointInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cb3e-114">RestoreFromRestorePointInputObjectByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] [-PerformanceLevel <String>] -SourceSqlPoolObject <PSSynapseSqlPool>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cb3e-115">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1cb3e-115">DESCRIPTION</span></span>
<span data-ttu-id="1cb3e-116">A **Restore-AzSynapseSqlPool** parancsmag visszaállítja az Azure Synapse Analytics SQL-készletet bármely SQL-készlet biztonsági másolatából vagy visszaállítási pontjából.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-116">The **Restore-AzSynapseSqlPool** cmdlet restores an Azure Synapse Analytics SQL pool from a backup or a restore point of any SQL pool.</span></span>
<span data-ttu-id="1cb3e-117">A visszaállított SQL-készlet új SQL-készletként jön létre.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-117">The restored SQL pool is created as a new SQL pool.</span></span>

## <span data-ttu-id="1cb3e-118">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1cb3e-118">EXAMPLES</span></span>

### <span data-ttu-id="1cb3e-119">1. példa</span><span class="sxs-lookup"><span data-stu-id="1cb3e-119">Example 1</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="1cb3e-120">Ez a parancs egy Azure Synapse Analytics SQL-készletet hoz létre úgy, hogy visszaállítja az előfizetés bármely SQL-készletének legutóbbi biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-120">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="1cb3e-121">2. példa</span><span class="sxs-lookup"><span data-stu-id="1cb3e-121">Example 2</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="1cb3e-122">Ez a parancs egy Azure Synapse Analytics SQL-készletet hoz létre úgy, hogy az előfizetés bármely SQL-készletéből visszaállítási pontot használva helyreállít vagy másol egy korábbi állapotot.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-122">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="1cb3e-123">3. példa</span><span class="sxs-lookup"><span data-stu-id="1cb3e-123">Example 3</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="1cb3e-124">Ez a parancs létrehoz egy Azure Synapse Analytics SQL-készletet úgy, hogy visszaállítja az előfizetés bármely SQL-készletének legutóbbi biztonsági másolatát erőforrás-azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-124">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="1cb3e-125">4. példa</span><span class="sxs-lookup"><span data-stu-id="1cb3e-125">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws | Restore-AzSynapseSqlPool -FromRestorePoint -Name ContosoSqlPool -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="1cb3e-126">Ez a parancs egy Azure Synapse Analytics SQL-készletet hoz létre úgy, hogy az előfizetés bármely SQL-készletéből egy visszaállítási pontot használva helyreállít vagy másol egy erőforrás-azonosítóval egy korábbi állapotot.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-126">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="1cb3e-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1cb3e-127">PARAMETERS</span></span>

### <span data-ttu-id="1cb3e-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1cb3e-128">-AsJob</span></span>
<span data-ttu-id="1cb3e-129">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1cb3e-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1cb3e-130">-BackupResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cb3e-130">-BackupResourceGroupName</span></span>
<span data-ttu-id="1cb3e-131">Az erőforráscsoport neve, amelyből létre kell hozni az SQL-készletobjektumot.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-131">The resource group name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb3e-132">-BackupResourceId</span><span class="sxs-lookup"><span data-stu-id="1cb3e-132">-BackupResourceId</span></span>
<span data-ttu-id="1cb3e-133">A visszaállítható biztonsági másolat SQL-készletobjektum erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-133">The resource identifier of backup SQL pool object to restore from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb3e-134">-BackupSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="1cb3e-134">-BackupSqlPoolName</span></span>
<span data-ttu-id="1cb3e-135">Annak az SQL-készletobjektumnak a neve, amelyből létre kell hoznia az SQL-készletet.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-135">The name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet
Aliases: BackupDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb3e-136">-BackupSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="1cb3e-136">-BackupSqlPoolObject</span></span>
<span data-ttu-id="1cb3e-137">SQL-készlet bemeneti objektuma, amely általában a folyamaton keresztül áthalad.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-137">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: RestoreFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb3e-138">-BackupWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1cb3e-138">-BackupWorkspaceName</span></span>
<span data-ttu-id="1cb3e-139">A synapse workspace name of bakcup SQL pool object to create from.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-139">The Synapse workspace name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet
Aliases: BackupServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb3e-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cb3e-140">-DefaultProfile</span></span>
<span data-ttu-id="1cb3e-141">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cb3e-142">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="1cb3e-142">-FromBackup</span></span>
<span data-ttu-id="1cb3e-143">Azt jelzi, hogy az előfizetésben az SQL-készlet legutóbbi biztonsági másolatából kell visszaállítani.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-143">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupIdByParentObjectParameterSet, RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet, RestoreFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb3e-144">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="1cb3e-144">-FromRestorePoint</span></span>
<span data-ttu-id="1cb3e-145">Azt jelzi, hogy az előfizetés bármely SQL-készletéből ki kell használnia egy visszaállítási pontot egy korábbi állapot helyreállításához vagy egy korábbi állapotból való másoláshoz.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-145">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet, RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet, RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb3e-146">-Name</span><span class="sxs-lookup"><span data-stu-id="1cb3e-146">-Name</span></span>
<span data-ttu-id="1cb3e-147">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-147">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="1cb3e-148">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="1cb3e-148">-PerformanceLevel</span></span>
<span data-ttu-id="1cb3e-149">Az SQL-készlethez hozzárendelni szükséges SQL-szolgáltatásréteg és teljesítményszint.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-149">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="1cb3e-150">Például DW2000c.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-150">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet, RestoreFromRestorePointNameByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb3e-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cb3e-151">-ResourceGroupName</span></span>
<span data-ttu-id="1cb3e-152">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-152">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupNameByNameParameterSet, RestoreFromBackupInputObjectByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb3e-153">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="1cb3e-153">-RestorePoint</span></span>
<span data-ttu-id="1cb3e-154">A visszaállítás pillanatfelvételi ideje.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-154">Snapshot time to restore.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb3e-155">-SourceResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cb3e-155">-SourceResourceGroupName</span></span>
<span data-ttu-id="1cb3e-156">A forrás SQL-készlet objektumának erőforráscsoportneve, amelyből létre kell hozni.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-156">The resource group name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb3e-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="1cb3e-157">-SourceResourceId</span></span>
<span data-ttu-id="1cb3e-158">A forrás SQL-készlet objektumának erőforrás-azonosítója, amelyből létre kell hozni.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-158">The resource identifier of source SQL pool object to create from.</span></span>

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

### <span data-ttu-id="1cb3e-159">-SourceSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="1cb3e-159">-SourceSqlPoolName</span></span>
<span data-ttu-id="1cb3e-160">A forrás SQL-készlet objektumának neve, amelyből létre kell hozni.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-160">The name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases: SourceDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb3e-161">-SourceSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="1cb3e-161">-SourceSqlPoolObject</span></span>
<span data-ttu-id="1cb3e-162">SQL-készlet bemeneti objektuma, amely általában a folyamaton keresztül áthalad.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-162">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb3e-163">-SourceWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1cb3e-163">-SourceWorkspaceName</span></span>
<span data-ttu-id="1cb3e-164">A Synapse munkaterületének neve a forrás SQL-készlet objektumból, amelyből létre kell hoznia.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-164">The Synapse workspace name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases: SourceServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb3e-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="1cb3e-165">-Tag</span></span>
<span data-ttu-id="1cb3e-166">Az erőforráshoz társított címkék karakterlánc-karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-166">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="1cb3e-167">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1cb3e-167">-WorkspaceName</span></span>
<span data-ttu-id="1cb3e-168">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-168">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupNameByNameParameterSet, RestoreFromBackupInputObjectByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb3e-169">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1cb3e-169">-WorkspaceObject</span></span>
<span data-ttu-id="1cb3e-170">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-170">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RestoreFromBackupIdByParentObjectParameterSet, RestoreFromBackupNameByParentObjectParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1cb3e-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1cb3e-171">-Confirm</span></span>
<span data-ttu-id="1cb3e-172">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cb3e-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cb3e-173">-WhatIf</span></span>
<span data-ttu-id="1cb3e-174">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cb3e-175">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cb3e-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cb3e-176">CommonParameters</span></span>
<span data-ttu-id="1cb3e-177">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cb3e-178">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1cb3e-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cb3e-179">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1cb3e-179">INPUTS</span></span>

### <span data-ttu-id="1cb3e-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1cb3e-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="1cb3e-181">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1cb3e-181">OUTPUTS</span></span>

### <span data-ttu-id="1cb3e-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="1cb3e-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="1cb3e-183">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1cb3e-183">NOTES</span></span>

## <span data-ttu-id="1cb3e-184">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1cb3e-184">RELATED LINKS</span></span>
