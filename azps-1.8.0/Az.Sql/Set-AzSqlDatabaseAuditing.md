---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAuditing.md
ms.openlocfilehash: 511207be4094dae96f8d138124021ce2f8ed3913
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668803"
---
# <span data-ttu-id="f3673-101">Set-AzSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="f3673-101">Set-AzSqlDatabaseAuditing</span></span>

## <span data-ttu-id="f3673-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f3673-102">SYNOPSIS</span></span>
<span data-ttu-id="f3673-103">Az Azure SQL-adatbázisok naplózási beállításainak módosítása</span><span class="sxs-lookup"><span data-stu-id="f3673-103">Changes the auditing settings for an Azure SQL database.</span></span>

## <span data-ttu-id="f3673-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f3673-104">SYNTAX</span></span>

### <span data-ttu-id="f3673-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f3673-105">DefaultParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-BlobStorage] [-StorageAccountName <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3673-106">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="f3673-106">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-BlobStorage] -StorageAccountName <String>
 -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3673-107">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="f3673-107">EventHubSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-EventHub] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3673-108">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="f3673-108">LogAnalyticsSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-WorkspaceResourceId <String>] [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3673-109">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="f3673-109">BlobStorageByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-BlobStorage] [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3673-110">StorageAccountSubscriptionIdByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="f3673-110">StorageAccountSubscriptionIdByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-BlobStorage] -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3673-111">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="f3673-111">EventHubByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3673-112">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="f3673-112">LogAnalyticsByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3673-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="f3673-113">DESCRIPTION</span></span>
<span data-ttu-id="f3673-114">A **set-AzSqlDatabaseAuditing** parancsmag egy Azure SQL-adatbázis naplózási beállításait módosítja.</span><span class="sxs-lookup"><span data-stu-id="f3673-114">The **Set-AzSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="f3673-115">A parancsmag használatához a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paraméterrel keresse meg az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="f3673-115">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="f3673-116">A naplók rendeltetési helyét az alábbi kapcsoló paraméterek egyikének megadásával határozhatja meg: BlobStorage, LogAnalytics vagy EventHub (ha nincs megadva, az alapértelmezett érték a BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="f3673-116">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>
<span data-ttu-id="f3673-117">A házirend engedélyezéséhez vagy letiltásához használja az *állami* paramétert.</span><span class="sxs-lookup"><span data-stu-id="f3673-117">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="f3673-118">Ha a naplók a blob-tárolók, a *StorageAccountName* paraméterrel határozhatja meg a naplók tárolási fiókját és a *StorageKeyType* paramétert a tárolási kulcsok meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="f3673-118">When audit logs destination is blob storage, specify the *StorageAccountName* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="f3673-119">A naplók adatmegőrzését úgy is megadhatja, hogy az *RetentionInDays* paraméter értékét adja meg a naplók időszakának meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="f3673-119">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="f3673-120">Ha a parancsmag sikerrel jár, és a *PassThru* paramétert használja, az adatbázis-azonosítók mellett az aktuális naplózási beállításokat leíró objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="f3673-120">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing settings in addition to the database identifiers.</span></span>
<span data-ttu-id="f3673-121">Az adatbázis-azonosítók közé tartoznak a következők: a **ResourceGroupName** , a **kiszolgálónév** és a **databasename**.</span><span class="sxs-lookup"><span data-stu-id="f3673-121">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="f3673-122">Példák</span><span class="sxs-lookup"><span data-stu-id="f3673-122">EXAMPLES</span></span>

### <span data-ttu-id="f3673-123">1. példa: a blob-tároló naplózási házirendjének engedélyezése Azure SQL-adatbázisokban</span><span class="sxs-lookup"><span data-stu-id="f3673-123">Example 1: Enable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="f3673-124">2. példa: az Azure SQL-adatbázisok blob-tároló naplózási házirendjének letiltása</span><span class="sxs-lookup"><span data-stu-id="f3673-124">Example 2: Disable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="f3673-125">3. példa: egy Azure SQL-adatbázis blob-tároló naplózási házirendjének engedélyezése egy másik előfizetésből származó tárolási fiók használatával</span><span class="sxs-lookup"><span data-stu-id="f3673-125">Example 3: Enable the blob storage auditing policy of an Azure SQL database using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="f3673-126">Példa 4: a blob-tároló naplózási házirendjének engedélyezése az Azure SQL-adatbázisokban speciális szűréssel a T-SQL predikátum használatával</span><span class="sxs-lookup"><span data-stu-id="f3673-126">Example 4: Enable the blob storage auditing policy of an Azure SQL database with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="f3673-127">Példa 5: az Azure SQL-adatbázis blob-tároló naplózási házirendjéből származó speciális szűrési beállítások eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f3673-127">Example 5: Remove the advanced filtering setting from the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

### <span data-ttu-id="f3673-128">6. példa: az esemény-hub naplózási házirendjének engedélyezése Azure SQL-adatbázisokban</span><span class="sxs-lookup"><span data-stu-id="f3673-128">Example 6: Enable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHub -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="f3673-129">7. példa: az Azure SQL-adatbázisok esetén az esemény központi naplózási házirendjének letiltása</span><span class="sxs-lookup"><span data-stu-id="f3673-129">Example 7: Disable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHub
```

### <span data-ttu-id="f3673-130">8. példa: az Azure SQL-adatbázisok naplózási Analytics-naplózási házirendjének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="f3673-130">Example 8: Enable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="f3673-131">Példa 9: a log Analytics naplózási házirendjének letiltása Azure SQL-adatbázisokban</span><span class="sxs-lookup"><span data-stu-id="f3673-131">Example 9: Disable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics
```

### <span data-ttu-id="f3673-132">10. példa: az Azure SQL-adatbázisok naplózási házirendjének letiltása a csővezetéken keresztül</span><span class="sxs-lookup"><span data-stu-id="f3673-132">Example 10: Disable, through pipeline, the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAuditing -LogAnalytics -State Disabled
```

## <span data-ttu-id="f3673-133">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f3673-133">PARAMETERS</span></span>

### <span data-ttu-id="f3673-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3673-134">-AsJob</span></span>
<span data-ttu-id="f3673-135">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f3673-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f3673-136">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="f3673-136">-AuditAction</span></span>
<span data-ttu-id="f3673-137">A naplózási műveletek halmaza.</span><span class="sxs-lookup"><span data-stu-id="f3673-137">The set of audit actions.</span></span>  
<span data-ttu-id="f3673-138">A naplózandó támogatott műveletek a következők:</span><span class="sxs-lookup"><span data-stu-id="f3673-138">The supported actions to audit are:</span></span>  
<span data-ttu-id="f3673-139">Válassza</span><span class="sxs-lookup"><span data-stu-id="f3673-139">SELECT</span></span>  
<span data-ttu-id="f3673-140">FRISSÍTÉS</span><span class="sxs-lookup"><span data-stu-id="f3673-140">UPDATE</span></span>  
<span data-ttu-id="f3673-141">BESZÚRÁSA</span><span class="sxs-lookup"><span data-stu-id="f3673-141">INSERT</span></span>  
<span data-ttu-id="f3673-142">TÖRLÉSE</span><span class="sxs-lookup"><span data-stu-id="f3673-142">DELETE</span></span>  
<span data-ttu-id="f3673-143">VÉGREHAJTÁSA</span><span class="sxs-lookup"><span data-stu-id="f3673-143">EXECUTE</span></span>  
<span data-ttu-id="f3673-144">KAP</span><span class="sxs-lookup"><span data-stu-id="f3673-144">RECEIVE</span></span>  
<span data-ttu-id="f3673-145">HIVATKOZÁSOK: a naplózandó műveletek meghatározására szolgáló általános űrlap: [művelet] ON [Object] BY [Principal] Megjegyzés: [objektum] a fenti formátumban hivatkozhat egy objektumra (például tábla, nézet vagy tárolt eljárás), illetve egy teljes adatbázisra vagy sémára.</span><span class="sxs-lookup"><span data-stu-id="f3673-145">REFERENCES The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="f3673-146">Az utóbbi esetekben az Forms DATABASE:: [dbname] és a SCHEMA:: [SchemaName] használatban van.</span><span class="sxs-lookup"><span data-stu-id="f3673-146">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="f3673-147">Példa:</span><span class="sxs-lookup"><span data-stu-id="f3673-147">For example:</span></span>  
<span data-ttu-id="f3673-148">Válassza a dbo. Táblanév nyilvánosak szerint lehetőséget</span><span class="sxs-lookup"><span data-stu-id="f3673-148">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="f3673-149">Válassza az adatbázis: myDatabase nyilvánosak szerint lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f3673-149">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="f3673-150">SELECT on SCHEMA:: mySchema by Public</span><span class="sxs-lookup"><span data-stu-id="f3673-150">SELECT on SCHEMA::mySchema by public</span></span>  
<span data-ttu-id="f3673-151">További információ: https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="f3673-151">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3673-152">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="f3673-152">-AuditActionGroup</span></span>
<span data-ttu-id="f3673-153">A használni kívánt műveleti csoportok a következő kombinációk: Ez a művelet naplózza az adatbázissal végzett összes lekérdezést és tárolt eljárást, valamint a sikeres és sikertelen bejelentkezéseket:</span><span class="sxs-lookup"><span data-stu-id="f3673-153">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="f3673-154">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="f3673-154">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="f3673-155">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="f3673-155">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="f3673-156">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="f3673-156">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="f3673-157">Ez a fenti kombináció egyben az alapértelmezés szerint konfigurált halmaz.</span><span class="sxs-lookup"><span data-stu-id="f3673-157">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="f3673-158">Ezek a csoportok az adatbázissal szemben végrehajtott összes SQL-utasítást és tárolt eljárást lefoglalják, és nem használhatók együtt más csoportokkal, mert ez a művelet duplikálja a naplókat.</span><span class="sxs-lookup"><span data-stu-id="f3673-158">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="f3673-159">További információ: https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="f3673-159">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3673-160">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="f3673-160">-BlobStorage</span></span>
<span data-ttu-id="f3673-161">Megadja, hogy a naplók a blob-tárolók legyenek</span><span class="sxs-lookup"><span data-stu-id="f3673-161">Specifies that audit logs destination is blob storage</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3673-162">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f3673-162">-DatabaseName</span></span>
<span data-ttu-id="f3673-163">SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="f3673-163">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3673-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3673-164">-DefaultProfile</span></span>
<span data-ttu-id="f3673-165">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3673-165">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3673-166">-EventHub</span><span class="sxs-lookup"><span data-stu-id="f3673-166">-EventHub</span></span>
<span data-ttu-id="f3673-167">Azt adja meg, hogy a naplók cél az esemény középpontja</span><span class="sxs-lookup"><span data-stu-id="f3673-167">Specifies that audit logs destination is event hub</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3673-168">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="f3673-168">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="f3673-169">Az esemény-hub engedélyezési szabályának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="f3673-169">The resource Id for the event hub authorization rule</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3673-170">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="f3673-170">-EventHubName</span></span>
<span data-ttu-id="f3673-171">Az esemény központja neve.</span><span class="sxs-lookup"><span data-stu-id="f3673-171">The name of the event hub.</span></span> <span data-ttu-id="f3673-172">Ha a EventHubAuthorizationRuleResourceId megadásakor nincs megadva, az alapértelmezett esemény hub lesz kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="f3673-172">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3673-173">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3673-173">-InputObject</span></span>
<span data-ttu-id="f3673-174">Az adatbázis-objektum a naplózási házirend kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="f3673-174">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3673-175">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="f3673-175">-LogAnalytics</span></span>
<span data-ttu-id="f3673-176">Azt adja meg, hogy a naplók a naplózási naplókat jelentik</span><span class="sxs-lookup"><span data-stu-id="f3673-176">Specifies that audit logs destination is log analytics</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LogAnalyticsSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3673-177">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3673-177">-PassThru</span></span>
<span data-ttu-id="f3673-178">Azt adja meg, hogy a naplózási házirendet a parancsmag-végrehajtás végén szeretné-e kivenni.</span><span class="sxs-lookup"><span data-stu-id="f3673-178">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="f3673-179">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="f3673-179">-PredicateExpression</span></span>
<span data-ttu-id="f3673-180">A naplók szűréséhez használt T-SQL predikátum (WHERE záradék).</span><span class="sxs-lookup"><span data-stu-id="f3673-180">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3673-181">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3673-181">-ResourceGroupName</span></span>
<span data-ttu-id="f3673-182">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f3673-182">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3673-183">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="f3673-183">-RetentionInDays</span></span>
<span data-ttu-id="f3673-184">A naplók retenciós napjainak száma.</span><span class="sxs-lookup"><span data-stu-id="f3673-184">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3673-185">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="f3673-185">-ServerName</span></span>
<span data-ttu-id="f3673-186">SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="f3673-186">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3673-187">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="f3673-187">-State</span></span>
<span data-ttu-id="f3673-188">A házirend állapota.</span><span class="sxs-lookup"><span data-stu-id="f3673-188">The state of the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3673-189">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f3673-189">-StorageAccountName</span></span>
<span data-ttu-id="f3673-190">A tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="f3673-190">The name of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, BlobStorageByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageAccountSubscriptionIdSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3673-191">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f3673-191">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="f3673-192">A Storage Account előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="f3673-192">The storage account subscription id</span></span>

```yaml
Type: System.Guid
Parameter Sets: StorageAccountSubscriptionIdSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3673-193">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="f3673-193">-StorageKeyType</span></span>
<span data-ttu-id="f3673-194">Itt adhatja meg, hogy a tárterület-hozzáférési kulcsok közül melyik használható.</span><span class="sxs-lookup"><span data-stu-id="f3673-194">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3673-195">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="f3673-195">-WorkspaceResourceId</span></span>
<span data-ttu-id="f3673-196">A napló Analytics-munkaterületének erőforrás-azonosítója (log Analytics-munkaterületen), amelybe naplókat szeretne küldeni.</span><span class="sxs-lookup"><span data-stu-id="f3673-196">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="f3673-197">Példa:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="f3673-197">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

```yaml
Type: System.String
Parameter Sets: LogAnalyticsSet, LogAnalyticsByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3673-198">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f3673-198">-Confirm</span></span>
<span data-ttu-id="f3673-199">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f3673-199">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3673-200">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3673-200">-WhatIf</span></span>
<span data-ttu-id="f3673-201">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f3673-201">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3673-202">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f3673-202">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3673-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3673-203">CommonParameters</span></span>
<span data-ttu-id="f3673-204">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f3673-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3673-205">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f3673-205">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3673-206">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3673-206">INPUTS</span></span>

### <span data-ttu-id="f3673-207">System. String</span><span class="sxs-lookup"><span data-stu-id="f3673-207">System.String</span></span>

### <span data-ttu-id="f3673-208">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="f3673-208">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="f3673-209">Microsoft. Azure. Command. SQL. könyvvizsgálat. Model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="f3673-209">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="f3673-210">System. string []</span><span class="sxs-lookup"><span data-stu-id="f3673-210">System.String[]</span></span>

### <span data-ttu-id="f3673-211">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f3673-211">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f3673-212">System. GUID</span><span class="sxs-lookup"><span data-stu-id="f3673-212">System.Guid</span></span>

### <span data-ttu-id="f3673-213">System. null ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f3673-213">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f3673-214">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3673-214">OUTPUTS</span></span>

### <span data-ttu-id="f3673-215">Microsoft. Azure. Command. SQL. könyvvizsgálat. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="f3673-215">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="f3673-216">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f3673-216">NOTES</span></span>

## <span data-ttu-id="f3673-217">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3673-217">RELATED LINKS</span></span>
