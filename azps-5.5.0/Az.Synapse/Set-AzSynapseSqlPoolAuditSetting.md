---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 91691741fd7b26d8f33880dee252501c626a4bc6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162794"
---
# <span data-ttu-id="09f20-101">Set-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="09f20-101">Set-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="09f20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09f20-102">SYNOPSIS</span></span>
<span data-ttu-id="09f20-103">Egy Azure Synapse Analytics SQL-készlet naplózási beállításait módosítja.</span><span class="sxs-lookup"><span data-stu-id="09f20-103">Changes the auditing settings for an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="09f20-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="09f20-104">SYNTAX</span></span>

### <span data-ttu-id="09f20-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="09f20-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-AuditActionGroup <AuditActionGroup[]>] [-AuditAction <String[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09f20-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09f20-106">SetByParentObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AuditActionGroup <AuditActionGroup[]>] [-AuditAction <String[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09f20-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09f20-107">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-AuditActionGroup <AuditActionGroup[]>]
 [-AuditAction <String[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09f20-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="09f20-108">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-AuditActionGroup <AuditActionGroup[]>]
 [-AuditAction <String[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09f20-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="09f20-109">DESCRIPTION</span></span>
<span data-ttu-id="09f20-110">A **Set-AzSynapseSqlPoolAuditSetting** parancsmag módosítja az Azure Synapse Analytics SQL-készlet naplózási beállításait.</span><span class="sxs-lookup"><span data-stu-id="09f20-110">The **Set-AzSynapseSqlPoolAuditSetting** cmdlet changes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>
<span data-ttu-id="09f20-111">Ha a blobtár a naplók célhelye, a *StorageAccountResourceId* paramétert megadva határozza meg a naplók tárfiókját és a *StorageKeyType* paramétert a tárkulcsok meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="09f20-111">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="09f20-112">A naplók megőrzési időszakának meghatározásához a *RetentionInDays* paraméter értékét is meg kell határoznia a naplók időszakának meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="09f20-112">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="09f20-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="09f20-113">EXAMPLES</span></span>

### <span data-ttu-id="09f20-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="09f20-114">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary
```

<span data-ttu-id="09f20-115">Engedélyezze egy ContosoSqlPool nevű Azure Synapse Analytics SQL-készlet blobtárhely-naplózási házirendjét.</span><span class="sxs-lookup"><span data-stu-id="09f20-115">Enable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="09f20-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="09f20-116">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Disabled
```

<span data-ttu-id="09f20-117">Tiltsa le egy ContosoSqlPool nevű Azure Synapse Analytics SQL-készlet blobtárhely-naplózási házirendjét.</span><span class="sxs-lookup"><span data-stu-id="09f20-117">Disable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="09f20-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="09f20-118">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary -PredicateExpression "statement <> 'select 1'"
```

<span data-ttu-id="09f20-119">Engedélyezze a ContosoSqlPool nevű Azure Synapse Analytics SQL-készlet blobtárhely-naplózási házirendjét T-SQL predikátum használatával végzett speciális szűréssel.</span><span class="sxs-lookup"><span data-stu-id="09f20-119">Enable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool with advanced filtering using a T-SQL predicate.</span></span>

### <span data-ttu-id="09f20-120">4. példa</span><span class="sxs-lookup"><span data-stu-id="09f20-120">Example 4</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PredicateExpression ""
```

<span data-ttu-id="09f20-121">Távolítsa el a speciális szűrési beállítást egy ContosoSqlPool nevű Azure Synapse Analytics SQL-készlet naplózási házirendjében.</span><span class="sxs-lookup"><span data-stu-id="09f20-121">Remove the advanced filtering setting from the auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="09f20-122">5. példa</span><span class="sxs-lookup"><span data-stu-id="09f20-122">Example 5</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolAuditSetting -BlobStorageTargetState Disabled
```

<span data-ttu-id="09f20-123">Tiltsa le a ContosoSqlPool nevű Azure Synapse Analytics SQL-készlet blobtárhely-naplózási házirendjét a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="09f20-123">Disable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool through pipeline.</span></span>

## <span data-ttu-id="09f20-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09f20-124">PARAMETERS</span></span>

### <span data-ttu-id="09f20-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09f20-125">-AsJob</span></span>
<span data-ttu-id="09f20-126">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="09f20-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="09f20-127">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="09f20-127">-AuditAction</span></span>
<span data-ttu-id="09f20-128">A naplózási műveletek halmaza.</span><span class="sxs-lookup"><span data-stu-id="09f20-128">The set of audit actions.</span></span>

<span data-ttu-id="09f20-129">A támogatott naplóműveletek a következőek:</span><span class="sxs-lookup"><span data-stu-id="09f20-129">The supported actions to audit are:</span></span>

<span data-ttu-id="09f20-130">SELECT</span><span class="sxs-lookup"><span data-stu-id="09f20-130">SELECT</span></span>

<span data-ttu-id="09f20-131">FRISSÍTÉS</span><span class="sxs-lookup"><span data-stu-id="09f20-131">UPDATE</span></span>

<span data-ttu-id="09f20-132">INSERT</span><span class="sxs-lookup"><span data-stu-id="09f20-132">INSERT</span></span>

<span data-ttu-id="09f20-133">DELETE</span><span class="sxs-lookup"><span data-stu-id="09f20-133">DELETE</span></span>

<span data-ttu-id="09f20-134">EXECUTE</span><span class="sxs-lookup"><span data-stu-id="09f20-134">EXECUTE</span></span>

<span data-ttu-id="09f20-135">RECEIVE</span><span class="sxs-lookup"><span data-stu-id="09f20-135">RECEIVE</span></span>

<span data-ttu-id="09f20-136">HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09f20-136">REFERENCES</span></span>

<span data-ttu-id="09f20-137">A naplót ható művelet meghatározásának általános formája:</span><span class="sxs-lookup"><span data-stu-id="09f20-137">The general form for defining an action to be audited is:</span></span>

<span data-ttu-id="09f20-138">\[action \] ON object BY \[ \] \[ principal\]</span><span class="sxs-lookup"><span data-stu-id="09f20-138">\[action\] ON \[object\] BY \[principal\]</span></span>

<span data-ttu-id="09f20-139">Felhívjuk a figyelmét arra, hogy a fenti formátumban egy objektumra hivatkozhat, például egy táblára, nézetre vagy tárolt eljárásra, illetve egy teljes adatbázisra vagy \[ \] sémára.</span><span class="sxs-lookup"><span data-stu-id="09f20-139">Note that \[object\] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span>
<span data-ttu-id="09f20-140">Az utóbbi esetekben a DATABASE:: \[ dbname \] és SCHEMA:: \[ sémanevet \] használja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="09f20-140">For the latter cases, the forms DATABASE::\[dbname\] and SCHEMA::\[schemaname\] are used, respectively.</span></span>

<span data-ttu-id="09f20-141">Például:</span><span class="sxs-lookup"><span data-stu-id="09f20-141">For example:</span></span>

<span data-ttu-id="09f20-142">SELECT on dbo.myTable by public</span><span class="sxs-lookup"><span data-stu-id="09f20-142">SELECT on dbo.myTable by public</span></span>

<span data-ttu-id="09f20-143">SELECT on DATABASE::myDatabase by public</span><span class="sxs-lookup"><span data-stu-id="09f20-143">SELECT on DATABASE::myDatabase by public</span></span>

<span data-ttu-id="09f20-144">SELECT on SCHEMA::mySchema by public</span><span class="sxs-lookup"><span data-stu-id="09f20-144">SELECT on SCHEMA::mySchema by public</span></span>

<span data-ttu-id="09f20-145">További információ: https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="09f20-145">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="09f20-146">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="09f20-146">-AuditActionGroup</span></span>
<span data-ttu-id="09f20-147">A javasolt műveletcsoportok a következő kombinációk – ez naplóz minden lekérdezést és tárolt eljárást az adatbázison, valamint a sikeres és sikertelen bejelentkezéseket:</span><span class="sxs-lookup"><span data-stu-id="09f20-147">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>



<span data-ttu-id="09f20-148">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="09f20-148">"BATCH_COMPLETED_GROUP",</span></span>

<span data-ttu-id="09f20-149">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="09f20-149">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>

<span data-ttu-id="09f20-150">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="09f20-150">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>

<span data-ttu-id="09f20-151">Ez a fenti kombináció az alapértelmezés szerint konfigurált halmaz is.</span><span class="sxs-lookup"><span data-stu-id="09f20-151">This above combination is also the set that is configured by default.</span></span>
<span data-ttu-id="09f20-152">Ezek a csoportok az adatbázison végrehajtott összes SQL-utasításra és tárolt eljárásra vonatkoznak, és nem használhatók más csoportokkal együtt, mert ez ismétlődő naplókat eredményez.</span><span class="sxs-lookup"><span data-stu-id="09f20-152">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>

<span data-ttu-id="09f20-153">További információ: https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="09f20-153">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="09f20-154">-BlobstorageTargetState</span><span class="sxs-lookup"><span data-stu-id="09f20-154">-BlobStorageTargetState</span></span>
<span data-ttu-id="09f20-155">Azt jelzi, hogy a blobtároló a naplórekordok célhelyét jelenti-e.</span><span class="sxs-lookup"><span data-stu-id="09f20-155">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="09f20-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09f20-156">-DefaultProfile</span></span>
<span data-ttu-id="09f20-157">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="09f20-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09f20-158">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09f20-158">-InputObject</span></span>
<span data-ttu-id="09f20-159">SQL-készlet bemeneti objektuma, amely általában a folyamaton keresztül áthalad.</span><span class="sxs-lookup"><span data-stu-id="09f20-159">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="09f20-160">-Name</span><span class="sxs-lookup"><span data-stu-id="09f20-160">-Name</span></span>
<span data-ttu-id="09f20-161">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="09f20-161">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="09f20-162">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09f20-162">-PassThru</span></span>
<span data-ttu-id="09f20-163">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="09f20-163">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="09f20-164">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="09f20-164">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="09f20-165">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="09f20-165">-PredicateExpression</span></span>
<span data-ttu-id="09f20-166">A naplók szűréséhez használt T-SQL predikátum (WHERE záradék).</span><span class="sxs-lookup"><span data-stu-id="09f20-166">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="09f20-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09f20-167">-ResourceGroupName</span></span>
<span data-ttu-id="09f20-168">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="09f20-168">Resource group name.</span></span>

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

### <span data-ttu-id="09f20-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09f20-169">-ResourceId</span></span>
<span data-ttu-id="09f20-170">A Synapse SQL-készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="09f20-170">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="09f20-171">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="09f20-171">-RetentionInDays</span></span>
<span data-ttu-id="09f20-172">A naplók adatmegőrzési napjainak száma.</span><span class="sxs-lookup"><span data-stu-id="09f20-172">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="09f20-173">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="09f20-173">-StorageAccountResourceId</span></span>
<span data-ttu-id="09f20-174">A tárfiók erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="09f20-174">The storage account resource id</span></span>

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

### <span data-ttu-id="09f20-175">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="09f20-175">-StorageKeyType</span></span>
<span data-ttu-id="09f20-176">Meghatározza, hogy melyik tárelérési kulcsot kell használnia.</span><span class="sxs-lookup"><span data-stu-id="09f20-176">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="09f20-177">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="09f20-177">-WorkspaceName</span></span>
<span data-ttu-id="09f20-178">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="09f20-178">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="09f20-179">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="09f20-179">-WorkspaceObject</span></span>
<span data-ttu-id="09f20-180">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="09f20-180">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="09f20-181">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09f20-181">-Confirm</span></span>
<span data-ttu-id="09f20-182">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="09f20-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09f20-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09f20-183">-WhatIf</span></span>
<span data-ttu-id="09f20-184">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="09f20-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09f20-185">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="09f20-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09f20-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09f20-186">CommonParameters</span></span>
<span data-ttu-id="09f20-187">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09f20-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09f20-188">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09f20-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09f20-189">INPUTS</span><span class="sxs-lookup"><span data-stu-id="09f20-189">INPUTS</span></span>

### <span data-ttu-id="09f20-190">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="09f20-190">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="09f20-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="09f20-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="09f20-192">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09f20-192">OUTPUTS</span></span>

### <span data-ttu-id="09f20-193">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span><span class="sxs-lookup"><span data-stu-id="09f20-193">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="09f20-194">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="09f20-194">NOTES</span></span>

## <span data-ttu-id="09f20-195">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09f20-195">RELATED LINKS</span></span>
