---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/restore-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
ms.openlocfilehash: 2dae942470dba8a36258ffb8c813e08c664f2e26
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301703"
---
# <span data-ttu-id="695e7-101">Restore-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="695e7-101">Restore-AzSynapseSqlPool</span></span>

## <span data-ttu-id="695e7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="695e7-102">SYNOPSIS</span></span>
<span data-ttu-id="695e7-103">A szinapszis Analytics SQL-készlet visszaállítása.</span><span class="sxs-lookup"><span data-stu-id="695e7-103">Restores a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="695e7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="695e7-104">SYNTAX</span></span>

### <span data-ttu-id="695e7-105">RestoreFromBackupIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="695e7-105">RestoreFromBackupIdByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="695e7-106">RestoreFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="695e7-106">RestoreFromBackupIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="695e7-107">RestoreFromBackupNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="695e7-107">RestoreFromBackupNameByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="695e7-108">RestoreFromBackupNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="695e7-108">RestoreFromBackupNameByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-BackupResourceGroupName <String>] -BackupWorkspaceName <String> -BackupSqlPoolName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="695e7-109">RestoreFromBackupInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="695e7-109">RestoreFromBackupInputObjectByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] -BackupSqlPoolObject <PSSynapseSqlPool> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="695e7-110">RestoreFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="695e7-110">RestoreFromRestorePointIdByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="695e7-111">RestoreFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="695e7-111">RestoreFromRestorePointIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String> [-RestorePoint <DateTime>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="695e7-112">RestoreFromRestorePointNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="695e7-112">RestoreFromRestorePointNameByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] -PerformanceLevel <String> [-SourceResourceGroupName <String>]
 -SourceWorkspaceName <String> -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="695e7-113">RestoreFromRestorePointNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="695e7-113">RestoreFromRestorePointNameByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Tag <Hashtable>] [-SourceResourceGroupName <String>] -SourceWorkspaceName <String>
 -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="695e7-114">RestoreFromRestorePointInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="695e7-114">RestoreFromRestorePointInputObjectByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] [-PerformanceLevel <String>] -SourceSqlPoolObject <PSSynapseSqlPool>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="695e7-115">Leírás</span><span class="sxs-lookup"><span data-stu-id="695e7-115">DESCRIPTION</span></span>
<span data-ttu-id="695e7-116">A **Restore-AzSynapseSqlPool** parancsmag az Azure SZINAPSZIS Analytics SQL-készletét visszaállítja egy biztonsági másolatból vagy egy SQL-készlet visszaállítási pontjából.</span><span class="sxs-lookup"><span data-stu-id="695e7-116">The **Restore-AzSynapseSqlPool** cmdlet restores an Azure Synapse Analytics SQL pool from a backup or a restore point of any SQL pool.</span></span>
<span data-ttu-id="695e7-117">A helyreállított SQL-készlet új SQL-készletként jön létre.</span><span class="sxs-lookup"><span data-stu-id="695e7-117">The restored SQL pool is created as a new SQL pool.</span></span>

## <span data-ttu-id="695e7-118">Példák</span><span class="sxs-lookup"><span data-stu-id="695e7-118">EXAMPLES</span></span>

### <span data-ttu-id="695e7-119">Példa 1</span><span class="sxs-lookup"><span data-stu-id="695e7-119">Example 1</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="695e7-120">Ez a parancs az Azure szinapszis Analytics SQL-készletet hozza létre az előfizetésben lévő SQL-készlet legutóbbi biztonsági másolatával.</span><span class="sxs-lookup"><span data-stu-id="695e7-120">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="695e7-121">2. példa</span><span class="sxs-lookup"><span data-stu-id="695e7-121">Example 2</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="695e7-122">Ez a parancs egy Azure szinapszis-Analytics SQL-készletet hoz létre úgy, hogy az előfizetésben szereplő bármelyik SQL-alkalmazáskészlet visszaállítási pontját kihasználva visszaállíthatja vagy átmásolhatja az előző állapotát.</span><span class="sxs-lookup"><span data-stu-id="695e7-122">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="695e7-123">3. példa</span><span class="sxs-lookup"><span data-stu-id="695e7-123">Example 3</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="695e7-124">A parancs az Azure szinapszis Analytics SQL-készletet hozza létre az előfizetés SQL-készletének legutóbbi biztonsági másolatával az erőforrás-AZONOSÍTÓval.</span><span class="sxs-lookup"><span data-stu-id="695e7-124">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="695e7-125">4. példa</span><span class="sxs-lookup"><span data-stu-id="695e7-125">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws | Restore-AzSynapseSqlPool -FromRestorePoint -Name ContosoSqlPool -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="695e7-126">Ez a parancs egy Azure szinapszis-Analytics SQL-készletet hoz létre úgy, hogy az előfizetésben szereplő bármelyik SQL-alkalmazáskészlet visszaállítási pontját kikényszerítve állítja vissza az erőforrás-AZONOSÍTÓval egy korábbi állapotot.</span><span class="sxs-lookup"><span data-stu-id="695e7-126">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="695e7-127">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="695e7-127">PARAMETERS</span></span>

### <span data-ttu-id="695e7-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="695e7-128">-AsJob</span></span>
<span data-ttu-id="695e7-129">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="695e7-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="695e7-130">-BackupResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="695e7-130">-BackupResourceGroupName</span></span>
<span data-ttu-id="695e7-131">A bakcup tartozó SQL Pool objektum erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="695e7-131">The resource group name of bakcup SQL pool object to create from.</span></span>

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

### <span data-ttu-id="695e7-132">-BackupResourceId</span><span class="sxs-lookup"><span data-stu-id="695e7-132">-BackupResourceId</span></span>
<span data-ttu-id="695e7-133">A biztonsági másolat SQL-alkalmazáskészletének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="695e7-133">The resource identifier of backup SQL pool object to restore from.</span></span>

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

### <span data-ttu-id="695e7-134">-BackupSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="695e7-134">-BackupSqlPoolName</span></span>
<span data-ttu-id="695e7-135">Annak a bakcup az SQL Pool-objektumnak a neve, amelyből létre kíván hozni.</span><span class="sxs-lookup"><span data-stu-id="695e7-135">The name of bakcup SQL pool object to create from.</span></span>

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

### <span data-ttu-id="695e7-136">-BackupSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="695e7-136">-BackupSqlPoolObject</span></span>
<span data-ttu-id="695e7-137">Az SQL-készlet bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="695e7-137">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="695e7-138">-BackupWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="695e7-138">-BackupWorkspaceName</span></span>
<span data-ttu-id="695e7-139">A bakcup-hoz létrehozható SQL Pool objektum szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="695e7-139">The Synapse workspace name of bakcup SQL pool object to create from.</span></span>

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

### <span data-ttu-id="695e7-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="695e7-140">-DefaultProfile</span></span>
<span data-ttu-id="695e7-141">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="695e7-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="695e7-142">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="695e7-142">-FromBackup</span></span>
<span data-ttu-id="695e7-143">Azt jelzi, hogy az előfizetésben szereplő SQL-készlet legutóbbi biztonsági másolatáról vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="695e7-143">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

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

### <span data-ttu-id="695e7-144">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="695e7-144">-FromRestorePoint</span></span>
<span data-ttu-id="695e7-145">Azt jelzi, hogy az előfizetésben szereplő összes SQL-készlet visszaállítási pontjának tőkeáttételét egy korábbi állapot helyreállítása vagy másolása céljából használja.</span><span class="sxs-lookup"><span data-stu-id="695e7-145">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

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

### <span data-ttu-id="695e7-146">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="695e7-146">-Name</span></span>
<span data-ttu-id="695e7-147">A szinapszis SQL Pool neve.</span><span class="sxs-lookup"><span data-stu-id="695e7-147">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="695e7-148">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="695e7-148">-PerformanceLevel</span></span>
<span data-ttu-id="695e7-149">Az SQL-szolgáltatási szint és a teljesítmény szint az SQL-készlethez való hozzárendeléshez</span><span class="sxs-lookup"><span data-stu-id="695e7-149">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="695e7-150">Például DW2000c.</span><span class="sxs-lookup"><span data-stu-id="695e7-150">For example, DW2000c.</span></span>

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

### <span data-ttu-id="695e7-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="695e7-151">-ResourceGroupName</span></span>
<span data-ttu-id="695e7-152">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="695e7-152">Resource group name.</span></span>

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

### <span data-ttu-id="695e7-153">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="695e7-153">-RestorePoint</span></span>
<span data-ttu-id="695e7-154">Pillanatkép-idő a visszaállításhoz.</span><span class="sxs-lookup"><span data-stu-id="695e7-154">Snapshot time to restore.</span></span>

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

### <span data-ttu-id="695e7-155">-SourceResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="695e7-155">-SourceResourceGroupName</span></span>
<span data-ttu-id="695e7-156">A forrás SQL-készlet objektumból létrehozandó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="695e7-156">The resource group name of source SQL pool object to create from.</span></span>

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

### <span data-ttu-id="695e7-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="695e7-157">-SourceResourceId</span></span>
<span data-ttu-id="695e7-158">A forrás SQL-alkalmazáskészlet objektumból létrehozható erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="695e7-158">The resource identifier of source SQL pool object to create from.</span></span>

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

### <span data-ttu-id="695e7-159">-SourceSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="695e7-159">-SourceSqlPoolName</span></span>
<span data-ttu-id="695e7-160">A forrásként létrehozandó SQL Pool objektum neve.</span><span class="sxs-lookup"><span data-stu-id="695e7-160">The name of source SQL pool object to create from.</span></span>

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

### <span data-ttu-id="695e7-161">-SourceSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="695e7-161">-SourceSqlPoolObject</span></span>
<span data-ttu-id="695e7-162">Az SQL-készlet bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="695e7-162">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="695e7-163">-SourceWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="695e7-163">-SourceWorkspaceName</span></span>
<span data-ttu-id="695e7-164">A szinapszis munkaterület neve, amelyből a forrás SQL Pool objektum jön létre.</span><span class="sxs-lookup"><span data-stu-id="695e7-164">The Synapse workspace name of source SQL pool object to create from.</span></span>

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

### <span data-ttu-id="695e7-165">-Címke</span><span class="sxs-lookup"><span data-stu-id="695e7-165">-Tag</span></span>
<span data-ttu-id="695e7-166">Az erőforráshoz társított címkék karakterlánca, karakterláncok szótára</span><span class="sxs-lookup"><span data-stu-id="695e7-166">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="695e7-167">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="695e7-167">-WorkspaceName</span></span>
<span data-ttu-id="695e7-168">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="695e7-168">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="695e7-169">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="695e7-169">-WorkspaceObject</span></span>
<span data-ttu-id="695e7-170">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="695e7-170">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="695e7-171">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="695e7-171">-Confirm</span></span>
<span data-ttu-id="695e7-172">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="695e7-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="695e7-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="695e7-173">-WhatIf</span></span>
<span data-ttu-id="695e7-174">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="695e7-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="695e7-175">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="695e7-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="695e7-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="695e7-176">CommonParameters</span></span>
<span data-ttu-id="695e7-177">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="695e7-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="695e7-178">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="695e7-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="695e7-179">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="695e7-179">INPUTS</span></span>

### <span data-ttu-id="695e7-180">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="695e7-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="695e7-181">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="695e7-181">OUTPUTS</span></span>

### <span data-ttu-id="695e7-182">Microsoft. Azure. commands. szinapszis. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="695e7-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="695e7-183">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="695e7-183">NOTES</span></span>

## <span data-ttu-id="695e7-184">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="695e7-184">RELATED LINKS</span></span>
