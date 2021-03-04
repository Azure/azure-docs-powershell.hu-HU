---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 102d8f9e33a90d97cadb984a671797a89d6f3833
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939225"
---
# <span data-ttu-id="0aad0-101">Set-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="0aad0-101">Set-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="0aad0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0aad0-102">SYNOPSIS</span></span>
<span data-ttu-id="0aad0-103">Egy Azure Synapse Analytics SQL-készlet naplózási beállításait módosítja.</span><span class="sxs-lookup"><span data-stu-id="0aad0-103">Changes the auditing settings for an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="0aad0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0aad0-104">SYNTAX</span></span>

### <span data-ttu-id="0aad0-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0aad0-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-AuditActionGroup <AuditActionGroup[]>] [-AuditAction <String[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aad0-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0aad0-106">SetByParentObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AuditActionGroup <AuditActionGroup[]>] [-AuditAction <String[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aad0-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0aad0-107">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-AuditActionGroup <AuditActionGroup[]>]
 [-AuditAction <String[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aad0-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0aad0-108">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-AuditActionGroup <AuditActionGroup[]>]
 [-AuditAction <String[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0aad0-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0aad0-109">DESCRIPTION</span></span>
<span data-ttu-id="0aad0-110">A **Set-AzSynapseSqlPoolAuditSetting** parancsmag módosítja az Azure Synapse Analytics SQL-készlet naplózási beállításait.</span><span class="sxs-lookup"><span data-stu-id="0aad0-110">The **Set-AzSynapseSqlPoolAuditSetting** cmdlet changes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>
<span data-ttu-id="0aad0-111">Ha a blobtár a naplók célhelye, a *StorageAccountResourceId* paramétert megadva határozza meg a naplók tárfiókját és a *StorageKeyType* paramétert a tárkulcsok meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="0aad0-111">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="0aad0-112">A naplók megőrzési időszakának meghatározásához a *RetentionInDays* paraméter értékét megadva is megadhatja a naplók időszakát.</span><span class="sxs-lookup"><span data-stu-id="0aad0-112">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="0aad0-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0aad0-113">EXAMPLES</span></span>

### <span data-ttu-id="0aad0-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="0aad0-114">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary
```

<span data-ttu-id="0aad0-115">Engedélyezze egy ContosoSqlPool nevű Azure Synapse Analytics SQL-készlet blobtárhely-naplózási házirendjét.</span><span class="sxs-lookup"><span data-stu-id="0aad0-115">Enable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="0aad0-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="0aad0-116">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Disabled
```

<span data-ttu-id="0aad0-117">Tiltsa le egy ContosoSqlPool nevű Azure Synapse Analytics SQL-készlet blobtárhely-naplózási házirendjét.</span><span class="sxs-lookup"><span data-stu-id="0aad0-117">Disable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="0aad0-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="0aad0-118">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary -PredicateExpression "statement <> 'select 1'"
```

<span data-ttu-id="0aad0-119">Engedélyezze a ContosoSqlPool nevű Azure Synapse Analytics SQL-készlet blobtárhely-naplózási házirendjét T-SQL predikátum használatával végzett speciális szűréssel.</span><span class="sxs-lookup"><span data-stu-id="0aad0-119">Enable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool with advanced filtering using a T-SQL predicate.</span></span>

### <span data-ttu-id="0aad0-120">4. példa</span><span class="sxs-lookup"><span data-stu-id="0aad0-120">Example 4</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PredicateExpression ""
```

<span data-ttu-id="0aad0-121">Távolítsa el a speciális szűrési beállítást egy ContosoSqlPool nevű Azure Synapse Analytics SQL-készlet naplózási házirendjében.</span><span class="sxs-lookup"><span data-stu-id="0aad0-121">Remove the advanced filtering setting from the auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="0aad0-122">5. példa</span><span class="sxs-lookup"><span data-stu-id="0aad0-122">Example 5</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolAuditSetting -BlobStorageTargetState Disabled
```

<span data-ttu-id="0aad0-123">Tiltsa le a ContosoSqlPool nevű Azure Synapse Analytics SQL-készlet blobtárhely-naplózási házirendjét a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="0aad0-123">Disable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool through pipeline.</span></span>

## <span data-ttu-id="0aad0-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0aad0-124">PARAMETERS</span></span>

### <span data-ttu-id="0aad0-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0aad0-125">-AsJob</span></span>
<span data-ttu-id="0aad0-126">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0aad0-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0aad0-127">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="0aad0-127">-AuditAction</span></span>
<span data-ttu-id="0aad0-128">A naplózási műveletek halmaza.</span><span class="sxs-lookup"><span data-stu-id="0aad0-128">The set of audit actions.</span></span>

<span data-ttu-id="0aad0-129">A támogatott naplóműveletek a következőek:</span><span class="sxs-lookup"><span data-stu-id="0aad0-129">The supported actions to audit are:</span></span>

<span data-ttu-id="0aad0-130">SELECT</span><span class="sxs-lookup"><span data-stu-id="0aad0-130">SELECT</span></span>

<span data-ttu-id="0aad0-131">FRISSÍTÉS</span><span class="sxs-lookup"><span data-stu-id="0aad0-131">UPDATE</span></span>

<span data-ttu-id="0aad0-132">INSERT</span><span class="sxs-lookup"><span data-stu-id="0aad0-132">INSERT</span></span>

<span data-ttu-id="0aad0-133">DELETE</span><span class="sxs-lookup"><span data-stu-id="0aad0-133">DELETE</span></span>

<span data-ttu-id="0aad0-134">EXECUTE</span><span class="sxs-lookup"><span data-stu-id="0aad0-134">EXECUTE</span></span>

<span data-ttu-id="0aad0-135">RECEIVE</span><span class="sxs-lookup"><span data-stu-id="0aad0-135">RECEIVE</span></span>

<span data-ttu-id="0aad0-136">HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0aad0-136">REFERENCES</span></span>

<span data-ttu-id="0aad0-137">A naplót ható művelet meghatározásának általános formája:</span><span class="sxs-lookup"><span data-stu-id="0aad0-137">The general form for defining an action to be audited is:</span></span>

<span data-ttu-id="0aad0-138">\[action \] ON object BY \[ \] \[ principal\]</span><span class="sxs-lookup"><span data-stu-id="0aad0-138">\[action\] ON \[object\] BY \[principal\]</span></span>

<span data-ttu-id="0aad0-139">Felhívjuk a figyelmét arra, hogy a fenti formátumban egy objektumra hivatkozhat, például egy táblára, nézetre vagy tárolt eljárásra, illetve egy teljes adatbázisra vagy \[ \] sémára.</span><span class="sxs-lookup"><span data-stu-id="0aad0-139">Note that \[object\] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span>
<span data-ttu-id="0aad0-140">Az utóbbi esetekben a DATABASE:: \[ dbname \] és SCHEMA:: \[ sémanév \] használatos.</span><span class="sxs-lookup"><span data-stu-id="0aad0-140">For the latter cases, the forms DATABASE::\[dbname\] and SCHEMA::\[schemaname\] are used, respectively.</span></span>

<span data-ttu-id="0aad0-141">Például:</span><span class="sxs-lookup"><span data-stu-id="0aad0-141">For example:</span></span>

<span data-ttu-id="0aad0-142">SELECT on dbo.myTable by public</span><span class="sxs-lookup"><span data-stu-id="0aad0-142">SELECT on dbo.myTable by public</span></span>

<span data-ttu-id="0aad0-143">SELECT on DATABASE::myDatabase by public</span><span class="sxs-lookup"><span data-stu-id="0aad0-143">SELECT on DATABASE::myDatabase by public</span></span>

<span data-ttu-id="0aad0-144">SELECT on SCHEMA::mySchema by public</span><span class="sxs-lookup"><span data-stu-id="0aad0-144">SELECT on SCHEMA::mySchema by public</span></span>

<span data-ttu-id="0aad0-145">További információ: https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="0aad0-145">For more information, see https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aad0-146">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="0aad0-146">-AuditActionGroup</span></span>
<span data-ttu-id="0aad0-147">A javasolt műveletcsoportok a következő kombinációk – ez naplóz minden lekérdezést és tárolt eljárást az adatbázison, valamint a sikeres és sikertelen bejelentkezéseket:</span><span class="sxs-lookup"><span data-stu-id="0aad0-147">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>



<span data-ttu-id="0aad0-148">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="0aad0-148">"BATCH_COMPLETED_GROUP",</span></span>

<span data-ttu-id="0aad0-149">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="0aad0-149">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>

<span data-ttu-id="0aad0-150">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="0aad0-150">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>

<span data-ttu-id="0aad0-151">Ez a fenti kombináció az alapértelmezés szerint konfigurált halmaz is.</span><span class="sxs-lookup"><span data-stu-id="0aad0-151">This above combination is also the set that is configured by default.</span></span>
<span data-ttu-id="0aad0-152">Ezek a csoportok az adatbázison végrehajtott összes SQL-utasításra és tárolt eljárásra vonatkoznak, és nem használhatók más csoportokkal együtt, mert ez ismétlődő naplókat eredményez.</span><span class="sxs-lookup"><span data-stu-id="0aad0-152">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>

<span data-ttu-id="0aad0-153">További információ: https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="0aad0-153">For more information, see https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.AuditActionGroup[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aad0-154">-BlobstorageTargetState</span><span class="sxs-lookup"><span data-stu-id="0aad0-154">-BlobStorageTargetState</span></span>
<span data-ttu-id="0aad0-155">Azt jelzi, hogy a blobtároló a naplórekordok célhelyét jelenti-e.</span><span class="sxs-lookup"><span data-stu-id="0aad0-155">Indicates whether blob storage is a destination for audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aad0-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aad0-156">-DefaultProfile</span></span>
<span data-ttu-id="0aad0-157">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0aad0-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0aad0-158">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0aad0-158">-InputObject</span></span>
<span data-ttu-id="0aad0-159">SQL-készlet bemeneti objektuma, amely általában a folyamaton keresztül áthalad.</span><span class="sxs-lookup"><span data-stu-id="0aad0-159">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0aad0-160">-Name</span><span class="sxs-lookup"><span data-stu-id="0aad0-160">-Name</span></span>
<span data-ttu-id="0aad0-161">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="0aad0-161">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aad0-162">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0aad0-162">-PassThru</span></span>
<span data-ttu-id="0aad0-163">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="0aad0-163">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="0aad0-164">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="0aad0-164">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="0aad0-165">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="0aad0-165">-PredicateExpression</span></span>
<span data-ttu-id="0aad0-166">A naplók szűréséhez használt T-SQL predikátum (WHERE záradék).</span><span class="sxs-lookup"><span data-stu-id="0aad0-166">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="0aad0-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0aad0-167">-ResourceGroupName</span></span>
<span data-ttu-id="0aad0-168">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0aad0-168">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aad0-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0aad0-169">-ResourceId</span></span>
<span data-ttu-id="0aad0-170">A Synapse SQL-készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0aad0-170">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aad0-171">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="0aad0-171">-RetentionInDays</span></span>
<span data-ttu-id="0aad0-172">A naplók adatmegőrzési napjainak száma.</span><span class="sxs-lookup"><span data-stu-id="0aad0-172">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aad0-173">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="0aad0-173">-StorageAccountResourceId</span></span>
<span data-ttu-id="0aad0-174">A tárfiók erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="0aad0-174">The storage account resource id</span></span>

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

### <span data-ttu-id="0aad0-175">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="0aad0-175">-StorageKeyType</span></span>
<span data-ttu-id="0aad0-176">Meghatározza, hogy melyik tárelérési kulcsot kell használnia.</span><span class="sxs-lookup"><span data-stu-id="0aad0-176">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aad0-177">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0aad0-177">-WorkspaceName</span></span>
<span data-ttu-id="0aad0-178">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="0aad0-178">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aad0-179">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0aad0-179">-WorkspaceObject</span></span>
<span data-ttu-id="0aad0-180">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="0aad0-180">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0aad0-181">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0aad0-181">-Confirm</span></span>
<span data-ttu-id="0aad0-182">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0aad0-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0aad0-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0aad0-183">-WhatIf</span></span>
<span data-ttu-id="0aad0-184">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0aad0-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0aad0-185">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0aad0-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0aad0-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aad0-186">CommonParameters</span></span>
<span data-ttu-id="0aad0-187">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0aad0-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aad0-188">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0aad0-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aad0-189">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0aad0-189">INPUTS</span></span>

### <span data-ttu-id="0aad0-190">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0aad0-190">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="0aad0-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="0aad0-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="0aad0-192">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0aad0-192">OUTPUTS</span></span>

### <span data-ttu-id="0aad0-193">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span><span class="sxs-lookup"><span data-stu-id="0aad0-193">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="0aad0-194">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0aad0-194">NOTES</span></span>

## <span data-ttu-id="0aad0-195">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0aad0-195">RELATED LINKS</span></span>
