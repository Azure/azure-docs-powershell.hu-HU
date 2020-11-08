---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: 694b9811bf11454e232f1514b59b1b537e4720a5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184674"
---
# <span data-ttu-id="9954f-101">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="9954f-101">New-AzSynapseSqlPool</span></span>

## <span data-ttu-id="9954f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9954f-102">SYNOPSIS</span></span>
<span data-ttu-id="9954f-103">A szinapszis Analytics SQL-készlet létrehozása.</span><span class="sxs-lookup"><span data-stu-id="9954f-103">Creates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="9954f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9954f-104">SYNTAX</span></span>

### <span data-ttu-id="9954f-105">CreateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9954f-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9954f-106">CreateFromBackupIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9954f-106">CreateFromBackupIdByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9954f-107">CreateFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9954f-107">CreateFromBackupIdByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9954f-108">CreateFromBackupNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9954f-108">CreateFromBackupNameByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9954f-109">CreateFromBackupNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9954f-109">CreateFromBackupNameByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9954f-110">CreateFromBackupInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9954f-110">CreateFromBackupInputObjectByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -BackupSqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9954f-111">CreateFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9954f-111">CreateFromRestorePointIdByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9954f-112">CreateFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9954f-112">CreateFromRestorePointIdByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9954f-113">CreateFromRestorePointNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9954f-113">CreateFromRestorePointNameByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> [-SourceResourceGroupName <String>]
 -SourceWorkspaceName <String> -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9954f-114">CreateFromRestorePointNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9954f-114">CreateFromRestorePointNameByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-SourceResourceGroupName <String>] -SourceWorkspaceName <String>
 -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9954f-115">CreateFromRestorePointInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9954f-115">CreateFromRestorePointInputObjectByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-PerformanceLevel <String>] -SourceSqlPoolObject <PSSynapseSqlPool>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9954f-116">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9954f-116">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9954f-117">Leírás</span><span class="sxs-lookup"><span data-stu-id="9954f-117">DESCRIPTION</span></span>
<span data-ttu-id="9954f-118">A **New-AzSynapseSqlPool** parancsmag az Azure SZINAPSZIS Analytics SQL poolját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="9954f-118">The **New-AzSynapseSqlPool** cmdlet creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="9954f-119">Példák</span><span class="sxs-lookup"><span data-stu-id="9954f-119">EXAMPLES</span></span>

### <span data-ttu-id="9954f-120">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9954f-120">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

<span data-ttu-id="9954f-121">A parancs létrehoz egy Azure szinapszis-Analytics SQL-medencét.</span><span class="sxs-lookup"><span data-stu-id="9954f-121">This command creates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="9954f-122">2. példa</span><span class="sxs-lookup"><span data-stu-id="9954f-122">Example 2</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="9954f-123">Ez a parancs az Azure szinapszis Analytics SQL-készletet hozza létre az előfizetésben lévő SQL-készlet legutóbbi biztonsági másolatával.</span><span class="sxs-lookup"><span data-stu-id="9954f-123">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="9954f-124">3. példa</span><span class="sxs-lookup"><span data-stu-id="9954f-124">Example 3</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="9954f-125">Ez a parancs egy Azure szinapszis-Analytics SQL-készletet hoz létre úgy, hogy az előfizetésben szereplő bármelyik SQL-alkalmazáskészlet visszaállítási pontját kihasználva visszaállíthatja vagy átmásolhatja az előző állapotát.</span><span class="sxs-lookup"><span data-stu-id="9954f-125">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="9954f-126">4. példa</span><span class="sxs-lookup"><span data-stu-id="9954f-126">Example 4</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="9954f-127">A parancs az Azure szinapszis Analytics SQL-készletet hozza létre az előfizetés SQL-készletének legutóbbi biztonsági másolatával az erőforrás-AZONOSÍTÓval.</span><span class="sxs-lookup"><span data-stu-id="9954f-127">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="9954f-128">Példa 5</span><span class="sxs-lookup"><span data-stu-id="9954f-128">Example 5</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws |  New-AzSynapseSqlPool -FromRestorePoint -Name dwsql0554 -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/mandywtest/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="9954f-129">Ez a parancs egy Azure szinapszis-Analytics SQL-készletet hoz létre úgy, hogy az előfizetésben szereplő bármelyik SQL-alkalmazáskészlet visszaállítási pontját kikényszerítve állítja vissza az erőforrás-AZONOSÍTÓval egy korábbi állapotot.</span><span class="sxs-lookup"><span data-stu-id="9954f-129">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="9954f-130">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9954f-130">PARAMETERS</span></span>

### <span data-ttu-id="9954f-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9954f-131">-AsJob</span></span>
<span data-ttu-id="9954f-132">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9954f-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9954f-133">-BackupResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9954f-133">-BackupResourceGroupName</span></span>
<span data-ttu-id="9954f-134">A bakcup tartozó SQL Pool objektum erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9954f-134">The resource group name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9954f-135">-BackupResourceId</span><span class="sxs-lookup"><span data-stu-id="9954f-135">-BackupResourceId</span></span>
<span data-ttu-id="9954f-136">A biztonsági másolat SQL-alkalmazáskészletének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9954f-136">The resource identifier of backup SQL pool object to restore from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupIdByNameParameterSet, CreateFromBackupIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9954f-137">-BackupSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="9954f-137">-BackupSqlPoolName</span></span>
<span data-ttu-id="9954f-138">Annak a bakcup az SQL Pool-objektumnak a neve, amelyből létre kíván hozni.</span><span class="sxs-lookup"><span data-stu-id="9954f-138">The name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases: BackupDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9954f-139">-BackupSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="9954f-139">-BackupSqlPoolObject</span></span>
<span data-ttu-id="9954f-140">Az SQL-készlet bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="9954f-140">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: CreateFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9954f-141">-BackupWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9954f-141">-BackupWorkspaceName</span></span>
<span data-ttu-id="9954f-142">A bakcup-hoz létrehozható SQL Pool objektum szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="9954f-142">The Synapse workspace name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases: BackupServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9954f-143">-Szétválogatás</span><span class="sxs-lookup"><span data-stu-id="9954f-143">-Collation</span></span>
<span data-ttu-id="9954f-144">A szétválogatás az adatrendezési és-összehasonlító szabályokat határozza meg, az SQL-készlet létrehozása után azonban nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="9954f-144">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="9954f-145">Az alapértelmezett rendezési sorrend SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="9954f-145">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9954f-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9954f-146">-DefaultProfile</span></span>
<span data-ttu-id="9954f-147">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9954f-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9954f-148">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="9954f-148">-FromBackup</span></span>
<span data-ttu-id="9954f-149">Azt jelzi, hogy az előfizetésben szereplő SQL-készlet legutóbbi biztonsági másolatáról vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="9954f-149">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateFromBackupIdByNameParameterSet, CreateFromBackupIdByParentObjectParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet, CreateFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9954f-150">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="9954f-150">-FromRestorePoint</span></span>
<span data-ttu-id="9954f-151">Azt jelzi, hogy az előfizetésben szereplő összes SQL-készlet visszaállítási pontjának tőkeáttételét egy korábbi állapot helyreállítása vagy másolása céljából használja.</span><span class="sxs-lookup"><span data-stu-id="9954f-151">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9954f-152">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9954f-152">-Name</span></span>
<span data-ttu-id="9954f-153">A szinapszis SQL Pool neve.</span><span class="sxs-lookup"><span data-stu-id="9954f-153">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="9954f-154">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="9954f-154">-PerformanceLevel</span></span>
<span data-ttu-id="9954f-155">Az SQL-szolgáltatási szint és a teljesítmény szint az SQL-készlethez való hozzárendeléshez</span><span class="sxs-lookup"><span data-stu-id="9954f-155">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="9954f-156">Például DW2000c.</span><span class="sxs-lookup"><span data-stu-id="9954f-156">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9954f-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9954f-157">-ResourceGroupName</span></span>
<span data-ttu-id="9954f-158">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="9954f-158">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromBackupIdByNameParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupInputObjectByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9954f-159">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="9954f-159">-RestorePoint</span></span>
<span data-ttu-id="9954f-160">Pillanatkép-idő a visszaállításhoz.</span><span class="sxs-lookup"><span data-stu-id="9954f-160">Snapshot time to restore.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9954f-161">-SourceResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9954f-161">-SourceResourceGroupName</span></span>
<span data-ttu-id="9954f-162">A forrás SQL-készlet objektumból létrehozandó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9954f-162">The resource group name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9954f-163">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="9954f-163">-SourceResourceId</span></span>
<span data-ttu-id="9954f-164">A forrás SQL-alkalmazáskészlet objektumból létrehozható erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9954f-164">The resource identifier of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9954f-165">-SourceSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="9954f-165">-SourceSqlPoolName</span></span>
<span data-ttu-id="9954f-166">A forrásként létrehozandó SQL Pool objektum neve.</span><span class="sxs-lookup"><span data-stu-id="9954f-166">The name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases: SourceDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9954f-167">-SourceSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="9954f-167">-SourceSqlPoolObject</span></span>
<span data-ttu-id="9954f-168">Az SQL-készlet bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="9954f-168">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9954f-169">-SourceWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9954f-169">-SourceWorkspaceName</span></span>
<span data-ttu-id="9954f-170">A szinapszis munkaterület neve, amelyből a forrás SQL Pool objektum jön létre.</span><span class="sxs-lookup"><span data-stu-id="9954f-170">The Synapse workspace name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases: SourceServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9954f-171">-Címke</span><span class="sxs-lookup"><span data-stu-id="9954f-171">-Tag</span></span>
<span data-ttu-id="9954f-172">Az erőforráshoz társított címkék karakterlánca, karakterláncok szótára</span><span class="sxs-lookup"><span data-stu-id="9954f-172">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="9954f-173">-Verzió</span><span class="sxs-lookup"><span data-stu-id="9954f-173">-Version</span></span>
<span data-ttu-id="9954f-174">A szinapszis SQL Pool verziója.</span><span class="sxs-lookup"><span data-stu-id="9954f-174">Version of Synapse SQL pool.</span></span> <span data-ttu-id="9954f-175">Például 2 vagy 3.</span><span class="sxs-lookup"><span data-stu-id="9954f-175">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="9954f-176">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9954f-176">-WorkspaceName</span></span>
<span data-ttu-id="9954f-177">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="9954f-177">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromBackupIdByNameParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupInputObjectByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9954f-178">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9954f-178">-WorkspaceObject</span></span>
<span data-ttu-id="9954f-179">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="9954f-179">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateFromBackupIdByParentObjectParameterSet, CreateFromBackupNameByParentObjectParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByParentObjectParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9954f-180">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9954f-180">-Confirm</span></span>
<span data-ttu-id="9954f-181">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9954f-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9954f-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9954f-182">-WhatIf</span></span>
<span data-ttu-id="9954f-183">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9954f-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9954f-184">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9954f-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9954f-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9954f-185">CommonParameters</span></span>
<span data-ttu-id="9954f-186">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9954f-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9954f-187">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9954f-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9954f-188">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9954f-188">INPUTS</span></span>

### <span data-ttu-id="9954f-189">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9954f-189">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="9954f-190">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9954f-190">OUTPUTS</span></span>

### <span data-ttu-id="9954f-191">Microsoft. Azure. commands. szinapszis. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="9954f-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="9954f-192">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9954f-192">NOTES</span></span>

## <span data-ttu-id="9954f-193">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9954f-193">RELATED LINKS</span></span>
